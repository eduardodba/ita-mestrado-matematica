# Tema 01 — Análise Combinatória e Contagem 🔴

**Prioridade: ALTA.** Cai todo ano (1 a 3 questões). O padrão **coloração de sólidos com rotações**
apareceu em 2021, 2024, 2025 e 2026 — vale ouro dominar o método.

---

## 1. Conceitos e teoremas que você precisa saber

### 1.1 Princípio Fundamental da Contagem (multiplicativo)
Se uma decisão pode ser tomada de `m` formas e outra de `n` formas (independentes),
o total de combinações é `m × n`. Estende-se a quantas etapas quiser.

### 1.2 Permutação
- **Simples:** ordenar `n` objetos distintos → `P(n) = n!`
- **Com repetição:** `n` objetos com grupos repetidos (n₁, n₂, …) → `n! / (n₁! · n₂! · …)`
- **Circular:** ordenar `n` objetos em círculo → `(n−1)!` (fixa-se um para quebrar a rotação)

### 1.3 Arranjo e Combinação
- **Arranjo** (ordem importa), escolher `k` de `n`: `A(n,k) = n! / (n−k)!`
- **Combinação** (ordem NÃO importa): `C(n,k) = n! / [k!(n−k)!]`
- Relação útil: `C(n,k) = C(n, n−k)`.

### 1.4 Caminhos em grade (lattice paths)
Ir de um canto ao outro de uma grade m×n, só para direita/baixo:
número de caminhos = `C(m+n, m)` (escolher quais passos são "direita").
Para excluir um ponto B: `total − (caminhos que passam por B)`.

### 1.5 Contagem com simetria — Lema de Burnside 🌟
Para contar colorações distintas **a menos de rotações** (cubo, sólidos):

> Nº de colorações distintas = (1/|G|) · Σ (colorações fixadas por cada rotação g)

onde `|G|` = número de rotações do grupo de simetria.
- **Cubo:** o grupo de rotações tem **24** elementos.
- Para casos simples, dá para contar "na mão" fixando uma face de referência.

**Atalho prático para o cubo (pintar 6 faces com 6 cores distintas):**
`6! / 24 = 30` esquemas (foi essencialmente a questão 12 de 2025).

### 1.6 Interseções de diagonais / regiões
- Pontos de interseção das diagonais de um polígono convexo de n lados (posição genérica): `C(n,4)`
  (cada 4 vértices definem exatamente 1 cruzamento interno).
- `k` retas em posição genérica (sem paralelas, sem 3 concorrentes) dividem o plano em
  `1 + k + C(k,2)` regiões.

---

## 2. Resoluções comentadas (questões reais do ITA)

### 📌 2025 — Q11: Caminhos num quadrado
*"How many different paths from the highest vertex to the lowest one...following the arrows?"*

**Conceito:** caminhos em grade. Conta-se somando, em cada nó, o número de formas de chegar nele
(somando os nós anteriores que apontam para ele). O resultado foi **(e) 20**.
**Lição:** quando a figura não é uma grade retangular limpa, use a **soma acumulada nó a nó**
(mesma ideia do triângulo de Pascal). Rápido e sem erro.

### 📌 2025 — Q12: Pintar cubo com 6 cores (gabarito-tipo Burnside)
*"Six color inks... paint a face of a cube... equal if aligned by a single 3D rotation."*

**Resolução:** total de formas sem simetria = `6!`. O cubo tem `24` rotações. Logo
`6!/24 = 720/24 = 30`. Resposta: **(c) 30**.
**Lição:** decore `6!/24 = 30`. Esse número reaparece.

### 📌 2026 — Q5: Cubo com 2 faces vermelhas + 4 cores diferentes
*"Two faces red, the other four in 4 different colors... equal up to rotations."* Gabarito: **(a) 15**.

**Raciocínio (contagem direta por casos):**
As 2 faces vermelhas podem ser **opostas** ou **adjacentes** — contam-se os arranjos das 4 cores restantes
em cada caso, dividindo pelas rotações que preservam a configuração. O total dá **15**.
**Lição:** quando Burnside "cru" fica pesado, **separe em casos de posição relativa** (opostas vs. adjacentes)
e trate a simetria restante em cada caso.

### 📌 2024 — Q1: Coloração de poliedro (trapézios + triângulos)
*"6 isosceles trapezoids + 2 triangles... paint 3 of the 6 trapezoids black... up to rotations."*

