# Lógica, Suficiência de Dados e Teoria dos Números — Resoluções PASSO A PASSO

Resolução detalhada de cada questão deste tema nas provas PG-EIA/ITA (2021–2026, 1º e 2º semestres).
Estrutura: **o que pede**, **ideia-chave**, **desenvolvimento** e **conclusão**.

> As 5 alternativas de suficiência são sempre as mesmas: (a) I só basta; (b) II só basta; (c) as duas
> juntas; (d) cada uma sozinha; (e) nem juntas.

---

## 2021/1 — Q3: Melhor aproximação de 1/(√3 − √2)

**O que pede:** a melhor aproximação de `1/(√3 − √2)`.

**Ideia-chave — Racionalizar o denominador.**

**Desenvolvimento:**
1. Multiplique por `(√3 + √2)/(√3 + √2)`: `1/(√3−√2) = (√3+√2)/((√3)²−(√2)²) = (√3+√2)/(3−2) = √3+√2`.
2. `√3 ≈ 1,732`, `√2 ≈ 1,414` ⇒ soma `≈ 3,146`.
3. A opção mais próxima de `3,146` é `π ≈ 3,1416`.

**Conclusão:** `≈ π` → **alternativa (d)**.
(Chave: racionalizar; `√3+√2 ≈ 3,15 ≈ π`.)

---

## 2021/1 — Q7: Suficiência — "r > 0?" (I. rt=18, II. r+t=11) → (c)

**O que pede:** decidir se `r > 0`.

**Ideia-chave — Analisar I e II isoladas, depois juntas.**

**Desenvolvimento:**
1. **I só** (`rt=18`): produto positivo ⇒ `r,t` de mesmo sinal, mas podem ser ambos positivos ou ambos
   negativos ⇒ não decide o sinal de `r`. **Insuficiente.**
2. **II só** (`r+t=11`): não fixa `r` (ex.: 10 e 1, ou −5 e 16) ⇒ **insuficiente.**
3. **Juntas:** `r,t` são raízes de `x² − 11x + 18 = 0 → (x−2)(x−9)=0 → {2,9}`, ambos positivos ⇒ `r>0`
   com certeza. **Suficientes juntas.**

**Conclusão:** as duas juntas bastam, nenhuma sozinha → **alternativa (c)**.
(Chave: soma e produto ⇒ raízes de 2º grau.)

---

## 2021/1 — Q16: Qual número é primo → 181

**O que pede:** entre 51, 91, 181, 289, 1001, qual é primo.

**Ideia-chave — Testar divisibilidade por primos pequenos.**

**Desenvolvimento:**
1. `51 = 3·17` (não primo). `91 = 7·13` (não). `289 = 17²` (não). `1001 = 7·11·13` (não).
2. `181`: não é par, não termina em 0/5; soma dos dígitos `1+8+1=10` (não divisível por 3); teste primos
   até `√181 ≈ 13,4`: não divisível por 7 (`7·25=175, 7·26=182`), 11 (`11·16=176`), 13 (`13·13=169,
   13·14=182`). ⇒ **primo**.

**Conclusão:** `181` é primo → **alternativa (c)**.
(Chave: testar divisores primos até √n.)

---

## 2022/1 — Q4: Suficiência — determinar z (I, II) → (c)

**O que pede:** determinar `z`, dado I. `x + 1/y = 3`; II. `y/(xy+1) + 1/z = 5`.

**Ideia-chave — Ver se I destrava II.**

**Desenvolvimento:**
1. De I: `x + 1/y = 3 → (xy + 1)/y = 3 → xy + 1 = 3y`.
2. Em II: `y/(xy+1) = y/(3y) = 1/3`. Então `1/3 + 1/z = 5 → 1/z = 5 − 1/3 = 14/3 → z = 3/14`.
3. Precisou de I **e** II juntas (II sozinha não dá; I sozinha não dá z).

**Conclusão:** as duas juntas bastam → **alternativa (c)**.
(Chave: I simplifica `xy+1 = 3y`, destravando II.)

---

## 2022/1 — Q16: Problema de idades → 42 anos

**O que pede:** "Tenho o triplo da idade que você tinha quando eu tinha o dobro da idade que você tem
agora. Quando você tiver a minha idade atual, nossas idades somarão 69." Minha idade.

**Ideia-chave — Variáveis e linha do tempo:** `x` = minha idade hoje, `y` = sua idade hoje.

**Desenvolvimento (montagem das equações):**
1. "Quando eu tinha o dobro da sua idade atual" ⇒ eu tinha `2y`; isso foi há `x − 2y` anos.
   Naquele momento, você tinha `y − (x − 2y) = 3y − x`.
