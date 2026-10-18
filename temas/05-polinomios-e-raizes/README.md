# Tema 05 — Polinômios e Raízes 🟠

**Prioridade: MÉDIA-ALTA.** Cai quase todo ano. Foco em **natureza das raízes**
(reais/irracionais/inteiras), **relações de Girard** e **binômio de Newton**.

---

## 1. Conceitos e teoremas que você precisa saber

### 1.1 Teorema Fundamental da Álgebra
Um polinômio de grau `n` tem exatamente `n` raízes complexas (contando multiplicidade).
Raízes complexas de polinômio **real** vêm em pares conjugados (`a+bi` e `a−bi`).

### 1.2 Relações de Girard (soma e produto das raízes)
Para `ax² + bx + c = 0`: soma `= −b/a`, produto `= c/a`.
Para grau `n` com raízes `r₁,…,rₙ`:
- soma das raízes `= −a_{n−1}/aₙ`
- produto das raízes `= (−1)ⁿ·a₀/aₙ`

### 1.3 Natureza das raízes ⭐ (o que mais cai)
- **Teorema das raízes racionais:** se `p/q` é raiz de polinômio de coef. inteiros,
  então `p | a₀` (termo independente) e `q | aₙ` (líder). Lista candidatos a testar.
- **Teorema de Bolzano (mudança de sinal):** se `f(a)` e `f(b)` têm sinais opostos,
  há pelo menos uma raiz real em `(a,b)`.
- **Discriminante** (2º grau) `Δ = b²−4ac`: `Δ>0` duas reais distintas; `Δ=0` uma dupla; `Δ<0` complexas.
- Função **monótona crescente** (ex.: `x³+x` sempre cresce) cruza o zero **uma única vez** → 1 raiz real.

### 1.4 Binômio de Newton
`(x+y)ⁿ = Σ C(n,k)·x^(n−k)·yᵏ`, `k=0..n`.
- **Termo geral:** `T_{k+1} = C(n,k)·x^(n−k)·yᵏ`.
- **Termo independente de x:** iguale o expoente de x a zero e resolva para `k`.
- Soma dos coeficientes de `P(x)` = `P(1)`.

### 1.5 Fatorações úteis
- `a²−b² = (a−b)(a+b)`
- `a³±b³ = (a±b)(a²∓ab+b²)`
- `(a±b)² = a²±2ab+b²`; `(a±b)³ = a³±3a²b+3ab²±b³`
- Quadrado perfeito escondido: `x²+2xy+y² = (x+y)²` (útil em "mark the statement").

---

## 2. Resoluções comentadas (questões reais do ITA)

### 📌 2025 — Q7: `x³ + x − 10 = 0`, natureza das raízes
Gabarito: **(d) tem uma raiz real racional** (verifique com teste de raiz).

**Resolução:** candidatas racionais: divisores de 10 → `±1,±2,±5,±10`. Teste `x=2`: `8+2−10=0` ✔.
Logo `x=2` é raiz racional. Fatorando: `(x−2)(x²+2x+5)=0`; o fator quadrático tem `Δ=4−20<0`
→ as outras duas são complexas. Então **uma única raiz real (racional)**.
**Lição:** **teste os divisores do termo independente** antes de qualquer coisa.

### 📌 2025 — Q3: Termo independente de x em `(x + 1/x²)ⁿ`
Gabarito: **(c) n divisível por 3**.

**Resolução:** termo geral `C(n,k)·x^(n−k)·(x⁻²)ᵏ = C(n,k)·x^(n−3k)`.
Independente de x ⟺ `n−3k=0` ⟺ `n=3k` ⟺ **n múltiplo de 3**.
**Lição:** **iguale o expoente total de x a zero** e veja a condição sobre `n`.

### 📌 2026 — Q7: Expressão com `(1+√3)` (binômio disfarçado)
*"`4(1+√3) − 6(1+√3)² + 4(1+√3)³ − (1+√3)⁴`"* Gabarito: **(d) −8**.

