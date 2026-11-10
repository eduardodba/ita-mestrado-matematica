# Resolução comentada — Matemática · 2022 / 2º semestre (PG-EIA · ITA)

**Prova:** [`../Prova_PG-EIA_2022-2oSem.pdf`](../Prova_PG-EIA_2022-2oSem.pdf) — aplicada em **16 de maio de 2022**.
**Formato:** 16 questões de múltipla escolha (a–e), enunciados em inglês, **90 minutos**, sem calculadora.
**Gabarito oficial:** `1-c 2-e 3-a 4-d 5-c 6-b 7-e 8-a 9-e 10-b 11-d 12-a 13-e 14-a 15-c&d (anulada) 16-e`.

> **O que este arquivo entrega.** As **16 questões resolvidas passo a passo**: diagnóstico, conta completa,
> por que a alternativa correta é correta, **por que as outras caem**, armadilhas e o padrão da banca.
> Esta prova tem **gabarito oficial** (ao fim do arquivo `.txt`, incluindo a errata da Q15).

> **Sobre o nome.** É a prova de Matemática do processo seletivo do PG-EIA/ITA, múltipla escolha estilo
> GMAT — a "prova de GMAT/GMATE" do 2º semestre de 2022. No repositório, o PDF é o
> `Prova_PG-EIA_2022-2oSem.pdf`.

**Recado rápido:** prova de **muitas questões de 1 minuto** (Q4, Q10, Q12, Q14, Q16) intercaladas com
duas armadilhas de leitura (Q3 e Q15). A Q15 é **anulada**: duas alternativas (c e d) são verdadeiras.

---

## 1. Gabarito relâmpago

| Questão | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 | 13 | 14 | 15 | 16 |
|:-------:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
| **Resposta** | **c** | **e** | **a** | **d** | **c** | **b** | **e** | **a** | **e** | **b** | **d** | **a** | **e** | **a** | **c & d**\* | **e** |

\* Q15 é **anulada**: (c) e (d) são ambas verdadeiras. O gabarito oficial marcou (e), e a própria folha de
respostas traz a errata "errado, respostas corretas: c & d".

---

## 2. Raio-X da prova

| # | Assunto | Resp. | Nível | Tempo-alvo |
|:-:|---------|:-----:|:-----:|:----------:|
| 1 | Coeficiente de x⁴ em (1+x)(1−x)ⁿ | c | médio | 3 min |
| 2 | Triângulo equilátero inscrito em isósceles | e | difícil | 5 min |
| 3 | Três reservatórios com vazões (achar a errada) | a | médio | 4 min |
| 4 | Raiz comum com x²−5x+4 = 0 | d | fácil | 1 min |
| 5 | Sistema com y² e z³: nº de soluções | c | médio | 2,5 min |
| 6 | Suficiência: eventos independentes (Euler) | b | difícil | 5 min |
| 7 | Qual matriz tem determinante 1 | e | médio | 3 min |
| 8 | Suficiência: aluguel de carro (tabela) | a | médio | 3 min |
| 9 | Derivadas de arcsin/arccos/arctan | e | fácil | 2 min |
| 10 | Preço de garrafas (proporção) | b | fácil | 1 min |
| 11 | Equação logarítmica | d | médio | 3 min |
| 12 | Trabalho conjunto (Alice e Bob) | a | fácil | 1 min |
| 13 | Ângulos notáveis (15°, 105°) | e | fácil | 2 min |
| 14 | Encontro de caminhantes | a | fácil | 1,5 min |
| 15 | Convergência de cos^{n+1}(nθ) | c&d | difícil | 4 min |
| 16 | Área do tapete (moldura) | e | fácil | 1 min |

**Leitura estratégica.** Sete questões resolvem em ≤ 2 min (4, 9, 10, 12, 13, 14, 16) = 7 acertos.
As caras são Q2 (rasteira de ângulos), Q6 (independência com duas incógnitas) e Q15 (sequência
trigonométrica). Soma dos tempos-alvo: **~43 min** — sobra tempo; use-o para reler Q3 e Q15.

---

## 3. Resoluções

### Q1 · Coeficiente de x⁴ — **(c) n(n−1)(n−2)(n−7)/24**

**Enunciado.** O coeficiente de x⁴ obtido ao expandir e somar `(1+x)(1−x)ⁿ` é:
(a) (n−1)(n−2)(n−3)(n−4)/12 · (b) n(n−1)(n−2)(n−4)/24 · (c) n(n−1)(n−2)(n−7)/24 ·
(d) n(n−1)(n−2)(n−5)/24 · (e) n(n−1)(n−2)(n−5)/120

**Passo 1 — quem contribui para x⁴.** Em `(1+x)·P(x)`, o coeficiente de x⁴ é
`[x⁴]P + [x³]P`. Com `P = (1−x)ⁿ`:

```
P = Σ_k C(n,k)(−1)^k x^k
[x⁴]P = C(n,4)(−1)⁴ = C(n,4)
[x³]P = C(n,3)(−1)³ = −C(n,3)
```

