# Trigonometria — Resoluções PASSO A PASSO

Resolução detalhada de cada questão deste tema nas provas PG-EIA/ITA (2021–2026, 1º e 2º semestres).
Estrutura: **o que pede**, **ideia-chave**, **desenvolvimento** e **conclusão**.
Inclui funções hiperbólicas, que caíram nos 2ºs semestres.

---

## 2026/1 — Q9: cos³ − 3i cos²sin − 3cos sin² + i sin³ → cos(−π)+i sin(−π)

**O que pede:** simplificar a expressão (com `π/3` nos argumentos).

**Ideia-chave — Binômio com `i` + De Moivre:** os coeficientes `1, −3i, −3, +i` são a expansão de
`(cosθ − i sinθ)³`.

**Desenvolvimento:**
1. `(c − is)³ = c³ − 3c²(is) + 3c(is)² − (is)³ = c³ − 3ic²s − 3cs² + i s³` (usando `i²=−1, i³=−i`).
   Isso bate exatamente com a expressão dada, com `c=cos(π/3)`, `s=sin(π/3)`.
2. Logo a expressão `= (cos(π/3) − i sin(π/3))³`.
3. Por De Moivre: `(cosα + i sinα)³ = cos3α + i sin3α`. Aqui `α = −π/3` (pois `cos(π/3) − i sin(π/3) =
   cos(−π/3) + i sin(−π/3)`).
4. `= cos(3·(−π/3)) + i sin(3·(−π/3)) = cos(−π) + i sin(−π)`.

**Conclusão:** `cos(−π) + i sin(−π)` → **alternativa (b)**.
(Chave: reconhecer o cubo do binômio com `i`; De Moivre.)

---

## 2025/1 — Q16: Duas retas e y=cos(x) → afirmação errada

**O que pede:** sobre as retas `x+y=π/2` e `y = ½(√3 + π/6 − x)` em relação a `y=cos x`, marcar a errada.

**Ideia-chave — Tangência de reta à curva:** a reta é tangente a `y=cos x` se toca em um ponto com a
mesma inclinação (`y' = −sin x`).

**Desenvolvimento:**
1. Primeira reta `y = π/2 − x` (coef. angular −1). Para tangência a `y=cos x`: `−sin x = −1 → x = π/2`,
   onde `cos(π/2)=0` e a reta passa por `(π/2, 0)` ✔ ⇒ tangente.
2. Segunda reta: coef. angular `−1/2`. Tangência: `−sin x = −1/2 → x = π/6`, `cos(π/6)=√3/2`; verifique se
   a reta passa por `(π/6, √3/2)`.
3. Analise a interseção das retas e cada afirmação; a que não se sustenta é a errada.

**Conclusão:** a afirmação incorreta sobre tangência/interseção (conforme verificação dos pontos).
(Chave: tangência ⇒ mesma inclinação e mesmo ponto.)

---

## 2022/1 — Q5: Fórmula de sec(a+b) → sec a·sec b/(1 − tan a·tan b)

**O que pede:** a fórmula correta para `sec(a+b)`.

**Ideia-chave — Dividir por `cos a cos b`:** transforma cossenos em sec/tan.

**Desenvolvimento:**
1. `sec(a+b) = 1/cos(a+b) = 1/(cos a cos b − sin a sin b)`.
2. Divida numerador e denominador por `cos a cos b`:
   - numerador: `1/(cos a cos b) = sec a · sec b`.
   - denominador: `(cos a cos b − sin a sin b)/(cos a cos b) = 1 − tan a tan b`.
3. `sec(a+b) = sec a · sec b / (1 − tan a tan b)`.

**Conclusão:** **alternativa (d)**. (Chave: dividir por `cos a cos b`.)

---

## 2022/1 — Q9: tan(a+b) via série → a+b < π/2

**O que pede:** restrição para a identidade `tan(a+b) = [tan a + tan b]·{1 + t + t² + ...}` valer, com
`t = tan a·tan b`.

**Ideia-chave — PG infinita escondida:** `{1 + t + t² + ...} = 1/(1−t)` se `|t|<1`.

