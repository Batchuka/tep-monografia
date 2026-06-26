# Elaboração — Seção 2.3: Diagnóstico de Qualidade de Malhas (CLPM)

> Arquivo de rascunho — segunda versão, revisada a partir de:
> - art2_ (GPT especializado em Bradu 2018)
> - art7_ (GPT especializado em Tilaro 2017)
> - art8_ (GPT especializado em Tilaro 2018)
> - ft_Automatic-PID-Performance-Monitoring (anotações do próprio artigo — Bradu 2018)
> - ft_Assessment-of-Control-Loop-Performance (anotações — Harris 1989)
> - ft_An-Expert-Knowledge-Based-Methodology (anotações — Tilaro 2017)
> - ft_Model-Learning-Algorithms-for-Anomaly-Detection (anotações — Tilaro 2018)
> - ft_Condition-Monitoring-of-Bearing-Damage (anotações — Lessmeier 2016)

---

## Texto proposto

---

A qualidade de uma malha de controle não é binária: um controlador pode estar em modo automático e
ainda assim apresentar desempenho degradado. Malhas excessivamente agressivas podem induzir
oscilações e desgaste de atuadores; malhas conservadoras demais respondem lentamente e permitem a
propagação de distúrbios; e restrições de atuador, ruído de medição ou perturbações externas podem
comprometer o comportamento da malha sem necessariamente acionar alarmes discretos. Em plantas com
centenas ou milhares de controladores, a identificação manual de condições degradadas torna-se
impraticável, motivando técnicas de \textit{control loop performance monitoring} (CLPM). O objetivo
do CLPM não é controlar melhor diretamente, mas transformar históricos de sinais da malha —
setpoint, variável medida e saída do controlador — em indicadores de desempenho que permitam
priorizar quais malhas exigem análise especializada \cite{Bradu2018}.

### Benchmark de variância mínima e o índice de Harris

O trabalho de \citeonline{Harris1989} tornou-se um marco clássico na avaliação quantitativa de
desempenho de malhas fechadas ao propor um benchmark baseado em controle de variância mínima. A
ideia central é que, para processos representáveis por funções de transferência lineares sujeitos a
perturbações aditivas, existe um limite inferior teórico para a variância da variável controlada:
a variância que seria obtida por um controlador de variância mínima (MVC), dado o atraso discreto
inerente ao processo. A principal contribuição de Harris é que esse limite pode ser estimado a
partir de dados rotineiros de operação em malha fechada, sem necessidade de experimentos de
identificação ou conhecimento completo do modelo da planta — basta conhecer o atraso discreto
efetivo $f$ (número de períodos de amostragem entre a ação de controle e seu efeito mensurável
na saída).

A estimativa de $\sigma^2_{\text{mv}}$ é obtida ajustando-se um modelo univariado de séries
temporais à variável controlada em malha fechada e extraindo a variância do erro de previsão $f+1$
passos à frente. Essa variância corresponde à parcela da saída que não pode ser removida por
feedback antes que o efeito do atraso se manifeste. Na literatura, essa decomposição aparece
associada aos primeiros coeficientes da representação de médias móveis ou aos coeficientes de Markov
da dinâmica de perturbação \cite{Harris1989}. Uma propriedade diagnóstica importante: sob controle
de variância mínima, a autocorrelação da variável controlada é nula além do lag $f$. Portanto,
autocorrelação significativa para lags maiores que $f$ indica que o controlador não está extraindo
todo o desempenho possível.

Em muitas formulações posteriores de CLPM, o desempenho é expresso como uma razão normalizada:

\begin{equation}
  \eta = \frac{\sigma^2_{\text{mv}}}{\sigma^2_y}
  \label{eq:harris_index}
\end{equation}

\noindent Valores próximos de 1 indicam operação próxima ao benchmark de variância mínima; valores
baixos indicam que a variância observada é substancialmente maior do que o limite teoricamente
alcançável. Deve-se observar, contudo, que o índice não identifica a causa da degradação: um baixo
$\eta$ pode decorrer de má sintonia, mas também de atraso excessivo, saturação de atuador, ruído de
medição, falta de ação feedforward ou perturbação não medida. Quando $\eta$ está próximo de 1, mas a
variância absoluta ainda é alta, a causa é estrutural — reduz-se a variância mínima apenas por
modificações no processo, como redução de atraso, troca de variável manipulada ou adição de
feedforward \cite{Harris1989}.

### Transição para indicadores operacionais de larga escala

Embora o benchmark de Harris forneça uma referência teórica robusta, sua aplicação prática pressupõe
hipóteses de linearidade e requer o conhecimento do atraso discreto efetivo $f$, que pode não ser
trivialmente disponível em plantas industriais complexas. Abordagens posteriores de CLPM buscaram
métricas mais simples de implantar em larga escala, substituindo o benchmark ótimo por indicadores
estatísticos calculados diretamente dos históricos das malhas. É nesse contexto que se insere o
Índice de Preditividade aplicado por \citeonline{Bradu2018} no sistema criogênico do LHC.