**Passo 2 — somar.**

```
coef = C(n,4) − C(n,3) = n(n−1)(n−2)(n−3)/4! − n(n−1)(n−2)/3!
     = n(n−1)(n−2)[(n−3) − 4]/24
     = n(n−1)(n−2)(n−7)/24
```

**Resposta: (c).**

**Conferência numérica.** n = 5: `(1+x)(1−x)⁵` → coeficiente de x⁴ = −5; fórmula: `5·4·3·(−2)/24 = −5` ✔.
n = 8: fórmula `8·7·6·1/24 = 14`; expansão direta dá 14 ✔.

**Por que as outras caem.** (b) e (d) trocam o "−4" do denominador por outra conta (esquecem que
`C(n,3) = n(n−1)(n−2)/6` tem 6, não 24); (a) é o produto dos quatro últimos fatores (sem o n);
(e) divide por 120 (`5!`), como se fosse `C(n,5)`.

**Padrão.** Coeficiente em produto de dois polinômios: some os produtos dos coeficientes que "casam" nos
graus. E `C(n,4) − C(n,3)` sempre cai numa forma fatorada com `(n−7)` — sinal de que a conta está certa.

---

### Q2 · Equilátero inscrito no isósceles — **(e) nenhuma das relações**

**Enunciado.** Na Figura 1, `CA = CB` (ABC isósceles) e o triângulo equilátero DEF está inscrito, com
D sobre CA, E sobre CB e F sobre AB. Sendo `a = ∠CDE`, `b = ∠FEB` e `c = ∠AFD`:
(a) a = (c+b)/2 · (b) a = (c−b)/2 · (c) c = (a−b)/2 · (d) c = (a−b)/b · (e) nenhuma dessas

**O desenho (esquemático).**

```
          C
         / \
        D---E        DEF é equilátero (∠D = ∠E = ∠F = 60°)
       / \ / \
      A---F---B      CA = CB (isósceles)
```

Seja `β = ∠A = ∠B` (base do isósceles); então `∠C = 180° − 2β`.

**Passo 1 — triângulo CDE.** `∠DCE = ∠ACB = 180° − 2β` e `∠CDE = a`, logo

```
∠CED = 180° − (180° − 2β) − a = 2β − a
```

**Passo 2 — no vértice E.** `EC` e `EB` são raios opostos, então

```
∠DEB = 180° − ∠CED = 180° − 2β + a
```

E, como `EF` está entre `ED` e `EB` e `∠DEF = 60°`:

```
∠DEB = ∠DEF + ∠FEB = 60° + b
⇒ 180° − 2β + a = 60° + b   ⇒   a − b = 2β − 120°        (I)
```

**Passo 3 — no vértice D.** `DC` e `DA` são opostos, e `DF` está entre `DE` e `DA`:

```
∠CDA = 180° = a + ∠FDE + ∠ADF = a + 60° + ∠ADF
⇒ ∠ADF = 120° − a
```

No triângulo ADF: `∠DAF = β` e `∠AFD = c` ⇒ `∠ADF = 180° − β − c`. Igualando:

```
120° − a = 180° − β − c     ⇒     a − c = β − 60°        (II)
```

**Passo 4 — eliminar β.** De (I): `β − 60° = (a − b)/2`. Substituindo em (II):

```
a − c = (a − b)/2
2a − 2c = a − b
a + b = 2c        ⇒        c = (a + b)/2
```

**Passo 5 — comparar com as alternativas.** A relação verdadeira é `c = (a+b)/2`, que **não** está entre
(a), (b), (c) nem (d) → **(e) nenhuma dessas**.

**Resposta: (e).**

**Conferência numérica.** Com β = 50° (por exemplo), as relações dão `a = b − 20°` e `c = b − 10°`, ou
seja, `c = (a+b)/2` ✔ — e nenhuma das alternativas se verifica para todo b.

**Armadilha.** As alternativas (a) e (b) têm a "cara" da relação `c = (a+b)/2` com os papéis de a e c
trocados — é o erro de quem monta a cadeia de ângulos no sentido errado (por exemplo, confundir `∠CDE`
com `∠EDA`).

**Padrão.** Ângulos num vértice com três retas: escreva as somas de 180° com cuidado e **nomeie** cada
ângulo auxiliar. Depois elimine o parâmetro (aqui β). O resultado "bonito" costuma ser a média dos outros
dois.

---

### Q3 · Três reservatórios: qual afirmação é errada — **(a)**

**Enunciado.** A: 180 L, vazão 3 L/s. B: 100 L, vazão 2 L/s. C: 200 L, capacidade 250 L, vazão 4 L/s;
C recebe o que sai de A e B; se transbordar, o excesso é descartado. Marque a **errada**:
(a) C enche em 1 min 40 s · (b) C esvazia em 2 min · (c) C nunca transborda · (d) A esvazia em 60 s ·
(e) B esvazia em 50 s

