# Elaboração — Seção 2.5: Integração e Modelagem Industrial: OPC UA e a Família IEC 62541

> Arquivo de rascunho — **segunda versão**, revisada a partir de 9 pares de arquivos de revisão especializada:
> - art6_ (UNICOS) + ft_UNICOS
> - book1_DigitalTwin + ft_DigitalTwin
> - book2_Introduction + ft_OPC-UA-Introduction
> - book2_Services + ft_OPC-UA-Services
> - book2_System-Architecture + ft_OPC-UA-System-Architecture
> - IEC_62264-1 + ft_IEC_62264-1
> - IEC_62541-1 + ft_IEC_62541-1
> - IEC_62541-3 + ft_IEC_62541-3
> - IEC 62541-8 + ft_IEC_62541-8

---

## Texto proposto

---

O diagnóstico de qualidade de malhas transformou séries temporais de processo em estados reconhecíveis: malha saudável, malha degradada, comportamento oscilatório, condição anômala. Essa transformação é necessária, mas insuficiente. O CLPM produz indicadores sobre o comportamento das malhas; ele não modela a planta como um sistema acessível a agentes externos, nem expõe variáveis, equipamentos, alarmes e históricos em uma forma que qualquer cliente externo possa navegar e interpretar. A mesma instituição que aplica diagnóstico de malhas no sistema criogênico do LHC desenvolveu o \textit{framework} UNICOS \cite{Gayet2004} exatamente para endereçar essa lacuna: organizar a planta como uma hierarquia de objetos de controle (*Process Control Objects* --- PCOs) com atributos de modo, estado e intertravamento, tornando-a acessível a sistemas supervisórios de forma estruturada. Para que uma camada supervisória possa observar o estado da planta, subscrever mudanças, consultar históricos e solicitar ações sobre equipamentos, é necessário que a planta exponha suas entidades em um modelo de informação estruturado, padronizado e independente de implementação. Esse é o problema que o OPC UA endereça.

O \textbf{OPC UA} (\textit{OPC Unified Architecture}), formalizado como família de normas internacionais \textbf{IEC~62541} \cite{IEC62541_1}, surgiu da necessidade de substituir os padrões clássicos OPC — baseados em COM/DCOM da Microsoft, restritos ao ecossistema Windows — por uma arquitetura independente de plataforma, orientada a serviços e com segurança nativa por criptografia de chave pública \cite{Mahnke2009intro}. A norma unifica funções antes fragmentadas em padrões distintos: acesso a dados em tempo real (DA), alarmes e eventos (AE) e acesso histórico (HDA). O elemento mais importante dessa arquitetura não é a camada de transporte — a especificação separa explicitamente os serviços abstratos de interação cliente-servidor dos mapeamentos concretos de comunicação \cite{Mahnke2009services} — mas o \textbf{modelo de informação}: o OPC UA define como entidades industriais são representadas, organizadas e expostas, não apenas como são transportadas.

### Espaço de Endereçamento e Modelo de Informação

O conceito central da IEC~62541-3 \cite{IEC62541_3} é o \textbf{espaço de endereçamento} (\textit{Address Space}): uma estrutura de nós (\textit{Nodes}) interconectados por referências tipadas (\textit{References}), que organiza de forma uniforme todos os dados, metadados, métodos e eventos expostos por um servidor OPC UA. Cada nó possui uma classe (\textit{NodeClass}) que define seu papel:

- **Object**: representa uma entidade industrial (e.g., reator, malha de controle, compressor).
- **Variable**: expõe um valor observável com *timestamp*, qualidade e tipo de dado.
- **Method**: define uma operação invocável por clientes autorizados.
- **ObjectType / VariableType**: tipos reutilizáveis que permitem modelar entidades de domínio.

Essa estrutura transforma a planta de uma coleção plana de *tags* numéricas para um **modelo de informação navegável**: um cliente externo pode descobrir a hierarquia do servidor com `Browse`, ler atributos e valores com `Read`, escrever variáveis autorizadas com `Write`, subscrever mudanças de valor e eventos com `Subscription`/`MonitoredItems`, e invocar operações com `Call` — tudo por serviços padronizados, independentes da implementação interna do servidor \cite{Mahnke2009services}. Essa distinção é relevante: um cliente OPC UA não depende do conhecimento prévio dos detalhes internos do simulador ou do fornecedor; ele descobre a estrutura navegando o modelo e acessando os metadados de cada nó.

