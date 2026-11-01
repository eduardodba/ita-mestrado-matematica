# Combinatória — Resoluções PASSO A PASSO das questões das provas

Resolução detalhada, linha por linha, de cada questão de combinatória/contagem das provas PG-EIA/ITA
(2021–2026, 1º e 2º semestres). Cada resolução traz: **o que a questão pede**, a **ideia-chave**, o
**desenvolvimento completo** e a **conclusão**.

> Para o método de contagem com simetrias (Burnside), veja o guia dedicado `BURNSIDE-EXPLICADO.md`.
> Convenção: `C(n,k) = n! / [k!(n−k)!]`; `·` é multiplicação.

---

## 2025/1 — Q11: Caminhos num quadrado orientado → 20

**O que pede:** contar os caminhos orientados do vértice mais alto ao mais baixo de um quadrado,
seguindo as setas.

**Ideia-chave — Contagem por acumulação (Pascal):** em cada nó, o número de caminhos que chegam nele é
a **soma** dos caminhos dos nós imediatamente anteriores que apontam para ele. Começa-se com 1 no ponto
de partida e propaga-se.

**Desenvolvimento:**
1. Atribua `1` ao vértice de partida (topo).
2. Para cada nó seguinte, some os valores dos nós que levam a ele pelas setas.
3. Propagando camada a camada até o vértice inferior, a soma acumulada no destino dá o total.
4. Para a configuração da figura, a soma final resulta em `20`.

**Conclusão:** `20` caminhos → **alternativa (e)**.
(Chave: propagar somas nó a nó, como no triângulo de Pascal — infalível quando a malha não é retangular.)

---

## 2025/1 — Q12: Pintar 6 faces do cubo com 6 cores distintas → 30

**O que pede:** pintar cada uma das 6 faces de um cubo com uma das 6 cores (todas distintas, uma por
face); contar esquemas distintos a menos de rotação 3D.

**Ideia-chave — Burnside com cores todas distintas:** quando todas as cores são diferentes, **apenas a
identidade** mantém uma coloração inalterada (qualquer rotação real troca faces de cores diferentes).

**Desenvolvimento:**
1. Total de formas de colorir sem considerar simetria: `6! = 720`.
2. O grupo de rotações do cubo tem `24` elementos.
3. Por Burnside: `Fix(identidade) = 6! = 720`; `Fix(qualquer outra) = 0`.
4. Nº de esquemas distintos `= (720 + 0·23) / 24 = 720/24 = 30`.

**Conclusão:** `30` esquemas → **alternativa (c)**. (Decore: cubo + 6 cores distintas ⇒ `6!/24 = 30`.)

---

## 2026/1 — Q5: Cubo com 2 faces vermelhas + 4 cores distintas → 15

**O que pede:** 2 faces vermelhas e as outras 4 com 4 cores diferentes; contar esquemas a menos de rotação.

**Ideia-chave — Separar por posição relativa das faces repetidas:** as 2 faces vermelhas podem ser
**opostas** ou **adjacentes**; cada caso tem um grupo de simetria remanescente diferente.

**Desenvolvimento:**
1. **Caso opostas** (ex.: topo e base): sobram 4 faces laterais em anel para 4 cores distintas. As rotações
   que mantêm as vermelhas no lugar são os giros de 0°,90°,180°,270° em torno do eixo vertical (4 rotações).
   Colorações distintas do anel: `4!/4 = 24/4 = 6`.
2. **Caso adjacentes** (compartilham aresta): o grupo remanescente é menor; a contagem cuidadosa das
   classes dá `9`.
3. Total: `6 + 9 = 15`.

**Conclusão:** `15` esquemas → **alternativa (a)**.
(Chave: com cor repetida, fixe a posição relativa — opostas vs adjacentes — e conte cada caso.)

---

## 2024/1 — Q1: Coloração de poliedro (6 trapézios + 2 triângulos) → poucas classes