**Passo 1 — linha do tempo das vazões.** Enquanto A e B têm água, entram em C `3 + 2 = 5 L/s`; C perde
4 L/s → **saldo +1 L/s**. Quando B esvazia (em `100/2 = 50 s`), entra só 3 L/s → saldo **−1 L/s**. Quando
A esvazia (em `180/3 = 60 s`), não entra nada → saldo **−4 L/s**.

**Passo 2 — fases.**

```
Fase 1  (0 → 50 s):   C: 200 + 1·t          →  C(50) = 250 L  (cheio)
Fase 2  (50 → 60 s):  C: 250 − 1·(t−50)     →  C(60) = 240 L
Fase 3  (t ≥ 60 s):   C: 240 − 4·(t−60)     →  C = 0 em t = 120 s
```

**Passo 3 — julgar cada item.**

- **(a)** "C enche em 1 min 40 s" = 100 s → **FALSO**: ele fica cheio em **50 s**.
- **(b)** C esvazia em 2 min = 120 s ✔ **verdadeira**.
- **(c)** C chega **exatamente** a 250 L em t = 50 s e depois só cai — **nunca ultrapassa**, logo não
  transborda ✔ **verdadeira**.
- **(d)** A: `180/3 = 60 s` ✔ **verdadeira**.
- **(e)** B: `100/2 = 50 s` ✔ **verdadeira**.

**Resposta: (a).**

**Conferência (simulação).** Simulando em passos de 1 ms: cheio em t ≈ 50,0 s e vazio em t ≈ 120,0 s ✔.

**Armadilha.** (a) é calculada com a vazão **inicial** de C "errada": `200 → 250` com saldo +2 L/s (usando
6 L/s de entrada) daria 25 s; com saldo +1 dá 50 s; 100 s é o valor de quem usa saldo +0,5 L/s (esquecendo
que B para em 50 s). Note que (c) é verdadeira **por pouco**: C atinge o teto mas não o ultrapassa.

**Padrão.** Problemas com vazões que mudam: **monte a linha do tempo** das mudanças (quando cada
reservatório esvazia) e resolva por fases. Sempre verifique se o "cheio na capacidade" ocorre antes da
mudança de fase.

---

### Q4 · Raiz comum — **(d) 3x² − 3 = 0**

**Enunciado.** Qual equação tem raiz em comum com `x² − 5x + 4 = 0`?
(a) x²+1=0 · (b) x²−x−2=0 · (c) x²−10x−5=0 · (d) 3x²−3=0 · (e) x²−2x−3=0

**Passo 1 — raízes da referência.** `x² − 5x + 4 = (x−1)(x−4)` → raízes **1 e 4**.

**Passo 2 — testar as opções pelas raízes.**

- (a) `x² + 1 = 0` → `±i` (não reais) ✘.
- (b) `x² − x − 2 = (x−2)(x+1)` → 2, −1 ✘.
- (c) `x² − 10x − 5 = 0` → `5 ± √30` ✘ (irracionais).
- (d) `3x² − 3 = 0` → `x² = 1` → **x = 1** ✔ (raiz comum!).
- (e) `x² − 2x − 3 = (x−3)(x+1)` → 3, −1 ✘.

**Resposta: (d).**

**Conferência.** `x = 1`: `3(1) − 3 = 0` ✔ e `1 − 5 + 4 = 0` ✔.

**Armadilha.** (b) e (e) têm aparência "fatorável" e tentam quem não calcula as raízes; (c) parece ter
raízes "quase 1" (dá ≈ −0,48 e 10,48).

**Padrão.** "Raiz comum" resolve-se **achando as raízes** e testando; não expanda nem divida polinômios.

---

### Q5 · Sistema com y² e z³ — **(c) 2 soluções**

**Enunciado.** `x − y² + z³ = −2` (1); `x + y² − z³ = 8` (2); `x − y² − z³ = 0` (3). Quantos conjuntos
de raízes reais para (x, y, z)?
(a) 6 · (b) 3 · (c) 2 · (d) 1 · (e) nenhum

**Passo 1 — trocar variáveis.** `u = y²` (u ≥ 0) e `v = z³`:

```
(1) x − u + v = −2
(2) x + u − v = 8
(3) x − u − v = 0
```

**Passo 2 — eliminar.** `(1) − (3)`: `2v = −2 → v = −1`.
`(1) + (3)`: `2x − 2u = −2 → x − u = −1`.
Em (2): `x + u − (−1) = 8 → x + u = 7`.

**Passo 3 — resolver.** `x − u = −1` e `x + u = 7` → **x = 3**, **u = 4**.

**Passo 4 — voltar.** `u = y² = 4 → y = ±2`; `v = z³ = −1 → z = −1` (única raiz real).

```
(3, 2, −1)   e   (3, −2, −1)     →  2 conjuntos
```

**Resposta: (c) 2 soluções.**

**Conferência.** (3, 2, −1): `3 − 4 − 1 = −2` ✔; `3 + 4 + 1 = 8` ✔; `3 − 4 + 1 = 0` ✔.

