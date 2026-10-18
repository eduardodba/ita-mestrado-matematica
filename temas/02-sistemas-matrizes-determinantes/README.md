# Tema 02 — Sistemas Lineares, Matrizes e Determinantes 🔴

**Prioridade: ALTA.** Cai todo ano. O padrão **"discutir quantas soluções o sistema tem"**
(0, 1 ou ∞) apareceu em 2021, 2024, 2025 e 2026.

---

## 1. Conceitos e teoremas que você precisa saber

### 1.1 Matrizes — operações
- Soma/multiplicação por escalar: elemento a elemento.
- **Produto:** `(AB)ᵢⱼ = Σₖ aᵢₖ·bₖⱼ`. ⚠️ **Não é comutativo**: `AB ≠ BA` em geral.
- **Identidade** `I`: `AI = IA = A`. **Inversa** `A⁻¹`: `AA⁻¹ = I` (existe sse `det A ≠ 0`).

### 1.2 Determinantes
- 2×2: `det[[a,b],[c,d]] = ad − bc`.
- 3×3: regra de Sarrus ou Laplace.
- Propriedades-chave:
  - `det(AB) = det(A)·det(B)`
  - `det(Aⁿ) = (det A)ⁿ`
  - Linha/coluna nula → det = 0.
  - Trocar duas linhas troca o sinal.
  - Somar múltiplo de uma linha a outra **não** altera o det (base do escalonamento).

### 1.3 Discussão de sistemas lineares `Ax = b` 🌟
Para um sistema **n×n** (quadrado):
- `det A ≠ 0` → **solução única** (sistema possível e determinado — SPD).
- `det A = 0` → **0 ou ∞ soluções** (precisa analisar o posto / consistência):
  - compatível → **infinitas** (SPI)
  - incompatível → **nenhuma** (SI)

**Sistema triangular** (como o de 2025 Q2): se os elementos da diagonal são todos ≠ 0,
há solução única. Ex.: `ax+by+cz=g; dy+ez=h; fz=i` tem solução única sse `a·d·f ≠ 0`.

### 1.4 Regra de Cramer
Para `Ax=b` com `det A ≠ 0`: `xᵢ = det(Aᵢ)/det(A)`, onde `Aᵢ` é `A` com a i-ésima coluna
trocada por `b`. Prática para sistemas pequenos.

### 1.5 Interpretação geométrica
- 2 variáveis: cada equação é uma **reta**. Solução única = retas concorrentes;
  ∞ = retas coincidentes; nenhuma = paralelas distintas.
- 3 variáveis: cada equação é um **plano**.

### 1.6 Equações matriciais
Resolver em `X` equações como `X² − 2X + 2I = 0`: trate como polinômio de matriz.
As raízes podem ser **várias matrizes** distintas (não só números). Verifique por substituição.

---

## 2. Resoluções comentadas (questões reais do ITA)

### 📌 2025 — Q2: Condição de solução única (sistema triangular)
*"...to know if the system has a unique solution, one should know the value of the product..."*
Sistema: `ax+by+cz=g; dy+ez=h; fz=i`.

**Resolução:** é triangular superior. O determinante é o produto da diagonal: `a·d·f`.
Solução única ⟺ `adf ≠ 0`. Resposta: **(c) adf**.
**Lição:** em sistema triangular, **det = produto da diagonal**.

### 📌 2025 — Q6: Determinante com logaritmos
*"The calculus of the determinant [[1, ln2, ln4],[−1, ln4, ln8],[1, ln8, ln16]]..."*

**Resolução:** escreva tudo em função de `ln2`: `ln4=2ln2`, `ln8=3ln2`, `ln16=4ln2`.
A matriz vira `[[1, ln2, 2ln2],[−1, 2ln2, 3ln2],[1, 3ln2, 4ln2]]`. Fatore `ln2` das colunas 2 e 3
e calcule o determinante numérico. Resultado: **(e) −4ln²(2)**.
**Lição:** **transforme logaritmos numa base comum** antes de calcular; fatore para simplificar.