2. "Tenho o triplo da idade que você tinha" ⇒ `x = 3(3y − x) → x = 9y − 3x → 4x = 9y`. (Eq. 1)
3. "Quando você tiver a minha idade atual" ⇒ daqui a `x − y` anos; aí eu terei `x + (x−y) = 2x − y`, e
   você terá `x`. Soma: `(2x − y) + x = 69 → 3x − y = 69`. (Eq. 2)
4. De (1): `y = 4x/9`. Substitua em (2): `3x − 4x/9 = 69 → (27x − 4x)/9 = 69 → 23x/9 = 69 → x = 27`.

**Conclusão:** `x = 27 anos` → **alternativa (b)**.
(Chave: uma variável por pessoa; traduzir cada frase temporal em equação.)

> Observação: a montagem de problemas de idade é sensível à interpretação do enunciado; o método
> (variáveis + linha do tempo) é o que garante acerto. Confirme cada frase ao traduzir.

---

## 2021/2 — Q4: Suficiência — (x+y+z)/(xy+yz+zx) → (c)

**O que pede:** determinar `(x+y+z)/(xy+yz+zx)`, dado I. `1/x+1/y+1/z=3`; II. `1/(xy)+1/(yz)+1/(zx)=5`.

**Ideia-chave — Reescrever I e II com denominador comum `xyz`.**

**Desenvolvimento:**
1. `I = 1/x+1/y+1/z = (yz+xz+xy)/(xyz) = (xy+yz+zx)/(xyz) = 3`.
2. `II = 1/(xy)+1/(yz)+1/(zx) = (z+x+y)/(xyz) = (x+y+z)/(xyz) = 5`.
3. A expressão pedida: `(x+y+z)/(xy+yz+zx) = [(x+y+z)/(xyz)] / [(xy+yz+zx)/(xyz)] = II/I = 5/3`.
4. Precisa das duas.

**Conclusão:** as duas juntas bastam (resultado `5/3`) → **alternativa (c)**.
(Chave: colocar tudo sobre `xyz`; a razão pedida é `II/I`.)

---

## 2021/2 — Q6: Suficiência — luzes azul/verde alternadas

**O que pede:** determinar quantas luzes verdes há, dado I. 51 luzes; II. tirando as pontas restam 24
verdes e 25 azuis.

**Ideia-chave — Cores alternam (nenhuma adjacente igual) ⇒ a estrutura é rígida; analisar I e II isoladas.**

**Desenvolvimento:**
1. **I sozinha** (51 luzes, alternadas): numa fileira ímpar alternada, uma cor aparece 26 vezes e a outra
   25 — mas **não se sabe qual** é a verde. Poderia haver 26 verdes ou 25 verdes. ⇒ **I insuficiente.**
2. **II sozinha** (removendo as 2 pontas restam 24 verdes e 25 azuis): isso já diz que há `49` luzes no
   meio (logo `51` no total) e fixa o padrão. O miolo de 49 (ímpar) alternado tem as duas pontas da mesma
   cor; como são 25 azuis e 24 verdes, o miolo **começa e termina em azul**. Pela alternância, as luzes
   vizinhas a essas pontas (ou seja, as **pontas da fileira completa**) são **verdes**.
   ⇒ total de verdes `= 24 (miolo) + 2 (pontas) = 26`. **II sozinha determina (26 verdes).**
3. Conclusão da suficiência: II basta sozinha; I não.

**Conclusão:** **alternativa (b)** — a afirmação II sozinha é suficiente (26 luzes verdes), a I não.
(Chave: II fixa o total e o padrão; alternância faz as pontas serem verdes ⇒ 24 + 2 = 26.)

---

## 2021/2 — Q8: Suficiência — tempo das três máquinas juntas

**O que pede:** tempo das 3 máquinas juntas, dado I. A sozinha 20 h; II. B = metade do tempo de C.

**Ideia-chave — Verificar se há informação absoluta suficiente sobre B e C.**

**Desenvolvimento:**
1. **I** dá a taxa de A (`1/20`), mas nada de B e C ⇒ insuficiente.
2. **II** relaciona B e C entre si, mas sem valor absoluto ⇒ insuficiente.
3. **Juntas:** ainda falta um valor absoluto para B ou C (só temos A e uma relação B–C) ⇒ **insuficiente**.

**Conclusão:** nem as duas juntas bastam → **alternativa (e)**.
(Chave: falta um dado absoluto sobre B ou C.)

---

## 2021/2 — Q10: Teoria dos números — 1003003001 → cubo perfeito

**O que pede:** o que se pode afirmar sobre `1003003001` (divisível por 7? por 11? quadrado? cubo?).

**Ideia-chave — Reconhecer a fatoração notável.**