### Família de Normas IEC 62541

A IEC~62541 é organizada em múltiplas partes, cada uma cobrindo um aspecto distinto da especificação. As partes mais relevantes para este trabalho:

| Parte | Título                   | Versa sobre                                                              |
| ----- | ------------------------ | ------------------------------------------------------------------------ |
| 1     | Visão Geral e Conceitos  | Fundamentos, terminologia e motivação do padrão                          |
| 3     | Modelo do Espaço de End. | Nós, referências, navegação — base de todo modelo de informação          |
| 4     | Serviços                 | Serviços abstratos cliente-servidor: Browse, Read, Write, Subscribe, Call |
| 8     | Acesso a Dados           | `AnalogItemType`, `DiscreteItemType`, unidade, faixa, qualidade          |
| 9     | Alarmes e Condições      | Modelo de alarmes e condições operacionais; limites e interlocks          |
| 11    | Acesso Histórico         | Séries temporais: leitura e agregação de dados históricos                |
| 14    | PubSub                   | Publish-subscribe sobre MQTT/AMQP/UDP                                    |

### Acesso a Dados: Parte 8

A **Parte 8** \cite{IEC62541_8} é particularmente relevante para expor variáveis de processo. Ela define o `DataItemType` como tipo base para dados vivos de automação, a partir do qual derivam três famílias:
- `AnalogItemType`: grandezas contínuas com unidade de engenharia (*EngineeringUnits*), faixa operacional (*EURange*) e faixa instrumental (*InstrumentRange*).
- `DiscreteItemType`: estados discretos como modos operacionais, flags ou sinalizadores.
- `ArrayItemType`: dados estruturados como espectros, curvas ou janelas de histórico.

As leituras OPC UA carregam *StatusCode* (qualidade *Good*/*Uncertain*/*Bad*) e *timestamp*, permitindo que clientes distingam valor numérico de confiabilidade da medição. As medições contínuas do TEP podem ser mapeadas conceitualmente a variáveis do tipo `AnalogItemType`, preservando unidade de engenharia e faixa operacional; medições provenientes de analisadores amostrados, com atraso inerente, requerem metadados temporais adicionais.

### Arquitetura de Sistema: Aggregating Server e Discovery

A arquitetura de sistema do OPC UA é concebida para operar em múltiplas camadas industriais, de dispositivos de campo até sistemas corporativos \cite{Mahnke2009arch}. O padrão básico é cliente-servidor: um cliente consome serviços oferecidos por um servidor. Para cenários com múltiplas fontes de informação, a norma descreve o padrão **Aggregating Server**: um servidor intermediário que incorpora um cliente OPC UA interno e consulta múltiplos servidores subjacentes, processando ou preparando os dados recebidos antes de devolvê-los ao cliente solicitante \cite{Mahnke2009arch}. Para uma camada supervisória que precisa consolidar variáveis de processo, diagnósticos de malha e restrições operacionais em um estado de mais alto nível, esse padrão oferece uma referência arquitetural importante: o orquestrador não precisa consumir diretamente cada sinal cru da planta, mas pode operar sobre um estado consolidado produzido por uma camada intermediária. O mecanismo de **Discovery** complementa essa arquitetura ao permitir que clientes localizem servidores disponíveis sem conhecer previamente todos os *endpoints*, reduzindo o acoplamento entre os componentes do sistema.

### IEC 62264 e Posicionamento no Nível 3

A norma **IEC~62264** \cite{IEC62264} (*Enterprise-Control System Integration*) organiza as funções industriais em níveis hierárquicos derivados do Modelo Purdue. O Nível 3 é o domínio do *Manufacturing Operations Management* (MOM): monitoramento de processos, gestão de produção, qualidade, manutenção e desempenho operacional. A norma organiza a informação desse domínio em quatro categorias: *schedule* (o que deve ser executado), *performance* (o que foi realizado), *definition* (como executar) e *capability* (quais recursos estão disponíveis). Essa estrutura é relevante para o projeto porque posiciona a camada supervisória proposta no Nível 3 — acima do controle regulatório direto (Níveis 0–2) — e porque aproxima a lógica industrial da lógica declarativa: a distinção entre o que deve ser feito (*schedule*/*definition*) e o que está sendo feito e o que é viável (*performance*/*capability*) guarda semelhança estrutural com a separação entre estado desejado e estado observado que fundamenta a reconciliação supervisória.

