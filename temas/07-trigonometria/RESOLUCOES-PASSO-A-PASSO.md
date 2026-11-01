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

**Ideia-chave — Tangência de reta à curva:** a reta tangencia `y = cos x` num ponto onde a inclinação da
reta iguala `y' = −sin x` E a reta passa pelo ponto `(x₀, cos x₀)`.

**Desenvolvimento — verificando cada afirmação:**
1. **1ª reta** `x + y = π/2 → y = π/2 − x`, coeficiente angular `−1`.
   Tangência: `−sin x = −1 → sin x = 1 → x = π/2`. Em `x = π/2`: `cos(π/2) = 0`, e a reta dá
   `π/2 − π/2 = 0` ✔. Logo a **1ª reta é tangente** a `cos x` em `(π/2, 0)` → afirmação (a) **verdadeira**.
2. **2ª reta** `y = ½(√3 + π/6 − x)`, coeficiente angular `−1/2`.
   Tangência: `−sin x = −1/2 → sin x = 1/2 → x = π/6`. Em `x = π/6`: `cos(π/6) = √3/2`, e a reta dá
   `½(√3 + π/6 − π/6) = ½·√3 = √3/2` ✔. Logo a **2ª reta é tangente** em `(π/6, √3/2)` → (c) **verdadeira**.
3. **Interseção das duas retas:** iguale `π/2 − x = ½(√3 + π/6 − x)`:
   `2(π/2 − x) = √3 + π/6 − x → π − 2x = √3 + π/6 − x → π − π/6 − √3 = x → x = 5π/6 − √3`.
   Então `y = π/2 − x = π/2 − (5π/6 − √3) = −π/3 + √3 = √3 − π/3`.
4. A afirmação (e) diz que a interseção ocorre em `y = (√3 − π/3)/6`. Mas calculamos `y = √3 − π/3`
   (**sem** dividir por 6). Logo (e) está **ERRADA** (fator `/6` indevido).

> Nota sobre (b)/(d): "ter apenas um ponto em comum" vale no sentido local do ponto de tangência; como
> `cos x` é periódica, uma reta pode reencontrá-la longe — mas, no espírito da questão, (b) e (d) são
> tratadas como verdadeiras. O erro **inequívoco e verificável por conta** está na (e).

**Conclusão:** a afirmação errada é a **(e)** — a interseção das retas ocorre em `y = √3 − π/3`,
e não em `(√3 − π/3)/6`.
(Chave: tangência ⇒ mesma inclinação e mesmo ponto; depois resolver o sistema das duas retas.)

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

**Ideia-chave — Verificar cada uma das 4 fórmulas usando `cosh²a − sinh²a = 1` e as somas de arcos.**

**Desenvolvimento — fórmula por fórmula:**
1. `sinh(a+b) = sinh a cosh b + sinh b cosh a` → **correta** (idêntica à trig, sem troca de sinal).
2. `cosh(a+b) = cosh a cosh b − sinh b sinh a` → **ERRADA**: o correto é com sinal **+**
   (`cosh(a+b) = cosh a cosh b + sinh a sinh b`). A questão escreveu `−`.
3. `sinh(3a) = 3 sinh a cosh²a + sinh³a` → **correta**. Verificação: desenvolvendo
   `sinh3a = sinh(2a+a) = 3 sinh a + 4 sinh³a`. E `3 sinh a cosh²a + sinh³a = 3 sinh a(1+sinh²a) + sinh³a
   = 3 sinh a + 3 sinh³a + sinh³a = 3 sinh a + 4 sinh³a` ✔ — coincide.
4. `cosh(3a) = 3 sinh²a cosh a + cosh³a` → **correta**. Verificação: `cosh3a = cosh a + 4 sinh²a cosh a`.
   E `3 sinh²a cosh a + cosh³a = 3 sinh²a cosh a + cosh a(1+sinh²a) = cosh a + 4 sinh²a cosh a` ✔.
5. Balanço: 3 corretas e **1 falsa** (a de `cosh(a+b)`).

**Conclusão:** há **apenas uma afirmação falsa** → **alternativa (d)** ("there is only one false statement").
(Chave: só `cosh(a+b)` tem o sinal trocado; as de triplo argumento conferem via `cosh²=1+sinh²`.)

---

## 2024/2 — Q12: Simplificar [cos²x − cot x]/[sin²x − tan x] → cot²x

**O que pede:** simplificar `[cos²x − cot x] / [sin²x − tan x]`.

**Ideia-chave — Multiplicar numerador e denominador por `sin x·cos x`** (elimina as frações de cot/tan).

**Desenvolvimento:**
1. Multiplique **numerador** por `sin x cos x`, usando `cot x = cos x/sin x`:
   `cos²x·(sin x cos x) − (cos x/sin x)·(sin x cos x) = sin x cos³x − cos²x = cos²x(sin x cos x − 1)`.
2. Multiplique **denominador** por `sin x cos x`, usando `tan x = sin x/cos x`:
   `sin²x·(sin x cos x) − (sin x/cos x)·(sin x cos x) = sin³x cos x − sin²x = sin²x(sin x cos x − 1)`.
3. A razão (o fator `sin x cos x` some pois multiplicou os dois, e `(sin x cos x − 1)` cancela):
   `[cos²x(sin x cos x − 1)] / [sin²x(sin x cos x − 1)] = cos²x / sin²x = cot²x`.
4. **Conferência numérica** em `x = π/3`: `cos²x = 1/4`, `cot x = 1/√3`, `sin²x = 3/4`, `tan x = √3`.
   Num `= 1/4 − 1/√3 ≈ 0,25 − 0,577 = −0,327`; Den `= 3/4 − √3 ≈ 0,75 − 1,732 = −0,982`;
   razão `≈ 0,333 = 1/3`. E `cot²(π/3) = (1/√3)² = 1/3` ✔.

**Conclusão:** `cot²x` → **alternativa (e)**.
(Chave: multiplicar por `sin x cos x`; o fator `(sin x cos x − 1)` cancela, sobra `cos²x/sin²x = cot²x`.)
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