**Armadilha.** (a) 6 = 2 (sinais de y) × 3 (raízes de z³ = −1, contando complexas) — mas o problema pede
**reais**. (d) 1 é de quem esquece o `±` do y².

**Padrão.** Sistema com potências pares/ímpares: substitua `u = y²`, `v = z³` e conte as raízes reais de
cada uma no fim. `y² = k > 0` dá **duas** soluções; `z³ = k` dá **uma**.

---

### Q6 · Independência estatística no diagrama — **(b) x determinado, y não**

**Enunciado.** A e B independentes; no diagrama de Euler, só A = x, A∩B = x²y, só B = y, e fora de A∪B = 1,
com `x·y ≠ 0`. O que se pode afirmar?
(a) x e y determinados · (b) x determinado, y não · (c) y determinado, x não · (d) nenhum, mas há relação ·
(e) nenhum e nenhuma relação

**Passo 1 — contar os conjuntos.**

```
|A| = x + x²y        |B| = y + x²y        |A∩B| = x²y
|U| = x + x²y + y + 1
```

**Passo 2 — impor independência.** `P(A∩B) = P(A)P(B)` ⟺ `|A∩B|·|U| = |A|·|B|`:

```
x²y·(x + x²y + y + 1) = (x + x²y)(x²y + y)
```

**Passo 3 — expandir e cancelar.** Esquerda:

```
x³y + x⁴y² + x²y² + x²y
```

Direita:

```
(x + x²y)(y + x²y) = xy + x³y + x²y² + x⁴y²
```

Igualando e cortando os termos comuns (`x³y`, `x⁴y²`, `x²y²`):

```
x²y = xy   ⇒   xy(x − 1) = 0   ⇒   x = 1     (pois xy ≠ 0)
```

**Passo 4 — interpretar.** A independência **força x = 1** (determinado!), mas **não impõe nada sobre y**
— qualquer y ≠ 0 serve. Logo x é determinável e y não.

**Resposta: (b).**

**Conferência.** Com x = 1 e y = 2: |A| = 1+2 = 3; |B| = 2+2 = 4; |A∩B| = 2; |U| = 1+2+2+1 = 6.
`P(A∩B) = 1/3` e `P(A)P(B) = (1/2)(2/3) = 1/3` ✔ independentes. Com y = 5: |A| = 6, |B| = 10, |A∩B| = 5,
|U| = 12 → 5/12 = (6/12)(10/12) ✔ — y livre.

**Armadilha.** (a) "ambos determinados" é o chute natural; (d) e (e) são para quem desiste da álgebra. O
ponto é que a equação **colapsa** (todos os termos de grau misto se cancelam), sobrando só `x²y = xy`.

**Padrão.** Independência em diagramas: use `#(A∩B)·|U| = #A·#B`, expanda e **cancele** — normalmente
sobra uma equação simples que fixa uma variável e deixa a outra livre.

---

### Q7 · Qual matriz tem determinante 1 — **(e) nenhuma**

**Enunciado.** Qual das matrizes tem determinante igual a 1? (a), (b), (c), (d) ou (e) nenhuma.

**Passo 1 — (a).**

```
det = (√2/2)(−√2/2) − (√2/2)(√2/2) = −1/2 − 1/2 = −1
```

**Passo 2 — (b).** Matriz antidiagonal `[[0, u],[v, 0]]` → `det = −uv`:

```
u = √2/2 − (√2/2)i,   v = √2/2 + (√2/2)i   ⇒   uv = (1/2) + (1/2) = 1
det = −1
```

**Passo 3 — (c).**

```
a = (√2/2)i,  d = −(√2/2)i  ⇒  ad = 1/2
b = −√2/4 − (√2/4)i,  c = −b  ⇒  bc = −b²,  b² = (1/8)(1+i)² = i/4  ⇒  bc = −i/4
det = ad − bc = 1/2 + i/4 ≠ 1
```

**Passo 4 — (d).**

```
det = 1·(−1) − (1+i)(1−i) = −1 − (1 − i²) = −1 − 2 = −3
```

**Passo 5 — concluir.** Nenhuma tem determinante 1 → **(e)**.

**Resposta: (e) nenhuma delas.**

**Conferência.** (a) é uma matriz de rotação/reflexão (det −1); (b) tem det −1 (antidiagonal com
`|uv| = 1`); (c) tem det complexo; (d) tem det −3.

**Armadilha.** (a) tem "cara" de matriz ortogonal (e de fato é, com det −1 — rotação/reflexão); quem
confunde `det = ±1` marca (a). (c) tenta quem só olha os módulos.

**Padrão.** Determinante 2×2: `ad − bc`, sempre. Com entradas complexas, lembre `i² = −1` e que o
determinante pode ser **complexo** (não precisa ser real).

---

### Q8 · Suficiência: tipo de carro alugado — **(a) só I basta**