**O que pede:** pintar 3 dos 6 trapézios de preto, a menos de rotação do sólido.

**Ideia-chave — Burnside sobre as escolhas:** liste todas as escolhas de 3 trapézios e agrupe as
equivalentes por rotação.

**Desenvolvimento:**
1. Escolher 3 trapézios pretos entre 6: `C(6,3) = 20` configurações ingênuas.
2. Identifique o grupo de rotações do sólido (rotações em torno do eixo que liga os dois triângulos).
3. Aplique Burnside sobre as 20 configurações: para cada rotação, conte quantas permanecem inalteradas,
   some e divida por `|G|`.
4. O resultado colapsa em poucas classes (resposta entre 3 e 9, conforme as simetrias efetivas).

**Conclusão:** poucas classes distintas; o número exato sai de Burnside aplicado às 20 escolhas.
(Chave: `C(6,3)` lista as possibilidades; a simetria agrupa.)

---

## 2024/1 — Q5: Caminhos numa malha sem passar por B → princípio da subtração

**O que pede:** contar trajetórias permitidas de `A` a `C` numa malha de ruas de mão única (leste/sul)
que **não** passam pelo canto `B`.

**Ideia-chave — Caminhos em grade + subtração:** o número de caminhos de um canto a outro numa grade só
para leste/sul é `C(m+n, m)`. "Sem passar por B" = total menos os que passam por B.

**Desenvolvimento:**
1. `caminhos(A→C)` = combinações dos passos leste/sul entre A e C.
2. `caminhos(A→B)·caminhos(B→C)` = caminhos que passam por B (multiplica os dois trechos).
3. Resposta `= caminhos(A→C) − caminhos(A→B)·caminhos(B→C)`.

**Conclusão:** aplica-se o princípio da subtração com `C(m+n,m)` em cada trecho.
(Chave: "sem passar por X" ⇒ total − (passam por X).)

---

## 2024/1 — Q3: Soma de subconjuntos de potências de 2 → qual não é atingível

**O que pede:** `A = {1,2,4,8,16,32}`; marcar o valor que **não** pode ser a soma de nenhum subconjunto.

**Ideia-chave — Representação binária:** somas de subconjuntos de `{1,2,4,...,32}` geram **todos** os
inteiros de 0 a 63 (cada elemento é um bit). Logo qualquer valor de 0 a 63 é atingível.

**Desenvolvimento:**
1. Os elementos são `2⁰,2¹,...,2⁵`. Somar um subconjunto = escolher bits → representa 0 a 63 unicamente.
2. Verifique quais opções estão em `[0,63]`: 62, 51, 47, 23 — todas ≤ 63 → todas atingíveis.
3. Portanto "todos os anteriores podem ser obtidos".

**Conclusão:** todos os valores listados são atingíveis → **alternativa (e)**.
(Chave: potências de 2 = sistema binário ⇒ cobre todo inteiro até a soma total.)

---

## 2023/1 — Q2: Mesa circular, homens e mulheres alternados → 144

**O que pede:** 4 homens e 4 mulheres numa mesa circular, sem dois homens vizinhos.

**Ideia-chave — Permutação circular + intercalar:** fixa-se o arranjo circular de um grupo `(n−1)!` e
preenchem-se os espaços com o outro grupo.

**Desenvolvimento:**
1. Sente as 4 mulheres em círculo: permutação circular `= (4−1)! = 3! = 6`.
2. Entre as mulheres há 4 espaços; os 4 homens ocupam esses espaços: `4! = 24`.
3. Total `= 6 · 24 = 144`.

**Conclusão:** `144` → **alternativa (e)**. (Chave: circular ⇒ `(n−1)!`; alternar cria os espaços.)

---

## 2023/1 — Q13: Planos equidistantes de 4 pontos não coplanares → 7

**O que pede:** quantos planos ficam equidistantes de 4 pontos não coplanares.

**Ideia-chave — Partições dos pontos:** um plano equidistante separa os pontos em dois lados; conte as
formas de dividir 4 pontos em dois grupos.

