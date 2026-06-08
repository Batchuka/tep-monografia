---
type: brainstorming
tema: ecossistema de controle industrial científico
gatilho: pesquisa sobre frameworks do CERN e tecnologias relacionadas ao TCC
conecta-com:
  - IEC 62541
data: 2026-06-06
tags:
  - Cap2-referencialTeorico
  - Cap5-conclusao
status: incubando
---

# bs_exploracao-tecnologias_20260606

## Ideia bruta

Enquanto desenvolvia o projeto, fui entendendo que o mundo do controle industrial científico (CERN, telescópios, aceleradores) tem um ecossistema rico e bem consolidado que é quase desconhecido na engenharia de automação convencional. As tecnologias que encontrei:

**Frameworks do CERN:**
- **JCOP** (Joint Controls Project, 1998) — framework de controle/supervisão de experimentos baseado em WinCC OA
- **UNICOS** (UNified Industrial Control System) — framework CERN para aplicações de controle industrial; tem variante open-source
  - **UNICOS-SCADA** — camada de supervisão
  - **UNICOS-CPC** (Continuous Process Controls) — controle de processos contínuos

**Frameworks de física experimental:**
- **EPICS** — infraestrutura de controle distribuído para aceleradores, telescópios e grandes experimentos; usa IOCs (Input/Output Controllers) e PVs (Process Variables) — análogo direto às XMEAS/XMV do TEP
- **TANGO Controls** — framework orientado a dispositivos; modela bomba, válvula, sensor como *device servers* com atributos, comandos e estados

**SCADA comercial:**
- **WinCC OA** (Siemens) — plataforma SCADA usada como base do JCOP; supervisão, alarmes, tendências, histórico

**Repositórios para explorar:**
- `epics-containers/example-services` — beamline simulada com Docker Compose; melhor ponto de entrada para entender EPICS na prática
- `epics-base/epics-base` — núcleo C/C++ do EPICS; IOC, records, Channel Access
- `ska-telescope/tango-example` — devices simples em PyTango (SKA Telescope)
- `bluesky/ophyd` — abstração de hardware em Python para orquestração experimental

**OPC UA como ponte:**
O OPC UA (IEC 62541) aparece como o protocolo de interoperabilidade que conecta esses mundos: EPICS pode publicar PVs via OPC UA; TANGO tem bridges OPC UA; WinCC OA fala OPC UA nativamente. É o "idioma comum" entre sistemas heterogêneos.

## Para qual capítulo isso vai?

Capítulo: **Cap 5 — Trabalhos Futuros** (seção sobre EPICS/TANGO e frameworks do CERN) e **Cap 2 — Referencial Teórico** (contexto de sistemas de controle científico como motivação para a abordagem proposta)

## Conexões identificadas

- [[notes/standard/IEC 62541]] — OPC UA como protocolo de integração entre esses frameworks
- 'Cap2-referencialteorico' — EPICS e TANGO como referência arquitetural para XMEAS/XMV como variáveis observáveis
- Cap5-conclusao — JCOP/UNICOS/EPICS como direção de evolução do laboratório TEP

## Próximo passo

- [ ] Criar nota `doc_cern-frameworks.md` com descrição técnica de JCOP, UNICOS e UNICOS-CPC
- [ ] Criar nota `doc_epics-tango.md` comparando EPICS e TANGO com a arquitetura do TEP
- [ ] Avaliar se a seção de trabalhos futuros do Cap 5 deve mencionar EPICS/TANGO explicitamente
- [ ] Clonar `epics-containers/example-services` para entender a estrutura de IOCs na prática
