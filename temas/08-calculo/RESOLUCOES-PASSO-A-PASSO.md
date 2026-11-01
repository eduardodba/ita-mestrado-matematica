# Cálculo — Resoluções PASSO A PASSO

Resolução detalhada de cada questão deste tema nas provas PG-EIA/ITA (2021–2026, 1º e 2º semestres).
Estrutura: **o que pede**, **ideia-chave**, **desenvolvimento** e **conclusão**.

---

## 2026/1 — Q8: Curva polar r = θ → derivada e tangente vertical

**O que pede:** avaliar duas afirmações sobre `r = θ` (θ≥0): a expressão de `dy/dx` e a condição de
tangente paralela ao eixo y.

**Ideia-chave — Converter de polar para cartesiano e usar a regra da cadeia:** um ponto em polares é
`(r, θ)`; em cartesianas é `x = r cosθ`, `y = r sinθ`. Como `r = θ` depende de `θ`, tanto `x` quanto `y`
são funções só de `θ`. A inclinação da curva é `dy/dx`, mas como não temos `y` em função de `x`
diretamente, usamos:
> `dy/dx = (dy/dθ) ÷ (dx/dθ)` — ambas as derivadas em relação ao parâmetro `θ`.

**Desenvolvimento:**
1. Substituindo `r = θ`: `x = θ·cosθ` e `y = θ·sinθ`.
2. Derive cada uma usando a **regra do produto** `(uv)' = u'v + uv'`:
   - `dx/dθ = d/dθ(θ·cosθ) = (1)·cosθ + θ·(−sinθ) = cosθ − θ sinθ`.
   - `dy/dθ = d/dθ(θ·sinθ) = (1)·sinθ + θ·(cosθ) = sinθ + θ cosθ`.
3. Portanto `dy/dx = (dy/dθ)/(dx/dθ) = (sinθ + θ cosθ)/(cosθ − θ sinθ)`.
   → A afirmação **(I)** escreveu a fração **de cabeça para baixo** (`(cosθ − θsinθ)/(sinθ + θcosθ)`),
   que seria `dx/dy`, não `dy/dx` ⇒ **(I) está ERRADA**.
4. **Tangente paralela ao eixo y** significa tangente **vertical** — uma reta vertical tem inclinação
   "infinita", o que acontece quando o **denominador** de `dy/dx` zera (e o numerador não):
   `dx/dθ = 0 → cosθ − θ sinθ = 0 → cosθ = θ sinθ → 1 = θ·(sinθ/cosθ) → θ·tanθ = 1`.
   → A afirmação **(II)** diz exatamente `θ tanθ = 1` ⇒ **(II) está CORRETA**.

**Conclusão:** (I) errada, (II) correta → **alternativa (c)**.
(Chave: curva em `θ` ⇒ `dy/dx = (dy/dθ)/(dx/dθ)`; **tangente vertical** ⇔ **denominador** `dx/dθ = 0`.)

---

## 2025/1 — Q5: Derivada de arcsin(arcsin x) (regra da cadeia)

Ver também `../04-funcoes-log-exp/RESOLUCOES-PASSO-A-PASSO.md` (2025/1-Q5).

**Ideia-chave — Regra da cadeia aninhada:** `d/dx f(g(x)) = f'(g(x))·g'(x)`.

**Desenvolvimento:**
1. `f(x) = arcsin(u)`, com `u = arcsin x`.
2. `d/dx arcsin(u) = u'/√(1−u²)`, com `u' = 1/√(1−x²)`.
3. `f'(x) = 1/[√(1−arcsin²x)·√(1−x²)]` (confere com a opção (d)).
4. A afirmação **errada** é a (a), sobre bijetividade/imagem da composição.

**Conclusão:** afirmação errada → **alternativa (a)**. (Chave: regra da cadeia + domínio da composição.)

---

## 2024/1 — Q13: Taxa de variação do perímetro de triângulo → derivada

