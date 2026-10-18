# Revisão das provas de 2º SEMESTRE — Sequências, PA/PG e Séries

Revisão completa das **5 provas de 2º semestre (2021 a 2025)** para este tema.
Gabaritos oficiais: 2022-2ºSem e 2025-2ºSem.

---

### 2024/2º — Q10: Sequência de Lucas/Fibonacci via complexos
Aₙ = (1/√(3)i)[((1+√3 i)/2)ⁿ − ((1−√3 i)/2)ⁿ], n∈ℕ. A sequência é composta de
(a) naturais · (b) inteiros (alguns negativos) · (c) racionais não inteiros · (d) reais com irracionais
· (e) complexos não reais
→ `(1±√3 i)/2` têm módulo 1 e argumento `±60°` → são `e^{±iπ/3}`. A fórmula é a de uma sequência real
(tipo seno). **Analise se os termos são inteiros.** *(híbrida com complexos — tema 09)*

### 2024/2º — Q13: Série geométrica com incógnita no denominador
2 + 4/m + 8/m² + ⋯ = 14/2 = 7. Find m.
(a) 5 · (b) 6 · (c) 7 · (d) 8 · (e) none
→ PG de 1º termo 2 e razão `2/m`: soma `= 2/(1−2/m) = 2m/(m−2) = 7 → 2m = 7m−14 → m = 14/5`?
não inteiro → provavelmente **(e)**. Confira a conta e a convergência (`|2/m|<1`).

---

### 2023/2º — Q6: Série alternada com raízes
Sₙ = Σ(−1)ⁱ√(2^{i−1}) = −1+√2−2+2√2−4+4√2−⋯ Find lim Sₙ.
(a) −∞ · (b) −3−√2 · (c) √2+1 · (d) +∞ · (e) no defined limit
→ Separe em duas PGs (termos pares e ímpares) de razão relacionada a √2; teste convergência.
Como `√2>1`, os termos **crescem** em módulo → provavelmente **sem limite definido / diverge**.

---

### 2022/2º — Q15: Convergência de sequência trigonométrica
aₙ = cos^{n+1}(nθ). Mark the right statement about convergence:
(a) converge para θ∈(0,π) · (b) θ∈(π,2π) · (c) θ=π · (d) θ=2π · (e) all true
**Gabarito: (e)** — analise `|cos(nθ)|≤1`; a potência `n+1` faz o termo tender a 0 (quando `|cos|<1`)
ou estabilizar. *(híbrida com trigonometria — tema 07)*

---

### 2021/2º — Q2: Soma telescópica / sistema triangular (ver tema 02)
xₖ = 2^{k−1}; x₁₀ = 512. Padrão de **sequência definida por somas parciais**.

---

## Observação sobre frequência (2º sem)
Sequências/séries aparece de forma moderada (como nos 1ºs semestres), muitas vezes **cruzada com
complexos** (2024/2) ou **trigonometria** (2022/2). O ponto a dominar: **reconhecer a PG**, achar a
razão e **testar convergência** pelo módulo da razão (`|q|<1`).

---

## Resoluções detalhadas

### 2024/2 — Q13 (PG com incógnita → provável (e))
`2 + 4/m + 8/m² + …` é PG de 1º termo `a=2` e razão `q=2/m`. Converge se `|2/m|<1` (|m|>2).
Soma `= a/(1−q) = 2/(1−2/m) = 2m/(m−2)`. Igualando a `7`: `2m = 7(m−2) → 2m = 7m−14 → 5m=14 → m=14/5`.
Como `14/5` não está entre as opções inteiras (a)-(d), a resposta é **(e) none of the above**.

### 2023/2 — Q6 (série alternada com √2 → diverge/sem limite)
`Sₙ = Σ(−1)ⁱ√(2^{i−1})`. Os termos em módulo são `√(2^{i−1}) = (√2)^{i−1}`, que **crescem** (razão √2 > 1).
Uma série cujos termos não tendem a zero **não converge**. Logo o limite não existe (ou é ±∞ dependendo
da soma parcial). Analise as somas pares/ímpares para a forma exata.

### 2022/2 — Q15 (cosⁿ⁺¹(nθ) convergência)
`|cos(nθ)| ≤ 1`. Se `|cos(nθ)|<1`, a potência `n+1` → 0. Nos casos `θ=π` e `θ=2π`, `cos(nθ)=±1`,
e a sequência estabiliza. Analisando todas as opções, **todas as afirmações se mostram verdadeiras**
→ **(e)**.

---

## Exercícios de treino (2º sem)

**T1.** Soma da PG infinita `5 + 5/2 + 5/4 + …`.

**T2.** Para que valores de `q` a PG infinita `Σ qⁿ` converge?

**T3.** A série `Σ (−1)ⁿ · 2ⁿ` converge? Por quê?

**T4.** Some `1 + 1/3 + 1/9 + 1/27 + …`.

---

## Gabarito dos exercícios (2º sem)

**T1.** Razão `1/2`: `S = 5/(1−1/2) = 10`.

**T2.** Converge ⟺ `|q| < 1`.

**T3.** **Não** converge: os termos `(−1)ⁿ2ⁿ` crescem em módulo (não tendem a zero).

**T4.** Razão `1/3`: `S = 1/(1−1/3) = 3/2`.
