---
annotation-target: articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf
titulo: Model Learning Algorithms for Anomaly Detection in CERN Control Systems
autor: Tilaro, F.; Bradu, B.; Berges, A.; Varela, C.; Roshchin, M.
ano:
fonte:
tema: politica_supervisao/tecnica
---

## O que diz


## O que me interessa


## Conexões

- [[]]

## Citação ABNT

```bibtex
@article{ART8,
  author  = {},
  title   = {},
  journal = {},
  year    = {},
}
```
























>%%
>```annotation-json
>{"created":"2026-06-18T00:57:48.485Z","text":"Segundo esse artigo, os dados informam o estado atual, o desempenho, a estabilidade e o comportamento geral do processo. Ele defende uma abstração portanto.\n\n```yaml\napiVersion: tep.lab/v1\nkind: ProcessUnit\nmetadata:\n  name: reactor\nstatus:\n  stability: Degraded\n  performance: BelowExpected\n  observedSignals:\n    - XMEAS_9   # reactor temperature\n    - XMV_10    # reactor cooling water valve\n```\nOu seja, o k8s não sabe que a temperatura é sei lá, 122.4c, ele sabe que está degradada.","updated":"2026-06-18T00:57:48.485Z","document":{"title":"Model Learning Algorithms for Anomaly Detection in CERN Control SystemsModel Learning Algorithms for Anomaly Detection in CERN Control Systems","link":[{"href":"urn:x-pdf:82924ab786d8a7dc9e12e085f805a8bd"},{"href":"vault:/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf"}],"documentFingerprint":"82924ab786d8a7dc9e12e085f805a8bd"},"uri":"vault:/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","target":[{"source":"vault:/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","selector":[{"type":"TextPositionSelector","start":2760,"end":2883},{"type":"TextQuoteSelector","exact":"source of useful information about the current state of the processes, their performance, stability and over-all behaviour.","prefix":"proper analysis, con-stitutes a ","suffix":" Obviously, an extensive analysi"}]}]}
>```
>%%
>*%%PREFIX%%proper analysis, con-stitutes a%%HIGHLIGHT%% ==source of useful information about the current state of the processes, their performance, stability and over-all behaviour.== %%POSTFIX%%Obviously, an extensive analysi*
>%%LINK%%[[#^u2k431tfjlm|show annotation]]
>%%COMMENT%%
>Segundo esse artigo, os dados informam o estado atual, o desempenho, a estabilidade e o comportamento geral do processo. Ele defende uma abstração portanto.
>
>```yaml
>apiVersion: tep.lab/v1
>kind: ProcessUnit
>metadata:
>  name: reactor
>status:
>  stability: Degraded
>  performance: BelowExpected
>  observedSignals:
>    - XMEAS_9   # reactor temperature
>    - XMV_10    # reactor cooling water valve
>```
>Ou seja, o k8s não sabe que a temperatura é sei lá, 122.4c, ele sabe que está degradada.
>%%TAGS%%
>
^u2k431tfjlm
