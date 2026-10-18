# Revisão das provas de 2º SEMESTRE — Combinatória e Contagem

Revisão completa das **5 provas de 2º semestre (2021 a 2025)** para este tema.
Enunciados no original (inglês), identificação ano/questão e gabarito quando divulgado
(2022-2ºSem e 2025-2ºSem têm gabarito oficial).

> Complementa o `QUESTOES-DAS-PROVAS.md` (que cobre os 1ºs semestres). Aqui estão só os 2ºs semestres.

---

### 2025/2º — Q4: Soma binomial
The value of the sum C(20,0) + C(20,1)·2 + C(20,2)·2² + ⋯ + C(20,20)·2²⁰ is
(a) 2⁴⁰ · (b) 9¹⁰ · (c) 20²⁰ · (d) 20! · (e) 40!/20!
**Gabarito: (b)** — é `(1+2)²⁰ = 3²⁰ = 9¹⁰` pelo binômio de Newton.

### 2025/2º — Q16: Probabilidade (desarranjo)
Four married couples; pairs formed by chance. Probability that each man dances with a woman other
than his wife.
(a) 1/4 · (b) 5/18 · (c) 5/16 · (d) 1/3 · (e) 3/8
**Gabarito: (e)** — desarranjo `D₄/4! = 9/24 = 3/8`.

---

### 2024/2º — Q4: Caminhos nas arestas de um tetraedro
A path along 5 edges of a tetrahedron (6 vértices em ordem, sem repetir aresta). How many different
proper paths can be formed along 5 of the 6 edges?
(a) 24 · (b) 36 · (c) 48 · (d) 60 · (e) 72

### 2024/2º — Q7: Empilhamento de esferas (pirâmide de base quadrada)
How many equal spheres can be stacked to form a pyramid with a square basis with six spheres in each
edge?
(a) 48 · (b) 56 · (c) 72 · (d) 91 · (e) 96
→ Soma dos quadrados: `1²+2²+...+6² = 91`. Resposta **(d) 91**.

### 2024/2º — Q14: Fatorial (equação)
The solution of (n+2)!(n−2)! / [(n+1)!(n−1)!] = 4 is a natural number that is also
(a) even · (b) perfect cube · (c) >10 · (d) divisible by 5 · (e) divisible by 3
→ Simplifica para `(n+2)/(n−1) = 4 → n = 2`... resolva e classifique.

---

### 2023/2º — Q4: Sinais + e − em fila (não dois "−" juntos)
p plus signs and q minus signs in a row, p+q=n, p>q−2, no two minus signs together. In how many
ways? (alternativas em C(n,r))
(a) C(n−q+1, q) · (b) C(q, p+q) · (c) (p+q)!/q! · (d) C(p+1, q) · (e) (p+q−1)!
→ Método "gaps": distribuir os `−` nos espaços entre/ao redor dos `+`.

### 2023/2º — Q5: Travessia do rio (3 casais ciumentos)
Three couples cross a river in a boat for up to two persons; no man with another's wife without her
husband. Minimal number of crossings.
(a) 8 · (b) 9 · (c) 10 · (d) 11 · (e) 12
→ Clássico problema de estado/busca. Resposta conhecida: **11**.

### 2023/2º — Q10: Simplificação com fatoriais
Simplify n[n! + (n−1)!] / [(n+1)! − n!]:
(a) n · (b) (n+1)/n · (c) (n−1)/n · (d) n/(n+1) · (e) n/(n−1)
→ Fatore `(n−1)!` e `n!`; reduz a expressão.

---

### 2022/2º — Q1: Coeficiente de x⁴ em (1+x)(1−x)ⁿ
The coefficient of x⁴ after expanding (1+x)(1−x)ⁿ:
(a) ... · (b) n(n−1)(n−2)(n−4)/24 · (c) n(n−1)(n−2)(n−7)/24 · (d) n(n−1)(n−2)(n−5)/24 · (e) .../120
**Gabarito: (c)** — some os termos de x⁴ de `(1−x)ⁿ` e de `x·(1−x)ⁿ`: `C(n,4) − C(n,3)`.

---

### 2021/2º — Q5: Triângulos a partir de 9 pontos (3 colineares não contam)
Triangle with two points on each edge (9 pontos ao todo). If 3 collinear points form no triangle, how
many triangles can be formed with 3 of the 9 points?
(a) 27 · (b) 72 · (c) 84 · (d) 9!/3! · (e) 9!
→ `C(9,3) − (triplas colineares)`. `C(9,3)=84`; subtraia as colineares de cada lado.