**O que pede:** `A(0,0)`, `C(0,1)` fixos, `B(1,t)` móvel; achar `dp/dt` do perímetro em `t=1`.

**Ideia-chave — Perímetro = soma de distâncias; derive em t (regra da cadeia em cada raiz).**

**Desenvolvimento:**
1. Lados:
   - `AC = 1` (constante, de (0,0) a (0,1)).
   - `AB = √((1−0)² + (t−0)²) = √(1 + t²)`.
   - `BC = √((1−0)² + (t−1)²) = √(1 + (t−1)²)`.
2. `p(t) = 1 + √(1+t²) + √(1+(t−1)²)`.
3. `dp/dt = t/√(1+t²) + (t−1)/√(1+(t−1)²)`.
4. Em `t=1`: `= 1/√2 + 0/√1 = 1/√2 = √2/2`.

**Conclusão:** `dp/dt = √2/2` → **alternativa (d)**.
(Chave: perímetro como soma de distâncias; derivar cada raiz pela cadeia.)

---

## 2024/1 — Q14: ∫₀^{π/2} e^{sin²x} sin x cos x dx → (e−1)/2

**O que pede:** calcular a integral definida.

**Ideia-chave — Substituição `u = sin²x`:** então `du = 2 sin x cos x dx`.

**Desenvolvimento:**
1. `u = sin²x → du = 2 sin x cos x dx → sin x cos x dx = du/2`.
2. Limites: `x=0 → u=0`; `x=π/2 → u=1`.
3. Integral: `∫₀¹ e^u · (du/2) = (1/2)∫₀¹ e^u du = (1/2)[e^u]₀¹ = (1/2)(e − 1)`.

**Conclusão:** `(e−1)/2` → **alternativa (b)**.
(Chave: reconhecer `sin x cos x dx` como meia diferencial de `sin²x`; trocar os limites.)

---

## 2023/1 — Q7: Derivadas de cosh(x)cos(x) → afirmação errada

**O que pede:** avaliar derivadas sucessivas de `f(x)=cosh x·cos x`.

**Ideia-chave — Regra do produto + derivadas de hiperbólicas (`cosh'=sinh`, `sinh'=cosh`).**

**Desenvolvimento:**
1. `f'(x) = sinh x·cos x + cosh x·(−sin x) = sinh x cos x − cosh x sin x` (confere (a)).
2. Derive novamente para checar `f''`, `f'''`, `f⁴` e as versões com `x/√2`.
3. A propriedade `d⁴/dx⁴[f(x/√2)] = −f(x/√2)` vem do fato de `cosh(x/√2)cos(x/√2)` satisfazer uma EDO de
   4ª ordem. Confira cada afirmação; todas se verificam ⇒ a resposta é "todas verdadeiras".

**Conclusão:** todas as afirmações são verdadeiras → **alternativa (e)**.
(Chave: produto + derivadas de hiperbólicas; o fator `1/√2` gera `d⁴/dx⁴ = −f`.)

---

## 2025/2 — Q1: Limite 0/0 com raízes → 9/8

**O que pede:** `lim_{x→2} (√(3x−2) − 2)/(√(4x+1) − 3)`.

**Ideia-chave — Forma 0/0 ⇒ L'Hôpital ou racionalização.**