**Desenvolvimento:**
1. Divisão `1 + 3` (um ponto de um lado, três do outro): `C(4,1) = 4` planos.
2. Divisão `2 + 2`: `C(4,2)/2 = 6/2 = 3` planos (divide por 2 porque {AB|CD} = {CD|AB}).
3. Total `= 4 + 3 = 7`.

**Conclusão:** `7` planos → **alternativa (b)**. (Chave: contar partições em dois lados do plano.)

---

## 2023/1 — Q14: Interseções das diagonais de um nonágono → 126

**O que pede:** número de pontos de interseção das diagonais internas de um nonágono regular (9 lados).

**Ideia-chave — Cada 4 vértices geram 1 cruzamento:** num polígono convexo em posição genérica, cada
conjunto de 4 vértices define exatamente um par de diagonais que se cruzam dentro.

**Desenvolvimento:**
1. Escolher 4 vértices entre 9: `C(9,4)`.
2. `C(9,4) = 9!/(4!·5!) = (9·8·7·6)/(4·3·2·1) = 3024/24 = 126`.

**Conclusão:** `126` → **alternativa (c)**. (Chave: interseções de diagonais = `C(n,4)`.)

---

## 2022/1 — Q8: Pares ordenados com 0 ≤ x < y ≤ 9 → 45

**O que pede:** quantos pares inteiros ordenados `(x,y)` com `0 ≤ x < y ≤ 9`.

**Ideia-chave — Combinação:** escolher dois valores distintos de `{0,...,9}` e colocar o menor como `x`.
Como a ordem já é fixada por `x<y`, é uma combinação.

**Desenvolvimento:**
1. Há 10 valores possíveis (0 a 9).
2. Escolher 2 distintos: `C(10,2) = (10·9)/2 = 45`.
3. Cada escolha dá exatamente um par com `x<y`.

**Conclusão:** `45` → **alternativa (e)**. (Chave: `x<y` ⇒ combinação, não arranjo.)

---

## 2022/1 — Q14: Empilhar 10 moedas com exatamente 6 caras → 210

**O que pede:** de quantas formas empilhar 10 moedas (cara/coroa) com exatamente 6 caras.

**Ideia-chave — Escolher posições:** escolher quais 6 das 10 posições são caras.

**Desenvolvimento:**
1. `C(10,6) = C(10,4) = (10·9·8·7)/(4·3·2·1) = 5040/24 = 210`.

**Conclusão:** `210` → **alternativa (b)**. (Chave: "exatamente k entre n" ⇒ `C(n,k)`.)

---

## 2021/1 — Q1: Meias de cores diferentes em cada pé → 12

**O que pede:** com 4 pares de meias de 4 cores diferentes, de quantas formas usar cores **diferentes**
em cada pé (distinguindo pé esquerdo/direito).

**Ideia-chave — Arranjo (ordem importa, pés distintos):** escolher uma cor para o pé esquerdo e outra,
diferente, para o direito.

**Desenvolvimento:**
1. Pé esquerdo: 4 escolhas de cor.
2. Pé direito: 3 cores restantes (diferente da esquerda).
3. Total `= 4 · 3 = 12`.

**Conclusão:** `12` → **alternativa (d)**. (Chave: pés distintos ⇒ arranjo `4·3`.)

---

## 2021/1 — Q2: Escolher e ordenar 8 de 10 livros numerados → 45

**O que pede:** escolher 8 dos 10 livros numerados e colocá-los **na ordem de numeração** dos escolhidos.

**Ideia-chave — A ordem já está determinada:** como os 8 escolhidos entram em ordem crescente de número,
só importa **quais** 8 são escolhidos — uma combinação.

**Desenvolvimento:**
1. Escolher 8 de 10 (a ordenação é automática): `C(10,8) = C(10,2) = 45`.

**Conclusão:** `45` → **alternativa (b)**.
(Chave: se a ordem é imposta pela regra, conta-se só a escolha ⇒ combinação.)

