# Revisão das provas de 2º SEMESTRE — Cálculo (Limites, Derivadas, Integrais)

Revisão completa das **5 provas de 2º semestre (2021 a 2025)** para este tema.
Gabaritos oficiais: 2022-2ºSem e 2025-2ºSem.

> **Os 2ºs semestres cobram MAIS cálculo que os 1ºs** — inclusive **limites** (que não apareciam antes),
> integrais impróprias e análise de funções. Reforce este tema.

---

## Quadro extra — Limites (novidade dos 2ºs semestres)
- **L'Hôpital:** se `lim f/g` dá `0/0` ou `∞/∞`, então `lim f/g = lim f'/g'`.
- Limite de `0/0` com raízes: **racionalize** (multiplique pelo conjugado) ou use L'Hôpital.
- Integral imprópria: `∫₀^∞` resolve-se por `lim_{b→∞} ∫₀^b`.

---

### 2025/2º — Q1: Limite com raízes (0/0)
lim_{x→2} (√(3x−2) − 2)/(√(4x+1) − 3)
(a) 1/2 · (b) 2/3 · (c) 3/4 · (d) 9/8 · (e) 4/3
**Gabarito: (d)** — em `x=2` dá `0/0`. Racionalize numerador e denominador (ou L'Hôpital):
`f'=3/(2√(3x−2))`, `g'=4/(2√(4x+1))` → em `x=2`: `(3/4)/(4/6)=(3/4)·(6/4)=9/8`.

### 2025/2º — Q3: Raiz da derivada (ver também tema 05)
f(x)=(x²−x−1)². A afirmação (e) diz que `x=1/2` é raiz de `f'`. Derive: `f'=2(x²−x−1)(2x−1)`;
`2x−1=0 → x=1/2` ✔. **A afirmação errada é a (c)** (forma fatorada incorreta).

---

### 2024/2º — Q2: Análise de f(x)=x·ln(1/x) (ver também tema 04)
Mark what one CANNOT say (limite, f(1), derivada, máximo, integral).
**Gabarito: (d)** — o máximo não é em `x=e⁻¹`. Derive `f'=ln(1/x)−1`; `f'=0 → ln(1/x)=1 → x=e⁻¹`...
analise com cuidado o domínio `(0,1]` e o sinal.

### 2024/2º — Q3: Função com f''=a constante (MRUV disfarçado)
f com f''=a≠0, f'(x₀)=b, f(x₀)=c. Avalie:
(I) f(x)=a(x−x₀)²+b(x−x₀)+c  (II) [f'(x₁)]² = [f'(x₀)]² + 2a[f(x₁)−f(x₀)]
→ (I) está errada (falta o ½: deveria ser `(a/2)(x−x₀)²`). (II) é a equação de Torricelli, **correta**.
**Lição:** `f''=a` constante → `f` é parábola `(a/2)(x−x₀)²+...`; análogo à cinemática (Torricelli).

---

### 2023/2º — Q9: Integral imprópria
∫₀^∞ x·e^{−x²} dx
(a) −1 · (b) 0 · (c) 1/2 · (d) 1 · (e) ∞
**Gabarito: (c)** — `u=x²`, `du=2x dx`: `½∫₀^∞ e^{−u} du = ½·[−e^{−u}]₀^∞ = ½·(0−(−1)) = 1/2`.

### 2023/2º — Q12: Resolver f'(x)=f(x) para f=√(1−x²)
For what real x does f'(x)=f(x), with f=√(1−x²)?
→ `f'=−x/√(1−x²)`. Iguale a `√(1−x²)`: `−x/√(1−x²)=√(1−x²) → −x=1−x² → x²−x−1=0 → x=(1±√5)/2`.
Só a raiz em `[−1,1]` serve: `x=(1−√5)/2`. (razão áurea de novo!)

### 2023/2º — Q15: Integral racional
∫₀^{e−1} (x+2)/(x+1) dx
(a) e−1 · (b) 2 · (c) e · (d) e+1 · (e) ∞
→ `(x+2)/(x+1) = 1 + 1/(x+1)`. Integral `= [x + ln(x+1)]₀^{e−1} = (e−1) + ln(e) − 0 = e−1+1 = e`.
Resposta **(c) e**.

---

### 2022/2º — Q9: Derivadas de arc-funções (ver tema 07)
`(arcsin)'+(arccos)'=0`, etc. **Gabarito (e) todas corretas.**

---

## Observação sobre frequência (2º sem)
Cálculo é **mais presente** nos 2ºs semestres: limites (2025/2), integrais definidas e impróprias
(2023/2 — duas questões!), análise de função/derivada (2024/2, 2025/2). Reforce:
**L'Hôpital/racionalização**, **integral por substituição**, **integral de função racional** (divisão),
e a conexão `f''=cte → parábola` (Torricelli).

---

## Resoluções detalhadas

### 2025/2 — Q1 (limite 0/0 → 9/8)
Em `x=2`: numerador `√4−2=0`, denominador `√9−3=0` → forma `0/0`.
**Racionalizando** (ou L'Hôpital):
`d/dx √(3x−2) = 3/(2√(3x−2))` → em x=2: `3/(2·2)=3/4`.
`d/dx √(4x+1) = 4/(2√(4x+1))` → em x=2: `4/(2·3)=2/3`.
Limite `= (3/4)/(2/3) = 9/8`. **Resposta (d).**

### 2023/2 — Q9 (integral imprópria → 1/2)
`∫₀^∞ x e^{−x²} dx`. Com `u=x²`, `du=2x dx`:
`= ½ ∫₀^∞ e^{−u} du = ½ [−e^{−u}]₀^∞ = ½ (0 − (−1)) = 1/2`. **Resposta (c).**

### 2023/2 — Q15 (integral racional → e)
`(x+2)/(x+1) = 1 + 1/(x+1)`. `∫₀^{e−1} [1 + 1/(x+1)] dx = [x + ln(x+1)]₀^{e−1}`
`= (e−1) + ln(e) − (0 + ln 1) = (e−1) + 1 − 0 = e`. **Resposta (c).**

### 2024/2 — Q3 (f''=a constante → Torricelli)
`f''=a` constante ⟹ `f'(x) = a(x−x₀) + b` ⟹ `f(x) = (a/2)(x−x₀)² + b(x−x₀) + c`.
- Statement (I) diz `a(x−x₀)²` (sem o ½) → **errada**.
- Statement (II) é `[f'(x₁)]² = [f'(x₀)]² + 2a[f(x₁)−f(x₀)]` → é a **equação de Torricelli**, **correta**.

### 2023/2 — Q12 (f'=f para √(1−x²))
`f = √(1−x²)`, `f' = −x/√(1−x²)`. Igualando: `−x/√(1−x²) = √(1−x²)` → `−x = 1−x²` →
`x² − x − 1 = 0` → `x = (1±√5)/2`. Só `(1−√5)/2 ≈ −0,618` está em `[−1,1]`. **Resposta (a).**

---

## Exercícios de treino (2º sem)

**T1.** `lim_{x→0} (sin x)/x`.

**T2.** `∫₀^∞ e^{−2x} dx`.

**T3.** `∫₁^2 (x+1)/x dx`.

**T4.** Se `f''(x) = 6` para todo x, `f'(0)=2`, `f(0)=1`, escreva `f(x)`.

---

## Gabarito dos exercícios (2º sem)

**T1.** `= 1` (limite fundamental).

**T2.** `[−½ e^{−2x}]₀^∞ = 0 − (−½) = 1/2`.

**T3.** `∫₁^2 (1 + 1/x) dx = [x + ln x]₁^2 = (2+ln2) − (1+0) = 1 + ln 2`.

**T4.** `f'(x)=6x+2`; `f(x)=3x²+2x+1`.