**Desenvolvimento (L'Hôpital):**
1. Em `x=2`: numerador `√4 − 2 = 0`; denominador `√9 − 3 = 0` ⇒ `0/0`.
2. Derive numerador: `d/dx √(3x−2) = 3/(2√(3x−2))`; em `x=2`: `3/(2·2) = 3/4`.
3. Derive denominador: `d/dx √(4x+1) = 4/(2√(4x+1))`; em `x=2`: `4/(2·3) = 2/3`.
4. Limite `= (3/4)/(2/3) = (3/4)·(3/2) = 9/8`.

**Conclusão:** `9/8` → **alternativa (d)**. (Chave: 0/0 ⇒ L'Hôpital; razão das derivadas.)

---

## 2025/2 — Q3: Raiz da derivada de (x²−x−1)²

Ver `../05-polinomios-e-raizes/RESOLUCOES-PASSO-A-PASSO.md` (2025/2-Q3).
Resumo: `f'=2(x²−x−1)(2x−1)` zera em `x₁,x₂` e em `x=1/2`; a forma fatorada errada é a (c).

---

## 2024/2 — Q2: Análise de f(x)=x·ln(1/x) → afirmação errada

**O que pede:** marcar o que **não** se pode dizer sobre `f(x)=x ln(1/x)` em `(0,1]`.

**Ideia-chave — Reescrever `f(x) = x ln(1/x) = −x ln x` e testar cada afirmação.**

**Desenvolvimento — afirmação por afirmação (gabarito oficial: (c)):**
1. (a) `lim_{x→0⁺} (−x ln x) = 0` ✔ **verdadeira** (`x` tende a 0 mais rápido que `ln x` tende a −∞).
2. (b) `f(1) = 1·ln(1) = 0` ✔ **verdadeira**.
3. (c) Derivada: `f'(x) = d/dx[x·ln(1/x)] = ln(1/x) + x·d/dx[ln(1/x)] = ln(1/x) + x·(−1/x) = ln(1/x) − 1`.
   A afirmação (c) escreve `df/dx = 1 + ln(1/x)`, ou seja `ln(1/x) + 1`. O correto é `ln(1/x) − 1`
   (sinal do termo constante trocado) → **(c) é FALSA**.
4. (d) Máximo: `f'(x) = 0 → ln(1/x) − 1 = 0 → ln(1/x) = 1 → 1/x = e → x = e^{−1}`. Como `f'' < 0` aí,
   é máximo ✔ **verdadeira**.
5. (e) Integral por partes: `∫ −x ln x dx = −[x²/2·ln x − x²/4] = −x²/2 ln x + x²/4 = (x²/4)(1 − 2 ln x) + C`
   ✔ **verdadeira** (coincide com a opção (e)).

**Conclusão:** a afirmação errada é a **(c)** — a derivada correta é `ln(1/x) − 1`, não `1 + ln(1/x)`.
(Chave: `f = −x ln x`; `f' = ln(1/x) − 1`; só o termo constante da (c) está com sinal trocado.
Gabarito oficial 2024/2: **2-c**.)

---

## 2024/2 — Q3: f'' = a constante → statements (Torricelli)

**O que pede:** avaliar (I) `f(x)=a(x−x₀)²+b(x−x₀)+c` e (II) `[f'(x₁)]² = [f'(x₀)]² + 2a[f(x₁)−f(x₀)]`.

**Ideia-chave — Integrar f''=a duas vezes; (II) é a equação de Torricelli.**

**Desenvolvimento:**
1. `f'' = a ⇒ f'(x) = a(x−x₀) + b` (usando `f'(x₀)=b`).
2. `f(x) = (a/2)(x−x₀)² + b(x−x₀) + c` (usando `f(x₀)=c`).
   → A afirmação (I) escreve `a(x−x₀)²` **sem o ½** ⇒ (I) é **errada**.
3. (II): com `v=f'`, aceleração `a`, posição `f`, vale `v₁² = v₀² + 2a·Δf` (Torricelli) ⇒ (II) **correta**.

**Conclusão:** (I) errada, (II) correta → **alternativa (c)**.
(Chave: integrar f''=a dá `(a/2)(x−x₀)²`; Torricelli para (II).)

---

## 2023/2 — Q9: ∫₀^∞ x e^{−x²} dx → 1/2

**O que pede:** calcular a integral imprópria.

**Ideia-chave — Substituição `u = x²`:** `du = 2x dx`.

**Desenvolvimento:**
1. `u = x² → du = 2x dx → x dx = du/2`.
2. Limites: `x=0 → u=0`; `x→∞ → u→∞`.
3. `∫₀^∞ x e^{−x²} dx = (1/2)∫₀^∞ e^{−u} du = (1/2)[−e^{−u}]₀^∞ = (1/2)(0 − (−1)) = 1/2`.

**Conclusão:** `1/2` → **alternativa (c)**. (Chave: `u=x²`; integral imprópria convergente.)

---

## 2023/2 — Q12: f'(x) = f(x) para f = √(1−x²) → x = (1−√5)/2

**O que pede:** para que `x` real vale `f'(x) = f(x)`, com `f=√(1−x²)`.

**Ideia-chave — Derivar e igualar.**

**Desenvolvimento:**
1. `f = (1−x²)^{1/2}`; `f' = (1/2)(1−x²)^{−1/2}·(−2x) = −x/√(1−x²)`.
2. `f' = f → −x/√(1−x²) = √(1−x²)`.
3. Multiplique por `√(1−x²)`: `−x = 1 − x²`.
4. `x² − x − 1 = 0 → x = (1 ± √5)/2`.
5. Só `x = (1−√5)/2 ≈ −0,618` está em `[−1,1]` (domínio de `f`).

**Conclusão:** `x = (1−√5)/2` → **alternativa (a)**.
(Chave: derivada de raiz; cair em `x²−x−1=0` — a razão áurea.)

---

## 2023/2 — Q15: ∫₀^{e−1} (x+2)/(x+1) dx → e

**O que pede:** calcular a integral.

**Ideia-chave — Dividir a fração:** `(x+2)/(x+1) = 1 + 1/(x+1)`.

**Desenvolvimento:**
1. `(x+2)/(x+1) = (x+1+1)/(x+1) = 1 + 1/(x+1)`.
2. `∫₀^{e−1} [1 + 1/(x+1)] dx = [x + ln(x+1)]₀^{e−1}`.
3. Em `x=e−1`: `(e−1) + ln(e) = (e−1) + 1 = e`. Em `x=0`: `0 + ln(1) = 0`.
4. Resultado: `e − 0 = e`.

**Conclusão:** `e` → **alternativa (c)**.
(Chave: dividir a fração antes de integrar; `∫1/(x+1)dx = ln(x+1)`.)

---

## 2022/2 — Q9: Derivadas de arcsin/arccos/arctan → todas corretas

**O que pede:** marcar a afirmação **errada** (ou "todas corretas").

**Ideia-chave — Derivadas das arc-funções:**
`(arcsin)' = 1/√(1−x²)`; `(arccos)' = −1/√(1−x²)`; `(arctan)' = 1/(1+x²)`.

**Desenvolvimento:**
1. `f'+g' = 1/√(1−x²) + (−1/√(1−x²)) = 0` ✔.
2. As demais afirmações sobre inversas e combinações das derivadas também se verificam.
3. Portanto todas as afirmações estão corretas.

**Conclusão:** todas corretas → **alternativa (e)**.
(Chave: `arcsin' + arccos' = 0`.)

---

## Mapa rápido: qual ferramenta usar

| Questão | Ferramenta central |
|---------|--------------------|
| 2023/1-Q7 | Produto + derivadas hiperbólicas |
| 2024/1-Q13 | Perímetro = soma de distâncias; derivar |
| 2024/1-Q14 | Substituição `u=sin²x` |
| 2025/1-Q5 | Regra da cadeia (arcsin∘arcsin) |
| 2026/1-Q8 | Derivada em polares; tangente vertical |
| 2022/2-Q9 | Derivadas de arc-funções |
| 2023/2-Q9 | Substituição `u=x²` (imprópria) |
| 2023/2-Q12 | Derivar raiz ⇒ `x²−x−1=0` |
| 2023/2-Q15 | Dividir fração + ∫1/(x+1) |
| 2024/2-Q2 | `f=−x ln x`, ponto crítico |
| 2024/2-Q3 | Integrar f''=a; Torricelli |
| 2025/2-Q1 | Limite 0/0 (L'Hôpital) |
| 2025/2-Q3 | Raiz da derivada (ver tema 05) |