**Enunciado.** Tabela de tarifas: Economy 14/dia, 50/semana; Compact 15/60; Midsize 16/70; Standard 17/80;
Luxury 19,50/100. A diária vale para cada dia (ou fração) **além** de múltiplos de 7 dias, até o teto
semanal. Maria alugou um dos tipos. I. O total foi $92. II. Alugou por 10 dias. Para saber o tipo:
(a) só I basta · (b) só II basta · (c) juntas bastam, nenhuma sozinha · (d) cada uma basta · (e) nem juntas

**Passo 1 — a regra de cobrança.** 10 dias = 1 semana + **3 dias** → `custo = semana + 3·diária`.

**Passo 2 — calcular para cada tipo.**

```
Economy:  50 + 3·14    = 92
Compact:  60 + 3·15    = 105
Midsize:  70 + 3·16    = 118
Standard: 80 + 3·17    = 131
Luxury:   100 + 3·19,50 = 158,50
```

**Passo 3 — testar as afirmações.**

- **I (total $92):** a tabela mostra que **só a Economy** dá 92 → **suficiente sozinha**.
- **II (10 dias):** o custo de 10 dias é diferente para cada tipo, mas sem o total não se sabe qual →
  **não suficiente**.

**Resposta: (a)** — I sozinha basta; II sozinha não.

**Conferência.** Com I, `92` é exclusivo da Economy (os demais totais são 105, 118, 131, 158,5) ✔.

**Armadilha.** (c) "juntas" parece natural, mas I **já** identifica o tipo — a informação dos 10 dias é
redundante para responder (embora seja útil para montar a conta). Em suficiência, pergunte sempre:
*"com esta informação sozinha, a resposta fica única?"*

**Padrão.** Suficiência com tabela: calcule a coluna inteira para o cenário da afirmação e veja se há
**um único** valor compatível.

---

### Q9 · Derivadas de arcsin, arccos, arctan — **(e) todas corretas**

**Enunciado.** `f = arcsin x`, `g = arccos x`, `h = arctan x` em seus domínios. Marque a errada:
(a) f′ + g′ = 0 · (b) f⁻¹(g(x)) = g⁻¹(f(x)) · (c) [f′(x)]⁻¹·g′(x) = −1 ·
(d) 1/h′(x) − 1/(f′(x)·g′(x)) = 2 · (e) todas corretas

**Passo 1 — derivadas.**

```
f′ = 1/√(1−x²)      g′ = −1/√(1−x²)      h′ = 1/(1+x²)
```

- **(a)** `f′ + g′ = 0` ✔ imediato.
- **(b)** `f⁻¹ = sin`, `g⁻¹ = cos`: `sin(g(x)) = sin(arccos x) = √(1−x²)` e
  `cos(f(x)) = cos(arcsin x) = √(1−x²)` → iguais ✔.
- **(c)** `(1/f′)·g′ = √(1−x²)·(−1/√(1−x²)) = −1` ✔.
- **(d)** `1/h′ = 1 + x²`; `f′·g′ = −1/(1−x²)` → `1/(f′g′) = −(1−x²) = x² − 1`. Então

```
1/h′ − 1/(f′g′) = (1 + x²) − (x² − 1) = 2   ✔
```

**Resposta: (e) todas as afirmações são corretas.**

**Conferência em x = 0.** f′ = 1, g′ = −1, h′ = 1: (a) 0 ✔; (c) (1/1)(−1) = −1 ✔; (d) 1 − 1/(−1) = 2 ✔.

**Armadilha.** (c) é a mais estranha de ler: `[f′(x)]⁻¹(g′(x))` significa `(1/f′(x))·g′(x)`. Quem lê
como `(f⁻¹)′(g(x))` acha −1 impossível e marca (c). Em prova, teste numericamente em x = 0 e pronto.

**Padrão.** `arcsin + arccos = π/2` (derivadas opostas); `sin(arccos x) = cos(arcsin x) = √(1−x²)`. Essas
duas identidades resolvem metade das questões de inversas trigonométricas.

---

### Q10 · Preço de garrafas — **(b) $85,20**

**Enunciado.** 5 garrafas de X custam $64,00; 7 de Y custam $163,80. Aos mesmos preços unitários, quanto
custam 3 X + 2 Y?
(a) 36,2 · (b) 85,2 · (c) 94,9 · (d) 95,8 · (e) 98,8

**Resolução.**

```
X = 64,00/5  = 12,80
Y = 163,80/7 = 23,40
3X + 2Y = 3·12,80 + 2·23,40 = 38,40 + 46,80 = 85,20
```

**Resposta: (b) $85,20.**

**Conferência.** `5·12,8 = 64` ✔; `7·23,4 = 163,8` ✔.

**Armadilha.** (a) 36,2 ≈ 38,4 − 2,2 (confusão com 2X+3Y? na verdade 2X+3Y = 25,6+70,2 = 95,8 = (d)!).
Ou seja, (d) é a troca de coeficientes; (a) é só 3X; (c) é 2Y+3X? não — é um valor próximo; o importante
é não trocar X e Y.

**Padrão.** Proporção: ache o **unitário** e depois multiplique. Cuidado com a ordem (3 X e 2 Y).