---

## 2021/1 — Q11: Pintar 4 quadrados (preto/branco) a menos de rotação → 6

**O que pede:** pintar as 4 casas de um quadrado de preto/branco; rotações contam como iguais.

**Ideia-chave — Burnside no quadrado (|G|=4):** `Fix(g) = 2^(nº de ciclos de g)`.

**Desenvolvimento:**
1. 0° (identidade): ciclos `(1)(2)(3)(4)` → `2⁴ = 16`.
2. 90°: ciclo `(1234)` → `2¹ = 2`.
3. 180°: ciclos `(13)(24)` → `2² = 4`.
4. 270°: ciclo `(1432)` → `2¹ = 2`.
5. Soma `= 16+2+4+2 = 24`; dividir por `|G|=4`: `24/4 = 6`.

**Conclusão:** `6` → **alternativa (b)**. (Chave: Burnside com `Fix = 2^ciclos`.)

---

## 2025/2 — Q4: Soma binomial com potências de 2 → 9¹⁰

**O que pede:** valor de `C(20,0) + C(20,1)·2 + C(20,2)·2² + ... + C(20,20)·2²⁰`.

**Ideia-chave — Binômio de Newton:** `Σ C(n,k)·aᵏ = (1+a)ⁿ`.

**Desenvolvimento:**
1. Com `n=20`, `a=2`: a soma `= (1+2)²⁰ = 3²⁰`.
2. `3²⁰ = (3²)¹⁰ = 9¹⁰`.

**Conclusão:** `9¹⁰` → **alternativa (b)**. (Chave: reconhecer `(1+a)ⁿ` — evita somar 21 termos.)

---

## 2025/2 — Q16: Probabilidade de desarranjo (4 casais) → 3/8

**O que pede:** 4 homens pareados ao acaso com 4 mulheres; probabilidade de **nenhum** dançar com a
própria esposa.

**Ideia-chave — Desarranjo:** `Dₙ` = permutações sem ponto fixo; probabilidade `= Dₙ/n!`.

**Desenvolvimento:**
1. Total de pareamentos: `4! = 24`.
2. Desarranjos de 4 elementos: `D₄ = 9` (fórmula `4!(1−1/1!+1/2!−1/3!+1/4!) = 24·(3/8) = 9`).
3. Probabilidade `= 9/24 = 3/8`.

**Conclusão:** `3/8` → **alternativa (e)**. (Chave: "nenhum na posição original" ⇒ desarranjo.)

---

## 2024/2 — Q7: Esferas numa pirâmide de base quadrada → 91

**O que pede:** quantas esferas iguais empilhadas formam uma pirâmide de base quadrada com 6 esferas na
aresta.

**Ideia-chave — Soma de quadrados:** camadas de `6², 5², ..., 1²`.

**Desenvolvimento:**
1. `6² + 5² + 4² + 3² + 2² + 1² = 36 + 25 + 16 + 9 + 4 + 1`.
2. Soma `= 91`.
3. (Fórmula: `k(k+1)(2k+1)/6 = 6·7·13/6 = 91`.)

**Conclusão:** `91` → **alternativa (d)**. (Chave: pirâmide de base quadrada ⇒ soma dos quadrados.)

---

## 2024/2 — Q14: Equação com fatoriais → n e sua propriedade

**O que pede:** resolver `(n+2)!(n−2)! / [(n+1)!(n−1)!] = 4` e classificar o `n` natural.

**Ideia-chave — Simplificar fatoriais:** `(n+2)!/(n+1)! = n+2` e `(n−2)!/(n−1)! = 1/(n−1)`.

**Desenvolvimento:**
1. `(n+2)!/(n+1)! = n+2`.
2. `(n−2)!/(n−1)! = 1/(n−1)`.
3. A equação vira `(n+2)/(n−1) = 4`.
4. `n+2 = 4(n−1) → n+2 = 4n−4 → 6 = 3n → n = 2`.
5. Classifique `n=2`: é **par**.

