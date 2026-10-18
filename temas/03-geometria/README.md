# Tema 03 — Geometria Plana e Espacial 🔴

**Prioridade: ALTA — o tema de MAIOR peso na prova.** De 2 a 4 questões por ano.
Recorrentes: círculos tangentes/inscritos, poliedros (contar faces/arestas/vértices, área, volume),
triângulos (pontos notáveis), sólidos de revolução.

---

## 1. Conceitos e teoremas que você precisa saber

### 1.1 Triângulos
- **Soma dos ângulos** internos = 180°.
- **Área:** `½·base·altura`; `½·a·b·sin(C)`; **Heron** `√[s(s−a)(s−b)(s−c)]`, `s=(a+b+c)/2`.
- **Lei dos senos:** `a/sinA = b/sinB = c/sinC = 2R`.
- **Lei dos cossenos:** `c² = a² + b² − 2ab·cosC`.
- **Pontos notáveis:**
  - *Baricentro* (medianas) — centro de massa, divide mediana em 2:1.
  - *Incentro* (bissetrizes) — centro do círculo **inscrito**.
  - *Circuncentro* (mediatrizes) — centro do círculo **circunscrito**.
  - *Ortocentro* (alturas).
- **Ponto de Fermat:** minimiza `PA+PB+PC`; se todos os ângulos < 120°, vê cada lado a 120°.

### 1.2 Círculos
- **Comprimento** `2πr`, **área** `πr²`.
- **Potência de ponto:** por um ponto externo P, `PA·PB = PC·PD` (secantes) e `PT² = PA·PB` (tangente).
- **Tangente** é perpendicular ao raio no ponto de contato.
- **Ângulo inscrito** = metade do ângulo central que subtende o mesmo arco.

### 1.3 Quadriláteros
- **Inscritível** (cabe num círculo) ⟺ ângulos opostos somam **180°**.
- **Circunscritível** (tem círculo inscrito) ⟺ soma dos lados opostos iguais: `AB+CD = BC+DA`.
- Área de quadrilátero com diagonais perpendiculares: `½·d₁·d₂`.

### 1.4 Polígonos regulares
- Ângulo interno de n lados: `(n−2)·180°/n`.
- Nº de diagonais: `n(n−3)/2`.
- Relação com círculos inscrito (apótema) e circunscrito.

### 1.5 Geometria espacial — poliedros
- **Relação de Euler:** `V − A + F = 2` (vértices − arestas + faces). ⭐ essencial para "contar elementos".
- **Cubo de aresta `l`:** V=8, A=12, F=6; volume `l³`; superfície `6l²`; diagonal `l√3`.
- **Poliedro truncado:** cada corte num vértice **remove** aquele vértice e **cria** novos
  vértices/arestas/faces. Conte com cuidado (ver 2025 Q10).
- **Tetraedro regular** de aresta `a`: volume `a³/(6√2)`; inscrito num cubo ocupa `1/3` do volume.

### 1.6 Volumes e sólidos de revolução
- Prisma/cilindro: `V = área da base × altura`.
- Pirâmide/cone: `V = ⅓ × área da base × altura`.
- Esfera: `V = (4/3)πr³`, superfície `4πr²`.
- **Sólido de revolução:** girar uma curva em torno de um eixo. Pode virar cone, cilindro,
  tronco de cone etc. (ver 2025 Q13).

---

## 2. Resoluções comentadas (questões reais do ITA)

### 📌 2026 — Q3: Quadrante e semicírculo tangente
*"AOB is a quadrant; semicircle CD is tangent to OA and OB. Ratio of areas."* Gabarito: **(b) 3:2**... (verifique).

**Resolução:** monte a relação geométrica entre o raio do quadrante `R` e o raio `r` do semicírculo
usando a tangência (distância do centro às retas = r). Expresse as áreas (`¼πR²` do quadrante,
`½πr²` do semicírculo) e simplifique a razão.
**Lição:** em tangência, **distância do centro à reta = raio**. É a chave para relacionar os raios.

### 📌 2026 — Q16: Três círculos inscritos num triângulo equilátero
*"Three circles of radius R inscribed in an equilateral triangle of side 2 cm. Find R."* Gabarito: **(a)**.

**Resolução:** por simetria, os três círculos iguais tangenciam os lados e entre si.
Use a altura do triângulo equilátero (`lado·√3/2`) e a geometria dos raios ao longo das bissetrizes.
**Lição:** explore a **simetria** (incentro, bissetrizes) e monte equações de distância.

### 📌 2025 — Q10: Cubo truncado nos vértices
*"From a cube of edge l, cubes of edge l/3 removed from all vertices. Mark the WRONG statement."*

**Resolução (contagem de elementos):**
- Cada vértice cortado vira uma pequena face triangular/quadrada; recalcule V, A, F.
- **Volume:** `l³ − 8·(l/3)³ = l³ − 8l³/27 = 19l³/27` ✔ (bate com a alternativa e).
- **Superfície:** pela geometria do corte, a área total **permanece `6l²`** (o que é removido de uma
  face reaparece nas novas faces) ✔.
