# Tema 07 — Trigonometria 🟠

**Prioridade: MÉDIA.** Aparece quase todo ano (em 2022 foi forte, ~3 questões).
Foco em **identidades** (soma de arcos, sec/tan), **equações trigonométricas** e **lei dos senos/cossenos**.

---

## 1. Conceitos e teoremas que você precisa saber

### 1.1 Identidades fundamentais
- `sin²x + cos²x = 1`
- `sec x = 1/cos x`, `csc x = 1/sin x`, `cot x = 1/tan x`, `tan x = sin x / cos x`
- `1 + tan²x = sec²x`; `1 + cot²x = csc²x`

### 1.2 Soma e diferença de arcos
- `sin(a±b) = sin a·cos b ± cos a·sin b`
- `cos(a±b) = cos a·cos b ∓ sin a·sin b`
- `tan(a±b) = (tan a ± tan b)/(1 ∓ tan a·tan b)`
- **sec(a+b)** (2022 Q5): `1/cos(a+b) = 1/(cos a cos b − sin a sin b)`. Dividindo por `cos a cos b`:
  `sec(a+b) = sec a · sec b / (1 − tan a · tan b)`.

### 1.3 Arco duplo
- `sin(2x) = 2 sin x cos x`
- `cos(2x) = cos²x − sin²x = 1 − 2sin²x = 2cos²x − 1`
- `tan(2x) = 2tan x/(1 − tan²x)`

### 1.4 Equações trigonométricas
- Reduza tudo a **uma função** (ex.: use `cos 2θ = 1−2sin²θ` para ficar só em `sin θ`).
- Resolva a equação algébrica e **conte as soluções no intervalo pedido** (ex.: `[0,π]`).
- Cuidado: nem toda solução algébrica está no intervalo — e pode haver mais de uma.

### 1.5 Lei dos senos e cossenos (ligação com geometria)
- Senos: `a/sinA = 2R`. Cossenos: `c² = a²+b²−2ab·cosC`.

### 1.6 Funções trigonométricas inversas
- `arcsin`, `arccos`, `arctan` com domínios/imagens restritos.
- Reta tangente a `y = arccos(x)` ou `arcsin(x)` usa a **derivada** (ver tema 08).

### 1.7 Soma infinita com tangente (PG!)
A série `1 + t + t² + …` com `t = tan a·tan b` converge se `|t|<1`, dando `1/(1−tan a tan b)`.
Isso conecta trig com PG infinita (2022 Q9).

---

## 2. Resoluções comentadas (questões reais do ITA)

### 📌 2022 — Q5: Fórmula de `sec(a+b)`
Gabarito: **(d)** `sec a·sec b/(1 − tan a·tan b)`.

**Resolução:** `sec(a+b)=1/cos(a+b)=1/(cos a cos b − sin a sin b)`. Divida numerador e denominador
por `cos a cos b`: numerador `→ 1/(cos a cos b)=sec a sec b`; denominador `→ 1 − tan a tan b`.
**Lição:** para transformar cosseno em sec/tan, **divida por `cos a cos b`**.

### 📌 2022 — Q9: Série `tan(a+b) = (tan a+tan b)·{1 + t + t² + …}`
**Resolução:** o fator entre chaves é PG infinita de razão `t = tan a·tan b`, somando `1/(1−t)`.
Isso reproduz a fórmula de `tan(a+b)` **se** `|tan a·tan b|<1`, o que ocorre quando `a+b<π/2`.
Gabarito: **(b) a+b < π/2**.
**Lição:** reconheça a **PG infinita escondida** e imponha `|razão|<1` para convergir.

### 📌 2022 — Q10: `cos(2θ) + 3sin(θ) − 2 = 0` em `[0,π]`
**Resolução:** `cos2θ = 1−2sin²θ`. Substitua: `1−2sin²θ+3sinθ−2=0 → 2sin²θ−3sinθ+1=0`.
Seja `s=sinθ`: `2s²−3s+1=0 → s=1 ou s=1/2`. Em `[0,π]`: `sinθ=1→θ=π/2` (1 sol);
`sinθ=1/2→θ=π/6 e 5π/6` (2 sol). Total **3 soluções**.
**Lição:** reduza a **uma função** (`sin`), resolva o 2º grau e **conte todas** no intervalo.

### 📌 2025 — Q16 / 2023 — Q11: Reta tangente a curva trigonométrica inversa
**Resolução:** derive (`d/dx arccos x = −1/√(1−x²)`), ache o ponto pedido (`y=π/3`), monte a reta
`y − y₀ = m(x − x₀)`.
**Lição:** reta tangente = **ponto + derivada no ponto** (liga trig inversa com cálculo).

### 📌 2026 — Q9: Potência de cosseno/seno (De Moivre disfarçado)
*"`cos³(π/3) − 3i cos²(π/3)sin(π/3) − 3cos(π/3)sin²(π/3) + i sin³(π/3)`"*
**Resolução:** os coeficientes `1,−3i,−3,i` = expansão de `(cosθ − i·? )`... na verdade é
`(cos θ − i sin θ)³`? Reagrupe como `(cos(π/3) − i sin(π/3))³`? Compare sinais e use **De Moivre**:
`(cosθ + i sinθ)³ = cos3θ + i sin3θ`. Ajuste o sinal → resposta em forma `cos(k) + i sin(k)`.
**Lição:** padrão `a³ ± 3a²bi ...` = **binômio com `i`** → aplique De Moivre.

---

## 3. Exercícios de treino

**E1.** Simplifique `sin(x)·cos(x)` em função de `sin(2x)`.

**E2.** Resolva `2sin²x − sin x − 1 = 0` em `[0, 2π)`.

**E3.** Calcule `cos(75°)` usando soma de arcos (`45°+30°`).

**E4.** Se `tan a = 2` e `tan b = 3`, quanto vale `tan(a+b)`?

**E5.** Prove que `1 + tan²x = sec²x`.

**E6.** Quantas soluções tem `cos(2x) = cos(x)` em `[0, 2π)`?

---

## 4. Gabarito e resoluções

**E1.** `sin x cos x = ½·sin(2x)`.

**E2.** `s=sin x`: `2s²−s−1=0 → (2s+1)(s−1)=0 → s=−1/2 ou s=1`.
`sin x=1→x=π/2`; `sin x=−1/2→x=7π/6, 11π/6`. **Três soluções.**

**E3.** `cos75°=cos(45+30)=cos45cos30−sin45sin30 = (√2/2)(√3/2)−(√2/2)(1/2) = (√6−√2)/4`.

**E4.** `tan(a+b)=(2+3)/(1−2·3)=5/(1−6)=5/(−5)= **−1**`.

**E5.** Divida `sin²x+cos²x=1` por `cos²x`: `tan²x + 1 = sec²x`. ∎

**E6.** `cos2x=2cos²x−1`. Equação: `2cos²x−1=cosx → 2c²−c−1=0 → (2c+1)(c−1)=0 → c=−1/2 ou 1`.
`cosx=1→x=0`; `cosx=−1/2→x=2π/3, 4π/3`. **Três soluções** em `[0,2π)`.
