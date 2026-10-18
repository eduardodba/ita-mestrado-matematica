# Tema 08 — Cálculo (Derivadas, Integrais, Taxas) 🟡

**Prioridade: APOIO — mas crescente.** 1 a 3 questões nos anos recentes (2024, 2025, 2026).
Foco em **regra da cadeia**, **taxa de variação**, **integrais definidas com substituição** e **coordenadas polares**.

> 💡 Você pediu especificamente a **regra da cadeia** — ela está na seção 1.2 e aparece em 2025 Q5 e 2024 Q13.

---

## 1. Conceitos e teoremas que você precisa saber

### 1.1 Derivadas básicas
| Função | Derivada |
|--------|----------|
| `xⁿ` | `n·x^(n−1)` |
| `eˣ` | `eˣ` |
| `ln x` | `1/x` |
| `sin x` | `cos x` |
| `cos x` | `−sin x` |
| `tan x` | `sec²x` |
| `arcsin x` | `1/√(1−x²)` |
| `arccos x` | `−1/√(1−x²)` |
| `arctan x` | `1/(1+x²)` |

### 1.2 Regra da cadeia ⭐ (você pediu!)
Para função composta `f(g(x))`:
> `d/dx f(g(x)) = f'(g(x)) · g'(x)`

**Em palavras:** derive a função de fora (mantendo o de dentro), multiplique pela derivada do de dentro.

**Exemplos:**
- `d/dx sin(x²) = cos(x²)·2x`
- `d/dx (3x+1)⁵ = 5(3x+1)⁴·3 = 15(3x+1)⁴`
- `d/dx arcsin(arcsin x) = 1/√(1−arcsin²x) · 1/√(1−x²)` ← **exatamente a 2025 Q5**
- `d/dx e^(sin²x) = e^(sin²x)·2 sin x cos x` ← aparece na 2024 Q14

**Regras que acompanham:**
- Produto: `(uv)' = u'v + uv'`
- Quociente: `(u/v)' = (u'v − uv')/v²`

### 1.3 Taxa de variação
A derivada `dp/dt` mede a **taxa de variação** de `p` no tempo. Em geometria dinâmica
(ex.: vértice que se move), derive a expressão (perímetro, área) em relação a `t`.

### 1.4 Integral definida
- `∫ xⁿ dx = x^(n+1)/(n+1)` (`n≠−1`); `∫ 1/x dx = ln|x|`.
- **Substituição (u-sub):** se `u=g(x)`, `du=g'(x)dx`. **Troque os limites** de integração para `u`.
  - Ex.: `∫₀^(π/2) e^(sin²x)·sinx·cosx dx`: note `sinx cosx dx = ½ d(sin²x)`. Com `u=sin²x`
    (de 0 a 1): `½∫₀¹ eᵘ du = ½(e−1)`.
- Área entre curvas; volume por `∫π[r(x)]²dx` (sólido de revolução).

### 1.5 Coordenadas polares
- `x = r cosθ`, `y = r sinθ`. Curva `r=f(θ)`.
- Derivada em cartesianas: `dy/dx = (dy/dθ)/(dx/dθ)`, com `x=r cosθ`, `y=r sinθ`.
- Tangente **vertical** quando `dx/dθ=0`; **horizontal** quando `dy/dθ=0`.

---

## 2. Resoluções comentadas (questões reais do ITA)

### 📌 2024 — Q14: `∫₀^(π/2) e^(sin²x)·sin x·cos x dx`
Gabarito: **(b) (e−1)/2**.

**Resolução:** substitua `u = sin²x` → `du = 2 sin x cos x dx` → `sin x cos x dx = du/2`.
Limites: `x=0→u=0`; `x=π/2→u=1`. Integral `= ½∫₀¹ eᵘ du = ½[eᵘ]₀¹ = ½(e−1)`.
**Lição:** reconheça `sin x cos x dx` como **meia diferencial de `sin²x`** e troque os limites.

### 📌 2024 — Q13: Taxa de variação do perímetro de um triângulo
*"Vertex B(1,t) moves in time t. Rate of change of perimeter at t=1."*

**Resolução:** escreva o perímetro `p(t)` = soma dos comprimentos dos lados (distâncias com raiz),
derive `dp/dt` e avalie em `t=1`. Usa **regra da cadeia** em cada raiz.
**Lição:** "rate of change" = **derivada**; derive a expressão e substitua o instante.

### 📌 2025 — Q5: Derivada de `arcsin(arcsin x)` (regra da cadeia pura)
**Resolução:** `d/dx arcsin(u) = u'/√(1−u²)` com `u=arcsin x`, `u'=1/√(1−x²)`.
Resultado: `1/[√(1−arcsin²x)·√(1−x²)]`. Uma das afirmações da questão testa isso.
**Lição:** **regra da cadeia** aninhada: derive de fora para dentro.

### 📌 2026 — Q8: Curva em coordenadas polares `r = θ`
*"Derivative dy/dx and condition for vertical tangent."*

**Resolução:** `x=θcosθ`, `y=θsinθ`. Derive em θ:
`dx/dθ = cosθ − θsinθ`, `dy/dθ = sinθ + θcosθ`. Então
`dy/dx = (sinθ+θcosθ)/(cosθ−θsinθ)`. Tangente paralela ao eixo y ⟺ `dx/dθ=0 ⟺ θtanθ=1`.
**Lição:** em polares, `dy/dx = (dy/dθ)/(dx/dθ)`; tangente vertical quando `dx/dθ=0`.

### 📌 2023 — Q7: Derivadas de `cosh(x)·cos(x)`
**Resolução:** aplique **regra do produto** repetidamente. Lembre `d/dx cosh x = sinh x`,
`d/dx sinh x = cosh x`. Verifique cada afirmação derivando.
**Lição:** funções hiperbólicas derivam "como" trig, mas **sem o sinal negativo** em cosh/sinh.

---

## 3. Exercícios de treino

**E1.** Derive `f(x) = (x² + 1)⁴`.

**E2.** Derive `g(x) = sin(3x)`.

**E3.** Calcule `∫₀¹ 2x·e^(x²) dx`.

**E4.** Derive `h(x) = ln(cos x)`.

**E5.** A área de um quadrado de lado `s` cresce. Se `s` aumenta a 2 cm/s, qual a taxa de variação
da área quando `s = 5 cm`?

**E6.** Calcule `∫₁^e (1/x) dx`.

---

## 4. Gabarito e resoluções

**E1.** Cadeia: `f'(x) = 4(x²+1)³·2x = 8x(x²+1)³`.

**E2.** Cadeia: `g'(x) = cos(3x)·3 = 3cos(3x)`.

**E3.** `u=x²`, `du=2x dx`. Limites 0→0, 1→1: `∫₀¹ eᵘ du = e−1`.

**E4.** Cadeia: `h'(x) = (1/cos x)·(−sin x) = −tan x`.

**E5.** `A=s²`, `dA/dt = 2s·ds/dt = 2·5·2 = **20 cm²/s**`.

**E6.** `[ln x]₁^e = ln e − ln 1 = 1 − 0 = **1**`.

---

## 5. Banco de questões reais

As questões deste tema nas 6 provas (2021–2026), com enunciado original em inglês e gabarito
(quando divulgado), estão em **[QUESTOES-DAS-PROVAS.md](QUESTOES-DAS-PROVAS.md)**.