### 📌 2026 — Q11: Equação matricial `X² − 2X + 2I = 0`
*"Mark the option which is NOT a root of the equation."* Gabarito: **(e)**.

**Resolução:** teste cada matriz por substituição direta (calcule `X²`, depois `X²−2X+2I`).
A que não zera é a resposta. As "raízes" dessa equação matricial correspondem a matrizes cujos
autovalores satisfazem `λ²−2λ+2=0` (ou seja `λ = 1±i`).
**Lição:** em equação matricial, **substitua e verifique**; lembre que `AB ≠ BA`.

### 📌 2024 — Q11: Discussão de sistema com parâmetros a, b
*"`x+ay=b; x+y=a`... mark the wrong statement."*

**Resolução:** subtraia as equações: `(a−1)y = b−a`.
- Se `a≠1`: `y` determinado → há solução (pelo menos uma). ✔
- Se `a=1`: vira `0·y = b−1`. Se `b=1` → ∞ soluções (reta); se `b≠1` → nenhuma.
Analise cada alternativa com esses casos para achar a **falsa**.
**Lição:** **isole o parâmetro** e separe os casos `a=1` vs `a≠1`.

### 📌 2024 — Q15: Potência de matriz de rotação (`A¹² = I`?)
*"Which option causes `A¹² = I` to be false?"*

**Resolução:** as matrizes são **rotações** por ângulos (`45°, 30°, 60°, 90°...`).
`Aⁿ` = rotação por `n·θ`. `A¹²=I` exige `12θ` múltiplo de `360°`. Ache o ângulo cujo `12θ`
não fecha a volta inteira.
**Lição:** **matriz de rotação** `[[cosθ,−sinθ],[sinθ,cosθ]]` elevada a n = rotação por `nθ`.

### 📌 2023 — Q8: Sistema 4×4
*"Solution of the system..."* Gabarito: **(c)** `x=8, y=−4, z=2, t=−1`.

**Resolução:** use as equações mais simples primeiro (`x+2y=0` e `t/y=1/4` dão relações diretas),
substitua nas demais. Ou **teste as alternativas** (mais rápido numa prova sem calculadora).
**Lição:** quando há alternativas numéricas, **substituir é frequentemente o caminho mais rápido**.

### 📌 2021 — Q10: Três planos no 1º octante
*"...three planes form a system which..."* Discussão geométrica: os três planos se cruzam?

**Lição:** 3 planos → analisar se concorrem num ponto (solução única), numa reta (∞) ou em nada.

---

## 3. Exercícios de treino

**E1.** Calcule `det[[2,1],[3,4]]`.

**E2.** Discuta o sistema em função de `k`: `{ x + y = 2 ; 2x + 2y = k }`. Para quais `k` há solução?
E quantas?

**E3.** Se `A = [[1,1],[0,1]]`, calcule `A³`.

**E4.** Para que valores de `m` o sistema `{ x + my = 1 ; mx + y = 1 }` tem **solução única**?

**E5.** Sabendo que `det A = 3` (matriz 3×3), quanto vale `det(2A)`?

**E6.** `A` é a matriz de rotação de `30°`. Qual o menor `n>0` tal que `Aⁿ = I`?

---

## 4. Gabarito e resoluções

**E1.** `2·4 − 1·3 = 8 − 3 = **5**`.

**E2.** As equações são proporcionais no lado esquerdo (`2x+2y = 2(x+y)`). Então precisamos `k = 2·2 = 4`.
- Se `k=4`: as duas equações são a mesma → **infinitas soluções** (SPI).
- Se `k≠4`: retas paralelas distintas → **nenhuma solução** (SI).

**E3.** `A² = [[1,2],[0,1]]`, `A³ = [[1,3],[0,1]]`. (Matriz de cisalhamento: o canto soma n.)

**E4.** `det = 1·1 − m·m = 1 − m²`. Solução única ⟺ `1−m² ≠ 0` ⟺ `**m ≠ ±1**`.

**E5.** `det(2A) = 2³·det A = 8·3 = **24**` (para 3×3, o escalar sai elevado à ordem n).

**E6.** Rotação de `30°`: precisamos `n·30° = 360°` → `**n = 12**`.
