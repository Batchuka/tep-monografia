# Elaboração — Seção 2.2: Controle Plant-Wide

> Arquivo de rascunho. Proposta de reescrita e expansão da seção `\section{Controle Plant-Wide}` do Cap2.
> Mantém o fio narrativo existente, remove menção ao Kubernetes (que pertence ao Cap5) e
> aprofunda a discussão de função de custo e controle self-optimizing.

---

## Texto proposto

---

Em plantas de processo contínuo, malhas de controle locais são necessárias, mas insuficientes para
garantir desempenho econômico e coordenação global. Cada controlador PID regula uma variável de seu
subsistema imediato, mas é incapaz de perceber os efeitos que suas ações propagam ao longo da planta
por meio de reciclos, transferências de massa e acoplamentos termodinâmicos. A consequência é que
perturbações de grande amplitude podem atravessar toda a cadeia de processo e provocar perda
econômica, saturação de variáveis, oscilações sustentadas ou degradação de qualidade em pontos
distantes da origem, sem que nenhum controlador local tenha autoridade para reagir \cite{Larsson2000}.

O problema não é de sintonia: cada PID pode estar corretamente ajustado para seu subsistema imediato
e, ainda assim, o conjunto falhar como sistema integrado. \citeonline{Larsson2000} identificam que o
campo de *plantwide control* trata de decisões estruturais — quais variáveis controlar, quais
medir, quais manipular e como conectá-las — e não do comportamento individual de cada malha. Os
autores revisam a literatura e identificam cinco tarefas estruturais que qualquer estratégia de
supervisão deve endereçar: (i) seleção de variáveis controladas (quais saídas manter no setpoint);
(ii) seleção de variáveis manipuladas (quais entradas usar para cada objetivo); (iii) seleção de
medições (quais variáveis medir para fechar as malhas); (iv) seleção da configuração de controle
(como parear variáveis controladas e manipuladas); e (v) seleção do tipo de controlador
(estrutura e grau de descentralização).
A ausência de uma resposta sistemática a essas perguntas é, segundo os autores, a principal causa de
estratégias de controle que funcionam individualmente mas falham quando integradas.

### Função de custo como ponto de partida

Antes de responder a qualquer uma dessas quatro perguntas, \citeonline{Skogestad2004} estabelece um
prerequisito frequentemente negligenciado: a definição explícita dos objetivos operacionais. Sem um
critério de desempenho claro, a escolha entre controlar temperatura do reator, vazão de reciclo ou
composição na purga torna-se arbitrária — uma questão de opinião ou convenção, não de análise.
Idealmente, esses objetivos devem ser combinados em uma função de custo escalar $J$ a ser minimizada:

> *"The operational objectives must be clearly defined before attempting to design a control system.
> Although this seems obvious, this step is frequently overlooked. Preferably, the operational
> objectives should be combined into a scalar cost function J to be minimized. In many cases,
> J may be simply selected as the operational cost."* \cite{Skogestad2004}

O artigo original de \citeonline{DOWNS1993} fornece exatamente essa função de custo para o TEP,
expressa em termos de custos operacionais com coeficientes numéricos específicos (Tabela~9 do artigo
original). De forma conceitual, a lógica econômica dessa função pode ser entendida como a soma
ponderada de cinco componentes de perda: (a) perda de reagentes não convertidos na corrente de purga;
(b) perda de matérias-primas na corrente de produto; (c) formação do subproduto F (reação~\ref{eq:rx3}),
que representa reagentes consumidos sem retorno econômico; (d) trabalho do compressor; e (e) consumo
de vapor. A representação agregada abaixo sintetiza essa estrutura como soma de custos por corrente ou
equipamento — mas não deve ser entendida como transcrição literal dos termos da Tabela~9:

\begin{equation}
  J = c_{\mathrm{purga}} \cdot \dot{m}_{\mathrm{purga}} + c_{\mathrm{prod}} \cdot \dot{m}_{\mathrm{MP,prod}} + c_F \cdot \dot{m}_F + c_{\mathrm{comp}} \cdot W_{\mathrm{comp}} + c_{\mathrm{vapor}} \cdot \dot{Q}_{\mathrm{vapor}}
  \label{eq:tep_cost}
\end{equation}

\noindent onde cada termo representa, respectivamente: custo das matérias-primas perdidas na purga,
custo das matérias-primas que saem com o produto, custo econômico atribuído à formação de F, custo
do trabalho de compressão e custo do vapor. O sinal de $J$ está formulado como custo (negativo de
lucro), de modo que minimizar $J$ corresponde a maximizar a eficiência operacional \cite{DOWNS1993}.

A existência dessa função de custo transforma as quatro perguntas de Larsson em perguntas técnicas
respondíveis: a melhor seleção de variáveis controladas é aquela que, sob incerteza de perturbações
e ruído, mantém $J$ mais próximo do seu valor ótimo $J^*$.

### Hierarquia de controle e escala de tempo

\citeonline{Skogestad2004} propõe organizar a resposta a essas perguntas em uma hierarquia de
camadas separadas por escala de tempo:

\begin{enumerate}
  \item \textbf{Controle regulatório}: malhas PID locais que estabilizam variáveis de processo em
        torno de um ponto de operação. Esse nível opera em escala de segundos a minutos e não possui
        visão global da planta.
  \item \textbf{Controle supervisório}: coordenação das malhas regulatórias via ajuste de setpoints
        e ativação/desativação de malhas, operando em escala de minutos a horas. Esse é o nível que
        reage a perturbações que transcendem os limites de uma única malha local.
  \item \textbf{Otimização em tempo real} (\textit{Real-Time Optimization} — RTO): recalculo dos
        setpoints ótimos das variáveis primárias com base nas condições econômicas vigentes e
        nas restrições ativas, operando em escala de horas a dias.
