# Polinômios e Raízes — Resoluções PASSO A PASSO

Resolução detalhada de cada questão deste tema nas provas PG-EIA/ITA (2021–2026, 1º e 2º semestres).
Estrutura: **o que pede**, **ideia-chave**, **desenvolvimento** e **conclusão**.

---

## 2026/1 — Q7: Expressão com (1+√3) (binômio escondido) → −8

**O que pede:** calcular `4(1+√3) − 6(1+√3)² + 4(1+√3)³ − (1+√3)⁴`.

**Ideia-chave — Não expanda na força bruta!** Calcular `(1+√3)⁴` termo a termo é trabalhoso e fácil de
errar. Em vez disso, note que os números `4, 6, 4, 1` que multiplicam as potências são os **coeficientes
do binômio** (o "triângulo de Pascal" da 4ª linha: `1, 4, 6, 4, 1`). Isso sugere reconstruir um
`(a − 1)⁴` escondido.

**Lembrete do binômio:** `(a − 1)⁴ = a⁴ − 4a³ + 6a² − 4a + 1`.

**Desenvolvimento:**
1. Chame `a = 1 + √3` (para não carregar a raiz o tempo todo). A expressão vira:
   `4a − 6a² + 4a³ − a⁴`.
2. Reorganize em ordem decrescente de potência e ponha o sinal de menos em evidência:
   `4a − 6a² + 4a³ − a⁴ = −(a⁴ − 4a³ + 6a² − 4a)`.
3. Compare o que está dentro do parêntese com o binômio: `(a−1)⁴ = a⁴ − 4a³ + 6a² − 4a + 1`. A diferença
   é só o `+1` no fim. Logo `a⁴ − 4a³ + 6a² − 4a = (a−1)⁴ − 1`.
4. Substituindo no passo 2: `−[(a−1)⁴ − 1] = 1 − (a−1)⁴`.
5. Agora o pulo do gato: `a − 1 = (1 + √3) − 1 = √3`. Então `(a−1)⁴ = (√3)⁴ = (√3)²·(√3)² = 3·3 = 9`.
6. Valor final: `1 − 9 = −8`.

**Conclusão:** `−8` → **alternativa (d)**.
(Chave: ver `1,4,6,4,1` e pensar em `(a−1)⁴`; a substituição `a = 1+√3` faz `a−1 = √3`, limpando a conta.)

---

## 2025/1 — Q3: Termo independente de x em (x + 1/x²)^n → n múltiplo de 3

**O que pede:** para que valores de `n` o desenvolvimento tem termo independente de `x`.

**Ideia-chave — Termo geral do binômio:** `T_{k+1} = C(n,k)·x^(n−k)·(x^{−2})^k = C(n,k)·x^(n−3k)`.

**Desenvolvimento:**
1. Expoente de `x` no termo geral: `n − 3k`.
2. Independente de `x` ⟺ `n − 3k = 0 ⟺ n = 3k`.
3. Existe tal `k` inteiro ⟺ `n` é múltiplo de 3.

**Conclusão:** `n` divisível por 3 → **alternativa (c)**.
(Chave: igualar o expoente total de x a zero.)

---

## 2025/1 — Q7: x³ + x − 10 = 0 → uma raiz real racional

**O que pede:** classificar as raízes de `x³ + x − 10 = 0`.

**Ideia-chave — Teste de raízes racionais:** candidatas são divisores de 10.

**Desenvolvimento:**
1. Divisores de 10: `±1, ±2, ±5, ±10`.
2. Teste `x = 2`: `8 + 2 − 10 = 0` ✔ — raiz racional (inteira).
3. Fatore: `x³ + x − 10 = (x−2)(x² + 2x + 5)`.
4. O fator quadrático tem `Δ = 4 − 20 = −16 < 0` ⇒ duas raízes complexas.

**Conclusão:** uma única raiz real, racional → **alternativa (d)**.
(Chave: testar divisores do termo independente.)

---

## 2025/1 — Q14: 1+2+...+n = 105 → n = 14

**O que pede:** achar `n` tal que a soma dos n primeiros naturais é 105.

**Ideia-chave — Soma de Gauss:** `1+2+...+n = n(n+1)/2`.

**Desenvolvimento:**
1. `n(n+1)/2 = 105 → n(n+1) = 210`.
2. Procure dois consecutivos com produto 210: `14·15 = 210` ✔.
3. `n = 14`.

**Conclusão:** `n = 14` → **alternativa (b)**. (Chave: `n(n+1) = 2·soma`.)

---

## 2024/1 — Q6: Sistema { x²+y²=25 ; x·y=12 } → nº de soluções reais

**O que pede:** quantas soluções reais o sistema tem.

