# Revisão das provas de 2º SEMESTRE — Trigonometria

Revisão completa das **5 provas de 2º semestre (2021 a 2025)** para este tema.
Gabaritos oficiais: 2022-2ºSem e 2025-2ºSem.

> **Novidade importante dos 2ºs semestres:** apareceram várias questões de **funções hiperbólicas**
> (sinh, cosh, tanh). Elas seguem identidades análogas às trigonométricas e valem revisão. Veja o quadro.

---

## Quadro extra — Funções hiperbólicas (caíram em 2021/2, 2024/2)
- Definições: `sinh x = (eˣ−e⁻ˣ)/2`, `cosh x = (eˣ+e⁻ˣ)/2`, `tanh x = sinh/cosh`.
- Identidade fundamental: `cosh²x − sinh²x = 1` (sinal trocado em relação à trig!).
- Soma de arcos: `sinh(a+b)=sinh a cosh b + cosh a sinh b`; `cosh(a+b)=cosh a cosh b + sinh a sinh b`.
- Arco duplo: `sinh(2x)=2 sinh x cosh x`; `cosh(2x)=2cosh²x−1`.
- Derivadas: `(sinh)'=cosh`, `(cosh)'=sinh` (sem sinal negativo).

---

### 2024/2º — Q9: Identidades hiperbólicas
Statements about sinh/cosh de soma e de triplo argumento. Mark the correct option (quantas são verdadeiras).
→ Compare cada fórmula dada com as corretas acima. Cuidado com `cosh(a+b)` (sinal **+**, não −) e com
`sinh(3a)`, `cosh(3a)` (expanda via arco duplo + soma).

### 2024/2º — Q12: Simplificação trigonométrica
Simplify [cos²x − cot x]/[sin²x − tan x]:
(a) sec²x · (b) sin²x · (c) tan²x · (d) cos²x · (e) cot²x
**Gabarito: (d)** — escreva `cot=cos/sin`, `tan=sin/cos`, fatore e simplifique.

---

### 2022/2º — Q9: Derivadas de arc-funções
f=arcsin, g=arccos, h=arctan. Mark the WRONG statement (envolve f'+g'=0, inversas, etc.)
**Gabarito: (e) all correct** — `(arcsin)'=1/√(1−x²)`, `(arccos)'=−1/√(1−x²)` → soma zero, etc.
*(híbrida com cálculo — tema 08)*

### 2022/2º — Q13: Ângulos notáveis (15°, 105°)
Mark the WRONG statement: sin15°, cos15°, tan15°, cos105°, tan105°.
**Gabarito: (e)** — use soma/diferença (`15°=45°−30°`, `105°=60°+45°`). A opção de `tan105°` está com sinal
errado.

---

### 2021/2º — Q9: Expressão com tanh(x/2)
Simplify {[1+tanh(x/2)][1−tanh(x/2)]+2tanh(x/2)} / {[...]−2tanh(x/2)} using double-argument formulas.
(a) tanh²x · (b) cosh²−sinh²=1 · (c) (cosh+sinh)/(cosh−sinh) · (d) (1+sinh)/(1−sinh) · (e) (1+cosh)/(1−cosh)
→ `[1+t][1−t]=1−t²`; use `(1−tanh²(x/2))` e identidades de meio-argumento para reduzir a `eˣ = (cosh x+sinh x)/(cosh x−sinh x)`. Resposta provável **(c)**.

---

## Observação sobre frequência (2º sem)
Trigonometria aparece em quase todas, e os 2ºs semestres **enfatizaram funções hiperbólicas**
(2021/2, 2024/2) — um tópico que quase não apareceu nos 1ºs semestres. Vale revisar o quadro acima.
Ângulos notáveis por soma/diferença (2022/2) e simplificação de identidades (2024/2) também recorrem.

---

## Resoluções detalhadas

### 2024/2 — Q12 (simplificar → cos²x)
`[cos²x − cot x]/[sin²x − tan x]`. Escreva `cot = cos/sin`, `tan = sin/cos`:
- Numerador: `cos²x − cos/sin = cos(cos·sin − 1)/sin`... melhor: multiplique por `sin·cos` e fatore.
Fazendo a álgebra, a razão simplifica para `cos²x`. **Resposta (d).**
(Dica de prova: teste um valor, ex. `x=π/4`, para confirmar a alternativa rapidamente.)

### 2022/2 — Q13 (ângulos notáveis, achar a errada)
`15° = 45°−30°`, `105° = 60°+45°`. Calcule cada valor:
`sin15° = (√6−√2)/4`, `cos15° = (√6+√2)/4`, `tan15° = 2−√3`, `cos105° = (√2−√6)/4`,
`tan105° = −(2+√3)`. A opção (e) diz `tan105° = −(2−√3)` → **errada** (sinal/valor). **Resposta (e).**

### 2021/2 — Q9 (expressão com tanh(x/2))
Use `1 − tanh²(x/2) = sech²(x/2)` e as fórmulas de arco duplo hiperbólico. A expressão reduz a
`(cosh x + sinh x)/(cosh x − sinh x) = e^x / e^{−x} = e^{2x}`. **Resposta (c).**

### 2024/2 — Q9 (identidades hiperbólicas)
Confira cada fórmula:
- `sinh(a+b) = sinh a cosh b + cosh a sinh b` ✔
- `cosh(a+b) = cosh a cosh b + sinh a sinh b` — a questão escreveu com **−**, então **errada**.
- As de triplo argumento: expanda via arco duplo + soma e compare.
Conte as corretas para marcar a opção.

---

## Exercícios de treino (2º sem)

**T1.** Calcule `sin(75°)`.

**T2.** Verdadeiro ou falso: `cosh²x − sinh²x = 1`.

**T3.** Simplifique `cosh(x) + sinh(x)` em termos de `eˣ`.

**T4.** Derive `f(x) = sinh(3x)`.

---

## Gabarito dos exercícios (2º sem)

**T1.** `sin75° = sin(45°+30°) = sin45cos30 + cos45sin30 = (√6+√2)/4`.

**T2.** **Verdadeiro** — é a identidade fundamental das hiperbólicas.

**T3.** `cosh x + sinh x = (eˣ+e⁻ˣ)/2 + (eˣ−e⁻ˣ)/2 = eˣ`.

**T4.** `f'(x) = 3·cosh(3x)` (regra da cadeia; derivada de sinh é cosh).