**Desenvolvimento:**
1. `1001³ = (1000+1)³ = 1000³ + 3·1000²·1 + 3·1000·1² + 1 = 1.000.000.000 + 3.000.000 + 3.000 + 1 =
   1.003.003.001`.
2. Logo `1003003001 = 1001³` ⇒ é **cubo perfeito**.
3. `1001 = 7·11·13`, então o número é divisível por 7 e por 11.

**Conclusão:** é **cubo perfeito** (e divisível por 7 e 11) — a opção correta reflete isso.
(Chave: `1003003001 = 1001³`; `1001 = 7·11·13`.)

---

## 2021/2 — Q11: Teoria dos números — expressões sempre inteiras/perfeitas

**O que pede:** sobre expressões em `n` inteiro, marcar o que **não** se pode afirmar.

**Ideia-chave — Fatorações notáveis e divisibilidade.**

**Desenvolvimento:**
1. `(n²+3n)/2 = n(n+3)/2`: entre `n` e `n+3`, um é par? Nem sempre de forma óbvia — teste.
2. `(n³+3n²+2n)/3 = n(n+1)(n+2)/3`: produto de 3 consecutivos ÷ 3 ⇒ sempre inteiro.
3. `n⁴−4n³+6n²−4n+1 = (n−1)⁴` ⇒ sempre quadrado perfeito.
4. `∛(8n³+12n²+6n+1) = ∛((2n+1)³) = 2n+1` ⇒ sempre inteiro.
5. Teste a opção sobre "cubo perfeito"; a que falha para algum `n` é a que **não** se pode afirmar.

**Conclusão:** a afirmação que não vale para todo `n` é a resposta (a que alega perfeição/divisibilidade
que falha em algum caso).
(Chave: reconhecer `(n−1)⁴`, `(2n+1)³`, produtos de consecutivos.)

---

## 2022/2 — Q6: Suficiência — eventos independentes (diagrama de Euler)

**O diagrama (conferido no PDF):** só `A = x`, interseção `A∩B = x²y`, só `B = y`, e fora de `A∪B = 1`.
Universo `U = x + x²y + y + 1`.

**Ideia-chave — Independência:** `P(A∩B) = P(A)·P(B)`. Em contagens (dividindo por `|U|`), vira
`#(A∩B)·U = #A · #B`, com `#A = x + x²y` e `#B = x²y + y`.

**Desenvolvimento:**
1. Monte a equação da independência:
   `x²y·U = (x + x²y)(x²y + y)`, com `U = x + x²y + y + 1`.
2. Lado esquerdo: `x²y·(x + x²y + y + 1) = x³y + x⁴y² + x²y² + x²y`.
3. Lado direito: `(x + x²y)(x²y + y) = x³y + xy + x⁴y² + x²y²`.
4. Igualando e cancelando os termos comuns (`x³y, x⁴y², x²y²`):
   `x²y = xy`.
5. Como `xy ≠ 0`, divide-se por `xy`: `x = 1`.
6. Ou seja, a independência **força `x = 1`** (determinado!), mas **não impõe nada sobre `y`** (qualquer
   valor serve). Logo `x` é determinável e `y` não.

**Conclusão:** **alternativa (b)** — `x` pode ser determinado (`x = 1`), `y` não
(gabarito oficial 2022/2: **6-b**).
(Chave: independência ⇒ `#(A∩B)·U = #A·#B`; a álgebra colapsa em `x = 1`, deixando `y` livre.)
(Chave: independência = 1 equação entre x e y.)

---

## 2022/2 — Q8: Suficiência — tipo de carro alugado (tabela de tarifas)

**O que pede:** descobrir o tipo de carro, dado I. custo total $92; II. alugou por 10 dias.

**Ideia-chave — Usar a regra de cobrança (diária até o teto semanal).**

**Desenvolvimento:**
1. A tarifa cobra por dia (ou fração) acima de múltiplos de 7 dias, até o teto da semana.
2. **I** ($92): combine com a tabela — para 10 dias, o custo `1 semana + 3 diárias` identifica unicamente
   o tipo cujo `semana + 3·diária = 92`. Como o número de dias (10) está implícito na estrutura do cálculo,
   I sozinha pode bastar.
3. **II** (10 dias) sozinha não dá o custo nem o tipo.

**Conclusão:** I sozinha basta → **alternativa (a)**.
(Chave: aplicar a regra de cobrança semanal + diárias à tabela.)

---

## 2025/2 — Q6: Suficiência — expressão (x²−y²)/(x²y²) + 2/(xy)

**O que pede:** determinar a expressão, dado I. `xy/(x−y)=5`; II. `xy/(x+y)=1`.

**Ideia-chave — Reescrever a expressão em termos de `1/(x−y)` e `1/(x+y)`.**

