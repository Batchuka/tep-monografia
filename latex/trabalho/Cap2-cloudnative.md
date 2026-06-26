# Elaboração — Seção 2.4: Cloud-Native como Paradigma de Orquestração Industrial

> Arquivo de rascunho — segunda versão, revisada a partir de:
> - art12_ (GPT especializado em Shuiguang 2023) + ft_Cloud-Native-Computing...
> - art5_ (GPT especializado em Burns 2016) + ft_Borg-Omega-and-Kubernetes
> - art10_ (GPT especializado em Johansson 2022) + ft_Kubernetes-Orchestration...
> - art11_ (GPT especializado em Mellado 2022) + ft_Design-of-an-IoT-PLC...

---

## Texto proposto

---

O termo \textit{cloud-native} designa uma abordagem de desenvolvimento e operação de sistemas
distribuídos que explora recursos típicos da computação em nuvem --- conteinerização,
microsserviços, orquestração automática de containers, DevOps e pipelines de entrega contínua
\cite{Shuiguang2023}. Conforme \citeonline{Shuiguang2023}, uma aplicação cloud-native pode ser
entendida como um sistema distribuído, elástico e escalável horizontalmente, composto por
microsserviços inter-relacionados empacotados em containers leves e orquestrados sobre múltiplos
servidores. Nesse paradigma, a orquestração é descrita pelos autores como a configuração, o
gerenciamento e a coordenação automatizados do ciclo de vida dos containers --- provisionamento,
implantação, agendamento, escalonamento, configuração de rede e balanceamento de carga --- de modo a
manter as funcionalidades da aplicação elásticas e disponíveis. O Kubernetes, originado do
gerenciador de clusters Borg do Google, é descrito pelos mesmos autores como o software open-source
de orquestração de containers mais popular e como um padrão de fato amplamente adotado pela
indústria.

\citeonline{Burns2016} documentam a evolução dos sistemas de orquestração do Google --- Borg, Omega
e Kubernetes --- e mostram que a força do Kubernetes está na combinação de uma API uniforme, objetos
extensíveis e separação explícita entre estado desejado e estado observado. Cada recurso Kubernetes
é representado como um objeto com dois campos centrais: \textit{Spec}, que descreve o estado
desejado, e \textit{Status}, que registra o estado observado em tempo de execução. Sobre essa
estrutura, operam controladores de reconciliação --- \textit{reconciliation controller loops} ---
que comparam continuamente o estado desejado ao estado observado e executam ações para convergir o
segundo em direção ao primeiro \cite{Burns2016}. Além disso, os autores destacam que a
conteinerização muda o paradigma operacional dos data centers: de uma perspectiva orientada a
máquinas para uma perspectiva orientada a aplicações, na qual gerenciar containers significa
gerenciar aplicações, não servidores. Essa combinação de API uniforme, objetos Spec/Status,
controladores de reconciliação e extensibilidade torna o Kubernetes uma plataforma de operação
declarativa para sistemas distribuídos complexos.

A atuação do Kubernetes, embora descrita por abstrações como objetos, serviços e configurações,
possui consequências concretas sobre a infraestrutura: processos são alocados em máquinas, instâncias
são criadas ou removidas, componentes falhos são detectados e reimplantados, rotas de comunicação são
atualizadas conforme o estado da aplicação e limites de CPU e memória são impostos por política
declarada. Para os objetivos deste trabalho, um aspecto particularmente relevante dessa arquitetura é
que decisões discretas de orquestração --- reimplantar um componente, atualizar uma rota,
reescalonar uma instância --- produzem efeitos diretos sobre quais serviços estão disponíveis e como
eles se comunicam. No ecossistema Kubernetes, essa lógica declarativa pode ser estendida pelo
\textit{Operator Pattern}, no qual controladores específicos de domínio observam recursos customizados
e executam ações de reconciliação sobre aplicações ou sistemas externos ao cluster.

A relevância desse paradigma para sistemas industriais não está em substituir controladores
regulatórios ou malhas de tempo real, mas em oferecer uma forma de organizar camadas superiores de
operação: implantação e ciclo de vida de serviços, supervisão de componentes distribuídos,
observabilidade, tolerância a falhas, aplicação de políticas e coordenação de estados operacionais.
Nesse enquadramento, cloud-native e Kubernetes são considerados como referências para a camada
supervisória e informacional do sistema, preservando a distinção entre controle regulatório da planta
e orquestração da infraestrutura de software.

\subsubsection*{Precedentes industriais}

Trabalhos recentes indicam que essa aproximação entre infraestrutura cloud-native e automação
industrial já é objeto de pesquisa. \citeonline{Johansson2022} investigam o uso de Kubernetes para
orquestrar nós controladores distribuídos virtualizados (\textit{Virtual Distributed Control Nodes},
VDCNs) em cenários de alta disponibilidade. O artigo não desloca a malha de controle em tempo real
para o Kubernetes; a lógica de controle permanece no interior dos VDCNs. Entretanto, a plataforma
passa a executar o agendamento situacional dos containers, gerenciar os laços de reconciliação que
empurram o estado atual em direção ao estado desejado e atualizar as rotas de comunicação conforme
o estado da aplicação --- o que determina qual instância VDCN recebe comandos OPC UA e, portanto,
qual controlador participa ativamente da operação. Diante de falhas, o Kubernetes detecta o nó
afetado e reimplanta o VDCN correspondente; no caso redundante, o backup assume como primário e o
Kubernetes cria um novo backup. Esse resultado é relevante porque mostra um precedente em que
Kubernetes é usado não apenas como infraestrutura genérica, mas como camada responsável por
recompor componentes de controle industrial diante de falhas, com efeito direto sobre a
continuidade operacional do sistema.