### Índice de Preditividade e a abordagem do CERN

O sistema criogênico do LHC opera milhares de malhas PID distribuídas ao longo do acelerador para
manter os imãs supercondutores na temperatura de operação. Nessa escala, a inspeção manual é
inviável: a revisão individual de cada malha exigiria centenas de horas de trabalho especializado
por ciclo \cite{Bradu2018}. O método proposto é \textit{model-free}: ele não utiliza nenhum modelo
físico do processo, operando exclusivamente sobre os sinais da própria malha — setpoint, variável
medida e saída do controlador.

O \textit{Predictability Index} (PI) é calculado em duas etapas. Primeiro, estima-se o erro futuro
da malha a partir de seus valores passados. Para um horizonte de predição $b$ e uma ordem de modelo
$m$, o erro previsto é:

\begin{equation}
  \hat{e}(t+b) = a_0 + a_1\,e(t) + a_2\,e(t-1) + \cdots + a_m\,e(t-m-1)
  \label{eq:pi_pred}
\end{equation}

A partir do resíduo de predição, calcula-se:

\begin{equation}
  \text{PI} = \frac{\sigma^2_r}{\text{mse}}
  \label{eq:pi_index}
\end{equation}

\noindent onde $\sigma^2_r$ é a variância do resíduo entre o erro medido e o erro previsto, e
$\text{mse}$ é o erro quadrático médio da malha. Operacionalmente, PI baixo indica comportamento
errático ou imprevisível; PI alto indica comportamento regular, compatível com o modelo de predição
adotado \cite{Bradu2018}.

Os parâmetros do método não são escolhidos arbitrariamente. Na implementação do CERN, eles são
derivados de grandezas operacionais: intervalo de amostragem $t_s$, janela de análise $T_W$ e
constante de tempo característica da malha $T$. A partir dessas grandezas, calculam-se o número de
amostras da janela $n = \lceil T_W/t_s \rceil$, o horizonte de predição $b = \lceil T/t_s \rceil$
e a ordem do modelo $m = 2b$. Essa estrutura evidencia uma preocupação prática: o método é
configurável por grupos de malhas, não ajustado individualmente para cada controlador.

A classificação de uma malha como problemática não depende apenas do valor bruto do PI. Os autores
adicionam duas condições operacionais para reduzir falsos positivos: (i) a saída do controlador deve
apresentar variação significativa ($\sigma_y > \bar{\sigma}_y$), evitando classificar como
degradadas malhas saturadas, inativas ou em modo manual; e (ii) a condição PI $< PI_L$ deve persistir
em mais de $N$ janelas dentro de um período de 24 horas, evitando que transientes breves sejam
interpretados como degradação estrutural \cite{Bradu2018}.

O limiar $PI_L$ não é uma constante universal. No artigo do CERN, ele é definido empiricamente por
grupos de controladores — temperatura, pressão, vazão e nível — com valores distintos conforme a
dinâmica e os objetivos operacionais de cada grupo. Portanto, qualquer aplicação do PI ao TEP exige
calibração específica por classe de variável.

Quando uma malha é declarada problemática pelo PI, o artigo classifica a causa em quatro categorias:
(i) \textit{tuning} — o controlador precisa ser resintonizado; (ii) \textit{process} — o controlador
não lida adequadamente com os distúrbios, inclusive por decorrência de restrições mecânicas; (iii)
\textit{noise} — a variável medida apresenta ruído excessivo para uma regulagem eficaz; e (iv)
\textit{false positive} — os parâmetros escolhidos para o cálculo do PI estão inadequados para
aquela malha específica. Esse esquema de classificação é importante: PI baixo não implica
diretamente em PID mal sintonizado. A causa exige diagnóstico complementar \cite{Bradu2018}.

### Detecção de padrões dinâmicos específicos

Além de índices globais de desempenho, trabalhos do mesmo grupo investigam a detecção de padrões
específicos de comportamento anômalo em séries temporais industriais.
\citeonline{Tilaro2017} propõem um método de detecção online de oscilações em sensores e atuadores
que combina análise espectral por transformada de Fourier discreta (DFT), filtro passa-faixa,
detecção de cruzamentos por zero e verificação de regularidade temporal. Uma propriedade importante
do método: oscilações em malhas industriais podem ocorrer mesmo quando o sistema opera em estado
nominal, sem acionar nenhum alarme discreto. O método transforma uma percepção antes dependente da
inspeção visual do especialista em uma condição computável, caracterizada por frequência dominante,
amplitude, período e índice de regularidade.

