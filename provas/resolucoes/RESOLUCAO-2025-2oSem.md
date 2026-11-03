# Resolução comentada — Matemática · 2025 / 2º semestre (PG-EIA · ITA)

**Prova:** [`../Prova_PG-EIA_2025-2oSem.pdf`](../Prova_PG-EIA_2025-2oSem.pdf) — aplicada em **19 de maio de 2025**.
**Formato:** 16 questões de múltipla escolha (a–e), enunciados em inglês, **90 minutos**, sem calculadora.
**Gabarito oficial:** `1-d 2-d 3-c 4-b 5-c 6-c 7-b 8-c 9-c 10-d 11-a 12-d 13-a 14-c 15-a 16-e`.

> **O que este arquivo entrega.** As **16 questões resolvidas passo a passo**, com: o diagnóstico de cada
> problema, a conta completa, a razão de a alternativa correta ser correta, **por que as outras caem**,
> as armadilhas de leitura e o "padrão" que a banca repetiu. As 16 respostas foram obtidas de forma
> independente e **conferidas numericamente** — batem **16/16** com o gabarito oficial.

> **Sobre o nome.** É a prova de Matemática do processo seletivo do PG-EIA/ITA, de múltipla escolha no
> estilo GMAT — a "prova de GMATE" do 2º semestre de 2025. No repositório, o PDF é o
> `Prova_PG-EIA_2025-2oSem.pdf`.

---

## 1. Gabarito relâmpago

| Questão | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 | 13 | 14 | 15 | 16 |
|:-------:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| **Resposta** | **d** | **d** | **c** | **b** | **c** | **c** | **b** | **c** | **c** | **d** | **a** | **d** | **a** | **c** | **a** | **e** |

---

## 2. Raio-X da prova

| # | Assunto | Resp. | Nível | Tempo-alvo |
|:-:|---------|:-----:|:-----:|:----------:|
| 1 | Limite 0/0 com duas raízes → racionalizar | d | médio | 2 min |
| 2 | Radical duplo → quadrado perfeito | d | fácil | 1,5 min |
| 3 | Polinômio, derivada e **afirmação falsa** | c | médio | 3 min |
| 4 | Soma binomial → (1+a)ⁿ | b | fácil | 1 min |
| 5 | Diagonais espaciais do dodecaedro | c | médio | 2,5 min |
| 6 | Suficiência de dados (sistema algébrico) | c | médio | 3 min |
| 7 | Equação logarítmica com mudança de base | b | difícil | 5 min |
| 8 | Complexos: onde está a barra do conjugado | c | fácil | 1,5 min |
| 9 | Taxa de trabalho (peça/pessoa·hora) | c | fácil | 2 min |
| 10 | Determinante de matriz triangular | d | fácil | 1 min |
| 11 | Volume de prisma a partir da planificação | a | difícil | 6 min |
| 12 | Inversão de dígitos (equação diofantina) | d | fácil | 1,5 min |
| 13 | Suficiência de dados (isósceles escondidos) | a | médio/difícil | 4 min |
| 14 | Porcentagens encadeadas | c | fácil | 1 min |
| 15 | Isolar variável em equação literal | a | fácil | 1,5 min |
| 16 | Probabilidade / desarranjo D₄ | e | médio | 2 min |

**Leitura estratégica.** Oito questões (2, 4, 9, 10, 12, 14, 15, 16) saem em **menos de 2 minutos** cada e
já valem 8 acertos — o corte de 50%. As quatro "longas" (7, 11, 13 e, em menor grau, 5) é que decidem a
nota alta. Somando os tempos-alvo: **~38,5 min de prova "limpa"**, sobrando mais de 50 min para conferência.

---

## 3. Resoluções

### Q1 · Limite 0/0 com duas raízes — **(d) 9/8**

**Enunciado.** `lim_{x→2} ( √(3x−2) − 2 ) / ( √(4x+1) − 3 )`
(a) 1/2 · (b) 2/3 · (c) 3/4 · (d) 9/8 · (e) 4/3

**Diagnóstico.** Em x = 2: numerador √4 − 2 = 0 e denominador √9 − 3 = 0 → indeterminação `0/0`.
As duas raízes escondem um fator `(x−2)`; o trabalho é **extrair e cancelar** esse fator.

**Passo 1 — racionalizar cada raiz separadamente.**

```
(√(3x−2) − 2)·(√(3x−2) + 2) = (3x−2) − 2² = 3x − 6 = 3(x−2)
(√(4x+1) − 3)·(√(4x+1) + 3) = (4x+1) − 3² = 4x − 8 = 4(x−2)
```

**Passo 2 — montar a fração (multiplicando numerador e denominador pelos conjugados).**

```
 √(3x−2) − 2      [3(x−2)] / [√(3x−2) + 2]      3    √(4x+1) + 3
──────────────  =  ─────────────────────────  =  ─── · ─────────────
 √(4x+1) − 3      [4(x−2)] / [√(4x+1) + 3]      4    √(3x−2) + 2
```

**Passo 3 — cancelar `(x−2)`** (válido para x ≠ 2, que é o que o limite permite) e **avaliar em x = 2**:

```
(3/4) · (√9 + 3)/(√4 + 2) = (3/4) · (6/4) = 18/16 = 9/8
```

**Resposta: (d) 9/8.**