\citeonline{Mellado2022} propõem o IoT-PLC, uma arquitetura baseada em containers para CLPs
orientados à Indústria 4.0, na qual cada funcionalidade --- controle regulatório, armazenamento de
dados de campo, interfaces sem fio --- é encapsulada em um container separado. O IoT-PLC é
posicionado como nó de fog computing, mantendo a execução próxima à planta enquanto permite
gerenciamento direto a partir da nuvem, reconfiguração a quente de malhas de controle e ajuste de
recursos computacionais sem interromper o processo. O artigo também utiliza um \textit{modelo de
dispositivo virtual} que abstrai a interface do controlador para camadas superiores. Embora não
constitua uma implementação baseada em Kubernetes, o IoT-PLC é relevante como antecedente
conceitual: ele mostra que a literatura industrial já considera plausível decompor funções de CLP
em componentes conteinerizados, reconfiguráveis e gerenciáveis externamente, e representa entidades
físicas por abstrações digitais acessíveis a camadas superiores --- uma preocupação compatível com a
lógica de recursos declarativos usada em arquiteturas cloud-native.

Em conjunto, esses trabalhos indicam uma convergência entre práticas cloud-native e sistemas
industriais, mas também delimitam seu escopo. Uma limitação importante é que o Kubernetes não foi
projetado para controle determinístico de tempo real: seus mecanismos de agendamento, reinicialização
e redistribuição de cargas são adequados para disponibilidade e operação de aplicações distribuídas,
mas não garantem, por si só, tempos de resposta compatíveis com malhas regulatórias industriais.
A contribuição mais defensável dos princípios cloud-native está na camada supervisória --- observação
de componentes distribuídos, manutenção de configurações desejadas, recomposição de serviços após
falhas e disponibilização de abstrações operacionais para camadas superiores ---, sem substituir a
execução determinística de controladores de baixo nível. A integração com sistemas industriais
pressupõe ainda uma camada de comunicação capaz de representar medições, comandos e estados de
equipamentos de forma estruturada; protocolos como OPC UA são relevantes nesse ponto, funcionando
como possível interface entre a camada de orquestração e os ativos de automação.

---

## Notas de revisão — correções aplicadas

1. **Antecipação do Cap5 removida.**
   As frases "é o mesmo que fundamenta a proposta de usar o Kubernetes como plataforma supervisória
   neste trabalho" e "precursor direto do CRD `PLCMachine` proposto neste trabalho" foram removidas.
   O texto agora formula conexões conceituais neutras, sem nomear a arquitetura própria deste
   trabalho antes do Cap5.

2. **Shuiguang2023 — atribuição corrigida.**
   O texto anterior atribuía ao artigo a tese "a essência do paradigma é a separação entre estado
   desejado e orquestração", o que é uma interpretação do autor, não necessariamente a tese central
   do artigo. Shuiguang2023 é agora usado para: (a) definição formal de cloud-native, (b) definição
   de orquestração como ciclo de vida automatizado de containers, (c) Kubernetes como padrão de fato.
   A conexão com estado desejado/reconciliação migrou corretamente para Burns2016.

3. **Burns2016 — expandido e menos simplificado.**
   O texto anterior reduzia Burns2016 ao "salto qualitativo = API declarativa". O texto revisado
   descreve a combinação completa: API uniforme, objetos Spec/Status, controladores de reconciliação,
   paradigma orientado a aplicações (não a máquinas), extensibilidade. A frase "salto qualitativo foi
   exatamente a API declarativa" foi removida. A citação direta de Spec/Status e do loop de
   reconciliação (verificada nas ft_ anotações do artigo original) torna a atribuição mais precisa.

4. **Johansson2022 — "mesmos níveis de disponibilidade" removido.**
   Substituído por: Kubernetes executa agendamento situacional, reconciliação, atualização de rotas
   e reimplantação de VDCNs após falha, com efeito direto sobre qual controlador participa da
   operação. O papel de OPC UA como protocolo de comunicação entre Kubernetes e VDCNs foi
   mencionado (baseado nas ft_ anotações que confirmam que roteamento Kubernetes afeta quem recebe
   OPC UA). A afirmação limitada a "demonstra viabilidade experimental" em vez de equivalência geral.

5. **Mellado2022 — "precursor direto" substituído por "antecedente conceitual".**
   O IoT-PLC usa Docker/containerização, não Kubernetes. A conexão com CRD foi removida.
   O artigo é posicionado como antecedente conceitual de: (a) decomposição de funções industriais
   em containers, (b) gestão externa via nuvem, (c) reconfiguração a quente, (d) modelo de
   dispositivo virtual para abstração com camadas superiores. O foco no paradigma fog computing
   (solução para integração IT/OT) foi incluído com base nas ft_ anotações.

6. **Parágrafo de transição adicionado.**
   Inserido entre os precedentes industriais e a definição de cloud-native: explicita que a
   relevância do paradigma está na camada supervisória, não na substituição do controle regulatório.
   Distingue orquestração de infraestrutura de software de controle regulatório da planta.

7. **Limitações adicionadas.**
   Parágrafo final explicita: Kubernetes não é plataforma de controle determinístico de tempo real;
   sua contribuição defensável está na camada supervisória; a integração com ativos industriais exige
   protocolos estruturados como OPC UA.

8. **Operator Pattern preparado.**
   Inserida menção ao Operator Pattern no terceiro parágrafo, criando a ponte para o Cap5 sem
   antecipar a arquitetura específica deste trabalho.