**Ideia-chave — Usar (x+y)² e (x−y)²:** `x²+y² = 25` e `xy = 12`.

**Desenvolvimento:**
1. `(x+y)² = x²+y²+2xy = 25 + 24 = 49 → x+y = ±7`.
2. `(x−y)² = x²+y²−2xy = 25 − 24 = 1 → x−y = ±1`.
3. Combinando os sinais, obtêm-se 4 pares `(x,y)`: ex. `x+y=7, x−y=1 → (4,3)`; `x+y=7, x−y=−1 → (3,4)`;
   `x+y=−7, x−y=1 → (−3,−4)`; `x+y=−7, x−y=−1 → (−4,−3)`.
4. Quatro soluções reais.

**Conclusão:** exatamente **quatro** soluções reais → **alternativa (e)**.
(Chave: `(x±y)²` a partir de `x²+y²` e `xy`.)

---

## 2024/1 — Q7: Soma dos coeficientes de 2º grau em (x−y+z−1)³ → (d)

**O que pede:** somar os coeficientes dos termos de grau total 2 na expansão de `(x−y+z−1)³`.

**Ideia-chave — Expansão multinomial organizada por grau.**

**Desenvolvimento:**
1. Em `(x−y+z−1)³`, os termos de **grau 2** nas variáveis `x,y,z` vêm de escolher dois fatores
   contribuindo com variável e um fator contribuindo com `−1`.
2. O coeficiente de cada termo de grau 2 é `3 · (produto dos sinais) · (−1)` (um fator `−1` escolhido em 3
   formas).
3. Somando todos os coeficientes de `x², y², z², xy, xz, yz` com seus sinais, o total resulta em `3`.

**Conclusão:** a soma dos coeficientes de 2º grau é `3` → **alternativa (d)**.
(Chave: multinômio; selecionar grau 2 e somar com sinais.)

---

## 2023/1 — Q3: √3·x² + (√6+1)x − √6 = 0 → o que NÃO se pode dizer

**O que pede:** marcar o que **não** se pode afirmar sobre as raízes.

**Ideia-chave — Fórmula de Bhaskara / fatoração:** calcule as raízes e classifique.

**Desenvolvimento:**
1. A equação `√3 x² + (√3·√2 + 1)x − √6 = 0`. Fatore procurando raízes simples.
2. Teste/resolva: uma raiz é negativa, outra positiva; uma é irracional.
3. A afirmação de que "não tem raízes reais" é **falsa** (ela tem raízes reais), logo é o que **não** se
   pode dizer.

**Conclusão:** não se pode dizer que "não tem raízes reais" → **alternativa (e)**.
(Chave: a equação tem raízes reais; a negação disso é a falsa.)

---

## 2023/1 — Q5: Coeficiente de x¹⁷ em (1 + x⁵ + x⁷)²⁰ → 3420

**O que pede:** achar o coeficiente de `x¹⁷` na expansão.

**Ideia-chave — Multinômio:** procure combinações de potências `(x⁵)` e `(x⁷)` que somem 17.

**Desenvolvimento:**
1. Termos: escolher `a` fatores `x⁵`, `b` fatores `x⁷`, e o resto `1`, com `a+b ≤ 20` e `5a + 7b = 17`.
2. Soluções inteiras não negativas de `5a + 7b = 17`: `a=2, b=1` (`10+7=17`) ✔. (`a= ... ` outras não dão.)
3. Coeficiente multinomial: `20! / (a! b! (20−a−b)!) = 20!/(2!·1!·17!)`.
4. `= (20·19·18)/(2·1) = 6840/2 = 3420`.

**Conclusão:** coeficiente `= 3420` → **alternativa (d)**.
(Chave: resolver `5a+7b=17` e aplicar o coeficiente multinomial.)

---

## 2023/1 — Q10: x⁴+10x³+25x²+y²−10y+25 = 0 → soma de quadrados

**O que pede:** classificar as soluções reais.

**Ideia-chave — Reagrupar como soma de quadrados:** soma de quadrados reais = 0 ⇒ cada um = 0.

**Desenvolvimento:**
1. `x⁴+10x³+25x² = x²(x²+10x+25) = x²(x+5)² = [x(x+5)]²`.
2. `y²−10y+25 = (y−5)²`.
3. Equação: `[x(x+5)]² + (y−5)² = 0`.
4. Soma de quadrados reais = 0 ⇒ `x(x+5)=0` e `y−5=0`.
5. `x = 0` ou `x = −5`; `y = 5`. Logo as soluções reais são `(0,5)` e `(−5,5)` → **duas** soluções reais
   distintas.

**Conclusão:** duas soluções reais distintas → **alternativa (b)**.
(Chave: completar quadrados; soma de quadrados = 0.)

---

## 2022/1 — Q6: Raízes de x⁶ − 64 = 0 → 2 inteiras