---

### Q11 · Equação logarítmica — **(d) duas raízes reais distintas**

**Enunciado.** `−log_{1/√e}(x) = ln(4x−3)`. Então:
(a) nenhuma raiz real · (b) uma raiz positiva · (c) uma raiz negativa · (d) duas raízes reais distintas ·
(e) mais de duas raízes positivas

**Passo 1 — simplificar a base.** `1/√e = e^{−1/2}`, então

```
log_{e^{−1/2}}(x) = ln x / (−1/2) = −2 ln x
```

**Passo 2 — montar a equação.**

```
−(−2 ln x) = ln(4x − 3)   ⇒   2 ln x = ln(4x − 3)
```

**Passo 3 — exponenciar.** `x² = 4x − 3` → `x² − 4x + 3 = 0` → **x = 1** ou **x = 3**.

**Passo 4 — domínio.** `x > 0` e `4x − 3 > 0 → x > 3/4`. Ambos 1 e 3 satisfazem ✔.

**Resposta: (d) duas raízes reais distintas (1 e 3).**

**Conferência.** x = 1: LHS `−log(1) = 0`; RHS `ln(1) = 0` ✔. x = 3: LHS `−(−2 ln 3) = 2,197`; RHS
`ln 9 = 2,197` ✔.

**Por que as outras caem.** (b) é para quem acha só x = 1 (ou descarta 3); (c) é impossível (domínio
x > 3/4); (a) e (e) são distratores.

**Padrão.** Sempre **troque a base para e** (`log_{1/√e} = −2ln`) e **exponencie** os dois lados; depois
confira o domínio. Note que as raízes 1 e 3 vêm de uma quadrática — é o caso "duas raízes" clássico.

---

### Q12 · Trabalho conjunto — **(a) 36 horas**

**Enunciado.** Alice sozinha faz o trabalho em 18 h; Alice e Bob juntos em 12 h. Em quanto tempo Bob
sozinho?
(a) 36 · (b) 24 · (c) 18 · (d) 12 · (e) 6

**Resolução.**

```
1/Bob = 1/12 − 1/18 = (3 − 2)/36 = 1/36     ⇒     Bob = 36 h
```

**Resposta: (a) 36 horas.**

**Conferência.** Juntos: `1/18 + 1/36 = 3/36 = 1/12` → 12 h ✔.

**Armadilha.** (b) 24 é `18·12/(18−12)`? não — é o "vizinho"; a conta errada comum é `1/12 + 1/18 = 5/36`
e concluir 7,2 h (nem está nas opções). Outra: fazer `18 − 12 = 6` (e).

**Padrão.** Trabalho: some as **taxas** (1/tempo), nunca os tempos. `1/T_conjunto = 1/T_A + 1/T_B`.

---

### Q13 · Ângulos notáveis — **(e) tan 105° está errada**

**Enunciado.** Marque a afirmação errada:
(a) sen 15° = (√2/4)(√3 − 1) · (b) cos 15° = (√2/4)(√3 + 1) · (c) tan 15° = 2 − √3 ·
(d) cos 105° = (√2/4)(1 − √3) · (e) tan 105° = −(2 − √3)

**Passo 1 — valores de 15°.** `15° = 45° − 30°`:

```
sen15° = sen45 cos30 − sen30 cos45 = (√2/2)(√3/2) − (1/2)(√2/2) = (√6 − √2)/4 = (√2/4)(√3 − 1)   ✔ (a)
cos15° = cos45 cos30 + sen45 sen30 = (√6 + √2)/4 = (√2/4)(√3 + 1)                                  ✔ (b)
tan15° = sen15/cos15 = (√3 − 1)/(√3 + 1) = 2 − √3                                                  ✔ (c)
```

**Passo 2 — 105° = 90° + 15°.**

```
cos105° = −sen15° = −(√6 − √2)/4 = (√2 − √6)/4 = (√2/4)(1 − √3)     ✔ (d)
tan105° = tan(90° + 15°) = −cot15° = −1/(2 − √3) = −(2 + √3)          ✘ (e) diz −(2 − √3)
```

**Resposta: (e).**

**Conferência numérica.** `tan105° ≈ −3,732`; `−(2+√3) ≈ −3,732` ✔ e `−(2−√3) ≈ −0,268` ✘.

**Armadilha.** `cot15° = 2 + √3` (racionalizando `1/(2−√3)`). Quem "simplifica" errado troca o sinal do
√3 e cai em (e). Note que (d) também engana pelo sinal: `(√2/4)(1−√3)` é negativo (1 − √3 < 0), como
deve ser.

**Padrão.** 15° e 105° são complementares/suplementares: `cos105 = −sen15` e `tan105 = −cot15 = −(2+√3)`.
Racionalize `1/(2−√3)` para ver o `2+√3` aparecer.

---

### Q14 · Encontro de caminhantes — **(a) 12 km**