\citeonline{Tilaro2018} estendem essa direção com métodos de aprendizado de modelos sobre dados
históricos de controle. Os autores exploram relações físicas e lógicas entre sinais — sensores em
uma mesma unidade de processo e relações entrada--saída de malhas de controle — para detectar
desvios coerentes em relação ao comportamento histórico esperado. Desvios persistentes funcionam
como sinais de aviso de possíveis anomalias futuras, ativando verificações por especialistas antes
que falhas se manifestem.

Além do diagnóstico de malhas de controle, a mesma lógica de transformar séries temporais em
estados supervisionáveis aparece no campo de monitoramento de condição de equipamentos.
\citeonline{Lessmeier2016} demonstram que sinais de corrente de motores elétricos — disponíveis em
inversores de frequência já existentes, sem sensores adicionais — carregam informação sobre danos em
mancais do sistema de acionamento. O estado relevante não é medido diretamente: ele é inferido a
partir de sinais imperfeitos por um classificador treinado sobre dados históricos. Esse artigo
generaliza o princípio: qualquer sinal disponível na planta pode ser fonte de diagnóstico de
condição, desde que interpretado por uma camada analítica especializada.

### Relevância para a arquitetura supervisória proposta

Esses trabalhos são relevantes para este projeto porque estabelecem a viabilidade de uma camada
intermediária entre sinais crus da planta e decisões supervisórias. Índices como Harris e PI,
métodos de detecção de oscilações e modelos de anomalia permitem transformar séries temporais de
baixo nível em estados diagnósticos de maior abstração: malha saudável, malha degradada,
comportamento oscilatório, variável ruidosa, relação sensor--atuador incoerente, condição mecânica
suspeita. Do ponto de vista arquitetural, esses estados são consumíveis por uma camada supervisória
sem que ela precise atuar diretamente sobre os sinais crus do controlador.

Uma observação crítica que emerge dessa literatura é que PI baixo não implica em
``resintonizar o PID''. Ele implica em ``a malha apresenta comportamento que não é bem explicado
pelo modelo de predição adotado; investigar a causa''. Essa separação entre detecção de anomalia e
ação corretiva é estruturalmente análoga ao padrão de sistemas distribuídos em que um observador
detecta um estado divergente e uma política separada decide a ação autorizada — sem que o observador
e o executor sejam o mesmo componente.

No contexto deste trabalho, o TEP oferece um ambiente adequado para investigar essas métricas, pois
disponibiliza múltiplas variáveis medidas e manipuladas sob condições de operação programáveis. A
calibração dos parâmetros de diagnóstico para as variáveis XMEAS e XMV do TEP será tratada na
metodologia experimental.

---

## Notas de revisão — respostas às questões abertas

As questões abertas da versão anterior foram respondidas pela revisão especializada:

1. **Harris vs. ARMA de ordem d**: CORRIGIDO. O texto anterior estava impreciso. Não se trata de
   "ARMA de ordem d". A estimativa usa um modelo univariado de série temporal para extrair a
   variância do erro de previsão $f+1$ passos à frente, onde $f$ é o atraso discreto efetivo.
   O "d" foi substituído por "$f$" para evitar conflito com a notação de grau de integração de
   modelos ARIMA.

2. **Parâmetros do PI ($m$, $b$, $n$)**: RESPONDIDO. Bradu (2018) define explicitamente
   $n = \lceil T_W/t_s \rceil$, $b = \lceil T/t_s \rceil$ e $m = 2b$. Incluídos no texto.

3. **Limiar PI < 0,7**: CORRIGIDO E REMOVIDO. O artigo usa limiares por grupos de controladores
   com valores como 0,2 e 0,4. O valor 0,7 aparece em um exemplo específico de uma malha
   considerada "boa" antes de uma alteração de sintonia — não como limiar metodológico geral.

4. **Tilaro 2017 e 2018**: INTEGRADOS. Cada artigo recebeu parágrafo próprio na subseção de
   padrões dinâmicos. Tilaro 2017 contribui com detecção de oscilações; Tilaro 2018 com
   aprendizado de modelos e coerência entre sinais.

5. **Conexão com o trabalho**: AJUSTADA. O parágrafo de conexão no Cap2 ficou conceitual. A
   calibração de parâmetros específicos para XMEAS/XMV do TEP foi deslocada explicitamente
   para o Cap4 (metodologia experimental).

6. **Relação Harris–PI**: RESOLVIDA. Harris é benchmark teórico de variância mínima (exige $f$,
   hipóteses de linearidade, avalia margem estrutural de melhoria). PI é indicador operacional de
   preditividade (model-free, parâmetros derivados de grandezas operacionais, funciona em
   larga escala). São complementares: PI indica prioridade de investigação; Harris ajuda a
   distinguir degradação potencialmente corrigível por feedback de limitações estruturais.

7. **Questão nova — Lessmeier 2016**: INCLUÍDO como extensão do princípio CLPM para
   monitoramento de condição mecânica. Relevante porque generaliza a ideia de "sinal
   disponível → estado inferido → condição supervisionável" para além de malhas de controle.
