# Resolução comentada — Matemática · 2024 / 2º semestre (PG-EIA · ITA)

**Prova:** [`../Prova_PG-EIA_2024-2oSem.pdf`](../Prova_PG-EIA_2024-2oSem.pdf) — aplicada em **20 de maio de 2024**.
**Formato:** 16 questões de múltipla escolha (a–e), enunciados em inglês, **90 minutos**, sem calculadora.
**Gabarito:** `1-b 2-c 3-c 4-e 5-c 6-e 7-d 8-c 9-d 10-b 11-e 12-e 13-e 14-a 15-c 16-d`.

> **O que este arquivo entrega.** As **16 questões resolvidas passo a passo**: diagnóstico, conta completa,
> por que a alternativa correta é correta, **por que as outras caem**, armadilhas de leitura e o padrão da
> banca. A prova de 2024/2 não trouxe chave oficial no PDF; as 16 respostas foram obtidas por resolução
> independente, **conferidas numericamente** e **cruzadas com as resoluções por tema deste repositório**.

> **Sobre o nome.** É a prova de Matemática do processo seletivo do PG-EIA/ITA, de múltipla escolha no
> estilo GMAT — a "prova de GMAT/GMATE" do 2º semestre de 2024. No repositório, o PDF é o
> `Prova_PG-EIA_2024-2oSem.pdf`.

**Recado rápido:** esta prova é **mais traiçoeira que a de 2025/2**. Quatro questões pedem "qual é a
**errada** / o que **não** se pode dizer" (Q2, Q6, Q9, Q16) e três respostas ficam em (e). O inimigo aqui é
a leitura, não a conta.

---

## 1. Gabarito relâmpago

| Questão | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 | 13 | 14 | 15 | 16 |
|:-------:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| **Resposta** | **b** | **c** | **c** | **e** | **c** | **e** | **d** | **c** | **d** | **b** | **e** | **e** | **e** | **a** | **c** | **d** |

---

## 2. Raio-X da prova

| # | Assunto | Resp. | Nível | Tempo-alvo |
|:-:|---------|:-----:|:-----:|:----------:|
| 1 | Reservatório: vazão com entrada e saída | b | fácil | 2 min |
| 2 | f(x) = x·ln(1/x): qual afirmação é falsa | c | médio | 4 min |
| 3 | f″ = a constante: Taylor e "Torricelli" | c | médio | 3 min |
| 4 | Caminhos de 5 arestas no tetraedro (trilhas em K₄) | e | difícil | 5 min |
| 5 | Sistema simétrico x²−xy+y² = 7, x³+y³ = 35 | c | médio | 3 min |
| 6 | Autovetores de matriz bloco-diagonal | e | médio | 3 min |
| 7 | Esferas empilhadas em pirâmide de base quadrada | d | fácil | 1,5 min |
| 8 | Valor de i^i | c | fácil | 2 min |
| 9 | Identidades hiperbólicas (quantas corretas) | d | médio | 3 min |
| 10 | Sequência complexa (De Moivre) | b | difícil | 4 min |
| 11 | Ordenar logaritmos de bases diferentes | e | fácil | 2 min |
| 12 | Simplificar (cos²x − cot x)/(sin²x − tan x) | e | médio | 3 min |
| 13 | PG infinita com incógnita | e | médio | 2,5 min |
| 14 | Equação com fatoriais | a | fácil | 2 min |
| 15 | Distância da reta à origem | c | fácil | 1,5 min |
| 16 | Círculos tangentes e tangentes comuns | d | difícil | 6 min |

**Leitura estratégica.** Seis questões (7, 14, 15, 11, 1, 8) saem em menos de 2 min cada e já dão 6 acertos.
As que decidem a nota são Q4 (contagem em grafo), Q10 (De Moivre) e Q16 (cadeia de teoremas de tangência).
Soma dos tempos-alvo: **~48 min**, sobrando ~40 min para revisão — use-os para reler os comandos
"wrong/not", que é onde esta prova machuca.

---

## 3. Resoluções

### Q1 · Reservatório: entrada e saída — **(b) 8 dias**

**Enunciado.** Com o rio fluindo para o reservatório e os comportas abertas, um reservatório cheio esvazia
em 24 dias. Vazio e com as comportas fechadas, ele enche em 12 dias. Cheio, com as comportas abertas e o
rio desviado, em quantos dias esvazia?
(a) 6 · (b) 8 · (c) 12 · (d) 15 · (e) 18

**Modelar em taxas (capacidade = 1).**

```
entrada do rio:          a = 1/12  (enche em 12 dias)
saída pelas comportas:   g = ?     (é o que queremos)
```

Com rio + comportas abertas, o reservatório **esvazia** em 24 dias → a saída é maior que a entrada e a
diferença é `1/24`:

```
g − a = 1/24     →     g = 1/24 + 1/12 = 1/24 + 2/24 = 3/24 = 1/8
```

Com o rio desviado, só a comporta age: tempo = `1/g = 8` dias.

**Resposta: (b) 8 dias.**

**Conferência.** Em 8 dias a comporta tira 8·(1/8) = 1 reservatório ✔. Em 24 dias com o rio entrando:
saída total 24/8 = 3, entrada 24/12 = 2, líquido 1 ✔.

**Armadilha.** Quem **subtrai** as taxas (`1/12 − 1/24 = 1/24`) conclui 24 dias — que nem está nas opções,
mas o "quase acerto" é (c) 12 (ignorar a saída). A regra: *entrada e saída se opõem; o tempo de esvaziar
com entrada é o tempo da saída "contra" a entrada*.

**Padrão.** "Enche em t₁, esvazia em t₂, com ambos abertos esvazia em t" → `1/t = 1/t₂ − 1/t₁`.
Sempre reduza a taxa por dia e trabalhe com capacidade 1.

---

### Q2 · f(x) = x·ln(1/x): qual afirmação é FALSA — **(c)**