**Enunciado.** Yasmim sai de A para B (22,5 km) a 1,5 km/h. Uma hora depois, Julia sai de B para A a
2 km/h. Quantos km Julia andou até o encontro?
(a) 12 · (b) 11,5 · (c) 11 · (d) 10,5 · (e) 9,75

**Passo 1 — onde estão quando Julia sai.** Yasmim já andou `1,5·1 = 1,5 km`; faltam `21 km`.

**Passo 2 — velocidade de aproximação.** `1,5 + 2 = 3,5 km/h` → tempo até o encontro `21/3,5 = 6 h`.

**Passo 3 — distância de Julia.** `2·6 = 12 km`.

**Resposta: (a) 12 km.**

**Conferência.** Yasmim andou `1,5·(1+6) = 10,5 km`; `10,5 + 12 = 22,5` ✔.

**Armadilha.** (e) 9,75 = `1,5·6,5` (distância de Yasmim se ela andasse 6,5 h) e (b)/(c) são valores de
quem erra o tempo (5,5 ou 5 h).

**Padrão.** Encontros: `d_total = v1·t1 + v2·t2` com `t1 = t2 + atraso`. Sempre confira a soma das
distâncias = distância total.

---

### Q15 · Convergência de cos^{n+1}(nθ) — **(c) e (d)** *(questão anulada)*

**Enunciado.** Sobre a sequência `a_n = cos^{n+1}(nθ)`, marque a correta (se todas, a última):
(a) converge para todo θ ∈ (0, π) · (b) converge para todo θ ∈ (π, 2π) · (c) converge para θ = π ·
(d) converge para θ = 2π · (e) todas as anteriores são verdadeiras

**Passo 1 — casos especiais.**

- **θ = π:** `cos(nπ) = (−1)^n` → `a_n = (−1)^{n(n+1)}`. Mas `n(n+1)` é **sempre par** → `a_n = 1` para
  todo n → **converge (para 1)** ✔ **(c) verdadeira**.
- **θ = 2π:** `cos(2πn) = 1` → `a_n = 1` → **converge** ✔ **(d) verdadeira**.

**Passo 2 — casos gerais.**

- θ = π/2: `cos(nπ/2) ∈ {0, 1, −1}` → `a_n ∈ {0, ±1}` → **não converge** (oscila). Logo (a) é falsa.
- θ = 3π/2: idem → (b) falsa.
- θ irracional múltiplo de π (ex.: θ = 1 rad): `cos(nθ)` é denso em [−1,1]; há subsequências com
  `|cos(nθ)| → 1` (aproximação diofantina) e outras com `cos(nθ) → 0` → **não converge**.

**Passo 3 — julgar as opções.** (c) e (d) são verdadeiras; (a) e (b) falsas; (e) falsa (pois (a) e (b)
falham). Portanto **duas alternativas corretas** → a questão **não tem resposta única** e foi **anulada**
(a própria folha traz: "15) e — errado, respostas corretas: c & d").

**Resposta: (c) e (d)** — questão anulada.

**Conferência numérica.** θ = π: aₙ = 1,0000 para todo n ✔. θ = 2π: aₙ = 1,0000 ✔. θ = 1: primeiros
termos 0,292; −0,072; 0,961; −0,119; 0,001; 0,752 — sem convergência ✔.

**Armadilha.** Quem marca (e) ("todas") acha que "θ = π e θ = 2π convergem" implica as outras — não
implica: (a) e (b) falam de **todo** θ no intervalo, e basta um contraexemplo (θ = π/2).

**Padrão.** Sequências da forma `[cos(nθ)]^{n+1}`: convergem só quando `cos(nθ)` é **constante** em n
(caso θ múltiplo de π) ou quando → 0. Para θ genérico, oscila. E cuidado com "para todo": um contraexemplo
derruba a afirmação.

---

### Q16 · Área do tapete — **(e) (a−2c)(b−2c)**

**Enunciado.** Piso retangular a × b coberto por um tapete, deixando uma faixa de c metros em cada uma das
quatro bordas. Área do tapete?
(a) ab − c(a+b) · (b) ab − 2c(a+b) · (c) ab − c² · (d) (a−c)(b−c) · (e) (a−2c)(b−2c)

**Resolução.** A faixa de c metros existe **dos dois lados** de cada dimensão, então o tapete mede

```
(a − 2c) por (b − 2c)      ⇒      Área = (a − 2c)(b − 2c)
```

**Resposta: (e).**

**Conferência.** a = 10, b = 8, c = 1: tapete `8 × 6 = 48`. E `ab − 2c(a+b) + 4c² = 80 − 36 + 4 = 48` ✔
(expansão de `(a−2c)(b−2c)`).

**Por que as outras caem.** (d) desconta c **uma vez** (faixa só de um lado); (b) é a expansão parcial
`ab − 2c(a+b)` (esquece os **quatro cantos**, `+4c²`); (a) e (c) são tentativas de simetria.

**Padrão.** "Faixa em volta" → descontar **2c** de cada dimensão. Se a questão pedir a área da **faixa**,
cuidado com a dupla contagem dos cantos: `ab − (a−2c)(b−2c) = 2c(a+b) − 4c²`.