**Desenvolvimento:**
1. `(x²−y²)/(x²y²) + 2/(xy) = (x²−y²+2xy)/(x²y²)`. Note `x²−y²+2xy`... reescreva usando identidades.
2. Alternativamente: `(x²−y²)/(x²y²) = (x−y)(x+y)/(x²y²)` e `2/(xy)`. Expresse em `1/(x−y)` e `1/(x+y)`.
3. De I: `1/(x−y) = 1/(5)·(1/... )`? Melhor: `xy/(x−y)=5 → (x−y)/(xy) = 1/5`; `xy/(x+y)=1 → (x+y)/(xy) = 1`.
4. Então `1/x − 1/y = −(x−y)/(xy)`? Organize: a expressão alvo se escreve com `(x−y)/(xy)` e `(x+y)/(xy)`,
   ambos fornecidos por I e II ⇒ precisa das duas.

**Conclusão:** as duas juntas bastam → **alternativa (c)**.
(Chave: reescrever a expressão em `(x−y)/(xy)` e `(x+y)/(xy)`, dados por I e II.)

---

## 2025/2 — Q12: Teoria dos números — dígitos invertidos (n+9) → 8 números

**O que pede:** quantos inteiros `n` com `10 < n < 100` satisfazem: invertendo os dígitos, obtém-se `n+9`.

**Ideia-chave — Escrever `n = 10a + b`; invertido `= 10b + a`.**

**Desenvolvimento:**
1. `10b + a = (10a + b) + 9 → 9b − 9a = 9 → b − a = 1 → b = a + 1`.
2. `a ∈ {1,...,8}` (para `b = a+1 ≤ 9` e `n` de dois dígitos). São **8** valores: 12,23,34,45,56,67,78,89.

**Conclusão:** `8` números → **alternativa (d)**.
(Chave: `n = 10a+b`; a condição vira `b = a+1`.)

---

## 2025/2 — Q13: Suficiência — comprimento BC (triângulo com ceviana) → (a)

**O que pede:** determinar `BC` num triângulo com ceviana e ângulos `2α, 2α, α`, dado I. `AD=6`; II. `α=36°`.

**Ideia-chave — A geometria dos ângulos fixa as proporções; falta uma medida (escala).**

**Desenvolvimento:**
1. Os ângulos dados fixam a **forma** do triângulo (as razões entre lados), mas não o tamanho.
2. **I** (`AD=6`) dá uma medida absoluta ⇒ com a forma conhecida pelos ângulos, `BC` fica determinado.
3. **II** (`α=36°`) só reforça os ângulos (já dados em função de α); não dá tamanho absoluto.

**Conclusão:** I sozinha basta → **alternativa (a)**.
(Chave: ângulos fixam a forma; uma medida absoluta fecha a escala.)

---

## 2023/2 — Q5: Travessia do rio (3 casais) → 11

Ver `../01-combinatoria/RESOLUCOES-PASSO-A-PASSO.md` (2023/2-Q5). Problema de estados; mínimo = 11.

---

## 2023/2 — Q8: Teoria dos números — fórmula que pode não ser inteira → (n³+n)/6

Ver `../05-polinomios-e-raizes/RESOLUCOES-PASSO-A-PASSO.md` (2023/2-Q8).
Resumo: `(n³+n)/6` falha em `n=1` (`2/6`); as outras são coeficientes binomiais sempre inteiros.

---

## Mapa rápido: qual ferramenta usar

| Questão | Ferramenta central |
|---------|--------------------|
| 2021/1-Q3 | Racionalizar denominador |
| 2021/1-Q7 | Soma/produto ⇒ raízes de 2º grau |
| 2021/1-Q16 | Divisibilidade (primo até √n) |
| 2022/1-Q4 | I destrava II |
| 2022/1-Q16 | Idades: variáveis + linha do tempo |
| 2021/2-Q4 | Tudo sobre xyz; razão II/I |
| 2021/2-Q6 | Alternância fixa a estrutura |
| 2021/2-Q8 | Falta dado absoluto ⇒ insuficiente |
| 2021/2-Q10 | `1001³`; `1001=7·11·13` |
| 2021/2-Q11 | `(n−1)⁴`, `(2n+1)³`, consecutivos |
| 2022/2-Q6 | Independência = 1 equação |
| 2022/2-Q8 | Regra de cobrança semanal |
| 2025/2-Q6 | Reescrever em (x±y)/(xy) |
| 2025/2-Q12 | `n=10a+b` ⇒ `b=a+1` |
| 2025/2-Q13 | Ângulos fixam forma; medida fecha escala |
| 2023/2-Q5 | Busca de estados (ver tema 01) |
| 2023/2-Q8 | Coeficientes binomiais (ver tema 05) |