### Encerramento

No âmbito deste referencial, o OPC UA e a IEC~62541 ocupam um papel específico: fornecem a linguagem padronizada pela qual a planta se torna um modelo de informação acessível a agentes externos. O CLPM define *o que* observar; o OPC UA define *como* esses observáveis são expostos em uma estrutura navegável, tipada e semanticamente organizada. A camada supervisória pode então operar sobre estados industriais interpretáveis — em vez de sinais brutos — sem assumir o papel de controlador regulatório. A implementação concreta dessa interface, incluindo as decisões de mapeamento das variáveis do TEP e os mecanismos de comunicação adotados, é tratada nos capítulos subsequentes.

---

## Notas de revisão — correções aplicadas

1. **Nome da seção alterado.**
   "OPC UA e a Família de Normas IEC~62541" → "Integração e Modelagem Industrial: OPC UA e a Família IEC~62541". O novo nome captura o papel da seção na narrativa: a avaliação de malhas (CLPM) expõe o que observar; a integração e modelagem (OPC UA) expõe como a planta se torna acessível.

2. **Parágrafo de transição adicionado (abertura).**
   Contrapõe o que o CLPM *não* faz: diagnostica, mas não modela a planta como objeto acessível a sistemas externos. Essa contração era a lacuna narrativa que motivava esta seção.

3. **"OPC UA é o protocolo e IEC 62541 é o vocabulário" — removido.**
   Substituído por: OPC UA é uma arquitetura de comunicação e modelagem de informação industrial; a IEC 62541 formaliza essa arquitetura. A IEC 62541 não é "o vocabulário" — é a família normativa que define serviços, modelo de informação, segurança e mapeamentos.

4. **"transportável sobre qualquer rede IP" — corrigido.**
   Removido. A especificação separa os serviços abstratos dos mapeamentos concretos de transporte. A frase original criava uma afirmação ampla sem base precisa.

5. **Part 4 — "API completa" — corrigido.**
   "API completa: Read, Write, Browse, Subscribe, Call" → "Serviços abstratos cliente-servidor: Browse, Read, Write, Subscribe, Call". Part 4 define serviços abstratos, não uma API de linguagem.

6. **"Alarmes e Condições — mapeável aos ISDs do TEP" — corrigido.**
   Substituído por "modelo de alarmes e condições operacionais; limites e interlocks". ISD é lógica de intertravamento/parada; Part 9 modela a *representação* de condições anormais, não a lógica de proteção em si.

7. **DeadBand — removido do texto principal.**
   Não é comportamento universal de toda Subscription. Mantida apenas a menção genérica a MonitoredItems e filtros de mudança.

8. **AnalogItemType — suavizado.**
   "metadados que as XMEAS do TEP possuem intrinsecamente" → formulação que reconhece que medições de analisadores amostrados requerem metadados adicionais.

9. **"IDV como métodos invocáveis" — removido do Cap2.**
   Decisão de engenharia, não consequência direta da norma. Movida para capítulos de metodologia/arquitetura.

10. **Parágrafo "integração futura prevista" — removido/substituído.**
    Eliminou referência a "gêmeo digital" (contradiz o posicionamento da revisão book1_DigitalTwin), a "integração futura prevista" (antecipa Cap4/5) e à arquitetura específica gRPC. Substituído por parágrafo de encerramento genérico e defensável.

11. **Aggregating Server — adicionado.**
    Novo parágrafo baseado em book2_System-Architecture (ft_). É o padrão arquitetural mais relevante para o TCC: o orquestrador consome um estado consolidado de múltiplas fontes, não sinais crus.

12. **Discovery — adicionado brevemente.**
    Mencionado como mecanismo de desacoplamento entre componentes do sistema.

13. **IEC 62264 — fortalecido.**
    Anterior: menção breve sem função. Agora: descreve o domínio MOM e as quatro categorias de informação (*schedule*/*performance*/*definition*/*capability*), conectando explicitamente ao Nível 3 e à distinção estado desejado/observado.

14. **"Digital Twin" — eliminado.**
    Revisão book1_DigitalTwin confirma: o TEP implementado em Rust não é um Digital Twin estrito (não há planta física sendo espelhada). Qualquer menção de Digital Twin foi removida desta seção.

15. **"adotado por praticamente todos os fabricantes relevantes" — suavizado.**
    Substituído por afirmação defensável baseada em referência normativa.