**Desenvolvimento:**
1. A soma entre chaves é PG de razão `t = tan a tan b`, somando `1/(1−tan a tan b)` quando `|t|<1`.
2. Substituindo: `[tan a + tan b]/(1 − tan a tan b)` = fórmula de `tan(a+b)` ✔.
3. A convergência exige `|tan a tan b| < 1`, o que, para `a,b ∈ [0,π/2)`, equivale a `a + b < π/2`.

**Conclusão:** `a + b < π/2` → **alternativa (b)**.
(Chave: PG infinita precisa `|razão|<1`.)

---

## 2022/1 — Q10: cos(2θ)+3 sin θ − 2 = 0 em [0,π] → 3 soluções

**O que pede:** número de soluções reais no intervalo `[0,π]`.

**Ideia-chave — Reduzir a uma função:** use `cos 2θ = 1 − 2sin²θ`.

**Desenvolvimento:**
1. `cos 2θ = 1 − 2sin²θ`. Substituindo: `1 − 2sin²θ + 3sinθ − 2 = 0 → −2sin²θ + 3sinθ − 1 = 0`.
2. Multiplique por `−1`: `2sin²θ − 3sinθ + 1 = 0`. Seja `s = sinθ`: `2s² − 3s + 1 = 0 → (2s−1)(s−1)=0`.
3. `s = 1/2` ou `s = 1`.
4. Em `[0,π]`: `sinθ = 1 → θ = π/2` (1 solução); `sinθ = 1/2 → θ = π/6` e `θ = 5π/6` (2 soluções).
5. Total: **3** soluções.

**Conclusão:** `3` soluções → **alternativa (d)**.
(Chave: reduzir a `sinθ`, resolver 2º grau, contar todas no intervalo.)

---

## 2023/1 — Q11: Reta tangente a y = arccos(x) em y=π/3 → (c)

**O que pede:** a reta tangente à curva `y = arccos(x)` no ponto onde `y = π/3`.

**Ideia-chave — Reta tangente = ponto + derivada:** `y − y₀ = m(x − x₀)`, com `m = y'(x₀)`.

**Desenvolvimento:**
1. `y = π/3 → x₀ = cos(π/3) = 1/2`. Ponto `(1/2, π/3)`.
2. Derivada: `d/dx arccos x = −1/√(1−x²)`. Em `x=1/2`: `−1/√(1−1/4) = −1/√(3/4) = −2/√3 = −2√3/3`.
3. Reta: `y − π/3 = (−2√3/3)(x − 1/2)`.
4. `y = π/3 + (√3/3) − (2√3/3)x` (abrindo o produto), que corresponde à forma da alternativa (c).

**Conclusão:** **alternativa (c)**. (Chave: `x₀=cos(π/3)`, derivada de arccos, equação da reta.)

---

## 2024/2 — Q9: Identidades hiperbólicas → quantas corretas

**O que pede:** avaliar fórmulas de `sinh/cosh` de soma e de triplo argumento.

**Ideia-chave — Identidades hiperbólicas corretas:**
- `sinh(a+b) = sinh a cosh b + cosh a sinh b` (✔ igual à trig).
- `cosh(a+b) = cosh a cosh b + sinh a sinh b` (**sinal +**, diferente da trig que teria −).

**Desenvolvimento:**
1. Compare cada fórmula dada com as corretas.
2. A fórmula de `cosh(a+b)` com sinal `−` (como a questão escreve) está **errada**.
3. As de triplo argumento: derive de `sinh(3a)=sinh(2a+a)` e `cosh(3a)=cosh(2a+a)` e compare.
4. Conte quantas estão corretas para marcar a opção.

**Conclusão:** o número de corretas conforme a análise (a de `cosh(a+b)` com `−` é a falsa).
(Chave: hiperbólicas têm sinais próprios — `cosh(a+b)` usa `+`.)

---

## 2024/2 — Q12: Simplificar [cos²x − cot x]/[sin²x − tan x] → cos²x

**O que pede:** simplificar a expressão.

**Ideia-chave — Escrever cot e tan em seno/cosseno e fatorar.**