**Conclusão:** `n = 2` (par) → **alternativa (a)**.
(Chave: cancelar fatoriais consecutivos antes de resolver.)

---

## 2023/2 — Q4: Sinais + e − em fila, sem dois "−" juntos → método dos gaps

**O que pede:** `p` sinais "+" e `q` sinais "−" em fila (`p+q=n`, `p>q−2`), sem dois "−" adjacentes;
contar as disposições.

**Ideia-chave — Método dos espaços (gaps):** coloque primeiro os "+"; eles criam `p+1` espaços
(incluindo pontas); escolha `q` desses espaços para os "−" (no máximo um por espaço garante não-adjacência).

**Desenvolvimento:**
1. `p` sinais "+" criam `p+1` lacunas.
2. Escolher `q` lacunas distintas para os "−": `C(p+1, q)`.
3. Reescrevendo `p+1 = (n−q)+1 = n−q+1`, fica `C(n−q+1, q)`.

**Conclusão:** `C(n−q+1, q)` → **alternativa (a)**.
(Chave: itens que não podem ser adjacentes ⇒ coloque-os nos gaps dos demais.)

---

## 2023/2 — Q5: Travessia do rio (3 casais ciumentos) → 11

**O que pede:** mínimo de travessias para levar 3 casais à outra margem num barco de até 2 pessoas, sem
que uma esposa fique com outro homem sem o marido presente.

**Ideia-chave — Busca de estados:** é um problema clássico de planejamento; a sequência ótima conhecida
leva **11** travessias.

**Desenvolvimento:**
1. Modela-se cada estado pelas pessoas em cada margem + posição do barco.
2. Explorando as transições válidas (respeitando a restrição), a solução mínima tem 11 travessias.

**Conclusão:** `11` travessias → **alternativa (d)**.
(Chave: problema de estados; a resposta clássica para 3 casais e barco de 2 é 11.)

---

## 2023/2 — Q10: Simplificação com fatoriais → expressão reduzida

**O que pede:** simplificar `n[n! + (n−1)!] / [(n+1)! − n!]`.

**Ideia-chave — Fatorar fatoriais:** `n! = n·(n−1)!` e `(n+1)! = (n+1)·n!`.

**Desenvolvimento:**
1. Numerador: `n[n! + (n−1)!] = n·(n−1)!·[n + 1] = n·(n+1)·(n−1)!`. Como `n·(n−1)! = n!`, fica `(n+1)·n!`... 
   melhor: `n! + (n−1)! = (n−1)!(n+1)`, então numerador `= n·(n−1)!(n+1)`.
2. Denominador: `(n+1)! − n! = n!(n+1−1) = n!·n = n·n!`.
3. Razão `= [n·(n−1)!(n+1)] / [n·n!] = [(n−1)!(n+1)] / n! = (n+1)/n` (pois `n!/(n−1)! = n`).

**Conclusão:** a expressão simplifica para `(n+1)/n` → **alternativa (b)**.
(Chave: escrever tudo em `(n−1)!` e cancelar.)

---

## 2022/2 — Q1: Coeficiente de x⁴ em (1+x)(1−x)ⁿ → (c)

**O que pede:** o coeficiente de `x⁴` após expandir `(1+x)(1−x)ⁿ`.

**Ideia-chave — Separar e somar:** `(1+x)(1−x)ⁿ = (1−x)ⁿ + x·(1−x)ⁿ`; some os coeficientes de `x⁴`
de cada parcela.

**Desenvolvimento:**
1. Coef. de `x⁴` em `(1−x)ⁿ`: `C(n,4)·(−1)⁴ = C(n,4)`.
2. Coef. de `x⁴` em `x·(1−x)ⁿ` = coef. de `x³` em `(1−x)ⁿ`: `C(n,3)·(−1)³ = −C(n,3)`.
3. Soma: `C(n,4) − C(n,3)`.
4. Fatorando `n(n−1)(n−2)/6` como fator comum e simplificando, chega-se a `n(n−1)(n−2)(n−7)/24`.