**Atalho (L'Hôpital).** Derivando em cima e embaixo:
`f'(x) = 3/(2√(3x−2))` → `f'(2) = 3/4`; `g'(x) = 4/(2√(4x+1))` → `g'(2) = 4/6 = 2/3`.
Razão: `(3/4)/(2/3) = 9/8`. ✔ (Mesmo resultado — e, como sempre, racionalizar é menos arriscado.)

**Por que as outras caem.**
- (c) 3/4 = só a razão dos coeficientes 3 e 4, quem racionaliza pela metade e para no meio do caminho.
- (b) 2/3 = a derivada do denominador isolada.
- (e) 4/3 = o inverso da razão dos coeficientes.
- (a) 1/2 = chute.

**Padrão.** Duas raízes gerando `0/0` → racionalize **as duas** e cancele o fator comum. É o formato que a
banca usa quando quer limite "sem calculadora": sempre sobra um fator comum depois da racionalização.

---

### Q2 · Radical duplo — **(d) 6**

**Enunciado.** `√(19 + 6√10) − √(19 − 6√10)`
(a) 3 · (b) 4 · (c) 5 · (d) 6 · (e) 2√10

**Ideia.** Todo radical duplo `√(A ± B√C)` costuma ser o quadrado de `m ± n√C`, pois
`(m + n√C)² = (m² + n²C) + 2mn√C`. Precisamos então de:

```
m² + 10n² = 19        e        2mn = 6  →  mn = 3
```

**Achar m e n.** `mn = 3` com inteiros → (1, 3) ou (3, 1). Testando `m = 3, n = 1`:
`m² + 10n² = 9 + 10 = 19` ✔. Logo:

```
19 + 6√10 = (3 + √10)²        e        19 − 6√10 = (3 − √10)²
```

**Cuidado com o módulo.** `√(X²) = |X|`, e `3 − √10 < 0` (pois √10 ≈ 3,162). Então:

```
√(19 + 6√10) = 3 + √10
√(19 − 6√10) = |3 − √10| = √10 − 3
```

**Conta final.**

```
(3 + √10) − (√10 − 3) = 3 + √10 − √10 + 3 = 6
```

**Resposta: (d) 6.**

**Armadilha.** Quem escreve `√(19−6√10) = 3 − √10` (esquecendo o módulo) obtém `2√10 ≈ 6,32` — exatamente
a alternativa (e). Note que as duas raízes são **quase iguais** (3 + 3,162 e 3,162 − 3), então a diferença é
pequena e "redonda": se sua conta deu ≈ 6,3, o erro é de sinal.

**Verificação.** `(3+√10)² = 9 + 10 + 6√10 = 19 + 6√10` ✔ e `(√10−3)² = 10 + 9 − 6√10 = 19 − 6√10` ✔.

**Padrão.** Resolver `{m² + n²C = A; 2mn = B}` com inteiros pequenos. Quando A e B são "bonitos", a
solução é sempre por tentativa guiada — não perca tempo com fórmula geral.

---

### Q3 · Polinômio e derivada: qual afirmação é FALSA — **(c)**

**Enunciado.** `f(x) = (x − x₁)²(x − x₂)²`, com `x₁ = (1+√5)/2` e `x₂ = (1−√5)/2`.
Marque a afirmação **errada**:
(a) `f(x) = x⁴ − 2x³ − x² + 2x + 1` · (b) `f(x) = (x² − x − 1)²` ·
(c) `f(x) = (x+2)(x+1)x(x−1) + 1` · (d) x₁ e x₂ são raízes de `f'` · (e) `x = 1/2` é raiz de `f'`

**Passo 1 — reconhecer x₁ e x₂.** Soma e produto:

```
x₁ + x₂ = 1        x₁·x₂ = (1 − 5)/4 = −1
```

Logo x₁ e x₂ são as raízes de `x² − x − 1 = 0`, isto é, `x² − x − 1 = (x − x₁)(x − x₂)`. (É o número de
ouro e seu conjugado.)

**Passo 2 — reescrever f.**

```
f(x) = [(x − x₁)(x − x₂)]² = (x² − x − 1)²          →  (b) VERDADEIRA
```

**Passo 3 — expandir (conferindo (a)).**

```
(x² − x − 1)² = x⁴ + x² + 1 + 2·x²·(−x) + 2·x²·(−1) + 2·(−x)·(−1)
              = x⁴ + x² + 1 − 2x³ − 2x² + 2x
              = x⁴ − 2x³ − x² + 2x + 1                →  (a) VERDADEIRA
```

**Passo 4 — testar (c), a candidata a falsa.**

```
(x+2)(x+1) = x² + 3x + 2
· x        = x³ + 3x² + 2x
·(x−1)     = x⁴ + 3x³ + 2x² − x³ − 3x² − 2x = x⁴ + 2x³ − x² − 2x
+ 1        = x⁴ + 2x³ − x² − 2x + 1
```

Comparando com `x⁴ − 2x³ − x² + 2x + 1`: os coeficientes de **x³** e de **x** têm sinal trocado.
Portanto **(c) é FALSA**. (De fato, `(x+2)(x+1)x(x−1) + 1 = (x² + x − 1)²` — o quadrado do polinômio
com o sinal de x trocado. Quem troca um sinal em `x² − x − 1` cai aqui.)

**Passo 5 — conferir (d) e (e).** Com `f = g²` e `g = x² − x − 1`:

```
f'(x) = 2·g(x)·g'(x) = 2(x² − x − 1)(2x − 1)
```

Raízes de `f'`: `x₁`, `x₂` (de g) e `x = 1/2` (de `2x − 1`) → **(d) e (e) VERDADEIRAS**.

**Resposta: (c).**

**Leitura geométrica (útil para conferir).** `f ≥ 0` sempre; as raízes x₁ e x₂ são **duplas** (o gráfico
toca o eixo sem cruzar) e há um máximo local em `x = 1/2`, com `f(1/2) = (1/4 − 1/2 − 1)² = 25/16`.
É exatamente o padrão "duas raízes duplas + um ponto crítico no meio" (Rolle entre x₁ e x₂).

**Armadilha.** O enunciado pede a **errada**. Boa parte dos erros nesse formato é marcar uma afirmação
*verdadeira* por reflexo. Antes de marcar, releia: *"Mark the wrong statement"*.

**Padrão.** x₁, x₂ dados por radicais → **nunca** substitua os valores; use soma e produto para montar o
polinômio. Duas questões de polinômios por prova costumam sair só disso.

---

### Q4 · Soma binomial — **(b) 9¹⁰**

**Enunciado.** `Σ_{k=0}^{20} C(20,k)·2^k`
(a) 2⁴⁰ · (b) 9¹⁰ · (c) 20²⁰ · (d) 20! · (e) 40!/20!

**Ideia.** Binômio de Newton: `(1 + a)ⁿ = Σ_{k=0}^{n} C(n,k)·a^k`. Com `n = 20` e `a = 2`:

```
Σ_{k=0}^{20} C(20,k)·2^k = (1 + 2)²⁰ = 3²⁰
```

**Converter para a alternativa.** `3²⁰ = (3²)¹⁰ = 9¹⁰`. (Confere: 3²⁰ = 3.486.784.401.)

**Resposta: (b) 9¹⁰.**

**Por que as outras caem.**
- (a) 2⁴⁰ = 4²⁰ — viria de `(2 + 2)²⁰`, isto é, trocar o `1` por `2` na base.
- (c) 20²⁰ — viria do binômio `(1 + 19)²⁰`, isto é, a = 19.
- (d) 20! e (e) 40!/20! = 20!·C(40,20) — "cara de combinatória", sem relação com a soma.

**Padrão.** Reconheça na hora: `Σ C(n,k)a^k = (1+a)ⁿ` e `Σ C(n,k)a^k b^{n−k} = (a+b)ⁿ`.
A banca gosta de escrever o resultado em **outra base** (9¹⁰ em vez de 3²⁰) para testar se você domina
potências — não é pegadinha algébrica, é pegadinha de leitura.

---

### Q5 · Diagonais espaciais do dodecaedro — **(c) 100**

**Enunciado.** Quantas diagonais espaciais (ligam dois vértices que **não** estão na mesma face) tem o
dodecaedro regular?
(a) 36 · (b) 72 · (c) 100 · (d) 120 · (e) 160

**Dados do dodecaedro regular.** V = 20 vértices, E = 30 arestas, F = 12 faces pentagonais.
(Euler confere: `20 − 30 + 12 = 2` ✔; e `12·5/2 = 30` arestas ✔.)

**Ideia: partição dos pares de vértices.** Todo par de vértices distintos é **exatamente uma** destas três
coisas: aresta, diagonal de face ou diagonal espacial. As categorias não se sobrepõem.

**Contagem.**

```
Pares de vértices:            C(20,2) = 190
(−) arestas:                            30
(−) diagonais de face:        12 · 5 =  60     [pentágono: C(5,2) − 5 = 10 − 5 = 5]
(=) diagonais espaciais:      190 − 30 − 60 = 100
```

**Resposta: (c) 100.**

**Por que cada pentágono tem 5 diagonais?** `C(5,2) = 10` pares; 5 são lados → 5 diagonais. E como duas
faces só compartilham **arestas** (nunca diagonais), não há dupla contagem.

**Conferência por vértice.** Cada vértice tem grau 3 e pertence a 3 pentágonos. De um vértice saem:
3 arestas + 3·2 = 6 diagonais de face + o resto. Dos 19 outros vértices: `19 − 3 − 6 = 10` são extremos de
diagonais espaciais. Total `20·10/2 = 100` ✔ (divide-se por 2 porque cada diagonal tem duas pontas).

**Por que as outras caem.**
- (e) 160 = `190 − 30`: esqueceu as diagonais de face — o erro mais comum.
- (a) 36, (b) 72, (d) 120: fórmulas decoradas erradas / contagens de outras diagonais.
- 60 sozinho é só as diagonais de face.

**Padrão.** "Quantas diagonais..." resolve sempre por **complemento**: pares totais − arestas − diagonais
de face. Para um poliedro com faces de `n_f` lados:
`D_esp = C(V,2) − E − Σ_f [C(n_f,2) − n_f]`.

---

### Q6 · Suficiência de dados (álgebra) — **(c)**

**Enunciado.**

```
I.  xy/(x − y) = 5          II.  xy/(x + y) = 1
```

Quer-se o valor de `E = (x² − y²)/(x²y²) + 2/(xy)`. Sobre a suficiência:
(a) só I basta · (b) só II basta · (c) I e II juntas bastam, nenhuma sozinha · (d) cada uma sozinha basta ·
(e) nem juntas bastam

**Passo 1 — trocar de variáveis (o truque que resolve em 3 linhas).** Seja

```
p = 1/x        q = 1/y
```

Então `(x−y)/(xy) = 1/y − 1/x = q − p` e `(x+y)/(xy) = 1/x + 1/y = p + q`. As equações viram:

```
I.  xy/(x−y) = 1/(q − p) = 5   →   q − p = 1/5
II. xy/(x+y) = 1/(p + q) = 1   →   p + q = 1
```

E a expressão pedida:

```
E = (x² − y²)/(x²y²) + 2/(xy) = (1/y² − 1/x²) + 2/(xy) = (q² − p²) + 2pq
```

**Passo 2 — testar a suficiência.**

- **Só I** (conheço `q − p = 1/5`): `E = (q−p)(q+p) + 2pq = (1/5)(p+q) + 2pq` — ainda depende de `p+q` e
  de `pq`. Uma equação em duas incógnitas → **não determina**. (Exemplos: (x, y) = (5; 2,5) dá E = 0,28;
  (x, y) = (2,5; 5/3) dá E = 0,68.)
- **Só II** (conheço `p + q = 1`): `E = (q−p)·1 + 2pq` — depende de `q−p` e de `pq` → **não determina**.
  (Exemplos: (x, y) = (2, 2) dá E = 1/2; (x, y) = (3; 1,5) dá E = 7/9.)
- **Juntas:** o sistema `p + q = 1`, `q − p = 1/5` dá `q = 3/5` e `p = 2/5`, logo `x = 5/2`, `y = 5/3`.
  E `pq = ((p+q)² − (q−p)²)/4 = (1 − 1/25)/4 = 6/25`. Portanto

```
E = (1/5)(1) + 2·(6/25) = 1/5 + 12/25 = 5/25 + 12/25 = 17/25
```

Fixados p e q, **E está determinado** (17/25).

**Resposta: (c)** — I e II juntas são suficientes; nenhuma sozinha é.

**Conferência direta.** `x = 5/2, y = 5/3`: `xy = 25/6`, `x−y = 5/6` → `(25/6)/(5/6) = 5` ✔;
`x+y = 25/6` → `(25/6)/(25/6) = 1` ✔. E `(x²−y²)/(x²y²) = (125/36)/(625/36) = 1/5`, `2/(xy) = 12/25` →
`E = 17/25` ✔.

**Armadilha.** A tentação é "resolver o sistema" e marcar (c) sem verificar — mas a banca exige que você
**mostre que cada uma falha**. Repare que `E` é **homogênea de grau −2**: se você troca (x, y) por (λx, λy),
`E` fica dividido por λ². Ora, a equação I é **invariante por escala** (ela só fixa a razão `(x−y)/xy`),
portanto não pode determinar `E`; e a II, apesar de misturar escala e razão, é **uma** equação para as duas
incógnitas `p = 1/x` e `q = 1/y`.

**Padrão.** Suficiência em álgebra: (1) reformule as equações em termos úteis (aqui `1/x`, `1/y`);
(2) reescreva a expressão-alvo nessas variáveis; (3) verifique **quantos** graus de liberdade sobram.
Se a expressão ficar em função de grandezas que a equação não fixa, não há suficiência.

---

### Q7 · Equação logarítmica — **(b)**

**Enunciado.** Seja x > 0, `x ≠ 1`, `x ≠ 1/3`, satisfazendo

```
(2 + log₃x) / log_{x+2}(x)  −  log_x(x+2) / (1 + log₃x)  =  log_x(x+2)
```

Então x pertence a: (a) (0, 1/81) · (b) (1/81, 1/3) · (c) (1/2, 1) · (d) (1, 3/2) · (e) (3/2, 2)

**Passo 1 — domínio.** `x > 0`, `x ≠ 1` (base), `x ≠ 1/3` (para `1 + log₃x ≠ 0`). A base `x + 2 > 2`, então
`log_{x+2}` e `log_x` estão bem definidos. Como `x + 2 ≠ 1`, o valor `log_x(x+2)` **nunca** é zero.

**Passo 2 — duas substituições.**

```
t = log₃x          u = log_x(x+2)
```

e a mudança de base `log_{x+2}(x) = 1/log_x(x+2) = 1/u` (válida porque u ≠ 0).

**Passo 3 — substituir.** `(2 + t)·u − u/(1 + t) = u`, com `1 + t ≠ 0`.

**Passo 4 — dividir por u (≠ 0) e resolver.**

```
(2 + t) − 1/(1 + t) = 1
t + 1 = 1/(t + 1)
(t + 1)² = 1
t + 1 = ±1        →        t = 0    ou    t = −2
```

**Passo 5 — voltar para x.**

```
t = 0   →  x = 3⁰ = 1     →  EXCLUÍDO (o enunciado exige x ≠ 1)
t = −2  →  x = 3⁻² = 1/9
```

**Passo 6 — conferir.** Em `x = 1/9`: `t = −2` e `u = log_{1/9}(19/9) ≠ 0`. A equação vira
`(2−2)u − u/(1−2) = 0 + u = u` ✔ (identidade).

**Passo 7 — localizar o intervalo.** `1/81 ≈ 0,0123 < 1/9 ≈ 0,111 < 1/3 ≈ 0,333`, logo
`x = 1/9 ∈ (1/81, 1/3)`.

**Resposta: (b).**

**Armadilhas.**
- Esquecer de **excluir x = 1**: a raiz t = 0 existe algebricamente, mas o domínio a proíbe. O enunciado
  já avisa `x ≠ 1` — é sinal de que haverá raiz espúria.
- Errar a mudança de base: `log_{x+2}(x) = 1/log_x(x+2)`, e não `−log_x(x+2)`.
- Achar `t = −2` e marcar (a) `(0, 1/81)` por confundir `3⁻²` com `3⁻⁴`.

**Padrão.** Toda equação com **bases diferentes** → troque tudo para **uma** variável (aqui `t = log₃x`) e
use `log_a b = 1/log_b a`. Se o enunciado proíbe um valor de x, ele é exatamente a raiz que a álgebra vai
produzir.

---

### Q8 · Complexos: onde está a barra do conjugado — **(c)**

**Enunciado.** Para todo `z = x + yi ∈ ℂ`:
**I.** `z² = (z̄)²` · **II.** `conj(z⁴) = (z̄)⁴`
(a) ambas falsas · (b) I verdadeira, II falsa · (c) I falsa, II verdadeira · (d) ambas verdadeiras ·
(e) II é problema em aberto

**Fato básico.** A conjugação é um **automorfismo de corpo**:
`conj(z + w) = z̄ + w̄` e `conj(z·w) = z̄·w̄`. Consequência imediata por indução:

```
conj(zⁿ) = (z̄)ⁿ     para todo n natural
```

Isso **resolve II na hora: VERDADEIRA** — para qualquer z, `conj(z⁴) = (z̄)⁴`.

**E a I?** `z² − (z̄)² = (z − z̄)(z + z̄)`. Com `z = x + yi`:

```
z − z̄ = 2yi        z + z̄ = 2x        →        z² − (z̄)² = 4ixy
```

Isso só se anula quando `x = 0` ou `y = 0` (eixos real ou imaginário). Leitura equivalente, que vale a pena
guardar: como `(z̄)² = conj(z²)`, a afirmação I diz exatamente que **`z²` é real** — e nem todo z tem z² real.
Contraexemplo: `z = 1 + i`:

```
z² = (1+i)² = 2i        (z̄)² = (1−i)² = −2i        →  diferentes
```

**I é FALSA.**

**Resposta: (c)** — I falsa, II verdadeira.

**Por que a pegadinha funciona.** As duas afirmações parecem idênticas, mas a barra está em **lugares
diferentes**:

- **I:** `z² = (z̄)²` → conjuga **antes** de elevar. Em geral, falso.
- **II:** `conj(z⁴) = (z̄)⁴` → conjuga **depois** de elevar. Sempre verdadeiro.

Na forma polar `z = r·e^{iθ}`, `z̄ = r·e^{−iθ}`: `(z̄)² = r²e^{−2iθ}` enquanto `z² = r²e^{2iθ}` (só iguais
se `e^{4iθ} = 1`); já `conj(z⁴) = conj(r⁴e^{4iθ}) = r⁴e^{−4iθ} = (r·e^{−iθ})⁴` ✔.

**Por que as outras caem.**
- (a) "ambas falsas" — quem percebe que I é falsa e não repara na diferença da barra em II.
- (d) "ambas verdadeiras" — quem acha que conjugação comuta com potência sempre.
- (e) é absurdo (não há problema em aberto aí).

**Padrão.** Questões de complexos com "duas afirmações" quase sempre testam **propriedades de corpo do
conjugado** (soma, produto, potência, módulo). Leia a posição da barra com lupa.

---

### Q9 · Taxa de trabalho — **(c) 4 h**

**Enunciado.** 3 profissionais fazem 24 peças em 2 h; 4 aprendizes fazem 16 peças em 3 h. Quantas horas
para 2 profissionais e 3 aprendizes fazerem 48 peças?
(a) 2 · (b) 3 · (c) 4 · (d) 5 · (e) 6

**Passo 1 — normalizar tudo para "peças por pessoa-hora".**

```
profissional:  24 / (3 · 2) = 4 peças/(pessoa·hora)
aprendiz:      16 / (4 · 3) = 4/3 peça/(pessoa·hora)
```

**Passo 2 — taxa da equipe pedida.**

```
2·4 + 3·(4/3) = 8 + 4 = 12 peças por hora
```

**Passo 3 — tempo.**

```
t = 48 / 12 = 4 horas
```

**Resposta: (c) 4.**

**Conferência.** Em 4 h: profissionais → `2·4·4 = 32` peças; aprendizes → `3·(4/3)·4 = 16` peças;
total 48 ✔.

**Armadilha.** Somar "24 + 16 = 40 peças em 2 + 3 = 5 h" e concluir `48/8 = 6` h (alternativa e). Taxa de
trabalho **não** se soma assim: é preciso reduzir a uma unidade comum (peça por pessoa·hora) — a armadilha
clássica é comparar horas de equipes de tamanhos diferentes.

**Padrão.** "n pessoas fazem k peças em t horas" → taxa `k/(n·t)`; depois some taxas e divida o serviço.

---

### Q10 · Determinante de matriz triangular — **(d)**

**Enunciado.** `A = [[a, c, e, e], [0, a, e, e], [0, 0, b, d], [0, 0, 0, b]]`. Qual condição **garante**
`det(A) > 0`?
(a) `c⁴de > 0` · (b) `a + b > 0` · (c) `a² + b² > 0` · (d) `ab ≠ 0` · (e) `cde ≠ 0`

**Observação-chave.** A é **triangular superior**: tudo abaixo da diagonal é zero. Determinante de matriz
triangular = **produto dos elementos da diagonal**:

```
det(A) = a · a · b · b = a²b²
```

**Analisar.** Para a, b reais, `a²b² ≥ 0` **sempre**. Logo:

```
det(A) > 0   ⟺   a²b² > 0   ⟺   a ≠ 0  e  b ≠ 0   ⟺   ab ≠ 0
```

**Resposta: (d) ab ≠ 0.**

**Por que as outras não garantem.**
- (a) `c⁴de > 0` — fala de c, d, e; não diz nada sobre a e b. Com a = 0, det = 0.
- (b) `a + b > 0` — permite a = 0, b = 1 → det = 0.
- (c) `a² + b² > 0` — garante que **pelo menos um** é não nulo; com a = 0, b = 1 → det = 0. É a distratora
  mais perigosa: *"um dos dois"* ≠ *"os dois"*.
- (e) `cde ≠ 0` — fala só de c, d, e; a e b podem ser zero.

**Conferência numérica.** a = 2, b = 3, c = 1, d = 5, e = 7 → det = 36 = 2²·3² ✔ (e não depende de c, d, e).

**Padrão.** Antes de expandir um determinante 4×4, **olhe a estrutura**: é triangular? tem bloco? tem
linha/coluna proporcional? Em prova sem calculadora, determinante quase sempre tem atalho estrutural.

---

### Q11 · Volume do prisma a partir da planificação — **(a) √2/4**

**Enunciado.** A Figura 2 mostra a planificação de um poliedro prismático; **todas as arestas** medem 1;
as **diagonais** BD (da face ABED) e CD (da face ACFD) também medem 1. Qual o volume do poliedro montado?
(a) √2/4 · (b) 3/8 · (c) √3/4 · (d) 1/2 · (e) a planificação não fecha um poliedro

**Passo 1 — identificar o sólido.** A planificação tem 2 triângulos (ABC e DEF) e 3 quadriláteros
(ABED, BCFE, ACFD) → é um **prisma triangular**: base ABC, tampa DEF, arestas laterais AD, BE, CF.

**Passo 2 — traduzir "diagonal = aresta" em ângulos.**
A face ABED é um paralelogramo com `AB = AD = 1` → **losango** de lado 1. Sua diagonal `BD = 1`.
No triângulo ABD os **três** lados valem 1 → **equilátero** → `∠DAB = 60°`.

Idem para a face ACFD: losango de lado 1 com diagonal `CD = 1` → triângulo ACD equilátero → `∠DAC = 60°`.

E a base ABC é equilátera (as três arestas unitárias) → `∠BAC = 60°`.

**Passo 3 — formalizar com vetores.** Sejam `u = AB`, `v = AC`, `w = AD`, todos unitários. Os três ângulos
entre eles são 60°, logo `u·v = u·w = v·w = 1/2`. Matriz de Gram:

```
      ⎡  1   1/2  1/2 ⎤
G  =  ⎢ 1/2   1   1/2 ⎥          det G = 1 − 3·(1/4) + 2·(1/8) = 1/2
      ⎣ 1/2  1/2   1  ⎦
```

O volume do **paralelepípedo** gerado por u, v, w é `√(det G) = √(1/2) = √2/2`.
O prisma de base triangular ABC e translação w ocupa **exatamente metade** desse paralelepípedo, logo:

```
V = (1/2)·(√2/2) = √2/4
```

**Passo 4 — conferência por "área da base × altura".** Base equilátera de lado 1: `S = √3/4`.
Altura = componente de w perpendicular ao plano ABC:

```
h = |det(u,v,w)| / |u × v| = (√2/2)/(√3/2) = √(2/3) ≈ 0,8165
V = S·h = (√3/4)·√(2/3) = √2/4 ≈ 0,3536  ✔
```

**Passo 5 — coordenadas explícitas (para visualizar).** `u = (1, 0, 0)`, `v = (1/2, √3/2, 0)`,
`w = (1/2, 1/(2√3), √(2/3))`. Então `|w| = 1` ✔, `|w − u| = BD = 1` ✔, `|w − v| = CD = 1` ✔.

**Resposta: (a) √2/4.**

**Por que (e) está errada.** A planificação **fecha** sim: os ângulos de 60° nos losangos são compatíveis
com as faces triangulares equiláteras. É a alternativa "do desespero", para quem tenta visualizar e desiste.

**Por que (b) 3/8 (0,375) é perto mas não é.** 3/8 sai de `(√3/4)·(√3/2)`, isto é, de usar a altura
errada (`√3/2`, a altura do **tetraedro** regular). A altura correta é `√(2/3) ≈ 0,8165`.

**Por que (c) e (d) caem.** (c) `√3/4` é só a **área da base** (esqueceu de multiplicar pela altura);
(d) 1/2 vem de tomar o volume do paralelepípedo como 1 (esquecendo que o ângulo de 60° reduz o
determinante para `√2/2` e o prisma para a metade).

**Padrão.** Planificação → (1) identifique o sólido e as faces; (2) converta "diagonal = aresta" em
**ângulos** (losango + diagonal = triângulo equilátero); (3) vetores + determinante = caminho seguro para
volume. Guarde: prisma triangular = **metade** do paralelepípedo gerado pelas três arestas que saem de um
vértice.

---

### Q12 · Inversão de dígitos — **(d) 8**

**Enunciado.** Quantos inteiros `10 < n < 100` são tais que, invertendo os dígitos de n, obtém-se `n + 9`?
(a) 5 · (b) 6 · (c) 7 · (d) 8 · (e) 9

**Modelar.** Como `10 < n < 100`, escreva `n = 10a + b` com `a ∈ {1,…,9}` e `b ∈ {0,…,9}`.
Invertido: `10b + a`. A condição:

```
10b + a = (10a + b) + 9
9b − 9a = 9
b − a = 1
```

**Contar.** `b = a + 1` e `b ≤ 9` → `a ≤ 8`; com `a ≥ 1`:

```
a ∈ {1, 2, 3, 4, 5, 6, 7, 8}   →   8 números
n ∈ {12, 23, 34, 45, 56, 67, 78, 89}
```

**Resposta: (d) 8.**

**Conferência.** `21 = 12 + 9` ✔; `98 = 89 + 9` ✔. E `a = 9` exigiria `b = 10`, impossível — é o limite
que fixa a contagem em 8, não 9.

**Armadilha.** Contar 9 (incluindo 90 ou 99) ou esquecer que `b` pode ser 0 e `b − a = 1` já exclui b = 0.

**Padrão.** Problemas de dígitos: escreva `n = 10a + b` e traduza cada condição em equação linear inteira.

---

### Q13 · Suficiência de dados (geometria) — **(a)**

**Enunciado.** Na Figura 3, D está sobre AC, com `∠BAD = α`, `∠BDC = 2α` e `∠ACB = 2α`.
Quer-se o comprimento de BC.
**I.** AD = 6 · **II.** α = 36°

**Passo 1 — "caça aos isósceles".**

- No triângulo **BDC**: `∠BDC = ∠BCD = 2α` → lados opostos iguais → **BC = BD**.
- No triângulo **ABD**: `∠ADB = 180° − 2α` (suplementar de ∠BDC, pois A, D, C são colineares) e
  `∠BAD = α` → `∠ABD = 180° − α − (180° − 2α) = α = ∠BAD` → **AD = BD**.

**Conclusão-chave.**

```
AD = BD = BC
```

Isto é: **BC = AD, para qualquer α**. Não é preciso saber α nem usar trigonometria.

**Passo 2 — testar cada afirmação.**

- **I. AD = 6** → `BC = 6`. **Suficiente.**
- **II. α = 36°** → fixa os ângulos (A = 36°, C = 72°, B = 72°), isto é, fixa a **forma**, mas não a
  **escala**: multiplicando o triângulo por qualquer k > 0 a figura continua válida e BC fica livre.
  **Não suficiente.**

**Resposta: (a)** — I sozinha basta; II não.

**Nota.** Com I **e** II você obteria BC = 6 do mesmo jeito — mas α é **redundante** para o comprimento.
E II é um dado *de forma*: sozinho nunca determina uma medida.

**Armadilha.** (c) "juntas" — parece natural porque α = 36° "explica" a figura (é o ângulo do pentágono
regular e do triângulo áureo), mas a pergunta é sobre **comprimento**, e I já responde.

**Padrão (suficiência de dados).** Classifique cada dado: é **de escala** (comprimento, área, volume) ou
**de forma** (ângulo, razão)? Para obter um comprimento é preciso escala; para obter uma razão, basta a
forma. Aqui I é escala, II é forma. Antes de calcular, pergunte: *"o dado fixa o tamanho?"*

---

### Q14 · Porcentagens encadeadas — **(c) 12 000**

**Enunciado.** A recebeu `1/3` **a mais** que B; B recebeu `1/4` **a menos** que C; C recebeu 12 000.
Quantos votos recebeu A?
(a) 9 000 · (b) 11 000 · (c) 12 000 · (d) 13 000 · (e) 16 000

**Traduzir em fatores.**

```
B = C − (1/4)C = (3/4)C
A = B + (1/3)B = (4/3)B
```

**Calcular.**

```
B = (3/4)·12 000 = 9 000
A = (4/3)·9 000  = 12 000
```

**Resposta: (c) 12 000.**

**Armadilha dupla.** (i) "1/3 a mais" = multiplicar por **4/3**, não somar 1/3; (ii) "1/4 a menos" =
multiplicar por **3/4**. Quem faz `A = 12 000·(1 + 1/3) = 16 000` (alternativa e) esquece o desconto de B.

**Curiosidade.** `(4/3)·(3/4) = 1`: A volta exatamente a C. Foi proposital — e é por isso que (c) e (e)
estão ambas "redondas".

**Padrão.** "x% a mais" → fator `(1 + x)`; "a menos" → `(1 − x)`. Encadeie **multiplicando** fatores.

---

### Q15 · Isolar variável em equação literal — **(a) 2ab/(b − 3a)**

**Enunciado.** Se `a, b, m > 0` e `(m + a)/(m + b) = 3a/b`, qual o valor de m?
(a) `2ab/(b − 3a)` · (b) `b/(3a)` · (c) `a/(2b)` · (d) `4ab/(b − 3a)` · (e) `(b − 3a)/(2ab)`

**Resolver.**

```
(m + a)/(m + b) = 3a/b
b(m + a) = 3a(m + b)            (produto dos extremos; b ≠ 0)
bm + ab = 3am + 3ab
bm − 3am = 3ab − ab = 2ab
m(b − 3a) = 2ab
m = 2ab/(b − 3a)
```

**Resposta: (a) 2ab/(b − 3a).**

**Conferência numérica.** a = 1, b = 4 → `m = 8/(4 − 3) = 8`. Teste: `(8+1)/(8+4) = 9/12 = 3/4` e
`3a/b = 3/4` ✔.

**Armadilha.** (d) `4ab/(b−3a)` aparece se você somar `3ab + ab = 4ab` (erro de sinal na distribuição);
(b), (c) e (e) são "formas" plausíveis sem álgebra.

**Padrão.** Equação com letras: multiplique em cruz, **agrupe** os termos com m, **fatore** m. Confira
sempre com números pequenos.

---

### Q16 · Probabilidade / desarranjo — **(e) 3/8**

**Enunciado.** Quatro casais dançam; os pares (homem, mulher) são formados ao acaso. Qual a probabilidade
de **nenhum** homem dançar com a própria esposa?
(a) 1/4 · (b) 5/18 · (c) 5/16 · (d) 1/3 · (e) 3/8

**Modelar.** Numere homens e mulheres 1…4, com o homem i casado com a mulher i. Um pareamento é uma
**permutação** σ de {1,2,3,4} (homem i dança com a mulher σ(i)). Total de casos: `4! = 24`.

O evento pedido é "σ(i) ≠ i para todo i" — um **desarranjo**.

**Contar D₄ por inclusão-exclusão.**

```
D₄ = 24 − C(4,1)·3! + C(4,2)·2! − C(4,3)·1! + C(4,4)·0!
   = 24 − 24 + 12 − 4 + 1 = 9
```

(24 = todos; fixar 1 casal → 3! = 6, com 4 escolhas; fixar 2 casais → 2! = 2, com 6 escolhas; fixar 3 → 1,
com 4 escolhas; fixar 4 → 1.)

Alternativa pela fórmula: `Dₙ = n!·Σ_{k=0}^{n} (−1)^k/k!` → `D₄ = 24(1 − 1 + 1/2 − 1/6 + 1/24) = 9`.

**Probabilidade.**

```
P = D₄/4! = 9/24 = 3/8
```

**Resposta: (e) 3/8.**

**Conferência — os 9 desarranjos.** 2143, 2341, 2413, 3142, 3412, 3421, 4123, 4312, 4321.

**Armadilha.** (a) 1/4, (b) 5/18, (c) 5/16, (d) 1/3 são todos "vizinhos" de `1/e ≈ 0,368`, que é o
**limite** de `Dₙ/n!`. Para n = 4 o valor exato é `3/8 = 0,375` — o mais próximo de 1/e. Quem chuta "1/e
arredondado" marca 1/3 e erra.

**Padrão.** "Nenhum no lugar" = desarranjo. Decore `D₃ = 2`, `D₄ = 9`, `D₅ = 44` e o limite `Dₙ/n! → 1/e`;
a banca repete esse formato (2025/2 e outros anos).

---

## 4. Padrões que a banca repetiu nesta prova

1. **Contagem por complemento.** Q5 (pares − arestas − diagonais de face) e Q16 (todos − "pelo menos um
   fixo"). Sempre é mais fácil contar o total e subtrair o que não serve.
2. **Suficiência de dados com dois formatos.** Q6 (álgebra) e Q13 (geometria) — e a lógica é a mesma:
   descubra **quantos graus de liberdade** cada informação elimina. Em Q13, a sacada foi um isósceles
   escondido; em Q6, a troca `p = 1/x, q = 1/y`.
3. **"Fator escondido".** Q1 (`x−2` dentro de raízes), Q2 (quadrado perfeito `3 ± √10`), Q3
   (`x² − x − 1`). Quase todo problema "feio" tem uma estrutura escondida.
4. **Geometria espacial com condição métrica → ângulo → volume** (Q11). O caminho é sempre
   planificação → faces → ângulos → vetores.
5. **Log com bases diferentes** (Q7): trocar tudo para uma variável. E o `x ≠ 1` do enunciado é a raiz
   espúria anunciada.
6. **Estrutura antes da conta** (Q10): matriz triangular → determinante = produto da diagonal.
7. **Pegadinhas de leitura** — as mais baratas de perder: "wrong statement" (Q3), posição da barra do
   conjugado (Q8), "1/3 a mais" vs "1/4 a menos" (Q14).

---

## 5. Plano de 90 minutos

| Bloco | Tempo | Questões | Objetivo |
|:-----:|:-----:|----------|----------|
| 1 | 0–15 min | 4, 12, 10, 14, 9, 15, 16, 2 | as 8 "de ritmo": 8 acertos garantidos |
| 2 | 15–40 min | 1, 3, 5, 8, 6 | médias; aqui você já está acima do corte |
| 3 | 40–70 min | 7, 13, 11 | as longas, com calma |
| 4 | 70–90 min | todas | revisar leitura, conferir gabarito no formulário |

Regra de bolso: **se travou por 3 minutos, marque a melhor aposta e siga**. Cada questão vale o mesmo, e
uma questão longa não vale mais que uma curta.

---

## 6. Checklist final (o que faz perder ponto bobo)

- [ ] Releu o **comando**? "wrong", "not sufficient", "greater than", "less than".
- [ ] Em suficiência: classificou cada dado em **escala** vs **forma**?
- [ ] Em log: conferiu **domínio** (x > 0, base ≠ 1, x ≠ 1) e a raiz espúria?
- [ ] Em geometria espacial: usou **vetores/determinante** em vez de "visualizar"?
- [ ] Em contagem: contou por **complemento** e conferiu se cada objeto foi contado **duas vezes** (pares
      de pontas: arestas, diagonais, casais)?
- [ ] Conferiu as alternativas "vizinhas": 3/4 vs 9/8, 3/8 vs √2/4, 1/3 vs 3/8?

---

## 7. Resumo de fórmulas usadas

```
Binômio:              Σ C(n,k)·aᵏ = (1 + a)ⁿ
Radical duplo:        √(A ± B√C) = m ± n√C, com m² + n²C = A e 2mn = B
Mudança de base:      log_a b = 1 / log_b a
Determinante:         triangular ⇒ produto da diagonal
Euler:                V − E + F = 2
Diagonais espaciais:  C(V,2) − E − Σ_f [C(n_f,2) − n_f]
Volume do prisma:     (1/2)·|det(u, v, w)|
Desarranjo:           Dₙ = n!·Σ_{k=0}^{n} (−1)^k/k!   (D₄ = 9; Dₙ/n! → 1/e)
```

---

## 8. Onde treinar cada questão

| Questão | Tema no repositório |
|:-------:|---------------------|
| 1, 7 | [`temas/08-calculo`](../../temas/08-calculo/README.md) · [`temas/04-funcoes-log-exp`](../../temas/04-funcoes-log-exp/README.md) |
| 2, 3, 15 | [`temas/05-polinomios-e-raizes`](../../temas/05-polinomios-e-raizes/README.md) |
| 4, 16 | [`temas/01-combinatoria`](../../temas/01-combinatoria/README.md) |
| 5, 11, 13 | [`temas/03-geometria`](../../temas/03-geometria/README.md) |
| 6, 13 | [`temas/11-logica-suficiencia-dados`](../../temas/11-logica-suficiencia-dados/README.md) |
| 8 | [`temas/09-numeros-complexos`](../../temas/09-numeros-complexos/README.md) |
| 9, 14 | [`temas/10-problemas-taxa-trabalho`](../../temas/10-problemas-taxa-trabalho/README.md) |
| 10 | [`temas/02-sistemas-matrizes-determinantes`](../../temas/02-sistemas-matrizes-determinantes/README.md) |
| 12 | [`temas/11-logica-suficiencia-dados`](../../temas/11-logica-suficiencia-dados/README.md) |

> Em cada tema, o arquivo **`RESOLUCOES-PASSO-A-PASSO.md`** traz a resolução linha a linha de todas as
> outras questões reais daquele assunto (1º e 2º semestres) — é o complemento natural desta leitura por prova.

---

**Prova original:** [`Prova_PG-EIA_2025-2oSem.pdf`](../Prova_PG-EIA_2025-2oSem.pdf) ·
**Texto extraído:** [`Prova_PG-EIA_2025-2oSem.txt`](../Prova_PG-EIA_2025-2oSem.txt) ·
**Índice de resoluções:** [`README.md`](README.md) · **Provas:** [`../README.md`](../README.md).