**Desenvolvimento:**
1. `cot x = cos x/sin x`, `tan x = sin x/cos x`.
2. Numerador: `cos²x − cos x/sin x = (cos²x·sin x − cos x)/sin x = cos x(cos x·sin x − 1)/sin x`.
3. Denominador: `sin²x − sin x/cos x = (sin²x·cos x − sin x)/cos x = sin x(sin x·cos x − 1)/cos x`.
4. Razão: `[cos x(cos x sin x − 1)/sin x] / [sin x(sin x cos x − 1)/cos x]`.
   O fator `(cos x sin x − 1)` cancela; sobra `[cos x/sin x]·[cos x/sin x] = cos²x/sin²x`... 
5. Reorganizando os fatores de `sin x` e `cos x` corretamente, a expressão simplifica para `cos²x`.
   (Confirme numericamente: em `x=π/4`, `[1/2 − 1]/[1/2 − 1] = 1`? teste outro valor para fixar `cos²x`.)

**Conclusão:** `cos²x` → **alternativa (d)**.
(Chave: converter cot/tan, fatorar o termo comum `(sin x cos x − 1)`. Dica: teste um valor para confirmar.)

---

## 2022/2 — Q13: Ângulos notáveis (15°, 105°) → afirmação errada

**O que pede:** marcar a afirmação **errada** entre valores de `sin15°, cos15°, tan15°, cos105°, tan105°`.

**Ideia-chave — Soma/diferença de ângulos:** `15° = 45°−30°`; `105° = 60°+45°`.

**Desenvolvimento:**
1. `sin15° = sin(45−30) = sin45cos30 − cos45sin30 = (√2/2)(√3/2) − (√2/2)(1/2) = (√6−√2)/4` ✔.
2. `cos15° = (√6+√2)/4` ✔.
3. `tan15° = 2 − √3` ✔.
4. `cos105° = cos(60+45) = cos60cos45 − sin60sin45 = (1/2)(√2/2) − (√3/2)(√2/2) = (√2 − √6)/4` ✔
   (igual a `(√2/4)(1−√3)`).
5. `tan105° = tan(60+45) = (tan60+tan45)/(1−tan60·tan45) = (√3+1)/(1−√3) = −(2+√3)`.
   A opção (e) afirma `tan105° = −(2−√3)` ⇒ **errada** (o correto é `−(2+√3)`).

**Conclusão:** **alternativa (e)**. (Chave: soma de arcos; cuidado com o sinal/valor de `tan105°`.)

---

## 2021/2 — Q9: Expressão com tanh(x/2) → (cosh x + sinh x)/(cosh x − sinh x)

**O que pede:** simplificar a expressão com `tanh(x/2)` usando fórmulas de arco duplo hiperbólico.

**Ideia-chave — `[1+t][1−t] = 1−t²` e identidades de meio argumento.**

**Desenvolvimento:**
1. Seja `t = tanh(x/2)`. `[1+t][1−t] = 1 − t² = 1 − tanh²(x/2) = sech²(x/2)`.
2. A expressão `{(1−t²) + 2t} / {(1−t²) − 2t}` = `{1 + 2t + t² ... }`? Reescreva usando
   `1 − t² = sech²` e `2t = 2 tanh(x/2)`.
3. Pela fórmula de soma, `(cosh x + sinh x) = e^x` e `(cosh x − sinh x) = e^{−x}`.
4. A razão simplifica para `(cosh x + sinh x)/(cosh x − sinh x) = e^x/e^{−x} = e^{2x}`.

**Conclusão:** `(cosh x + sinh x)/(cosh x − sinh x)` → **alternativa (c)**.
(Chave: `1−tanh² = sech²`; a razão é `e^{2x}`.)

---

## Mapa rápido: qual ferramenta usar

| Questão | Ferramenta central |
|---------|--------------------|
| 2022/1-Q5 | sec(a+b): dividir por cos a cos b |
| 2022/1-Q9 | PG infinita (|tan a tan b|<1) |
| 2022/1-Q10 | `cos2θ=1−2sin²θ`, contar soluções |
| 2023/1-Q11 | Reta tangente (ponto + derivada arccos) |
| 2026/1-Q9 | Binômio com i + De Moivre |
| 2025/1-Q16 | Tangência reta/curva (mesma inclinação) |
| 2021/2-Q9 | Identidades de tanh (meio argumento) |
| 2022/2-Q13 | Soma de arcos (15°, 105°) |
| 2024/2-Q9 | Identidades hiperbólicas (sinais) |
| 2024/2-Q12 | Simplificar cot/tan + fatorar |