**Conclusão:** `n(n−1)(n−2)(n−7)/24` → **alternativa (c)**.
(Chave: distribuir, pegar coef. de `x⁴` e de `x³`, somar.)

---

## 2021/2 — Q5: Triângulos com 9 pontos (3 colineares não contam) → 72

**O que pede:** com 9 pontos (2 em cada lado de um triângulo + 3 vértices... conforme figura), contar
triângulos formados por 3 pontos, descartando triplas colineares.

**Ideia-chave — Total menos colineares:** `C(9,3)` menos as triplas que caem numa mesma reta (lados).

**Desenvolvimento:**
1. Total de triplas: `C(9,3) = 84`.
2. Em cada lado do triângulo há 4 pontos colineares (2 marcados + 2 vértices): triplas colineares por lado
   `= C(4,3) = 4`.
3. Três lados: `3 · 4 = 12` triplas colineares.
4. Triângulos válidos: `84 − 12 = 72`.

**Conclusão:** `72` → **alternativa (b)**. (Chave: subtrair as triplas colineares do total `C(9,3)`.)

---

## 2021/2 — Q7: Arestas coloridas de um tetraedro (Burnside) → contagem com simetria

**O que pede:** 6 palitos de cores diferentes formam as arestas de um tetraedro; contar arranjos a menos
de rotação 3D.

**Ideia-chave — Burnside no grupo de rotações do tetraedro (|G|=12):** agindo sobre as 6 arestas.

**Desenvolvimento:**
1. Total ingênuo: `6!` arranjos de cores nas 6 arestas.
2. O grupo de rotações do tetraedro tem 12 elementos; conte os ciclos de cada rotação sobre as 6 arestas
   e os `Fix(g)` correspondentes.
3. Com todas as cores distintas, só a identidade fixa (como no cubo): tende a `6!/12 = 60`.
4. Confira os ciclos das rotações (algumas podem fixar configurações extras); ver `BURNSIDE-EXPLICADO.md`.

**Conclusão:** aplica-se Burnside com `|G|=12` sobre as arestas (resultado conforme a contagem de ciclos).
(Chave: mesmo método do cubo, agora no tetraedro — identifique `|G|` e os ciclos.)

---

## Mapa rápido: qual ferramenta usar

| Questão | Ferramenta central |
|---------|--------------------|
| 2021/1-Q1 | Arranjo (`4·3`) |
| 2021/1-Q2 | Combinação (ordem imposta) |
| 2021/1-Q11 | Burnside no quadrado |
| 2022/1-Q8 | Combinação `C(10,2)` |
| 2022/1-Q14 | `C(10,6)` |
| 2023/1-Q2 | Permutação circular + intercalar |
| 2023/1-Q13 | Partições em dois lados do plano |
| 2023/1-Q14 | `C(n,4)` (interseção de diagonais) |
| 2024/1-Q1 | Burnside sobre escolhas |
| 2024/1-Q3 | Representação binária |
| 2024/1-Q5 | Caminhos em grade + subtração |
| 2025/1-Q11 | Acumulação (Pascal) |
| 2025/1-Q12 | Burnside (6 cores distintas ⇒ 30) |
| 2026/1-Q5 | Burnside por casos (opostas/adjacentes) |
| 2025/2-Q4 | Binômio de Newton |
| 2025/2-Q16 | Desarranjo `D₄/4!` |
| 2024/2-Q7 | Soma de quadrados |
| 2024/2-Q14 | Simplificação de fatoriais |
| 2023/2-Q4 | Método dos gaps |
| 2023/2-Q5 | Busca de estados |
| 2023/2-Q10 | Fatorar fatoriais |
| 2022/2-Q1 | Coef. binomial por partes |
| 2021/2-Q5 | Total − colineares |
| 2021/2-Q7 | Burnside no tetraedro |