---

## 4. Padrões que a banca repetiu nesta prova

1. **Duas de suficiência de dados** (Q6 e Q8), com lógicas diferentes: Q6 é **álgebra** (uma equação que
   fixa x e deixa y livre); Q8 é **tabela** (o total identifica o tipo). Sempre pergunte: "com esta
   informação sozinha, a resposta fica única?".
2. **Três de "afirmação errada / anulada"** (Q3, Q13, Q15) — leia o comando e teste **todas** as opções.
3. **Ângulos e trigonometria** (Q2, Q13): rastreamento de ângulos e valores de 15°/105°.
4. **Log com base "estranha"** (Q11): converter `1/√e` para `e^{−1/2}` e exponenciar.
5. **Proporção/trabalho/encontro** (Q10, Q12, Q14): unitarizar (preço por garrafa, taxa por hora, km/h).
6. **Determinantes** (Q7): `ad − bc` sempre, com complexos incluídos.

---

## 5. Plano de 90 minutos

| Bloco | Tempo | Questões | Objetivo |
|:-----:|:-----:|----------|----------|
| 1 | 0–12 min | 4, 10, 12, 14, 16 | 5 acertos rápidos |
| 2 | 12–35 min | 1, 5, 7, 9, 11, 13 | médias |
| 3 | 35–75 min | 3, 8, 2, 6, 15 | longas e suficiência |
| 4 | 75–90 min | todas | revisar comandos (Q3, Q15) e conferir |

Regra: **3 min travado → marque e siga**. Nesta prova, Q2 e Q6 valem o mesmo que Q16.

---

## 6. Checklist final

- [ ] Releu "**wrong statement**", "**may not**", "**mark the correct**", "**for all**"?
- [ ] Em suficiência, testou cada afirmação **sozinha**?
- [ ] Em log, trocou a base para `e` e verificou o domínio?
- [ ] Em trigonometria, conferiu o sinal (`cos105° < 0`, `tan105° = −(2+√3)`)?
- [ ] Em "para todo θ", procurou um contraexemplo?
- [ ] Em geometria com faixa, descontou `2c` de **cada** dimensão?

---

## 7. Resumo de fórmulas usadas

```
Coeficiente de x⁴:         em (1+x)(1−x)ⁿ: C(n,4) − C(n,3) = n(n−1)(n−2)(n−7)/24
Ângulos:                   sen15° = (√6−√2)/4 ; cos15° = (√6+√2)/4 ; tan15° = 2−√3
                           tan105° = −(2+√3) ; cos105° = −sen15°
Independência:             #(A∩B)·|U| = #A·#B
Determinante 2×2:          ad − bc
Sistema:                   u = y² (2 soluções) ; v = z³ (1 solução)
Log:                       log_{1/√e} x = −2 ln x ; log_a b = ln b/ln a
Trabalho:                  1/T = 1/T_A + 1/T_B
Encontro:                  d = v₁t₁ + v₂t₂
Sequências:                [cos(nθ)]^{n+1} converge só em casos especiais (θ múltiplo de π)
Faixa em volta:            (a−2c)(b−2c)
```

---

## 8. Onde treinar cada questão

| Questão | Tema no repositório |
|:-------:|---------------------|
| 1, 16 | [`temas/01-combinatoria`](../../temas/01-combinatoria/README.md) |
| 2, 13 | [`temas/07-trigonometria`](../../temas/07-trigonometria/README.md) |
| 3, 8, 10, 12, 14 | [`temas/10-problemas-taxa-trabalho`](../../temas/10-problemas-taxa-trabalho/README.md) |
| 4, 5 | [`temas/05-polinomios-e-raizes`](../../temas/05-polinomios-e-raizes/README.md) |
| 5, 7 | [`temas/02-sistemas-matrizes-determinantes`](../../temas/02-sistemas-matrizes-determinantes/README.md) |
| 6, 8 | [`temas/11-logica-suficiencia-dados`](../../temas/11-logica-suficiencia-dados/README.md) |
| 9 | [`temas/08-calculo`](../../temas/08-calculo/README.md) |
| 11 | [`temas/04-funcoes-log-exp`](../../temas/04-funcoes-log-exp/README.md) |
| 15 | [`temas/06-sequencias-pa-pg-series`](../../temas/06-sequencias-pa-pg-series/README.md) |

> Em cada tema, o arquivo **`RESOLUCOES-PASSO-A-PASSO.md`** traz a resolução linha a linha das questões
> reais daquele assunto — é o complemento natural desta leitura por prova.

---

**Prova original:** [`Prova_PG-EIA_2022-2oSem.pdf`](../Prova_PG-EIA_2022-2oSem.pdf) ·
**Texto extraído:** [`Prova_PG-EIA_2022-2oSem.txt`](../Prova_PG-EIA_2022-2oSem.txt) ·
**Índice de resoluções:** [`README.md`](README.md) · **Provas:** [`../README.md`](../README.md).