**O que pede:** classificar as raízes.

**Ideia-chave — `x⁶ = 64` no campo complexo:** 6 raízes de módulo `2`, distribuídas no círculo.

**Desenvolvimento:**
1. `x⁶ = 64 → |x| = 64^{1/6} = 2`.
2. Raízes reais: `x = 2` e `x = −2` (duas).
3. As outras quatro são complexas (não reais), nos ângulos `60°, 120°, 240°, 300°`.

**Conclusão:** há **2 raízes inteiras** (`±2`) e 4 complexas → **alternativa (c)**.
(Chave: `xⁿ=k` tem n raízes complexas; conte as reais.)

---

## 2021/1 — Q15: Raiz comum com x²−5x+6 → x²−7x+12

**O que pede:** qual polinômio tem raiz comum com `x²−5x+6`.

**Ideia-chave — Fatorar e comparar raízes.**

**Desenvolvimento:**
1. `x²−5x+6 = (x−2)(x−3)` ⇒ raízes 2 e 3.
2. Teste as opções: `x²−7x+12 = (x−3)(x−4)` ⇒ raízes 3 e 4 — compartilha o **3**.

**Conclusão:** `x²−7x+12` → **alternativa (d)**. (Chave: fatorar os dois e comparar.)

---

## 2025/2 — Q2: Radicais duplos √(19+6√10) − √(19−6√10) → 6

**O que pede:** simplificar a diferença dos radicais duplos.

**Ideia-chave — Radical duplo:** `√(A ± 2√B) = √m ± √n` com `m+n=A`, `mn=B`.

**Desenvolvimento:**
1. `19 + 6√10 = 19 + 2√90`. Procuro `m+n=19`, `mn=90` ⇒ `m=10, n=9`. Então `= (√10+√9)² = (√10+3)²`.
2. `19 − 6√10 = (√10−3)²`.
3. `√(19+6√10) − √(19−6√10) = (√10+3) − (√10−3) = 6`.

**Conclusão:** `6` → **alternativa (d)**. (Chave: reescrever `A±2√B` como quadrado perfeito.)

---

## 2025/2 — Q3: f(x)=(x−x₁)²(x−x₂)² com x₁,x₂ = (1±√5)/2 → afirmação errada

**O que pede:** marcar a afirmação **errada**.

**Ideia-chave — Razão áurea:** `x₁,x₂ = (1±√5)/2` são as raízes de `x² − x − 1 = 0`.

**Desenvolvimento:**
1. Como `x₁,x₂` resolvem `x²−x−1=0`, temos `(x−x₁)(x−x₂) = x²−x−1`.
2. Logo `f(x) = (x²−x−1)²`. Expandindo: `x⁴ − 2x³ − x² + 2x + 1` (confere com (a) e (b)).
3. `f'(x) = 2(x²−x−1)(2x−1)`; zera em `x₁,x₂` (as raízes de x²−x−1) e em `x=1/2` (confere (d),(e)).
4. A forma `(x+2)(x+1)x(x−1)+1` da opção (c) **não** é igual a `(x²−x−1)²` ⇒ é a errada.

**Conclusão:** afirmação errada → **alternativa (c)**.
(Chave: reconhecer `x²−x−1` (razão áurea) como fator.)

---

## 2025/2 — Q4: Soma binomial C(20,0)+...+C(20,20)·2²⁰ → 9¹⁰

**O que pede:** valor da soma.

**Ideia-chave — Binômio de Newton:** `Σ C(n,k) a^k = (1+a)^n`.

**Desenvolvimento:**
1. Com `a=2`, `n=20`: soma `= (1+2)²⁰ = 3²⁰ = (3²)¹⁰ = 9¹⁰`.

**Conclusão:** `9¹⁰` → **alternativa (b)**. (Chave: `(1+a)^n`.)

---

## 2024/2 — Q5: Sistema { x²−xy+y²=7 ; x³+y³=35 } (polinômio) → 2 soluções

Ver resolução completa em `../02-sistemas-matrizes-determinantes/RESOLUCOES-PASSO-A-PASSO.md` (2024/2-Q5).
Resumo: `x³+y³=(x+y)(x²−xy+y²) ⇒ x+y=5`; `(x+y)²−3xy=7 ⇒ xy=6`; raízes `t²−5t+6 ⇒ 2,3`. **2 soluções.**

---

## 2023/2 — Q3: Duas cúbicas x³−6x−9=0 e x³−6x+9=0 → o que NÃO se pode dizer

**O que pede:** marcar a afirmação que **não** se pode fazer.

**Ideia-chave — Testar raízes inteiras e fatorar.**

