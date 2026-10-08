# Análise de graus de liberdade do TEP em Larsson & Skogestad (2000)

Este arquivo resume, para uso na monografia, a análise de graus de liberdade do Tennessee Eastman Process (TEP) conforme apresentada no artigo **“Plantwide control — A review and a new design procedure”** de Larsson e Skogestad (2000).

> Observação importante: o artigo revisa e resume resultados aplicados ao TEP, mas nem todos os detalhes estão explicitamente listados nele. Quando uma informação não aparece diretamente, isso é indicado.

---

## 1. Extração do artigo

### 1.1 Graus de liberdade do TEP em regime estacionário

**O que o artigo diz:**  
Na seção 7.4, o artigo afirma que uma análise de graus de liberdade revela que o TEP possui:

> **8 graus de liberdade em regime estacionário.**

**O que não está no artigo:**  
O artigo **não lista quais são esses 8 graus de liberdade** como variáveis manipuladas específicas, nem faz a correspondência direta com as 12 variáveis manipuladas `XMV`.

A referência indicada para a análise detalhada é o trabalho específico de Larsson e Skogestad sobre controle *self-optimizing* do TEP:

> Larsson, T. and Skogestad, S. (2000). *Self-optimizing control of a large-scale plant: The Tennessee Eastman process.*

---

### 1.2 Restrições ativas no ponto ótimo do Modo 1

**O que o artigo diz:**  
Na seção 7.4, o artigo afirma que, no caso nominal, isto é, no **Modo 1**, há:

> **5 restrições ativas no ponto ótimo.**

O artigo atribui essa informação a **Ricker (1995)**.

**Onde aparecem os nomes prováveis dessas restrições:**  
Na seção 7.1, o artigo resume o resultado de Ricker (1995), dizendo que é ótimo operar com:

1. pressão do reator no máximo;
2. nível do reator no mínimo;
3. velocidade do agitador no máximo;
4. abertura da válvula de vapor no mínimo;
5. abertura da válvula de reciclo do compressor no mínimo, na maioria dos casos.

**Separação rigorosa:**  
O artigo **não apresenta explicitamente** a frase “as 5 restrições ativas do Modo 1 são...”.  
A lista acima é uma conexão interpretativa entre o resumo de Ricker (1995) na seção 7.1 e a afirmação da seção 7.4 sobre as 5 restrições ativas.

---

### 1.3 Três graus de liberdade restantes

**O que o artigo diz:**  
Como há 8 graus de liberdade em regime estacionário e 5 restrições ativas no ponto ótimo nominal, o artigo afirma que sobram:

> **3 graus de liberdade não restringidos.**

**O que não está no artigo:**  
O artigo **não identifica esses 3 graus livres como manipuladores específicos**. Ele passa diretamente para a discussão de quais variáveis controladas são boas escolhas para consumir esses graus de liberdade livres.

---

### 1.4 Variáveis controladas boas e ruins para os 3 graus livres

**Boas escolhas indicadas pelo artigo:**  
O artigo afirma que boas propriedades *self-optimizing* são obtidas controlando, além das variáveis em restrições ativas:

1. temperatura do reator;
2. vazão de reciclo ou trabalho do compressor;
3. composição de A na purga ou na alimentação do reator.

O artigo também afirma que a sugestão de Ricker (1996), composta por:

1. temperatura do reator;
2. A na alimentação do reator;
3. C na alimentação do reator;

está entre as melhores escolhas do ponto de vista *self-optimizing*.

**Escolhas ruins indicadas pelo artigo:**  

O artigo afirma que:

1. a composição do inerte B **não deve ser controlada** no caso estudado;
2. para produção fixa, também não devem ser escolhidas como variáveis controladas:
   - vazões de alimentação dos reagentes;
   - vazão de purga;
   - vazão de alimentação do reator.

---

## 2. Código TikZ para figura

Código para colar dentro de um ambiente `figure`.