\end{enumerate}

A separação em camadas é justificada não apenas pela diferença de escala de tempo, mas pela
diferença de informação disponível em cada nível. A camada regulatória opera com medições locais e
sem modelo da planta inteira. A camada supervisória opera sobre os setpoints das malhas regulatórias,
sem necessidade de acessar diretamente as válvulas. A RTO, por sua vez, resolve um problema de
otimização estacionária para determinar os setpoints ótimos que a camada supervisória deve
perseguir \cite{Skogestad2004}.

### Controle self-optimizing e a perda econômica $L$

O conceito central que conecta a função de custo $J$ à estrutura de controle é o de
\textbf{controle self-optimizing}: escolher variáveis controladas $c$ tais que, mantidas em
setpoint fixo, levem automaticamente aos ajustes ótimos das variáveis manipuladas quando ocorrem
perturbações — sem necessidade de reotimização explícita \cite{Skogestad2004}. Para quantificar
quando uma escolha de $c$ é suficientemente boa, define-se a \textbf{perda econômica} $L$:

\begin{equation}
  L = J(u, d) - J^*(d)
  \label{eq:loss}
\end{equation}

\noindent onde $J(u,d)$ é o valor real da função de custo quando a política de setpoint fixo é
aplicada sob perturbação $d$, e $J^*(d)$ é o valor ótimo que seria atingido com reotimização
completa. O controle self-optimizing é alcançado quando existe uma política de setpoint constante
que resulta em perda $L$ aceitável para o espectro esperado de perturbações — sem reotimizar
\cite{Skogestad2004}.

A implicação prática é significativa: se as variáveis controladas forem bem escolhidas, o supervisor
não precisa resolver um problema de otimização a cada perturbação — basta regular $c$ no setpoint.
A escolha errada das variáveis controladas, por outro lado, pode resultar em perda econômica
elevada mesmo que todas as malhas estejam corretamente sintonizadas.

### Aplicação ao TEP: análise de graus de liberdade

\citeonline{Larsson2000} aplicam essa metodologia diretamente ao TEP. Uma análise de graus de
liberdade no estado estacionário revela que o processo possui 8 graus de liberdade manipuláveis.
No modo nominal (Modo~1), 5 desses graus estão consumidos por restrições economicamente ativas —
variáveis que operam em seu limite operacional ótimo e, portanto, devem ser mantidas nesses limites
como restrições, não como alvos de setpoint livre. Restam 3 graus de liberdade não restringidos,
para os quais é necessário escolher variáveis self-optimizing.

Avaliando sistematicamente as alternativas pela perda $L$ calculada com a função de custo de
Downs~\& Vogel, os autores concluem que boas escolhas self-optimizing incluem: temperatura do
reator (XMEAS$_9$), vazão de reciclo ou trabalho do compressor (XMEAS$_5$ ou XMEAS$_{20}$), e
composição de A na purga ou na alimentação do reator. Notavelmente, a fração molar do inerte B —
frequentemente indicada por outros autores — é identificada como uma má escolha nesse contexto:
controlá-la em setpoint fixo resulta em perda econômica mais elevada do que as alternativas acima
\cite{Larsson2000}.

Essa análise revela a função concreta que uma camada supervisória deve exercer no TEP: não apenas
estabilizar a planta, mas garantir que as variáveis primárias $c$ — aquelas identificadas como
self-optimizing — permaneçam próximas de seus setpoints ótimos frente às perturbações IDV. Qualquer
arquitetura supervisória proposta pode ser avaliada, em última instância, pelo valor de $L$ que
produz em simulação.

### Conexão com este trabalho

A hierarquia de Skogestad fornece o enquadramento teórico para a separação de responsabilidades
na arquitetura proposta neste trabalho: a camada regulatória é implementada pelo conjunto de
controladores PID do \texttt{ControllerBank}; a camada supervisória é o objeto de investigação
central deste trabalho — responsável por coordenar setpoints, modos e condições observadas das
malhas regulatórias frente a perturbações e transições operacionais. A camada de otimização em
tempo real, que determinaria os setpoints ótimos de $c$ via minimização de $J$, fica fora do
escopo deste trabalho e constitui extensão natural. O TEP, com sua função de custo explícita e
seus 41~XMEAS e 12~XMV, é um ambiente adequado para avaliar se um supervisor consegue manter a
planta próxima do ótimo operacional sem requerer reotimização a cada perturbação.

---

## Notas de revisão

- **Removido**: referência ao Kubernetes/Operator no parágrafo de fechamento (pertence ao Cap5,
  não ao referencial teórico).
- **Adicionado**: parágrafo sobre função de custo $J$ como prerequisito da escolha de variáveis
  controladas, ancorado em Skogestad2004 e Downs&Vogel1993.
- **Adicionado**: definição explícita da perda econômica $L$ e do controle self-optimizing.
- **Adicionado**: análise de graus de liberdade do TEP (8 DOF, 5 ativos, 3 livres) com as
  variáveis self-optimizing identificadas por Larsson&Skogestad(2000).
- **Equação \ref{eq:tep_cost}**: verificar se os coeficientes da função de custo do TEP valem a
  pena ser explicitados em tabela (conforme Tabela~9 do original) ou se o texto prosa já basta.
- **Equação \ref{eq:loss}**: checar numeração para não colidir com Harris index (eq. 3) e PI index.
- A fórmula de $J$ como soma de custos está apresentada em forma genérica; se quiser a forma
  exata com os valores numéricos da Tabela~9 de Downs & Vogel, isso pode ser incluído como
  subequação ou tabela.