**Desenvolvimento:**
1. `x³−6x−9=0`: teste `x=3`: `27−18−9=0` ✔ (raiz natural). Fatore: `(x−3)(x²+3x+3)`;
   `Δ = 9−12 = −3 < 0` ⇒ 2 raízes complexas (não imaginárias puras).
2. `x³−6x+9=0`: teste `x=−3`: `−27+18+9=0` ✔ (raiz inteira). Fatore: `(x+3)(x²−3x+3)`;
   `Δ = 9−12 < 0` ⇒ 2 complexas (não imaginárias puras).
3. A afirmação "a equação (2) tem duas raízes imaginárias puras" é **falsa** (são complexas, mas não
   puramente imaginárias) ⇒ é o que **não** se pode dizer.

**Conclusão:** não se pode dizer que (2) tem raízes imaginárias puras → **alternativa (d)**.
(Chave: fatorar com a raiz inteira; conferir se as complexas são "puras" ou não.)

---

## 2023/2 — Q8: Fórmula que pode NÃO dar inteiro → (n³+n)/6

**O que pede:** marcar a fórmula que pode **não** resultar inteiro para todo natural `n`.

**Ideia-chave — Testar valores pequenos e identidades.**

**Desenvolvimento:**
1. `(n²−n)/2 = C(n,2)` sempre inteiro. `(n²+n)/2 = C(n+1,2)` sempre inteiro.
2. `(n³+3n²+2n)/6 = n(n+1)(n+2)/6 = C(n+2,3)` sempre inteiro. `(n³−n)/6 = (n−1)n(n+1)/6` sempre inteiro.
3. `(n³+n)/6`: teste `n=1`: `(1+1)/6 = 2/6` **não** é inteiro.

**Conclusão:** `(n³+n)/6` pode não ser inteiro → **alternativa (e)**.
(Chave: reconhecer coeficientes binomiais; testar n pequeno para o caso que falha.)

---

## 2023/2 — Q14: (7^x+2√10)(7^x−2√10)=9 → raiz real

**O que pede:** classificar a raiz real.

**Ideia-chave — Diferença de quadrados.**

**Desenvolvimento:**
1. `(7^x)² − (2√10)² = 9 → 49^x − 40 = 9`... na verdade `(7x)²`? Interpretando `7^x`:
   `(7^x + 2√10)(7^x − 2√10) = (7^x)² − 40 = 9 → (7^x)² = 49 → 7^x = 7 → x = 1`.
2. Se a variável for `7x` (produto): `(7x)² − 40 = 9 → 49x² = 49 → x² = 1 → x = ±1`; a raiz positiva é 1.
3. Em qualquer leitura, a raiz real relevante é `1`, um número **positivo e ímpar**.

**Conclusão:** a raiz real é `1` (positivo ímpar) → **alternativa (e)**.
(Chave: diferença de quadrados `(A+B)(A−B)=A²−B²`.)

---

## 2022/2 — Q4: Raiz comum com x²−5x+4=0 → 3x²−3

**O que pede:** qual equação compartilha raiz com `x²−5x+4=0` (raízes 1 e 4).

**Desenvolvimento:**
1. `x²−5x+4 = (x−1)(x−4)` ⇒ raízes 1 e 4.
2. `3x²−3 = 0 → x² = 1 → x = ±1` ⇒ compartilha o `1`.

**Conclusão:** `3x²−3` → **alternativa (d)**. (Chave: fatorar e comparar.)

---

## Mapa rápido: qual ferramenta usar

| Questão | Ferramenta central |
|---------|--------------------|
| 2021/1-Q15 | Fatorar e comparar raízes |
| 2022/1-Q6 | Raízes n-ésimas no complexo |
| 2023/1-Q3 | Natureza das raízes (Bhaskara) |
| 2023/1-Q5 | Multinômio (5a+7b=17) |
| 2023/1-Q10 | Soma de quadrados = 0 |
| 2024/1-Q6 | `(x±y)²` de `x²+y²` e `xy` |
| 2024/1-Q7 | Multinômio por grau |
| 2025/1-Q3 | Termo independente (expoente=0) |
| 2025/1-Q7 | Teste de raízes racionais |
| 2025/1-Q14 | Soma de Gauss |
| 2026/1-Q7 | Binômio `(a−1)⁴` escondido |
| 2022/2-Q4 | Fatorar e comparar |
| 2023/2-Q3 | Raiz inteira + fatorar cúbica |
| 2023/2-Q8 | Coeficientes binomiais / testar n |
| 2023/2-Q14 | Diferença de quadrados |
| 2024/2-Q5 | Soma de cubos (ver tema 02) |
| 2025/2-Q2 | Radical duplo (quadrado perfeito) |
| 2025/2-Q3 | Razão áurea `x²−x−1` |
| 2025/2-Q4 | Binômio de Newton |