**Enunciado.** `f(x) = x·ln(1/x)` em (0, 1]. "One cannot say that":
(a) lim_{x→0} f(x) = 0 · (b) f(1) = 0 · (c) f′(x) = 1 + ln(1/x) ·
(d) f tem máximo em x = e⁻¹ · (e) ∫f dx = (1/4)x²[1 − 2ln(x)] + C

**Passo 1 — reescrever.** `ln(1/x) = −ln x`, logo `f(x) = −x·ln x`.

**Passo 2 — checar cada item.**

- **(a)** `lim_{x→0⁺} x ln x = 0` (indeterminação `0·∞`; L'Hôpital em `ln x/(1/x)` dá `(1/x)/(−1/x²) = −x → 0`),
  então `f → 0` ✔.
- **(b)** `f(1) = 1·ln 1 = 0` ✔.
- **(c)** Derive com a regra do produto:
  `f′(x) = ln(1/x) + x·(−1/x) = ln(1/x) − 1`. A alternativa diz `1 + ln(1/x)` → **FALSA** ✗.
- **(d)** `f′(x) = 0 ⟺ ln(1/x) = 1 ⟺ x = e⁻¹`; e `f″(x) = −1/x < 0` → máximo ✔.
- **(e)** `∫x ln(1/x)dx = −∫x ln x dx = −[x²/2·ln x − x²/4] = −x²/2·ln x + x²/4 = (x²/4)(1 − 2ln x)` ✔
  (confira derivando: `x/2 − x ln x − x/2 = −x ln x = x ln(1/x)`).

**Resposta: (c).**

**Armadilha (a mais didática da prova).** A derivada de `ln(1/x)` é `−1/x` (regra da cadeia). Quem
"esquece" o sinal obtém `+1/x` e chega exatamente em `1 + ln(1/x)` — que é a alternativa (c). Ou seja, a
alternativa errada foi construída a partir do erro clássico.

**Padrão.** `f = x·ln(1/x)` é a "entropia" que a banca adora: `f(0⁺) = 0`, `f(1) = 0`, máximo em `e⁻¹`,
integral `(x²/4)(1 − 2ln x)`. Vale memorizar o pacote.

---

### Q3 · f″ = a constante: Taylor e "Torricelli" — **(c)**

**Enunciado.** `f″(x) = a ≠ 0` em [x₀, x₁], `f′(x₀) = b`, `f(x₀) = c`. Julgue:
**(I)** `f(x) = a(x−x₀)² + b(x−x₀) + c`
**(II)** `[f′(x₁)]² = [f′(x₀)]² + 2a[f(x₁) − f(x₀)]`

**Passo 1 — integrar duas vezes.**

```
f′(x) = b + a(x − x₀)
f(x)  = c + b(x − x₀) + (a/2)(x − x₀)²
```

Logo **(I) está errada**: falta o fator `1/2` no termo quadrático (só valeria se `a` já fosse "a/2", isto é,
se `a` fosse a metade de f″). (I) é a fórmula de Torricelli escrita com a aceleração errada.

**Passo 2 — provar (II).** Derive `(f′)²`:

```
d/dx [ (f′(x))² ] = 2·f′(x)·f″(x) = 2a·f′(x)
```

Integrando de x₀ a x₁: `(f′(x₁))² − (f′(x₀))² = 2a[f(x₁) − f(x₀)]`, isto é, **(II)** ✔.

**Resposta: (c)** — (II) correta, (I) errada.

**Leitura física.** (II) é a equação de Torricelli `v² = v₀² + 2a·Δs` para aceleração constante.
(I) é o "espaço do MRUV" sem o `1/2` — o erro de quem decora `at²` em vez de `at²/2`.

**Verificação numérica.** a = 6, x₀ = 1, x₁ = 2,5, b = 2, c = 1:
`f(2,5) = 1 + 2·1,5 + 3·(1,5)² = 10,75`; `f′(2,5) = 2 + 6·1,5 = 11` → `121`.
E `b² + 2a(f(x₁) − f(x₀)) = 4 + 12·(9,75) = 4 + 117 = 121` ✔.

**Armadilha.** "a ≠ 0" no enunciado é a pista de que (I) **não** é identidade geral (se a = 0, (I) e a
fórmula correta coincidem). Em questões "as duas afirmações", teste sempre o caso extremo.

**Padrão.** `f″ = constante` → `f` é parábola `(a/2)(x−x₀)² + b(x−x₀) + c`; a relação entre `(f′)²` e `f`
é a versão "energia" do problema. Cai em 2024/2 e é o mesmo esqueleto de cinemática.

---

### Q4 · Caminhos de 5 arestas no tetraedro — **(e) 72**

**Enunciado.** Um caminho ao longo de 5 arestas do tetraedro é descrito pela sequência dos 6 vértices, sem
repetir aresta (exemplo: 1→2→3→4→1→3). Quantos caminhos próprios existem usando 5 das 6 arestas?
(a) 24 · (b) 36 · (c) 48 · (d) 60 · (e) 72

**Modelar como grafo.** O tetraedro é `K₄`: 4 vértices, 6 arestas, todos os pares ligados. Um caminho de
5 arestas sem repetição é uma **trilha** (trail) de comprimento 5 em K₄, isto é, uma sequência
`v₀v₁v₂v₃v₄v₅` com arestas duas a duas distintas.

**Observação-chave.** Uma trilha de comprimento 5 usa **5 das 6** arestas → ela **omite exatamente uma
aresta** e = {p, q}.

**Passo 1 — quem são os extremos.** Em K₄ todo vértice tem grau 3 (ímpar). Ao remover `e = {p,q}`,
`p` e `q` ficam com grau 2 (par) e os outros dois vértices `r, s` ficam com grau 3 (ímpar). Uma trilha que
usa *todas* as 5 arestas restantes é uma **trilha de Euler** de `K₄ − e`, e ela **tem de começar em r e
terminar em s** (os dois vértices ímpares) — ou o contrário.

**Passo 2 — contar para uma aresta omitida (por simetria, todas dão o mesmo).** Omita `12`. As arestas são
13, 14, 23, 24, 34 e os extremos obrigatórios são 3 e 4. Contando as trilhas 3 → 4:

```
3-1-4-3-2-4        3-1-4-2-3-4
3-2-4-1-3-4        3-2-4-3-1-4
3-4-1-3-2-4        3-4-2-3-1-4
```

São **6** trilhas de 3 para 4 (poderiam ser listadas por força bruta em ~1 min: de 3 saem 3 arestas, e em
cada ramo a sequência fica quase forçada).

**Passo 3 — multiplicar.**

```
6 arestas omitidas  ×  2 sentidos (r→s e s→r)  ×  6 trilhas  =  72
```

**Resposta: (e) 72.**

**Conferência por força bruta.** Enumerando todas as sequências de 6 vértices de K₄ com arestas distintas,
o computador acha exatamente **72** — e 12 por aresta omitida (6 em cada sentido) ✔.

**Por que as outras caem.** (a) 24 = 4! (permutações dos 4 vértices, coisa diferente); (b) 36 e (c) 48 são
contagens parciais (por exemplo, só os caminhos que começam num vértice fixo dão 72/4 = 18, e só um sentido
dá 36); (d) 60 = 72 − 12.

**Padrão.** "Caminho sem repetir aresta" = **trilha**; se o caminho usa todas as arestas do grafo, é
**trilha de Euler**, e o critério dos **dois vértices ímpares** diz onde ela começa e termina. Em K₄, isso
reduz o problema a "escolher a aresta omitida × contar trilhas de Euler".

---

### Q5 · Sistema simétrico — **(c) 2 soluções reais**

**Enunciado.** `x² − xy + y² = 7` e `x³ + y³ = 35`. Quantas soluções reais?
(a) nenhuma · (b) 1 · (c) 2 · (d) 3 · (e) 6

**Passo 1 — trocar para soma e produto.** Sejam

```
s = x + y          p = xy
```

Então (identidades simétricas):

```
x² − xy + y² = (x+y)² − 3xy = s² − 3p = 7
x³ + y³      = (x+y)³ − 3xy(x+y) = s³ − 3ps = 35
```

**Passo 2 — eliminar p.** Da primeira, `p = (s² − 7)/3`. Substituindo na segunda:

```
s³ − 3s·(s² − 7)/3 = 35
s³ − s(s² − 7) = 35
7s = 35      →      s = 5
```

**Passo 3 — voltar.** `p = (25 − 7)/3 = 6`. Logo x e y são as raízes de

```
t² − s·t + p = 0     →     t² − 5t + 6 = 0     →     t ∈ {2, 3}
```

**Passo 4 — contar.** As soluções ordenadas são `(2, 3)` e `(3, 2)` → **2 soluções reais**.

**Resposta: (c) 2 soluções reais.**

**Conferência.** `(2,3)`: 4 − 6 + 9 = 7 ✔; 8 + 27 = 35 ✔. `(3,2)`: idem por simetria ✔.

**Armadilha.** (b) "1 solução" é para quem acha o par {2,3} e esquece que a ordem importa (o sistema é
simétrico, mas as soluções são pares ordenados). (e) "6" viria de contar as raízes complexas de algum
polinômio auxiliar — não há.

**Padrão.** Sistema simétrico → sempre `s = x+y`, `p = xy`, usar `x²+y² = s²−2p`,
`x²−xy+y² = s²−3p`, `x³+y³ = s³−3ps`. O grau do sistema cai para 1 em s.

---

### Q6 · Autovetores da matriz bloco-diagonal — **(e)**

**Enunciado.**
```
      ⎡  1   −0,3   0  ⎤
M  =  ⎢ −0,3   1    0  ⎥
      ⎣  0     0   1,3 ⎦
```
Qual **não** é autovetor?
(a) (√2/2, −√2/2, 0)ᵀ · (b) (0, 0, 1)ᵀ · (c) (√3/3, −√3/3, √3/3)ᵀ · (d) (1, 1, 0)ᵀ ·
(e) (√3/3, √3/3, √3/3)ᵀ

**Passo 1 — ver a estrutura.** M é **bloco-diagonal**: o bloco 2×2

```
B = ⎡ 1   −0,3 ⎤
    ⎣ −0,3  1  ⎦
```

nas duas primeiras coordenadas, e o escalar 1,3 na terceira. Autovetores de M são "montados" com
autovetores de B nas duas primeiras posições (terceira = 0) **ou** com (0,0,1).

**Passo 2 — diagonalizar B.** `B = I − 0,3·J` com `J = [[0,1],[1,0]]`. Os autovetores de J são `(1,1)`
(λ = 1) e `(1,−1)` (λ = −1). Logo:

```
(1, 1)   → λ = 1 − 0,3 = 0,7
(1, −1)  → λ = 1 + 0,3 = 1,3
(0,0,1)  → λ = 1,3
```

**Passo 3 — testar cada alternativa: calcule M·v e veja se sai um múltiplo de v.**

```
(a) v = (1,−1,0):   M·v = 1,3·(1,−1,0)      ✔  λ = 1,3
(b) v = (0, 0,1):   M·v = 1,3·(0,0,1)       ✔  λ = 1,3
(c) v = (1,−1,1):   M·v = 1,3·(1,−1,1)      ✔  λ = 1,3
(d) v = (1, 1,0):   M·v = 0,7·(1,1,0)       ✔  λ = 0,7
(e) v = (1, 1,1):   M·v = (0,7 , 0,7 , 1,3) ✘  não é múltiplo de (1,1,1)
```

Em (e), as duas primeiras coordenadas pediriam λ = 0,7 e a terceira pediria λ = 1,3 — não existe um λ
único.

**Resposta: (e).**

**Por que (c) funciona e (e) não?** Em (c) as duas primeiras coordenadas estão no autovetor `(1,−1)`
(λ = 1,3) **e** a terceira também tem λ = 1,3 → tudo se alinha. Em (e) as duas primeiras estão em `(1,1)`
(λ = 0,7), mas a terceira insiste em λ = 1,3 → autovetor "misturado", que não existe.

**Armadilha.** Quem só verifica "M·v tem as mesmas coordenadas?" erra; a condição é **paralelismo**,
`M·v = λ·v` com o **mesmo** λ em todas as coordenadas não nulas.

**Padrão.** Matriz bloco-diagonal: os autovalores são a união dos espectros dos blocos; autovetor é
autovetor de **um** bloco estendido com zeros nos demais — nunca uma "mistura" de autovetores de blocos
diferentes.

---

### Q7 · Esferas empilhadas na pirâmide — **(d) 91**

**Enunciado.** Quantas esferas iguais formam uma pirâmide de base quadrada com **seis** esferas em cada
aresta da base?
(a) 48 · (b) 56 · (c) 72 · (d) 91 · (e) 96

**Modelar.** O empilhamento de esferas iguais forma camadas quadradas: a base tem `6×6`, a camada seguinte
`5×5` (as esferas se acomodam nas "covas" da de baixo), e assim por diante até `1×1`:

```
camada 1 (base): 6² = 36
camada 2:        5² = 25
camada 3:        4² = 16
camada 4:        3² =  9
camada 5:        2² =  4
camada 6 (topo): 1² =  1
```

**Somar.**

```
Σ_{k=1}^{6} k² = 6·7·13/6 = 91
```

**Resposta: (d) 91 esferas.**

**Conferência.** 36 + 25 = 61; +16 = 77; +9 = 86; +4 = 90; +1 = 91 ✔.

**Por que as outras caem.** (b) 56 = `36 + 16 + 4` — soma só das camadas de mesma paridade (quem "pula"
camadas); (a) 48, (c) 72 e (e) 96 vêm de contar menos camadas que o necessário ou de tratar o empilhamento
como um prisma de esferas. O teste rápido: a pirâmide **tem** que ter 6 camadas, e a menor delas tem 1
esfera.

**Padrão.** Pirâmide de base quadrada com n esferas por aresta → `Σ_{k=1}^{n} k² = n(n+1)(2n+1)/6`.
Guarde também `Σk³` para pirâmides cúbicas.

---

### Q8 · Valor de i^i — **(c)**

**Enunciado.** Se `i = √−1`, então `i^i` vale:
(a) 1 · (b) −1 · (c) exp(−π/2 + 2kπ), k ∈ ℤ · (d) i + 1 · (e) sinh(−1)

**Passo 1 — escrever i na forma exponencial.** `i = e^{i(π/2 + 2kπ)}`, k ∈ ℤ.

**Passo 2 — usar a definição `a^b = e^{b·ln a}`.**

```
i^i = e^{i·ln i} = e^{i·i(π/2 + 2kπ)} = e^{−(π/2 + 2kπ)} = e^{−π/2 − 2kπ}
```

Como k percorre **todos** os inteiros, `−2kπ` e `+2kπ` descrevem o mesmo conjunto:

```
i^i = exp(−π/2 + 2kπ),   k ∈ ℤ
```

**Resposta: (c).**

**Conferência numérica.** Valor principal (k = 0): `e^{−π/2} ≈ 0,2079`. Note que **i^i é real** — o
resultado surpreende, mas é real e positivo.

**Por que as outras caem.** (a) 1 e (b) −1 esqueceram o logaritmo complexo (acharam que `i^i = 1` porque
"i·i = −1" ou que "a potência de i é ±1"); (d) i + 1 mistura módulo e fase; (e) `sinh(−1) ≈ −1,175` é
apenas um número parecido em "cara", sem relação (a armadilha é que o valor principal é pequeno e a banca
coloca outro valor pequeno).

**Padrão.** `a^b = e^{b ln a}` com `ln a` **multivalente** (`= ln|a| + i(arg a + 2kπ)`). SEMPRE escreva a
base na forma polar antes de elevar a expoente complexo.

---

### Q9 · Identidades hiperbólicas: quantas são verdadeiras — **(d)**

**Enunciado.** Julgue as afirmações:
1. `sinh(a+b) = sinh(a)cosh(b) + sinh(b)cosh(a)`
2. `cosh(a+b) = cosh(a)cosh(b) − sinh(b)sinh(a)`
3. `sinh(3a) = 3sinh(a)cosh²(a) + sinh³(a)`
4. `cosh(3a) = 3sinh²(a)cosh(a) + cosh³(a)`

**Passo 1 — afirmação 1: VERDADEIRA.** É a fórmula de adição do seno hiperbólico, análoga a
`sin(a+b) = sin a cos b + sin b cos a`.

**Passo 2 — afirmação 2: FALSA.** A fórmula correta é

```
cosh(a+b) = cosh(a)cosh(b) + sinh(a)sinh(b)        (SINAL +, não −)
```

Comparação numérica em a = 1,1, b = 0,4: `cosh(1,5) ≈ 2,3524`; com `+` dá 2,3524 ✔; com `−` dá 1,2552 ✗.
É o "cosseno da soma" imitando o cosseno trigonométrico (que tem o **−**).

**Passo 3 — afirmação 3: VERDADEIRA.**

```
3 sinh a cosh²a + sinh³a = 3 sinh a(1 + sinh²a) + sinh³a
                        = 3 sinh a + 3 sinh³a + sinh³a
                        = 3 sinh a + 4 sinh³a = sinh(3a)   ✔
```

**Passo 4 — afirmação 4: VERDADEIRA.**

```
3 sinh²a cosh a + cosh³a = cosh a(3 sinh²a + cosh²a)
                        = cosh a(3 sinh²a + 1 + sinh²a)
                        = cosh a(1 + 4 sinh²a) = 4cosh³a − 3cosh a = cosh(3a)  ✔
```

(usando `cosh² = 1 + sinh²` e depois `sinh² = cosh² − 1`).

**Resposta: (d)** — há **exatamente uma** afirmação falsa (a 2).

**Por que as outras caem.** (e) "todas verdadeiras" é a armadilha-mãe: quem acha o `−` "natural" (por
analogia com `cos(a+b)`) marca (e). (c) "duas corretas" seria o caso se você errasse também a 3 ou a 4.
(b) e (a) exigiriam erros grosseiros.

**Padrão.** As fórmulas hiperbólicas são as trigonométricas com **trocas de sinal** sistemáticas:
`sinh` "imita" `sin`; `cosh(a+b)` tem **+**; `cosh(2a) = cosh²a + sinh²a`; `cosh² − sinh² = 1`
(enquanto `cos² + sin² = 1`). A banca explora justamente esses sinais.

---

### Q10 · Sequência complexa (De Moivre) — **(b)**

**Enunciado.**
```
A_n = (1/(√3 i)) · [ ((1 + √3 i)/2)^n − ((1 − √3 i)/2)^n ],   n ∈ ℕ
```
A sequência é composta de:
(a) naturais (todos ≥ 0) · (b) inteiros (alguns negativos) · (c) racionais (alguns não inteiros) ·
(d) reais (alguns irracionais) · (e) complexos (alguns não reais)

**Passo 1 — reconhecer números complexos unitários.**

```
(1 ± √3 i)/2 = cos(±60°) + i·sin(±60°) = e^{±iπ/3}
```

**Passo 2 — De Moivre.**

```
((1+√3i)/2)^n = e^{inπ/3}        ((1−√3i)/2)^n = e^{−inπ/3}
```

**Passo 3 — a diferença é `2i·sin`.**

```
e^{inπ/3} − e^{−inπ/3} = 2i·sin(nπ/3)
A_n = (1/(√3 i))·2i·sin(nπ/3) = (2/√3)·sin(nπ/3)
```

**Passo 4 — quais valores `sin(nπ/3)` assume para n inteiro?** `nπ/3` é múltiplo de 60°, então

```
sin(nπ/3) ∈ { 0, ±√3/2 }        (nunca ±1: ±90° não é múltiplo de 60°)
```

Logo

```
A_n ∈ { 0, +1, −1 }
```

**Resposta: (b)** — são **inteiros**, e alguns são **negativos** (n = 4, 5, 10, 11, ...).

**Conferência (primeiros termos).**

```
n:     0   1   2   3   4   5   6   7   8   9   10  11
A_n:   0   1   1   0  −1  −1   0   1   1   0  −1  −1
```

**Por que as outras caem.** (a) falha em n = 4 (dá −1); (c) falha porque **todos** são inteiros; (d) falha
porque `2/√3` (o valor irracional) **nunca** aparece, já que o seno nunca vale ±1 nesses ângulos — é a
distratora mais sedutora, porque o coeficiente `2/√3` é irracional e a pessoa "vê" irracional na fórmula;
(e) falha porque a parte imaginária sempre cancela.

**Padrão.** Expressões `[(a+bi)^n − (a−bi)^n]` com `a² + b² = 1` são sempre `2i·sin(nθ)` (e as com `+` são
`2cos(nθ)`). Reconhecer isso transforma a questão em trigonometria de ângulos notáveis.

---

### Q11 · Ordenar logaritmos — **(e) r < p < q**

**Enunciado.** `p = log₃2`, `q = log_{√3}4`, `r = log_{1/3}√2`. Ordem correta:
(a) p < q < r · (b) r < q < p · (c) q < r < p · (d) p < r < q · (e) r < p < q

**Passo 1 — reduzir tudo à base 3 e a p.** Use `log_a b = log_c b / log_c a`:

```
q = log_{√3}4 = log₃4 / log₃√3 = (2log₃2)/(1/2) = 4·log₃2 = 4p
r = log_{1/3}√2 = (1/2·log₃2)/log₃(1/3) = (p/2)/(−1) = −p/2
```

```
p = p          q = 4p          r = −p/2
```

**Passo 2 — sinal.** `p = log₃2 > 0` (porque 2 > 1). Então

```
r = −p/2 < 0 < p < 4p = q        →        r < p < q
```

**Resposta: (e).**

**Conferência numérica.** p ≈ 0,6309; q ≈ 2,5237; r ≈ −0,3155 ✔.

**Armadilha.** `log_{1/3}` tem base **menor que 1** → inverte o sinal: quem "ignora" a base fracionária
acha r positivo e escolhe uma ordem errada (tipicamente (a) p < q < r ou (d) p < r < q). Outra armadilha é
tratar `log_{√3}` como se fosse `log₃` (dá q = 2p em vez de 4p).

**Padrão.** Comparar logaritmos: reduza a **uma base** e compare os coeficientes; cuide do sinal quando a
base está entre 0 e 1.

---

### Q12 · Simplificar a expressão trigonométrica — **(e) cot²x**

**Enunciado.** Simplifique `(cos²x − cot x)/(sin²x − tan x)`:
(a) sec²x · (b) sin²x · (c) tan²x · (d) cos²x · (e) cot²x

**Passo 1 — abrir cot e tan.**

```
cos²x − cot x = cos²x − cos x/sin x = [cos²x·sin x − cos x]/sin x = cos x(cos x sin x − 1)/sin x
sin²x − tan x = sin²x − sin x/cos x = [sin²x·cos x − sin x]/cos x = sin x(sin x cos x − 1)/cos x
```

**Passo 2 — dividir e cancelar o fator comum `(sin x cos x − 1)`.**

```
cos²x − cot x     cos x(cos x sin x − 1)/sin x        cos²x
─────────────  =  ─────────────────────────────  =  ───────  = cot²x
sin²x − tan x     sin x(sin x cos x − 1)/cos x        sin²x
```

**Resposta: (e) cot²x.**

**Conferência em x = 45°.** `cos² = 1/2`, `cot = 1` → numerador `−1/2`; `sin² = 1/2`, `tan = 1` →
denominador `−1/2`; razão 1 = cot²45° ✔.

**Observação de domínio.** `sin x cos x − 1 ≠ 0` sempre (pois `sin x cos x = (1/2)sin 2x ≤ 1/2`), então o
cancelamento é legítimo para todo x do domínio (sin x ≠ 0, cos x ≠ 0).

**Armadilha.** Quem troca `cot = sin/cos` (ou `tan = cos/sin`) obtém `tan²x` (alternativa c) ou `1`. Escreva
`cot = cos/sin` e `tan = sin/cos` **antes** de mexer na fração.

**Padrão.** Fracções com `cot`/`tan` e `sin²`/`cos²`: reduza tudo a seno e cosseno, fatore
`(sin x cos x − 1)` e cancele. Sobra sempre `cos²/sin²` ou `sin²/cos²`.

---

### Q13 · PG infinita com incógnita — **(e) nenhum dos valores**

**Enunciado.** Para que `2 + 4/m + 8/m² + ⋯ = 14/2` seja verdade, m deve ser:
(a) 5 · (b) 6 · (c) 7 · (d) 8 · (e) nenhum dos valores acima

**Passo 1 — identificar a PG.** Primeiro termo `a₁ = 2`; razão `q = (4/m)/2 = 2/m`.
Convergência: `|q| < 1 ⟺ m > 2` (com m > 0).

**Passo 2 — soma da PG infinita.**

```
S = a₁/(1 − q) = 2/(1 − 2/m) = 2m/(m − 2)
```

**Passo 3 — impor a igualdade.** `14/2 = 7`:

```
2m/(m − 2) = 7
2m = 7m − 14
5m = 14
m = 14/5 = 2,8
```

**Passo 4 — comparar com as alternativas.** `14/5 = 2,8 ∉ {5, 6, 7, 8}` → **(e)**.

**Resposta: (e)** — nenhum dos valores (a solução é m = 14/5 = 2,8).

**Conferência.** Para m = 2,8: `q = 2/2,8 ≈ 0,7143`; `S = 2/(1 − 0,7143) = 2/0,2857 = 7` ✔. E m > 2, então a
série converge ✔.

**Por que as outras caem.** A solução exata é `14/5` — **mesmo numerador** do lado direito —, e a banca
explorou isso: quem "cancela" o 14 e resolve de cabeça tende a marcar (c) 7 (para m = 7 a soma é
`14/5 = 2,8`, não 7). (a) 5, (b) 6 e (d) 8 dão somas 3,33; 3,00; 2,67 — todas bem longe de 7.

**Armadilha.** Ler `14/2` como `14` (a barra some na pressa) leva a `2m/(m−2) = 14 → m = 7/3`, ainda fora
das opções — mas quem lê `14/2 = 7` e faz a conta errada marca (c). Confira sempre a convergência (`m > 2`).

**Padrão.** PG infinita: `S = a₁/(1 − q)`, e **sempre** verifique `|q| < 1`. A resposta "nenhuma das
anteriores" costuma aparecer quando a incógnita cai fora do conjunto testado.

---

### Q14 · Equação com fatoriais — **(a) par**

**Enunciado.** A solução de `(n+2)!(n−2)! / [(n+1)!(n−1)!] = 4` é um natural que também é:
(a) par · (b) cubo perfeito · (c) maior que 10 · (d) divisível por 5 · (e) divisível por 3

**Passo 1 — simplificar os fatoriais.**

```
(n+2)!/(n+1)! = n + 2
(n−2)!/(n−1)! = 1/(n − 1)
```

Logo a equação vira

```
(n + 2)/(n − 1) = 4
```

**Passo 2 — resolver.** `n + 2 = 4(n − 1) → n + 2 = 4n − 4 → 3n = 6 → n = 2`.
(Domínio: `n ≥ 2` para `(n−2)!` existir; n = 2 é válido.)

**Passo 3 — conferir e classificar.** `(4!·0!)/(3!·1!) = 24/6 = 4` ✔. E **n = 2 é par** → (a).

**Resposta: (a) par.**

**Por que as outras caem.** 2 não é cubo perfeito (b), não é > 10 (c), não é divisível por 5 (d) nem por 3
(e). As alternativas (d) e (e) são tentações para quem chega a n = 4 (erro de sinal na hora de isolar n).

**Padrão.** Fatorial: **sempre** simplifique antes de expandir, usando `(k+1)!/k! = k+1` e
`(k−1)!/k! = 1/k`. Em 2024/2 isso resolveu em duas linhas.

---

### Q15 · Distância da reta à origem — **(c) 12/5**

**Enunciado.** Uma reta passa por (3, 0) e (0, 4). A distância dessa reta à origem é:
(a) 2 · (b) √5 · (c) 12/5 · (d) 5/2 · (e) 3

**Passo 1 — equação da reta.** Forma segmentária: `x/3 + y/4 = 1`; multiplicando por 12:

```
4x + 3y = 12      →      4x + 3y − 12 = 0
```

**Passo 2 — distância ponto–reta.** Para a origem (0,0) e a reta `ax + by + c = 0`:

```
d = |a·0 + b·0 + c| / √(a² + b²) = |−12|/√(16 + 9) = 12/5
```

**Resposta: (c) 12/5 (= 2,4).**

**Conferência.** A área do triângulo é `(3·4)/2 = 6`; com hipotenusa 5, `d = 2·área/hipotenusa = 12/5` ✔
(outro caminho, bom para conferir).

**Por que as outras caem.** (d) 5/2 = 2,5 é o "vizinho" perigoso: vem de calcular a **hipotenusa** 5 e
tomar a sua metade — o erro de quem troca a fórmula da distância pela "metade da hipotenusa"; (b) √5 ≈ 2,24,
(a) 2 e (e) 3 são chutes ou trocas na fórmula (usar `a + b` no lugar de `√(a²+b²)`, por exemplo).

**Padrão.** Distância da origem: `|c|/√(a²+b²)`. Alternativa geométrica: `d = 2·Área/base maior`
(hipotenusa). Confira sempre com a área.

---

### Q16 · Círculos tangentes e tangentes comuns — **(d)**

**Enunciado.** Na Figura 2, A, B, C são colineares; `AB = 9` é o diâmetro da semicircunferência de centro
O; `BC = 4` é o diâmetro da de centro O′. As semicircunferências são tangentes e `BD` e `MN` são as
tangentes comuns. Marque a opção **errada**:
(a) BD é altura do triângulo ODO′ · (b) BD é mediana do triângulo MBN ·
(c) o triângulo MBN é retângulo · (d) MN = 6,5 · (e) ODO′ e MBN são semelhantes

**Montar o modelo.** Ponha B na origem e a reta AC no eixo x:

```
O  = (−4,5; 0)      raio R = 4,5
O′ = ( 2,0 ; 0)     raio r = 2
OO′ = 6,5 = R + r   →  as circunferências são tangentes externas em B
```

`BD` é a tangente comum no ponto de tangência B → é **perpendicular a OO′** (portanto vertical).
`MN` é a outra tangente comum (externa), tocando a grande em M e a pequena em N; e **D = MN ∩ BD**.

**Passo 1 — tangentes de um mesmo ponto são iguais (a chave da questão).** De um ponto externo, as duas
tangentes a uma circunferência têm o **mesmo comprimento**:

```
do ponto D à circunferência grande:  DB = DM     (tangentes em B e M)
do ponto D à circunferência pequena: DB = DN     (tangentes em B e N)
                                   ⇒  DM = DN = DB
```

Consequência imediata: **D é o ponto médio de MN** e `DB = MN/2`.

**Passo 2 — medir MN (e DB).** A tangente comum **externa**, medida entre os pontos de tangência, é

```
MN = √( OO′² − (R − r)² ) = √( 6,5² − 2,5² ) = √(42,25 − 6,25) = √36 = 6
```

(Vem do triângulo retângulo formado pelos centros e pela paralela à tangente: cateto `R − r`, cateto `MN`,
hipotenusa `OO′`.) Logo `DB = MN/2 = 3`.

**Passo 3 — julgar (a), (b) e (c).**

- **(a) BD é altura de ODO′:** BD é perpendicular a OO′ (é a tangente no ponto de tangência B) e passa pelo
  vértice D, cortando OO′ em B → é a altura relativa ao lado OO′ ✔ **verdadeira**.
- **(b) BD é mediana de MBN:** D é o ponto médio de MN (Passo 1), e BD liga B a esse ponto médio →
  é mediana ✔ **verdadeira**.
- **(c) MBN é retângulo:** `DB = DM = DN` ⇒ M, B e N estão na circunferência de centro D e diâmetro MN ⇒
  `∠MBN` é reto (ângulo inscrito que "vê" o diâmetro) ✔ **verdadeira**.

**Passo 4 — julgar (e).** Primeiro, `∠ODO′ = 90°`: os triângulos retângulos ODB e ODM são congruentes
(hipotenusa OD comum, catetos OM = OB = R) → `OD` **bissecta** `MDB`; analogamente `O′D` **bissecta** `BDN`.
Como M, D, N são colineares, `∠MDB + ∠BDN = 180°` ⇒ `2∠BDO + 2∠BDO′ = 180°` ⇒ `∠ODO′ = 90°`.

Então ODO′ é retângulo em D, com catetos

```
OD  = √(4,5² + 3²) = √29,25 = 3√13/2        O′D = √(2² + 3²) = √13        ⇒  OD/O′D = 3/2
```

Do lado de MBN (reto em B): o triângulo `DBM` é isósceles (`DB = DM`), logo `∠BMN = 90° − β`, onde
`tan β = OB/BD = 4,5/3 = 3/2`. Assim

```
BN/MB = tan(∠BMN) = cot β = 2/3        ⇒        MB/BN = 3/2
```

Dois triângulos **retângulos** com catetos na mesma razão (3 : 2) são **semelhantes** (correspondência
O↔M, O′↔N, D↔B) ✔ **verdadeira**.

**Passo 5 — julgar (d).** `MN = 6`, e não `6,5` → **(d) é a FALSA** (6,5 é `OO′`, a distância entre os
centros).

**Resposta: (d)** — `MN = 6`.

**Passo 6 — checagem numérica (coordenadas).** A tangente externa é `y = −(5/12)x + 3`; ela toca a grande
em `M ≈ (−2,769; 4,154)` e a pequena em `N ≈ (2,769; 1,846)`. Aí `MN = 6`, `DM = DN = 3`, `D = (0,3)`,
`OD ≈ 5,408`, `O′D ≈ 3,606` — e todas as razões dão `13/12` ✔.

**Por que as outras caem.** (d) é a única falsa — e é a "traiçoeira", porque 6,5 aparece naturalmente na
conta (`OO′ = 4,5 + 2 = 6,5`). Quem confunde a **distância entre centros** com o **comprimento da tangente
comum** marca (d) como verdadeira e erra a questão.

**Padrão (cadeia de teoremas de tangência).** Em duas circunferências tangentes com tangente comum:
(1) **tangentes de um mesmo ponto são iguais** → D é ponto médio de MN e `DB = DM = DN`;
(2) daí **MBN é retângulo** e **BD é mediana/altura**;
(3) `MN = √(d² − (R−r)²)` para a tangente externa e `MN = √(d² − (R+r)²)` para a interna.
Essa cadeia resolve 90% das questões de tangência.

---

## 4. Padrões que a banca repetiu nesta prova

1. **Quatro questões de "qual é a errada"** (Q2, Q6, Q9, Q16). Nesta prova, o comando é o teste principal:
   em Q2 o erro é de sinal na derivada; em Q6 é o vetor "misturado"; em Q9 é o sinal do `cosh(a+b)`;
   em Q16 é confundir `OO′` com `MN`. **Sempre sublinhe o comando antes de resolver.**
2. **Identidades com sinal trocado** (Q9, Q12, Q2): a banca constrói a alternativa errada a partir do erro
   clássico (derivar `ln(1/x)` sem o `−`, trocar `cot = sin/cos`, pôr `−` no `cosh`).
3. **Simetria** (Q5): `s = x+y`, `p = xy` derruba o grau do sistema.
4. **Estrutura antes da conta** (Q6 bloco-diagonal; Q12 fator comum `sin x cos x − 1`; Q14 fatoriais que
   simplificam).
5. **Contagem em grafo** (Q4): trilha de comprimento 5 em K₄ = "omitir uma aresta" + Euler.
6. **Números complexos em três sabores** (Q8 potência complexa, Q10 De Moivre + seno, Q11 logaritmos):
   sempre passe para a forma polar/exponencial.
7. **Cadeia de tangência** (Q16): tangentes iguais → ponto médio → ângulo reto → semelhança; e a fórmula
   `√(d² − (R−r)²)`.

---

## 5. Plano de 90 minutos

| Bloco | Tempo | Questões | Objetivo |
|:-----:|:-----:|----------|----------|
| 1 | 0–15 min | 7, 15, 14, 11, 1, 8 | as 6 "de ritmo": 6 acertos rápidos |
| 2 | 15–35 min | 5, 6, 12, 13, 9 | médias; aqui você já passa do corte |
| 3 | 35–70 min | 2, 3, 10, 4, 16 | as longas (16 é a mais caras: 6 min) |
| 4 | 70–90 min | todas | reler comandos ("wrong", "cannot say") e conferir |

Regra de bolso: **3 minutos travado → marque a melhor aposta e siga**. Nesta prova, Q4 e Q16 valem o mesmo
que Q7 e Q15.

---

## 6. Checklist final

- [ ] Releu o comando? "wrong", "cannot say", "not an eigenvector", "none of the above".
- [ ] Derivou `ln(1/x)`, `cot`, `tan` com o sinal certo?
- [ ] Em identidades hiperbólicas, conferiu o sinal (`cosh(a+b)` tem **+**)?
- [ ] Em PG infinita, verificou `|q| < 1` e leu a fração do lado direito corretamente?
- [ ] Em tangência, distinguiu **distância entre centros** de **comprimento da tangente comum**?
- [ ] Em contagem em grafo, checou se o caminho é trilha (sem repetir aresta) e se a ordem importa?

---

## 7. Resumo de fórmulas usadas

```
Taxa com entrada e saída:   1/t = 1/t_saída − 1/t_entrada
Torricelli (f″ = a):        (f′(x₁))² = (f′(x₀))² + 2a[f(x₁) − f(x₀)]
Sistema simétrico:          x²−xy+y² = s²−3p ;  x³+y³ = s³−3ps
Trilha de Euler:            existe entre os dois vértices de grau ímpar
Bloco diagonal:             espectro = união dos espectros; autovetor = um bloco por vez
Soma de quadrados:          Σ_{k=1}^{n} k² = n(n+1)(2n+1)/6
Potência complexa:          i^i = exp(−π/2 + 2kπ), k ∈ ℤ
Hiperbólicas:               sinh3a = 3sinh a + 4sinh³a ; cosh3a = 4cosh³a − 3cosh a
De Moivre:                  [(a+bi)^n − (a−bi)^n] = 2i·sin(nθ), se a²+b² = 1
Mudança de base:            log_a b = log_c b / log_c a
PG infinita:                S = a₁/(1 − q), |q| < 1
Distância ponto–reta:       d = |ax₀ + by₀ + c| / √(a² + b²)
Tangente comum externa:     MN = √(d² − (R − r)²)  ·  tangentes de um ponto são iguais
```

---

## 8. Onde treinar cada questão

| Questão | Tema no repositório |
|:-------:|---------------------|
| 1, 13 | [`temas/10-problemas-taxa-trabalho`](../../temas/10-problemas-taxa-trabalho/README.md) · [`temas/06-sequencias-pa-pg-series`](../../temas/06-sequencias-pa-pg-series/README.md) |
| 2, 3 | [`temas/08-calculo`](../../temas/08-calculo/README.md) |
| 4, 7, 14 | [`temas/01-combinatoria`](../../temas/01-combinatoria/README.md) |
| 5, 6 | [`temas/02-sistemas-matrizes-determinantes`](../../temas/02-sistemas-matrizes-determinantes/README.md) |
| 8, 10 | [`temas/09-numeros-complexos`](../../temas/09-numeros-complexos/README.md) |
| 9 | [`temas/07-trigonometria`](../../temas/07-trigonometria/README.md) |
| 11 | [`temas/04-funcoes-log-exp`](../../temas/04-funcoes-log-exp/README.md) |
| 12 | [`temas/07-trigonometria`](../../temas/07-trigonometria/README.md) |
| 15, 16 | [`temas/03-geometria`](../../temas/03-geometria/README.md) |

> Em cada tema, o arquivo **`RESOLUCOES-PASSO-A-PASSO.md`** traz a resolução linha a linha das questões
> reais daquele assunto (1º e 2º semestres) — é o complemento natural desta leitura por prova.

---

**Prova original:** [`Prova_PG-EIA_2024-2oSem.pdf`](../Prova_PG-EIA_2024-2oSem.pdf) ·
**Texto extraído:** [`Prova_PG-EIA_2024-2oSem.txt`](../Prova_PG-EIA_2024-2oSem.txt) ·
**Índice de resoluções:** [`README.md`](README.md) · **Provas:** [`../README.md`](../README.md).