- Confira V, A, F — uma das afirmações numéricas é falsa (a resposta).
**Lição:** em sólido truncado, calcule **volume por subtração** e conte V/A/F com a **relação de Euler**.

### 📌 2025 — Q13: Sólido de revolução (tronco de cone)
*"Region between z=0, z=1 and the surface of revolution of the line from (1,0,0) to (0,1,1)."*

**Resolução:** girar o segmento em torno do eixo z gera um **tronco de cone** (raios 1 em baixo, 0 em cima... ou 1→? conforme o segmento). Volume por integral `∫π[r(z)]²dz` ou pela fórmula do tronco.
**Lição:** identifique o **sólido gerado** e aplique a fórmula de volume (ou integre a área das seções).

### 📌 2025 — Q15 / 2024 — Q12: Quadrilátero inscritível
*"...can this quadrilateral be inscribed in a circle?"*

**Resolução:** teste **ângulos opostos somam 180°** (inscritível) e, se for o caso,
`AB+CD = BC+DA` (circunscritível). Calcule a área decompondo em triângulos retângulos.
**Lição:** decore os dois critérios (inscritível vs circunscritível).

### 📌 2024 — Q2: Feixe de luz refletindo em paredes-espelho
*"Light enters a corner of a 4m square room, reflects off two walls..."*

**Resolução:** use o **método das reflexões** (desdobrar/refletir a sala): a trajetória vira
uma linha reta no plano "desdobrado". O comprimento é a distância reta nesse desdobramento.
**Lição:** reflexão em espelho → **desdobre o plano** e meça em linha reta.

### 📌 2023 — Q12: Círculo rolando sobre círculo (epiciclóide)
*"c2 rolls over c1 without slipping... angle of rotation of c2 about its own center."*

**Resolução:** quando um círculo de raio `r` rola **externamente** sobre outro de raio `R`,
ao percorrer um arco o pequeno gira `(R+r)/r` vezes o ângulo. Com `R=3r` e quarto de volta,
calcule o giro próprio.
**Lição:** rolamento externo adiciona uma volta "extra" (fator `(R+r)/r`, não só `R/r`).

### 📌 2023 — Q13: Planos equidistantes de 4 pontos
*"How many planes are equidistant from 4 non-coplanar points?"* Gabarito: **(b) 7**.

**Resolução:** separações possíveis dos 4 pontos em dois grupos por um plano: `1+3` (4 modos)
e `2+2` (3 modos) → **7 planos**.
**Lição:** conte as **partições** dos pontos em dois lados do plano.

### 📌 2021 — Q5: Potência de ponto (tangente e secante)
*"AC=12 tangent to circle, CD=8, AD=9, find AB."*

**Resolução:** potência do ponto: `AC² = AD·AB` (tangente² = produto da secante) → `144 = 9·AB` → `AB=16`?
Ajuste conforme a configuração exata da figura.
**Lição:** **potência de ponto** liga tangente e secante: `tangente² = externo × total`.

### 📌 2021 — Q14: Hexágono regular vs círculo de mesma área
*"Radius r of a circle with same area as a regular hexagon of side l. Ratio r/l?"*

**Resolução:** área do hexágono regular `= (3√3/2)l²`. Iguale a `πr²` e isole `r/l`.
**Lição:** decore **área do hexágono regular = (3√3/2)·lado²**.

---

## 3. Exercícios de treino

**E1.** Qual o volume de um cubo cuja diagonal mede `√3`?

**E2.** Um poliedro tem 6 faces e 8 vértices. Quantas arestas tem? (use Euler)

**E3.** Num triângulo de lados 7, 8 e 9, calcule a área (Heron).

**E4.** Um quadrilátero tem ângulos opostos de 100° e 80°. Ele é inscritível num círculo? E se fossem 100° e 90°?

**E5.** De um ponto externo P, uma secante corta o círculo em A e B com `PA=4`, `PB=9`.
Qual o comprimento do segmento tangente de P ao círculo?

**E6.** Qual a razão entre o volume de um tetraedro regular inscrito num cubo e o volume do cubo?

**E7.** Área de um hexágono regular de lado 2.

---

## 4. Gabarito e resoluções

**E1.** Diagonal do cubo `= l√3 = √3` → `l=1` → volume `= 1³ = **1**`.

**E2.** Euler: `V−A+F=2` → `8−A+6=2` → `A = **12**`.

**E3.** `s=(7+8+9)/2=12`. Área `=√[12·5·4·3]=√720 = 12√5 ≈ **26,83**`.

**E4.** Ângulos opostos somam `100+80=180` → **sim, inscritível**. Já `100+90=190 ≠ 180` → **não**.

**E5.** Potência de ponto: `PT² = PA·PB = 4·9 = 36` → `PT = **6**`.

**E6.** Tetraedro regular inscrito no cubo ocupa `**1/3**` do volume do cubo.

**E7.** Hexágono regular: `(3√3/2)·lado² = (3√3/2)·4 = **6√3 ≈ 10,39**`.
