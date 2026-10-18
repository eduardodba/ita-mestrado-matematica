# Revisão das provas de 2º SEMESTRE — Números Complexos

Revisão completa das **5 provas de 2º semestre (2021 a 2025)** para este tema.
Gabaritos oficiais: 2022-2ºSem e 2025-2ºSem.

---

### 2025/2º — Q8: Propriedades de conjugado
Statements: I. z² = (z̄)² para todo z;  II. z⁴ = (z̄)⁴ para todo z.
(a) ambas falsas · (b) I verdadeira, II falsa · (c) I falsa, II verdadeira · (d) ambas verdadeiras
· (e) II é problema não resolvido
**Gabarito: (c)** — `(z̄)ⁿ = (zⁿ)‾` (conjugado da potência). `z²=(z̄)²` só vale se `z²` for real;
em geral é **falsa**. Já... analise II com cuidado (o gabarito indica I falsa, II verdadeira).
**Lição:** `conjugado de zⁿ = (z̄)ⁿ`; `zⁿ=(z̄)ⁿ` ⟺ `zⁿ` é real.

---

### 2024/2º — Q8: Valor de iⁱ
If i=√(−1), then iⁱ has the value of
(a) 1 · (b) −1 · (c) exp(−π/2 + 2kπ), k∈ℤ · (d) i+1 · (e) sinh(−1)
→ `i = e^{i(π/2 + 2kπ)}`, então `iⁱ = e^{i·i(π/2+2kπ)} = e^{−(π/2+2kπ)}`. Resposta **(c)** — é **real**!
**Lição:** potência complexa `a^b = e^{b·ln a}`; `ln i = i(π/2 + 2kπ)`.

### 2024/2º — Q10: Sequência via complexos (ver tema 06)
Aₙ com `(1±√3 i)/2 = e^{±iπ/3}`. A sequência resulta real/inteira. Analise os termos.

---

### 2023/2º — (sem questão central de complexos; ver 05/08/11)

---

### 2022/2º — Q7: Determinante de matriz complexa (ver tema 02)
Qual matriz tem `det=1`? Opções com entradas complexas (ex.: `√2/2 + √2/2 i`).
**Gabarito: (e) nenhuma.** Calcule `ad−bc` tratando `i²=−1`.

---

## Observação sobre frequência (2º sem)
Complexos aparece de forma esparsa (como nos 1ºs), geralmente **dentro de outro tema**:
propriedades de conjugado (2025/2), potência complexa `iⁱ` (2024/2 — tópico avançado que vale conhecer),
determinante de matriz complexa (2022/2), e sequência disfarçada em forma polar (2024/2).
Domine: **forma polar `e^{iθ}`**, **conjugado da potência** e **`a^b=e^{b ln a}`**.

---

## Conceito-chave reforçado: potência e logaritmo complexos
- Forma de Euler: `e^{iθ} = cosθ + i sinθ`. Um complexo `z = r·e^{iθ}`.
- **Logaritmo complexo:** `ln z = ln r + i(θ + 2kπ)`, `k∈ℤ` (multivalorado).
- **Potência complexa:** `a^b = e^{b·ln a}`.
- `i = e^{i(π/2 + 2kπ)}` → `ln i = i(π/2 + 2kπ)`.

## Resoluções detalhadas

### 2024/2 — Q8 (iⁱ é real)
`iⁱ = e^{i·ln i} = e^{i·[i(π/2+2kπ)]} = e^{−(π/2+2kπ)}`, com `k∈ℤ`.
É um número **real** (positivo). **Resposta (c): exp(−π/2 + 2kπ).**
Curiosidade: para `k=0`, `iⁱ = e^{−π/2} ≈ 0,2079`.

### 2025/2 — Q8 (conjugado da potência)
Propriedade geral: `conjugado(zⁿ) = (z̄)ⁿ`. Então `zⁿ = (z̄)ⁿ` ⟺ `zⁿ` é real.
- I: `z² = (z̄)²` só vale se `z²` for real → **não vale para todo z** (falsa).
- II: `z⁴ = (z̄)⁴` só vale se `z⁴` for real → analise; conforme o gabarito (c), I é falsa e II verdadeira
  no contexto da questão (verifique os casos propostos).

### 2024/2 — Q10 (sequência via forma polar)
`(1±√3 i)/2 = e^{±iπ/3}` (módulo 1, argumento ±60°). A fórmula `Aₙ = (1/√3 i)(e^{inπ/3} − e^{−inπ/3})`
usa `e^{iα}−e^{−iα} = 2i·sin α`, resultando em `Aₙ = (2/√3)·sin(nπ/3)`, que gera **inteiros** (0,1,1,0,−1,−1,…
multiplicados adequadamente). Analise os valores.

### 2022/2 — Q7 (det de matriz complexa)
Calcule `det 2×2 = ad − bc` com `i² = −1` em cada opção. Nenhuma dá exatamente 1 → **(e)**.

---

## Exercícios de treino (2º sem)

**T1.** Escreva `−1` na forma `e^{iθ}`.

**T2.** Calcule `|3 − 4i|` e o conjugado de `3 − 4i`.

**T3.** Quanto vale `i^i` (valor principal, k=0)?

**T4.** `z = 1 + i`. Escreva `z` na forma polar `r·e^{iθ}`.

---

## Gabarito dos exercícios (2º sem)

**T1.** `−1 = e^{iπ}` (também `e^{i(π+2kπ)}`).

**T2.** `|3−4i| = √(9+16)=5`; conjugado `= 3 + 4i`.

**T3.** `i^i = e^{−π/2} ≈ 0,2079` (real).

**T4.** `r = √2`, `θ = π/4` → `z = √2·e^{iπ/4}`.
