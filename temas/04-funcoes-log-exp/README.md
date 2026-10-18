# Tema 04 — Funções, Logaritmos e Exponenciais 🟠

**Prioridade: MÉDIA-ALTA.** Cai quase todo ano. Destaque para **equações exponenciais
redutíveis ao 2º grau** (`4^x − 2^(x+2) + 3 = 0`) e **propriedades de logaritmo**.

---

## 1. Conceitos e teoremas que você precisa saber

### 1.1 Funções — ideias-chave
- **Domínio** (onde a função existe), **imagem** (valores que assume).
- **Injetora** (não repete imagem), **sobrejetora** (cobre todo o contradomínio),
  **bijetora** (as duas) → só bijetora tem **inversa**.
- Função **par** `f(−x)=f(x)` (simétrica ao eixo y); **ímpar** `f(−x)=−f(x)` (simétrica à origem).
- Inversa: reflete o gráfico na reta `y=x`; `f(f⁻¹(x)) = x`.

### 1.2 Exponenciais
- `aˣ·aʸ = a^(x+y)`, `(aˣ)ʸ = a^(xy)`, `a⁰=1`.
- `4ˣ = (2²)ˣ = (2ˣ)²`. ⭐ **Substituição** `u = 2ˣ` transforma muitas equações em 2º grau.
- `2^(x+2) = 2ˣ·2² = 4·2ˣ`.
- Exponencial é sempre **positiva**: `aˣ > 0`. Descarte raízes de `u` que sejam ≤ 0.

### 1.3 Logaritmos
- Definição: `log_a(b) = c ⟺ aᶜ = b` (com `a>0, a≠1, b>0`).
- Propriedades:
  - `log(xy) = log x + log y`
  - `log(x/y) = log x − log y`
  - `log(xⁿ) = n·log x`
  - **Mudança de base:** `log_a(b) = log(b)/log(a) = 1/log_b(a)`
- `ln` = logaritmo natural (base `e ≈ 2,718`).
- **Domínio:** argumento do log deve ser **> 0** — sempre cheque e descarte soluções inválidas.

### 1.4 Gráficos
- `y = log_a(x)` cresce devagar; passa por `(1,0)`; assíntota no eixo y.
- Relações de leitura de gráfico aparecem (ex.: 2026 Q10 com `log₁₀`).

---

## 2. Resoluções comentadas (questões reais do ITA)

### 📌 2026 — Q4: Equação exponencial `4^x − 2^(x+2) + 3 = 0`
Gabarito: **(c) tem duas soluções reais**.

**Resolução:** `4ˣ = (2ˣ)²` e `2^(x+2) = 4·2ˣ`. Seja `u = 2ˣ > 0`:
`u² − 4u + 3 = 0` → `(u−1)(u−3)=0` → `u=1` ou `u=3`.
Ambos positivos ✔ → `2ˣ=1 → x=0` e `2ˣ=3 → x=log₂3`. **Duas soluções reais.**
**Lição:** padrão clássico — substitua `u=2ˣ`, resolva o 2º grau, **mantenha só u>0**.

### 📌 2026 — Q10: Gráfico de `y = log₁₀(x)` com OA = BC
**Resolução:** traduza as distâncias no gráfico em relações entre `log` dos pontos.
`OA = BC` vira uma igualdade entre logaritmos que, simplificada, dá a relação entre `a,b,c`.
**Lição:** leitura de gráfico de log = **transformar distâncias em equações de log**.

### 📌 2025 — Q5: `f(x) = arcsin(arcsin(x))` (função composta + inversa)
*"Mark the wrong statement."* Gabarito: **(a)**.

**Resolução:** analise domínio (precisa `arcsin(x) ∈ [−1,1]`), se é ímpar, e a derivada
pela **regra da cadeia**. Uma das afirmações sobre imagem/bijeção é falsa.
**Lição:** composição de inversas exige cuidado com **domínio encadeado**; derivada pela cadeia.

### 📌 2023 — Q9: Simplificar `log_a(√(a³/b))`
Gabarito: **(e) nenhuma vale para todo a,b**.

**Resolução:** `log_a(√(a³/b)) = ½·log_a(a³/b) = ½(3 − log_a b)`.
Compare com as alternativas — as que usam `log(3)` ou `logb(a)` de forma incorreta falham.
**Lição:** aplique `log(√X)=½log X` e `log(a³)=3` (na base a); cuidado com trocas de base.

### 📌 2022 — Q7: Qual expressão dividida por `ln(x+1)` dá número racional?
**Resolução:** fatore os argumentos. `ln(x⁴−4x³+6x²−4x+1)=ln((x−1)⁴)=4ln(x−1)` — não é `ln(x+1)`.
Procure a opção cujo `ln` seja **múltiplo de `ln(x+1)`**. `x²−1=(x−1)(x+1)`... analise cada uma.
**Lição:** **fatore** o argumento do log para revelar `ln(x+1)` como fator.

### 📌 2021 — Q4: `1/x^(ln x + 2) = e`
**Resolução:** aplique `ln` nos dois lados: `−(ln x + 2)·ln x = 1`. Seja `t=ln x`:
`−(t+2)t = 1` → `t²+2t+1=0` → `(t+1)²=0` → `t=−1` → `ln x = −1` → `x = 1/e`.
**Lição:** **tome `ln` dos dois lados** e substitua `t=ln x` para virar polinômio.

---

## 3. Exercícios de treino

**E1.** Resolva `9ˣ − 4·3ˣ + 3 = 0`.

**E2.** Simplifique `log₂(32) + log₃(1/9)`.

**E3.** Se `log x = 0,30` e `log y = 0,48`, quanto vale `log(x²y)`?

**E4.** Qual o domínio de `f(x) = ln(x² − 4)`?

**E5.** A função `f(x) = x³` é par, ímpar ou nenhuma? E `g(x)=x²+1`?

**E6.** Resolva `2^(2x) − 5·2ˣ + 4 = 0`.

---

## 4. Gabarito e resoluções

**E1.** `u=3ˣ`: `u²−4u+3=0 → u=1 ou 3`. `3ˣ=1→x=0`; `3ˣ=3→x=1`. **x ∈ {0, 1}**.

**E2.** `log₂32 = 5` (pois `2⁵=32`); `log₃(1/9)=log₃(3⁻²)=−2`. Soma = `5+(−2)= **3**`.

**E3.** `log(x²y)=2log x + log y = 2(0,30)+0,48 = 0,60+0,48 = **1,08**`.

**E4.** Precisa `x²−4>0` → `x<−2` ou `x>2` → **(−∞,−2) ∪ (2,+∞)**.

**E5.** `x³`: `f(−x)=−x³=−f(x)` → **ímpar**. `x²+1`: `g(−x)=x²+1=g(x)` → **par**.

**E6.** `u=2ˣ`: `u²−5u+4=0 → (u−1)(u−4)=0 → u=1 ou 4`. `2ˣ=1→x=0`; `2ˣ=4→x=2`. **x ∈ {0, 2}**.

---

## 5. Banco de questões reais

As questões deste tema nas 6 provas (2021–2026), com enunciado original em inglês e gabarito
(quando divulgado), estão em **[QUESTOES-DAS-PROVAS.md](QUESTOES-DAS-PROVAS.md)**.