### 2021/2º — Q7: Arestas coloridas do tetraedro (Burnside!) 🌟
Six sticks (same length, different colors) form the edges of a tetrahedron. Two arrangements equal if
a 3-D rotation aligns same-color sticks. How many different arrangements?
(a) 4 · (b) 6 · (c) 8 · (d) 24 · (e) 30
→ **Burnside** no grupo de rotações do tetraedro (|G|=12) agindo sobre as 6 arestas:
`6!/12 = 720/12 = 60`? Cuidado — conte os ciclos de cada rotação (ver `BURNSIDE-EXPLICADO.md`).
Este é mais um caso do padrão de coloração com simetria.

---

## Observação sobre frequência (2º sem)
Combinatória seguiu **forte** também nos 2ºs semestres: binômio de Newton (2022, 2025),
contagem geométrica (2021, 2024), fatoriais (2023, 2024), Burnside (2021/2º — tetraedro),
desarranjo/probabilidade (2025). Confirma a prioridade ALTA do tema.

---

## Conceitos novos que os 2ºs semestres cobraram (revisão)

### Binômio de Newton aplicado a somas
`Σ C(n,k)·aᵏ = (1+a)ⁿ`. Em 2025/2-Q4, `a=2` dá `(1+2)²⁰ = 3²⁰ = 9¹⁰`. Reconhecer essa identidade
economiza todo o trabalho de somar 21 termos.

### Desarranjo (permutação caótica)
Número de permutações de `n` elementos em que **nenhum** fica na posição original:
`Dₙ = n!·(1 − 1/1! + 1/2! − 1/3! + … + (−1)ⁿ/n!)`.
Valores úteis: `D₃=2`, `D₄=9`, `D₅=44`.
Probabilidade de desarranjo total = `Dₙ/n!`. Em 2025/2-Q16: `D₄/4! = 9/24 = 3/8`.

### Soma de quadrados (empilhamento de esferas)
Pirâmide de base quadrada com `k` esferas na aresta tem `1²+2²+…+k² = k(k+1)(2k+1)/6` esferas.
Para `k=6`: `6·7·13/6 = 91` (2024/2-Q7).

### Contagem por "gaps" (objetos que não podem ficar juntos)
Para posicionar itens que **não podem ser adjacentes**, primeiro arrume os outros, depois insira os
restritos nos **espaços entre eles** (gaps). Usado em 2023/2-Q4 (sinais − não adjacentes) e em
2023/1-Q2 (homens/mulheres na mesa).

---

## Resoluções detalhadas

### 2024/2 — Q7 (empilhamento de esferas → 91)
Base quadrada com 6 esferas na aresta: as camadas têm 6², 5², 4², 3², 2², 1² esferas.
`36+25+16+9+4+1 = 91`. **Resposta (d).**

### 2025/2 — Q16 (desarranjo → 3/8)
4 homens pareados ao acaso com 4 mulheres; queremos que **nenhum** dance com a própria esposa.
Total de pareamentos = `4! = 24`. Favoráveis = desarranjos `D₄ = 9`. Probabilidade `= 9/24 = 3/8`.
**Resposta (e).**

### 2022/2 — Q1 (coeficiente de x⁴ → (c))
`(1+x)(1−x)ⁿ = (1−x)ⁿ + x(1−x)ⁿ`. Coeficiente de `x⁴`:
- de `(1−x)ⁿ`: `C(n,4)·(−1)⁴ = C(n,4)`
- de `x(1−x)ⁿ`: coeficiente de `x³` em `(1−x)ⁿ` = `C(n,3)·(−1)³ = −C(n,3)`
Total `= C(n,4) − C(n,3)`. Fatorando `n(n−1)(n−2)/24`, sai `n(n−1)(n−2)(n−7)/24`. **Resposta (c).**

### 2021/2 — Q5 (triângulos com 9 pontos → 72)
`C(9,3) = 84` triplas. Subtraia as **colineares**: cada lado tem 2 pontos + 2 vértices = 4 colineares,
dando `C(4,3)=4` por lado × 3 lados = 12. `84 − 12 = 72`. **Resposta (b).**

---

## Exercícios de treino (2º sem)

**T1.** Calcule `Σ_{k=0}^{10} C(10,k)·3ᵏ`.

**T2.** De quantas formas 5 pessoas podem ser pareadas com 5 cadeiras de modo que ninguém fique na
cadeira de mesmo número? (desarranjo)

**T3.** Quantas esferas há numa pirâmide de base triangular (tetraédrica) com 4 esferas na aresta?
(dica: números tetraédricos `C(k+2,3)`)

**T4.** Em quantas ordens 4 cartas vermelhas e 3 pretas podem ser enfileiradas sem duas pretas juntas?

---

## Gabarito dos exercícios (2º sem)

**T1.** `(1+3)¹⁰ = 4¹⁰ = 1.048.576`.

**T2.** `D₅ = 44`.

**T3.** Número tetraédrico: `C(4+2,3) = C(6,3) = 20` esferas.

**T4.** Arrume as 4 vermelhas: cria 5 gaps (_V_V_V_V_). Escolha 3 dos 5 gaps para as pretas:
`C(5,3) = 10` ordens.