**Resolução:** os coeficientes `4, −6, 4, −1` lembram o binômio. De fato, seja `a=1+√3`:
a expressão `= −(a⁴ − 4a³ + 6a² − 4a) = −[(a−1)⁴ − 1] = 1 − (a−1)⁴`.
Como `a−1=√3`: `(√3)⁴ = 9` → `1 − 9 = −8`.
**Lição:** coeficientes `1,4,6,4,1` gritam **`(a−1)⁴`** — reconheça o binômio escondido.

### 📌 2024 — Q7: Soma dos coeficientes de 2º grau em `(x−y+z−1)³`
Gabarito: **(d) 3** (confira). 

**Resolução:** expanda por multinômio, selecione os termos de grau total 2 (`x²,y²,z²,xy,...`)
e some seus coeficientes. Atalho: avalie derivadas/substituições que isolem o grau 2.
**Lição:** para "soma dos coeficientes de certo grau", use **expansão multinomial** organizada por grau.

### 📌 2023 — Q10: `x⁴+10x³+25x² + y²−10y+25 = 0` (soma de quadrados)
**Resolução:** `x⁴+10x³+25x² = x²(x²+10x+25) = x²(x+5)²= [x(x+5)]²`;
`y²−10y+25=(y−5)²`. Soma de dois quadrados = 0 ⟹ cada um = 0 → `x(x+5)=0` e `y=5`.
**Lição:** **soma de quadrados reais = 0** força cada parcela a zero.

### 📌 2022 — Q6: Raízes de `x⁶ − 64 = 0`
**Resolução:** `x⁶=64 → |x|=2`. Raízes reais: `x=2` e `x=−2` (2 inteiras); as outras 4 são complexas
(raízes sextas de 64 no plano complexo).
**Lição:** `xⁿ = k` tem n raízes complexas distribuídas no círculo; conte quantas são reais.

### 📌 2021 — Q15: Raiz comum com `x²−5x+6`
**Resolução:** `x²−5x+6=(x−2)(x−3)`, raízes 2 e 3. Procure a opção que também tenha 2 ou 3 como raiz.
`x²−7x+12=(x−3)(x−4)` compartilha o 3.
**Lição:** **fatore** os dois polinômios e compare as raízes.

---

## 3. Exercícios de treino

**E1.** Encontre as raízes racionais de `x³ − 6x² + 11x − 6 = 0`.

**E2.** Sem resolver, dê a soma e o produto das raízes de `2x² − 7x + 3 = 0`.

**E3.** Qual o termo independente de x no desenvolvimento de `(x + 2/x)⁶`?

**E4.** Mostre que `x³ + x − 1 = 0` tem exatamente uma raiz real (sem calculá-la).

**E5.** Fatore `x⁴ − 1`.

**E6.** Qual a soma dos coeficientes de `(2x − 1)⁵`?

---

## 4. Gabarito e resoluções

**E1.** Divisores de 6: `±1,±2,±3,±6`. Testando: `x=1` (1−6+11−6=0 ✔), `x=2` ✔, `x=3` ✔.
Raízes: **1, 2, 3** (`=(x−1)(x−2)(x−3)`).

**E2.** Soma `=−(−7)/2 = 7/2`; produto `= 3/2`.

**E3.** Termo geral `C(6,k)·x^(6−k)·(2/x)ᵏ = C(6,k)·2ᵏ·x^(6−2k)`. Independente: `6−2k=0→k=3`.
Termo `= C(6,3)·2³ = 20·8 = **160**`.

**E4.** `f(x)=x³+x−1`. `f'(x)=3x²+1>0` sempre → função **estritamente crescente** → cruza o zero
uma única vez → **exatamente uma raiz real**.

**E5.** `x⁴−1=(x²−1)(x²+1)=(x−1)(x+1)(x²+1)`.

**E6.** Soma dos coeficientes = `P(1) = (2·1−1)⁵ = 1⁵ = **1**`.