```latex
\centering
\begin{tikzpicture}[font=\small]

% --- dimensões ---
\def\w{1.15}
\def\h{1.0}

% --- barra de 8 graus de liberdade ---
\foreach \i in {0,...,4} {
  \draw[fill=black!20] (\i*\w,0) rectangle ++(\w,\h);
}
\foreach \i in {5,...,7} {
  \draw[fill=black!5] (\i*\w,0) rectangle ++(\w,\h);
}

% --- rótulos internos ---
\node[align=center] at (2.5*\w,0.5*\h) {5 restrições\\ativas};
\node[align=center] at (6.5*\w,0.5*\h) {3 graus\\livres};

% --- contorno geral ---
\draw[thick] (0,0) rectangle (8*\w,\h);
\draw[thick] (5*\w,0) -- (5*\w,\h);

% --- título da barra ---
\node[align=center,font=\bfseries] at (4*\w,1.55) {
TEP em regime estacionário: 8 graus de liberdade
};

% --- explicação das 5 restrições ---
\node[align=center,text width=5.3cm] at (2.5*\w,-1.05) {
Mantidos em limites economicamente ativos\\
no ponto ótimo nominal
};

% --- explicação dos 3 livres ---
\node[align=center,text width=5.0cm] at (6.5*\w,-1.05) {
Usados para escolher variáveis\\
controladas self-optimizing
};

% --- boas escolhas ---
\node[draw,fill=black!5,align=left,text width=5.4cm,anchor=north] at (6.5*\w,-2.0) {
\textbf{Boas escolhas indicadas:}\\
-- temperatura do reator;\\
-- vazão de reciclo ou trabalho do compressor;\\
-- composição de A na purga ou na alimentação.
};

% --- escolhas ruins ---
\node[draw,fill=black!15,align=left,text width=5.4cm,anchor=north] at (6.5*\w,-4.05) {
\textbf{Escolhas ruins indicadas:}\\
-- composição do inerte B;\\
-- vazões de alimentação dos reagentes;\\
-- vazão de purga ou alimentação do reator.
};

% --- observação sobre a fonte ---
\node[align=center,text width=9.0cm,font=\footnotesize] at (4*\w,-6.1) {
Nota: o artigo informa os 8 graus de liberdade, as 5 restrições ativas e os 3 graus livres,
mas não lista os 8 graus de liberdade como variáveis manipuladas específicas.
};

\end{tikzpicture}
```

Legenda sugerida:

```latex
\caption{Resumo da análise de graus de liberdade do TEP segundo Larsson e Skogestad:
8 graus de liberdade em regime estacionário, 5 restrições ativas no ótimo nominal e
3 graus livres para escolha de variáveis controladas self-optimizing.}
```

---

## 3. Tabela LaTeX alternativa

```latex
\begin{table}[ht]
\centering
\caption{Resumo da análise de graus de liberdade do TEP em Larsson e Skogestad.}
\label{tab:tep_dof_larsson_skogestad}
\begin{tabular}{p{0.28\textwidth} p{0.58\textwidth}}
\hline
\textbf{Item} & \textbf{Informação extraída do artigo} \\
\hline

Graus de liberdade em regime estacionário
&
O TEP possui 8 graus de liberdade em regime estacionário.
O artigo não lista quais são esses 8 graus como variáveis manipuladas específicas. \\

\hline

Restrições ativas no Modo 1
&
No modo nominal, 5 restrições estão ativas no ponto ótimo.
O artigo atribui essa informação a Ricker (1995). Em seção anterior, resume como
ótimos: pressão do reator máxima, nível do reator mínimo, velocidade do agitador máxima,
válvula de vapor mínima e, na maioria dos casos, válvula de reciclo do compressor mínima. \\

\hline

Graus livres restantes
&
Como 5 dos 8 graus de liberdade são consumidos por restrições ativas,
restam 3 graus de liberdade não restringidos. \\

\hline

Boas variáveis controladas
&
Temperatura do reator; vazão de reciclo ou trabalho do compressor;
composição de A na purga ou na alimentação do reator. O artigo também afirma que
a combinação proposta por Ricker (1996), com temperatura do reator, A na alimentação
e C na alimentação, está entre as melhores escolhas do ponto de vista self-optimizing. \\

\hline

Más variáveis controladas
&
Composição do inerte B não deve ser controlada no caso estudado.
Para produção fixa, o artigo também desencoraja selecionar vazões de alimentação
dos reagentes, vazão de purga ou vazão de alimentação do reator como variáveis controladas. \\

\hline
\end{tabular}
\end{table}
```

---

## 4. Observação crítica para a monografia

A figura é defensável se a legenda ou o texto ao redor deixar claro que o artigo fornece a decomposição:

\[
8 = 5 + 3
\]

mas **não lista os 8 manipuladores estacionários**.

Portanto, a formulação mais segura é:

> “Larsson e Skogestad reportam que o TEP possui 8 graus de liberdade em regime estacionário; no Modo 1, 5 restrições estão ativas no ótimo, restando 3 graus livres para a seleção de variáveis controladas self-optimizing.”

Evite escrever:

> “Os 8 graus de liberdade são...”

a menos que você use uma fonte adicional que liste explicitamente esses manipuladores, como Ricker (1995) ou o artigo específico de Larsson e Skogestad sobre *self-optimizing control* do TEP.
