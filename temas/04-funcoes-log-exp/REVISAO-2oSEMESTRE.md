# Revisão das provas de 2º SEMESTRE — Funções, Logaritmos e Exponenciais

Revisão completa das **5 provas de 2º semestre (2021 a 2025)** para este tema.
Gabaritos oficiais: 2022-2ºSem e 2025-2ºSem.

---

### 2025/2º — Q7: Equação logarítmica encaixada
If x>0, x≠1, x≠1/3 satisfies [2+log₃x]/[logₓ₊₂x − logₓ(x+2)] · [1/(1+log₃x)] = logₓ(x+2), then x belongs to
(a) (0,1/81) · (b) (1/81,1/3) · (c) (1/2,1) · (d) (1,3/2) · (e) (3/2,2)
**Gabarito: (b)** — use **mudança de base** para reduzir tudo a `log₃` e resolva a equação; localize o intervalo.

### 2025/2º — Q15: Equação com frações (isolamento)
If a,b,m>0 and (m+a)/(m+b) = 3a/b, what is m?
(a) 2ab/(b−3a) · (b) b/(3a) · (c) a/(2b) · (d) 4ab/(b−3a) · (e) (b−3a)/(2ab)
**Gabarito: (a)** — multiplique cruzado e isole `m`: `b(m+a)=3a(m+b) → m = 2ab/(b−3a)`.

---

### 2024/2º — Q2: Função x·ln(1/x) (análise + derivada + integral)
f(x)=x·ln(1/x) on (0,1]. Mark what one CANNOT say:
(a) lim_{x→0} f=0 · (b) f(1)=0 · (c) f'=1+ln(1/x) · (d) máximo em x=e⁻¹ · (e) ∫f dx = ...
**Gabarito: (d)** — derive e ache o ponto crítico; o máximo NÃO é em `e⁻¹` (verifique o sinal).
*(questão híbrida com cálculo — ver tema 08)*

### 2024/2º — Q11: Comparar logaritmos de bases diferentes
p=log₃2, q=log_{√3}4, r=log_{1/3}√2. Mark the correct ordering.
(a) p<q<r · (b) r<q<p · (c) q<r<p · (d) p<r<q · (e) r<p<q
**Gabarito: (a)... (verifique)** — converta todos para a **mesma base**: `q=log_{√3}4=4log₃2=4p`?
cuidado: `log_{√3}4 = 2·log₃4 = 4·log₃2 = 4p`; `r=log_{1/3}√2 = −½log₃2 = −p/2 < 0`. Ordene.

---

### 2023/2º — (sem questão central de log/exp; ver temas 05/08/11)

---

### 2022/2º — Q11: Equação log = ln
−log_{1/√e}(x) = ln(4x−3)
(a) no real roots · (b) one positive · (c) one negative · (d) two distinct real roots · (e) >2 positive
**Gabarito: (d)** — `log_{1/√e}(x) = ln x / ln(e^{−1/2}) = −2 ln x`. Então `2 ln x = ln(4x−3)`
→ `x² = 4x−3 → x²−4x+3=0 → x=1,3` (duas raízes reais).

---

### 2021/2º — Q3: ln(x)+ln(4−x)=1
(a) integer roots · (b) non-integer rational roots · (c) non-rational real roots · (d) no real roots · (e) none
→ `ln[x(4−x)] = 1 → x(4−x)=e → x²−4x+e=0`. `Δ=16−4e>0` → duas raízes reais irracionais.

### 2021/2º — Q12: Manipulação algébrica de frações
a=(x+y)/2, b=(x−y)/2, a'=(x+2y)/3, b'=x−y. Find b'/a'.
→ Expresse tudo em x,y e simplifique a razão até bater com uma das opções.

---

## Observação sobre frequência (2º sem)
Logaritmo apareceu em quase todas (2021/2, 2022/2, 2024/2, 2025/2). O padrão recorrente é
**mudança de base** para comparar/resolver (2024/2-Q11, 2025/2-Q7) e **log que vira equação de 2º grau**
(2022/2-Q11, 2021/2-Q3) — o mesmo tipo de raciocínio dos 1ºs semestres.

---

## Resoluções detalhadas

### 2024/2 — Q11 (ordenar logaritmos)
Converta tudo para base 3:
- `p = log₃2`
- `q = log_{√3}4 = ln4/ln√3 = (2ln2)/(½ln3) = 4·(ln2/ln3) = 4p`
- `r = log_{1/3}√2 = ln√2/ln(1/3) = (½ln2)/(−ln3) = −½·(ln2/ln3) = −p/2`
Como `p>0`: `r = −p/2 < 0 < p < 4p = q`. Logo `r < p < q` → **Resposta (e)**.
(Atenção: confira contra o gabarito da sua lista; o método é este.)

### 2022/2 — Q11 (log = ln → duas raízes)
`log_{1/√e}(x) = ln x / ln(e^{−1/2}) = ln x / (−½) = −2 ln x`.
A equação `−log_{1/√e}(x) = ln(4x−3)` vira `2 ln x = ln(4x−3)` → `x² = 4x−3` →
`x²−4x+3=0` → `x=1` ou `x=3`. Ambas com `4x−3>0` ✔. **Duas raízes → (d).**

### 2025/2 — Q15 (isolar m)
`(m+a)/(m+b) = 3a/b` → `b(m+a) = 3a(m+b)` → `bm + ab = 3am + 3ab` →
`bm − 3am = 2ab` → `m(b−3a) = 2ab` → `m = 2ab/(b−3a)`. **Resposta (a).**

### 2021/2 — Q3 (ln x + ln(4−x) = 1)
`ln[x(4−x)] = 1` → `x(4−x) = e` → `x² − 4x + e = 0`. `Δ = 16 − 4e ≈ 16 − 10,87 = 5,13 > 0`.
Duas raízes reais, **irracionais** (e não inteiras). Resposta: raízes reais não racionais.

---

## Exercícios de treino (2º sem)

**T1.** Ordene `log₂8`, `log₄16`, `log₃9`.

**T2.** Resolva `log₅(x) + log₅(x−4) = 1`.

**T3.** Simplifique `log_{1/2}(8)`.

**T4.** Resolva para `m`: `(m+2)/(m+1) = 4`.

---

## Gabarito dos exercícios (2º sem)

**T1.** `log₂8=3`, `log₄16=2`, `log₃9=2`. Ordem: `log₄16 = log₃9 = 2 < 3 = log₂8`.

**T2.** `log₅[x(x−4)]=1 → x(x−4)=5 → x²−4x−5=0 → (x−5)(x+1)=0`. Só `x=5` (domínio exige `x>4`).

**T3.** `log_{1/2}(8) = ln8/ln(1/2) = (3ln2)/(−ln2) = −3`.

**T4.** `m+2 = 4(m+1) → m+2 = 4m+4 → −3m = 2 → m = −2/3`.