**Conceito:** novamente contagem com simetria, agora num prisma/antiprisma. Enumere as escolhas
de 3 trapézios `C(6,3)=20` e agrupe as que são equivalentes por rotação. Resposta esperada: poucas classes.
**Lição:** `C(6,3)` lista as possibilidades; o trabalho é **agrupar por rotação**.

### 📌 2024 — Q5: Caminhos numa malha de ruas sem passar por B
*"...how many trajectories from A to C not passing through B?"*

**Resolução:** `caminhos(A→C) − caminhos(A→B)·caminhos(B→C)`, usando `C(m+n,m)` em cada trecho.
**Lição:** "sem passar por X" = **total menos os que passam por X**. Princípio da subtração.

### 📌 2023 — Q2: Mesa circular, homens e mulheres alternados
*"4 men and 4 women around a circular table, no man beside another."* Gabarito: **(e) 144**.

**Resolução:** fixa-se o círculo → permutação circular das mulheres `(4−1)! = 3! = 6`;
os homens ocupam os 4 espaços entre elas `4! = 24`. Total `6 × 24 = 144`.
**Lição:** **permutação circular = (n−1)!** e intercalar cria "espaços" a preencher.

### 📌 2023 — Q14: Interseções das diagonais de um nonágono
*"Number of intersection points of the internal diagonals of a regular nonagon."* Gabarito: **(c) 126**.

**Resolução:** cada 4 vértices geram 1 cruzamento → `C(9,4) = 126`.
**Lição:** decore **interseções de diagonais em polígono convexo = C(n,4)**.

### 📌 2021 — Q11: Pintar 4 quadrados (preto/branco) a menos de rotação
Burnside num quadrado (grupo de 4 rotações). Classes distintas de coloração.
**Lição:** quadrado tem 4 rotações (0°, 90°, 180°, 270°) → divida/conte por Burnside com `|G|=4`.

---

## 3. Exercícios de treino

> Resolva sem calculadora. Gabarito e resolução na seção 4.

**E1.** De quantas maneiras 5 pessoas podem se sentar em volta de uma mesa circular?

**E2.** Quantos anagramas distintos tem a palavra `BANANA`?

**E3.** Numa grade 3×3 (ir só para direita e para baixo), quantos caminhos ligam o canto
superior-esquerdo ao inferior-direito?

**E4.** De quantas formas pintar as 6 faces de um cubo usando exatamente 3 cores, com cada cor
em exatamente 2 faces, considerando colorações iguais a menos de rotação? *(desafio Burnside)*

**E5.** Quantos pontos de interseção têm as diagonais internas de um hexágono regular convexo
(em posição genérica)?

**E6.** Quantas comissões de 3 pessoas podem ser formadas a partir de 8 candidatos?

**E7.** (estilo ITA, em inglês) *In how many ways can the letters of the word `PROVA` be arranged
so that the vowels are always together?*

---

## 4. Gabarito e resoluções dos exercícios

**E1.** Permutação circular: `(5−1)! = 4! = **24**`.

**E2.** `BANANA`: 6 letras com A×3, N×2, B×1 → `6!/(3!·2!·1!) = 720/12 = **60**`.

**E3.** Grade 3×3 = 3 passos à direita + 3 para baixo → `C(6,3) = 20`. **20 caminhos.**

**E4.** Burnside no cubo (|G|=24). Resultado clássico: **6** colorações distintas.
Esboço: escolhas de pares de faces para cada cor, agrupadas pelas 24 rotações.
(As configurações dependem de quais pares de faces são opostos/adjacentes.)

**E5.** `C(6,4) = 15`. **15 pontos.** (Obs.: no hexágono *regular* há concorrência de 3 diagonais no centro,
o que reduz o número real; em posição *genérica* são 15. A prova do ITA usou o nonágono justamente
por não ter essa coincidência no padrão pedido.)

**E6.** Combinação (ordem não importa): `C(8,3) = 8!/(3!5!) = 56`. **56 comissões.**

**E7.** `PROVA` tem 5 letras, vogais O e A. Trate as vogais como bloco: `4!` arranjos do bloco+consoantes,
× `2!` internos do bloco = `24 × 2 = **48**`.

---

## 5. Banco de questões reais

As questões de combinatória das 6 provas (2021–2026), com enunciado original em inglês e gabarito
(quando divulgado), estão em **[QUESTOES-DAS-PROVAS.md](QUESTOES-DAS-PROVAS.md)**.
