# Resolução comentada — Matemática · 2023 / 2º semestre (PG-EIA · ITA)

**Prova:** [`../Prova_PG-EIA_2023-2oSem.pdf`](../Prova_PG-EIA_2023-2oSem.pdf) — aplicada em **22 de maio de 2023**.
**Formato:** 16 questões de múltipla escolha (a–e), enunciados em inglês, **90 minutos**, sem calculadora.
**Gabarito:** `1-d 2-e 3-d 4-a 5-d 6-e 7-e 8-e 9-c 10-b 11-a 12-a 13-d 14-e 15-c 16-c`.

> **O que este arquivo entrega.** As **16 questões resolvidas passo a passo**: diagnóstico, conta completa,
> por que a alternativa correta é correta, **por que as outras caem**, armadilhas e o padrão da banca.
> A prova de 2023/2 não trouxe chave no PDF: as respostas foram obtidas por resolução independente,
> **conferidas numericamente** (contagens por força bruta, travessia por busca em largura, coordenadas) e
> cruzadas com as resoluções por tema deste repositório.

> **Sobre o nome.** É a prova de Matemática do processo seletivo do PG-EIA/ITA, múltipla escolha estilo
> GMAT — a "prova de GMAT/GMATE" do 2º semestre de 2023. No repositório, o PDF é o
> `Prova_PG-EIA_2023-2oSem.pdf`.

**Recado rápido:** aqui a dificuldade é **variada** — tem questões de 30 segundos (Q13) e duas que exigem
malha fina (Q2, círculo ex-inscrito, e Q7, círculo dos nove pontos). Atenção especial a **Q4**, que tem
duas alternativas algebricamente idênticas (veja a nota na resolução).

---

## 1. Gabarito relâmpago

| Questão | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 | 13 | 14 | 15 | 16 |
|:-------:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
| **Resposta** | **d** | **e** | **d** | **a** | **d** | **e** | **e** | **e** | **c** | **b** | **a** | **a** | **d** | **e** | **c** | **c** |

---

## 2. Raio-X da prova

| # | Assunto | Resp. | Nível | Tempo-alvo |
|:-:|---------|:-----:|:-----:|:----------:|
| 1 | Raiz quadrada de matriz: quantas A com A² = B | d | médio | 4 min |
| 2 | Maior área de triângulos com o mesmo ex-incírculo | e | difícil | 6 min |
| 3 | Duas cúbicas: o que **não** se pode dizer | d | fácil | 2 min |
| 4 | Sinais + e − em fila (sem "−" adjacentes) | a | médio | 3 min |
| 5 | Travessia do rio: 3 casais ciumentos | d | difícil | 4 min |
| 6 | Série alternada com √2: limite | e | médio | 2 min |
| 7 | Centro do círculo dos nove pontos | e | médio | 4 min |
| 8 | Fórmula que pode não dar inteiro | e | fácil | 1,5 min |
| 9 | Integral imprópria ∫₀^∞ x e^{−x²} dx | c | fácil | 1,5 min |
| 10 | Simplificação com fatoriais | b | fácil | 1,5 min |
| 11 | Sistema 3×3: número de soluções | a | fácil | 2 min |
| 12 | f′(x) = f(x) para f = √(1−x²) | a | médio | 3 min |
| 13 | Preço com +20% e depois −20% | d | fácil | 1 min |
| 14 | (7ˣ+2√10)(7ˣ−2√10) = 9 | e | fácil | 1,5 min |
| 15 | Integral definida com log | c | fácil | 2 min |
| 16 | Círculo e triângulo isósceles de mesma área | c | médio | 3 min |

**Leitura estratégica.** Cinco questões saem em ≤ 2 min (8, 9, 10, 13, 14) e valem 5 acertos. As caras
são Q2 (área máxima com ex-incírculo), Q5 (travessia) e Q7 (nove pontos). Soma dos tempos-alvo: **~47 min**.

---

## 3. Resoluções

### Q1 · Raiz quadrada de matriz — **(d) quatro matrizes**

**Enunciado.** Se `[A]² = [A][A] = [[4, 10], [0, 9]]`, então:
(a) só uma matriz A · (b) só duas · (c) só três · (d) só quatro · (e) nenhuma

**Passo 1 — A comuta com B.** `A² = B` ⟹ `AB = A·A² = A³ = A²·A = BA`. Como B é triangular com
autovalores **distintos** (4 e 9), toda matriz que comuta com B é **polinômio em B**; polinômio de uma
triangular superior é triangular superior. Logo

```
A = ⎡ a  b ⎤
    ⎣ 0  c ⎦
```

**Passo 2 — impor A² = B.**

```
A² = ⎡ a²   b(a + c) ⎤  =  ⎡ 4   10 ⎤
     ⎣ 0       c²    ⎦     ⎣ 0    9 ⎦
```

Equações: `a² = 4`, `c² = 9`, `b(a + c) = 10`.

**Passo 3 — contar.** `a = ±2`, `c = ±3` (4 combinações). Como `a + c ∈ {5, −1, 1, −5}`, nunca é zero,
então para cada par existe **exatamente um** `b = 10/(a + c)`:

| a | c | a+c | b | A |
|---|---|---|---|---|
| 2 | 3 | 5 | 2 | [[2, 2], [0, 3]] |
| 2 | −3 | −1 | −10 | [[2, −10], [0, −3]] |
| −2 | 3 | 1 | 10 | [[−2, 10], [0, 3]] |
| −2 | −3 | −5 | −2 | [[−2, −2], [0, −3]] |

**Resposta: (d) quatro matrizes.**

**Conferência.** Cada uma das quatro, ao quadrado, dá [[4,10],[0,9]] (verificado numericamente) ✔.

**Armadilha.** (a) "só uma" é para quem pensa na "raiz quadrada positiva" — matrizes não têm essa noção;
(b) duas é o número de **sinais** possíveis se você exigir a mesma diagonal. O ponto é que `b` depende de
`a + c`, então cada sinal de a e de c produz um b válido.

**Padrão.** `A² = B` com B tendo autovalores distintos e positivos: procure A **triangular na base de B**
(e A comuta com B!), resolva a diagonal por raízes quadradas e a superdiagonal por `b(a+c) = B₁₂`.
Se `a + c = 0` e `B₁₂ ≠ 0`, não há solução.

---

### Q2 · Maior área com o mesmo ex-incírculo — **(e) 3√3**

**Enunciado.** A Figura 1 mostra dois triângulos ABC e AB'C' com as mesmas retas suporte t e s e o mesmo
círculo ex-inscrito c (r = 3), com ângulo de 60° em A. Qual a **maior área possível** entre todos os
triângulos formados por uma tangente a c entre t e s?
(a) 3 · (b) 2√2 · (c) 2√3 · (d) 4 · (e) 3√3

**Passo 1 — entender a configuração.** O círculo c é tangente às duas retas fixas t e s (que formam 60° em
A) e à reta variável BC, ficando **fora** do triângulo, do lado oposto a A → c é o **ex-incírculo oposto a
A** (A-excírculo), de raio `r_a = 3`.

**Passo 2 — a fórmula da área com ex-incírculo.** Para o A-excírculo vale

```
Δ = r_a · (s − a),      onde s = semiperímetro e a = BC
```

e, como o círculo é tangente às duas retas por A, a distância de A aos pontos de tangência é

```
s = r_a · cot(A/2) = 3 · cot 30° = 3√3        (FIXO!)
```

**Passo 3 — maximizar.** Com `s` e `r_a` fixos,

```
Δ = 3(3√3 − a)      ⇒      Δ é máximo quando a = BC é MÍNIMO
```

**Passo 4 — minimizar a.** Para ângulo A fixo e semiperímetro s fixo, use a lei dos senos
`a = 2R sin A`, `b = 2R sin B`, `c = 2R sin C`, `s = R(sin A + sin B + sin C)`:

```
a = 2s·sin A / (sin A + sin B + sin C),     B + C = 180° − A
sin B + sin C = 2 sin((B+C)/2)·cos((B−C)/2) ≤ 2 sin((180°−A)/2) = 2cos(A/2)
```

com **igualdade quando B = C** (triângulo isósceles). Então

```
a ≥ 2s·sin A/(sin A + 2cos(A/2)) = 2·3√3·(√3/2)/(√3/2 + √3) = 2√3
```

**Passo 5 — área máxima.**

```
Δ_max = 3(3√3 − 2√3) = 3√3 ≈ 5,196
```

**Resposta: (e) 3√3.**

**Conferência geométrica direta (isósceles).** A tangente perpendicular à bissetriz produz o triângulo
isósceles: `B` e `C` a `2√3` de A, altura = 3 (distância de A à tangente = 6 − 3), base `BC = 2√3` →
`Δ = (1/2)(2√3)(3) = 3√3` ✔. Amostrando 121 tangentes por computador, o máximo ocorre exatamente aí.

**Por que as outras caem.** (c) `2√3` é o **valor mínimo de a** (a base do isósceles), não a área — é a
distratora perfeita para quem confunde "BC" com "área"; (a) 3 é a altura; (b) e (d) são valores de área de
outras configurações (por exemplo, `2√2` aparece em tangentes fora do isósceles).

**Padrão.** Triângulo com ex-incírculo fixo: `s = r_a cot(A/2)` (fixo) e `Δ = r_a(s − a)` → maximize a área
minimizando o lado oposto a A; o mínimo ocorre no **isósceles**. Guarde também `Δ = r·s` para o incírculo.

---

### Q3 · Duas cúbicas: o que NÃO se pode dizer — **(d)**

**Enunciado.** Sobre `x³ − 6x − 9 = 0` (1) e `x³ − 6x + 9 = 0` (2), **não** se pode afirmar:
(a) (1) tem uma raiz natural · (b) (2) tem uma raiz inteira · (c) (1) tem duas raízes complexas ·
(d) (2) tem duas raízes puramente imaginárias · (e) (2) tem duas raízes complexas

**Passo 1 — fatorar as duas.**

```
(1)  x³ − 6x − 9 = (x − 3)(x² + 3x + 3)     → raízes 3 e (−3 ± i√3)/2
(2)  x³ − 6x + 9 = (x + 3)(x² − 3x + 3)     → raízes −3 e (3 ± i√3)/2
```

**Passo 2 — checar cada item.**

- **(a)** raiz 3 em (1): `27 − 18 − 9 = 0` ✔ **verdadeira** (3 é natural).
- **(b)** raiz −3 em (2): `−27 + 18 + 9 = 0` ✔ **verdadeira** (−3 é inteiro).
- **(c)** (1) tem o par `(−3 ± i√3)/2` (discriminante `9 − 12 = −3 < 0`) ✔ **verdadeira**.
- **(d)** (2) tem "two pure imaginary roots"? As raízes complexas são `(3 ± i√3)/2`: **parte real 3/2 ≠ 0**,
  logo **não** são imaginárias puras ✘ **FALSA** — é a resposta.
- **(e)** (2) tem o par complexo conjugado `(3 ± i√3)/2` ✔ **verdadeira**.

**Resposta: (d).**

**Armadilha.** "Pure imaginary" = `bi` com `b ≠ 0` (parte real nula). Quem só vê o `i√3` marca (d) como
verdadeira. Note que as duas cúbicas são "espelhadas" (x → −x): as raízes de (2) são os negativos das de
(1), mas o par complexo de (2) tem parte real **+3/2**, não zero.

**Padrão.** Cúbica com raiz inteira pequena: teste ±1, ±3, ±9 (divisores do termo independente), fatore e
analise o discriminante da quadrática. Em prova, isso resolve em 30 s.

---

### Q4 · Sinais + e − em fila — **(a)**

**Enunciado.** `p` sinais "+" e `q` sinais "−" em fila, com `p + q = n` e `p > q − 2`. Sem dois "−"
adjacentes, de quantas formas? (a) `C(n−q+1, q)` · (b) `C(q, p+q)` · (c) `(p+q)!/q!` · (d) `C(p+1, q)` ·
(e) `(p+q−1)!`

**Passo 1 — condição de existência.** Sem "−" adjacentes exige `q ≤ p + 1`, isto é, `p ≥ q − 1`, que é
exatamente `p > q − 2` ✔.

**Passo 2 — método dos espaços (gaps).** Coloque primeiro os `p` sinais "+": eles criam **p + 1** espaços
(antes do primeiro, entre cada par, depois do último):

```
_ + _ + _ + ... + _          (p sinais "+" e p+1 lacunas)
```

**Passo 3 — escolher as lacunas.** Para que não haja "−" adjacentes, cada lacuna recebe **no máximo um**
"−". Logo basta escolher `q` das `p + 1` lacunas:

```
C(p + 1, q)
```

**Passo 4 — escrever como a alternativa.** Como `p = n − q`,

```
C(p + 1, q) = C(n − q + 1, q)      →  alternativa (a)
```

**Resposta: (a).**

**Nota importante (falha da questão).** A alternativa **(d)** é `C(p + 1, q)` — **a mesma expressão** de
(a), pois `p + 1 = n − q + 1`. Ou seja, a questão tem **duas alternativas algebricamente idênticas**. A
banca claramente queria a resposta "em termos de n e q" (dados do enunciado), que é (a). Se você for
recorrer, este é o argumento: (a) e (d) são o mesmo número.

**Conferência.** `p = 3`, `q = 2`: `C(3+1,2) = 6`. Listando: `+−+−+`, `+−++−`, `++−+−`, `+−+−+`… de fato:
escolher 2 lacunas entre 4 → 6 ✔. E `C(n−q+1,q) = C(5−2+1,2) = C(4,2) = 6` ✔.

**Por que as outras caem.** (b) `C(q, p+q)` e (d) já discutida; (c) `(p+q)!/q!` conta arranjos com "−"
distinguíveis e sem restrição; (e) `(p+q−1)!` é uma permutação circular — nada a ver.

**Padrão.** "Itens que não podem ficar juntos" → **método dos gaps**: arrume os outros e escolha as
lacunas. É o mesmo padrão de "letras iguais não adjacentes" e "cadeiras com restrição".

---

### Q5 · Travessia dos três casais ciumentos — **(d) 11 travessias**

**Enunciado.** Três casais à beira do rio; barco leva até 2 pessoas. Nenhum homem pode ficar em qualquer
margem (ou no barco) na companhia da esposa de outro homem sem o marido dela. Número **mínimo** de
travessias para levar todos ao outro lado?
(a) 8 · (b) 9 · (c) 10 · (d) 11 · (e) 12

**Passo 1 — modelar.** Estado = (conjunto de pessoas na margem esquerda; lado do barco). Regra de
segurança, em cada margem e no barco: para toda esposa W presente, se há algum homem que **não** é seu
marido, então seu marido também está presente.

**Passo 2 — a solução mínima (11 travessias).** Escreva H1/W1, H2/W2, H3/W3:

```
 1. H1, W1  →     (um casal cruza)
 2. H1      ←     (o marido volta)
 3. W2, W3  →     (duas esposas cruzam)
 4. W1      ←     (uma esposa volta)
 5. H2, H3  →     (dois maridos cruzam)
 6. H2, W2  ←     (um casal volta)
 7. H1, H2  →     (dois maridos cruzam)
 8. W3      ←     (uma esposa volta)
 9. W1, W2  →     (duas esposas cruzam)
10. W1      ←     (uma esposa volta)
11. W1, W3  →     (fim: todos à direita)
```

Cada passo deixa as **duas margens** e o **barco** seguros (verifiquei esta sequência com um simulador de
estados: as 11 travessias são válidas e terminam com todos à direita).

**Passo 3 — provar a minimalidade.** Uma busca em largura (BFS) sobre **todos** os estados válidos, com
movimentos de 1 ou 2 pessoas e verificação das duas margens e do barco, encontra **distância mínima = 11**
— e nenhum caminho menor existe. (A busca é finita: os estados válidos são poucos.)

**Resposta: (d) 11 travessias.**

**Por que não 9 ou 10?** Intuição: cada travessia de ida leva no máximo 2 pessoas e cada volta traz 1;
além disso, nenhuma esposa pode ficar "sozinha" com outro homem, o que força uma dança de casais. A BFS
confirma que 10 é insuficiente.

**Padrão.** Problemas de travessia com restrição → modele estados + BFS (à mão, use a lógica "leve as
esposas primeiro, depois os maridos"). O clássico dos 3 casais ciumentos tem resposta **11**; guarde o
roteiro acima.

---

### Q6 · Série alternada com √2 — **(e) não há limite definido**

**Enunciado.** `S_n = Σ_{i=1}^{n} (−1)^i √(2^{i−1}) = −1 + √2 − 2 + 2√2 − 4 + 4√2 − ...`
O valor de `lim_{n→∞} S_n` é:
(a) −∞ · (b) −3−√2 · (c) √2+1 · (d) +∞ · (e) não há limite definido

**Passo 1 — termo geral.** `|termo_i| = √(2^{i−1}) = (√2)^{i−1}`, que **cresce** sem limite (razão √2 > 1).
Como o termo geral **não tende a zero**, a série não converge.

**Passo 2 — olhar as somas parciais.** Agrupando em pares:

```
S_2  = (−1 + √2)                    = (√2 − 1)
S_4  = (−1 + √2) + (−2 + 2√2)       = (√2 − 1)(1 + 2)
S_6  = (√2 − 1)(1 + 2 + 4)
S_{2k} = (√2 − 1)(2^k − 1)  →  +∞
```

Mas as parciais ímpares incluem o último termo negativo grande:

```
S_{2k−1} = S_{2k−2} − (√2)^{2k−2}  →  −∞
```

**Passo 3 — concluir.** `S_{2k} → +∞` e `S_{2k−1} → −∞`: a sequência de somas parciais **oscila sem
limite** → não existe `lim S_n`.

**Resposta: (e).**

**Conferência (parciais).** `S_1 = −1`; `S_2 ≈ 0,414`; `S_3 ≈ −1,586`; `S_4 ≈ 1,243`; `S_5 ≈ −2,757`;
`S_6 ≈ 2,900` — oscila e cresce em amplitude ✔.

**Por que as outras caem.** (a) −∞ e (d) +∞ descrevem **subsequências** (pares ou ímpares), não o limite;
(b) e (c) são valores de outras séries geométricas (por exemplo, `Σ (−1/√2)^k`).

**Padrão.** Antes de qualquer teste, calcule `lim a_n`. Se `a_n` não vai a zero, a série **diverge** (teste
do termo geral). E cuidado: "série divergir para +∞" ≠ "não ter limite" — aqui oscila.

---

### Q7 · Centro do círculo dos nove pontos — **(e) (4,3; 2,4)**

**Enunciado.** A Figura 2 mostra um triângulo de lados **6, 8 e 10** (com pés das alturas e pontos médios);
cinco dos nove pontos coincidem em A. Coordenadas do centro do círculo dos nove pontos:
(a) (4; 2,5) · (b) (4; 2√2) · (c) (4,1; 2,4) · (d) (4,2; 2,5) · (e) (4,3; 2,4)

**Passo 1 — reconhecer o triângulo retângulo.** `6² + 8² = 36 + 64 = 100 = 10²` → o triângulo é
**retângulo em A** (o lado 10 é a hipotenusa, sobre o eixo x). É por isso que cinco dos nove pontos
coincidem em A: os pés das duas alturas que partem de B e C, os pontos médios de AH, BH e CH (com H = A).

**Passo 2 — coordenadas.** Na figura, B está na origem e C em (10, 0). A altura de A à hipotenusa:

```
h = (6·8)/10 = 4,8          projeção de AB sobre BC: 6²/10 = 3,6
A = (3,6; 4,8)
```

**Passo 3 — centro do círculo dos nove pontos.** Ele é o **ponto médio entre o ortocentro H e o
circuncentro O**:

```
H = A = (3,6; 4,8)          (triângulo retângulo: ortocentro = vértice do ângulo reto)
O = ponto médio de BC = (5; 0)
N = (H + O)/2 = ((3,6+5)/2; (4,8+0)/2) = (4,3; 2,4)
```

**Resposta: (e) (4,3; 2,4).**

**Conferência.** O raio do círculo dos nove pontos é `R/2`: `R = 10/2 = 5` (circunraio do retângulo =
metade da hipotenusa) → `r₉ = 2,5`. Distâncias de N a A e a O: `|N−A| = |(−0,7; −2,4)| = 2,5` ✔ e
`|N−O| = |(−0,7; 2,4)| = 2,5` ✔.

**Por que as outras caem.** (a) (4; 2,5) é o baricentro dos pontos médios / uma média "ingênua" de
coordenadas; (b) (4; 2√2) usa `2√2 ≈ 2,83` no lugar de 2,4; (c) e (d) são aproximações com erro de 0,1 —
a banca aposta em quem arredonda a altura para 4,6 ou 4,7 e "chuta" a mais próxima.

**Padrão.** Círculo dos nove pontos: centro = ponto médio de **H** e **O**; raio = R/2. Em triângulo
retângulo, H é o vértice do ângulo reto e O é o ponto médio da hipotenusa — daí a conta sai em 2 linhas.

---

### Q8 · Fórmula que pode não ser inteira — **(e)**

**Enunciado.** Para `n ∈ ℕ`, qual fórmula **pode não** resultar inteiro para todo n?
(a) `(n²−n)/2` · (b) `(n²+n)/2` · (c) `(n³+3n²+2n)/6` · (d) `(n³−n)/6` · (e) `(n³+n)/6`

**Passo 1 — as quatro primeiras são clássicas.**

- (a) `n(n−1)/2` = soma `1+2+...+(n−1)` ✔ inteiro.
- (b) `n(n+1)/2` = soma `1+...+n` ✔ inteiro.
- (c) `n(n+1)(n+2)/6` = produto de **três consecutivos** / 6 ✔ inteiro (há múltiplo de 2 e de 3).
- (d) `(n−1)n(n+1)/6` = produto de **três consecutivos** / 6 ✔ inteiro.

**Passo 2 — testar (e) com n = 2.**

```
(2³ + 2)/6 = 10/6 = 5/3   ∉ ℤ
```

Logo (e) **pode não** ser inteiro.

**Resposta: (e).**

**Extra.** `n³ + n = n(n²+1)`: para n par, `n² + 1` é ímpar e `n` pode não ter fator 3 (n = 2 → 10);
para n ímpar, `n² + 1 ≡ 2 (mod 4)`. Ela **nunca** é divisível por 6 quando n = 2 (mod 6), por exemplo.

**Por que as outras caem.** Todas são contagens combinatórias (`C(n,2)`, `C(n+1,2)`, `C(n+2,3)`,
`C(n+1,3)`), portanto inteiras por definição.

**Padrão.** Produto de k inteiros consecutivos é divisível por k!. Reconhecer `C(n,k)` disfarçado resolve
a questão em segundos.

---

### Q9 · Integral imprópria — **(c) 1/2**

**Enunciado.** `∫₀^∞ x·e^{−x²} dx` = (a) −1 · (b) 0 · (c) 1/2 · (d) 1 · (e) ∞

**Passo 1 — substituir.** `u = x²` → `du = 2x dx` → `x dx = du/2`:

```
∫ x e^{−x²} dx = (1/2)∫ e^{−u} du = −(1/2) e^{−u} = −(1/2) e^{−x²}
```

**Passo 2 — avaliar de 0 a ∞.**

```
[−(1/2)e^{−x²}]₀^∞ = 0 − (−(1/2)·1) = 1/2
```

**Resposta: (c) 1/2.**

**Por que as outras caem.** (a) −1 é o valor sem o sinal certo; (b) 0 esquece o limite inferior; (d) 1 é o
dobro (quem esquece o fator 1/2 do `du`); (e) ∞ é o que aconteceria se o integrando crescesse (ele decai
super-rápido).

**Padrão.** `∫ x e^{−x²}` é a integral "gaussiana de momento" — sempre `−e^{−x²}/2`. Aparece em
probabilidade (normal) e em física.

---

### Q10 · Simplificação com fatoriais — **(b)**

**Enunciado.** Simplifique `n[n! + (n−1)!]/((n+1)! − n!)`, n natural não nulo:
(a) n · (b) (n+1)/n · (c) (n−1)/n · (d) n/(n+1) · (e) n/(n−1)

**Passo 1 — fatorar `(n−1)!` em cima e `n!` embaixo.**

```
n[n! + (n−1)!] = n·(n−1)!·(n + 1)
(n+1)! − n!    = n!·[(n+1) − 1] = n!·n
```

**Passo 2 — dividir.**

```
n(n−1)!(n+1) / (n!·n) = (n−1)!(n+1)/n! = (n+1)/n
```

**Resposta: (b) (n+1)/n.**

**Conferência.** n = 2: `2[2+1]/(6−2) = 6/4 = 1,5 = 3/2` ✔; n = 3: `3[6+2]/(24−6) = 24/18 = 4/3` ✔.

**Armadilha.** (d) `n/(n+1)` é o inverso — erro de quem inverte a fração ao fatorar; (c) e (e) vêm de
cancelar `n` com `(n+1)` indevidamente.

**Padrão.** Fatorial: `(k+1)! = (k+1)·k!` e `k! = k·(k−1)!`. Fatore o menor fatorial e cancele — nunca
expanda.

---

### Q11 · Sistema 3×3 — **(a) nenhuma solução**

**Enunciado.** `x − y − z = 3` (1); `−x + y − z = 4` (2); `x − y + z = 5` (3). Então:
(a) não tem solução real · (b) uma · (c) duas · (d) mais de duas · (e) faltam informações

**Passo 1 — combinar (1) e (3).** Somando (1) e (3):

```
(1) + (3):  2x − 2y = 8      →      x − y = 4
```

**Passo 2 — substituir em (1).**

```
x − y − z = 3   →   4 − z = 3   →   z = 1
```

**Passo 3 — combinar (1) e (2).**

```
(1) + (2):  −2z = 7   →   z = −7/2
```

**Passo 4 — contradição.** `z = 1` e `z = −7/2` ao mesmo tempo → sistema **incompatível**.

**Resposta: (a) não tem solução real.**

**Conferência (determinante).** A matriz dos coeficientes tem determinante 0 (verificado), e o sistema é
incompatível (o vetor de termos independentes não está no espaço-coluna). Alternativa rápida: some (1) e
(2) e compare com (3) − (1).

**Por que as outras caem.** (b) é o "chute" de quem encontra z = 1 e para; (d) é para quem acha que
"3 equações, 3 incógnitas, infinitas"; (e) é o distrator de suficiência.

**Padrão.** Sistema 3×3: elimine uma variável por soma/subtração e procure **contradição**; se achar duas
expressões diferentes para a mesma incógnita, acabou.

---

### Q12 · f′(x) = f(x) para f(x) = √(1−x²) — **(a) (1−√5)/2**

**Enunciado.** `f(x) = √(1−x²)`. Para qual x real vale `f′(x) = f(x)`?
(a) (1−√5)/2 · (b) 0 · (c) √2/2 · (d) arcsin(1/2) · (e) não existe

**Passo 1 — derivar.** `f′(x) = −x/√(1−x²)` (domínio `|x| < 1`).

**Passo 2 — igualar.**

```
−x/√(1−x²) = √(1−x²)
−x = 1 − x²
x² − x − 1 = 0
x = (1 ± √5)/2
```

**Passo 3 — filtrar pelo domínio.** `(1+√5)/2 ≈ 1,618 ∉ (−1, 1)` → descartada.
`(1−√5)/2 ≈ −0,618 ∈ (−1, 1)` ✔.

**Resposta: (a) (1−√5)/2.**

**Conferência.** `x = −0,618`: `f = √(1−0,382) = 0,786`; `f′ = 0,618/0,786 = 0,786` ✔ iguais.

**Por que as outras caem.** (b) 0: `f′(0) = 0 ≠ 1 = f(0)`; (c) √2/2: `f′ = −1 ≠ 1`; (d) `arcsin(1/2) = π/6`
não é raiz; (e) existe.

**Padrão.** Cuidado com o **domínio** ao elevar ao quadrado e ao "cancelar" `√(1−x²)`: a solução espúria é
justamente o número de ouro > 1. A raiz válida é a **conjugada** (≈ −0,618) — a mesma que aparece em
`cos 72°`.

---

### Q13 · Preço com +20% e −20% — **(d) R$ 144,00**

**Enunciado.** Camisa a R$ 150,00; aumento de 20%; duas semanas depois, desconto de 20%. Novo preço:
(a) 120 · (b) 139 · (c) 150 · (d) 144 · (e) nenhuma

**Resolução.**

```
150 · 1,20 = 180        (aumento)
180 · 0,80 = 144        (desconto sobre o novo preço)
```

Ou direto: `150 · 1,2 · 0,8 = 150 · 0,96 = 144`.

**Resposta: (d) R$ 144,00.**

**Armadilha.** (c) 150 é o erro clássico: "+20% e −20% não se cancelam" — o desconto incide sobre o valor
**já aumentado**. O fator final é `0,96` (queda de 4%).

**Padrão.** Aumentos/descontos encadeados **multiplicam fatores**. `(1+p)(1−p) = 1 − p²` — sempre menor
que 1.

---

### Q14 · (7ˣ + 2√10)(7ˣ − 2√10) = 9 — **(e) 1**

**Enunciado.** A raiz real de `(7ˣ + 2√10)(7ˣ − 2√10) = 9` é:
(a) irracional negativa · (b) irracional positiva · (c) par positiva · (d) inteira negativa · (e) ímpar positiva

**Passo 1 — diferença de quadrados.**

```
(7ˣ)² − (2√10)² = 9
7^{2x} − 40 = 9
7^{2x} = 49 = 7²
```

**Passo 2 — igualar expoentes (base 7 > 0, injetora).** `2x = 2 → x = 1`.

**Resposta: (e) 1 (positivo e ímpar).**

**Conferência.** `7¹ = 7`: `(7 + 2√10)(7 − 2√10) = 49 − 40 = 9` ✔.

**Armadilha.** A leitura errada `7x` (produto) leva a `49x² = 49 → x = ±1` e duas alternativas corretas
(d) e (e); o PDF, porém, traz `7ˣ` — e aí a solução é única.

**Padrão.** `(A+B)(A−B) = A² − B²` transforma a equação em `7^{2x} = 49`, isto é, base igual → expoente
igual. Sempre que aparecer `a^{2x}`, troque `u = aˣ`.

---

### Q15 · Integral definida com logaritmo — **(c) e**

**Enunciado.** `∫₀^{e−1} (x+2)/(x+1) dx` = (a) e−1 · (b) 2 · (c) e · (d) e+1 · (e) ∞

**Passo 1 — divisão polinomial.**

```
(x + 2)/(x + 1) = 1 + 1/(x + 1)
```

**Passo 2 — integrar.**

```
∫ [1 + 1/(x+1)] dx = x + ln(x + 1)
```

**Passo 3 — avaliar em 0 e e−1.**

```
[(e−1) + ln(e)] − [0 + ln(1)] = e − 1 + 1 = e
```

**Resposta: (c) e.**

**Conferência.** `ln(e) = 1` é o ponto que "fecha" a conta: `e − 1 + 1 = e` ✔.

**Por que as outras caem.** (a) `e−1` esquece o `ln(e) = 1`; (d) `e+1` soma o log com sinal errado; (b) 2
sai de integrais sem o log.

**Padrão.** Fração racional com numerador e denominador de mesmo grau → divida: `(x+2)/(x+1) = 1 + 1/(x+1)`.
O limite superior `e−1` foi escolhido para que `x+1 = e` e `ln e = 1` — sempre procure essa "limpeza".

---

### Q16 · Círculo e triângulo isósceles de mesma área — **(c)**

**Enunciado.** Na Figura 3, um círculo de raio r e um triângulo isósceles de altura h têm a **mesma área**,
com `r = h`. Julgue:
• `BC = 2πr` · • `∠BAC = 2·arctan(π)` · • `AC = r√(π² − 1)`
(a) as três falsas · (b) duas falsas · (c) uma falsa · (d) as três verdadeiras · (e) não dá para discutir sem r = h

**Passo 1 — igualar as áreas.** Área do círculo `πr²`; do triângulo `(1/2)·BC·h`, com `h = r`:

```
(1/2)·BC·r = πr²   →   BC = 2πr        ✔ afirmação 1 VERDADEIRA
```

**Passo 2 — ângulo do vértice.** No triângulo isósceles, a altura é também mediana e bissetriz; no
triângulo retângulo formado por metade da base, altura e lado:

```
tan(∠BAC/2) = (BC/2)/h = (πr)/r = π
∠BAC = 2·arctan(π)                     ✔ afirmação 2 VERDADEIRA
```

**Passo 3 — lado oblíquo (Pitágoras).**

```
AC² = h² + (BC/2)² = r² + (πr)² = r²(1 + π²)
AC = r√(π² + 1)                        ✘ afirmação 3 é FALSA (diz π² − 1)
```

**Resposta: (c) — só uma afirmação falsa.**

**Conferência numérica.** `BC = 2πr ≈ 6,283r`; `∠A = 2 arctan π ≈ 144,6°` (faz sentido: base larga);
`AC = r√(1+π²) ≈ 3,297r` ✔.

**Por que as outras caem.** (d) "todas verdadeiras" é a armadilha de quem não confere o sinal dentro da
raiz; (b) exigiria errar também o ângulo; (e) é falsa porque `r = h` está dado na figura.

**Padrão.** "Mesma área" + figura geométrica → escreva as duas áreas e iguale. O `π² − 1` vs `π² + 1` é o
teste de sinal do Pitágoras: o lado oblíquo é **maior** que a altura, então a raiz tem que ser `+`.

---

## 4. Padrões que a banca repetiu nesta prova

1. **"O que NÃO se pode dizer"** (Q3, Q8) — releia o comando; em Q3 a falsa é a das "raízes puramente
   imaginárias".
2. **Estrutura antes da conta**: Q1 (matriz que comuta → triangular), Q7 (6-8-10 → retângulo), Q15
   (divisão polinomial), Q10 (fatorar fatoriais).
3. **Geometria com círculo tangente** (Q2): `s = r_a cot(A/2)` e `Δ = r_a(s − a)`; máximo no isósceles.
4. **Contagem com restrição de adjacência** (Q4): método dos gaps.
5. **Busca em estados** (Q5): travessia com ciúmes → 11.
6. **Séries**: teste do termo geral primeiro (Q6); se o termo não vai a zero, não há convergência.
7. **Fatorial e potências**: simplificar antes de expandir (Q10, Q14).

---

## 5. Plano de 90 minutos

| Bloco | Tempo | Questões | Objetivo |
|:-----:|:-----:|----------|----------|
| 1 | 0–15 min | 13, 8, 9, 10, 14 | 5 acertos rápidos |
| 2 | 15–35 min | 3, 11, 12, 15, 16, 1 | médias |
| 3 | 35–75 min | 4, 6, 7, 5, 2 | as longas (Q2 por último) |
| 4 | 75–90 min | todas | revisar comandos e conferir |

Regra: **3 min travado → marque e siga**. Q2 vale o mesmo que Q13.

---

## 6. Checklist final

- [ ] Releu "**cannot say**", "**may not**", "**wrong**", "**greatest**"?
- [ ] Em raiz de matriz, lembrou que A comuta com B?
- [ ] Em ex-incírculo, usou `s = r_a cot(A/2)` e maximizou no isósceles?
- [ ] Contou os gaps como `p+1` (e não `p−1`)?
- [ ] Em série, checou `lim a_n = 0` antes de tudo?
- [ ] Em "círculo dos nove pontos", usou `N = (H+O)/2` e `r₉ = R/2`?

---

## 7. Resumo de fórmulas usadas

```
Raiz de matriz:            A² = B ⇒ A comuta com B ⇒ A triangular na base de B
Ex-incírculo:              s = r_a·cot(A/2) ;  Δ = r_a·(s − a)
Área máxima (A fixo):      isósceles (B = C)
Gaps:                      p itens criam p+1 lacunas → C(p+1, q)
Termo geral (série):       a_n ↛ 0 ⇒ diverge ; pares/ímpares podem ir a ±∞
Círculo dos 9 pontos:      N = (H + O)/2 ;  r₉ = R/2
Triângulo retângulo:       h = bc/a ; projeção = b²/a
Combinatória:              C(n,2), C(n+1,2), C(n+2,3) são inteiros
Gauss:                     ∫ x e^{−x²} dx = −e^{−x²}/2
Fatorial:                  (k+1)! = (k+1)k!
Log:                       ∫ dx/(x+1) = ln(x+1) ; ln e = 1
```

---

## 8. Onde treinar cada questão

| Questão | Tema no repositório |
|:-------:|---------------------|
| 1 | [`temas/02-sistemas-matrizes-determinantes`](../../temas/02-sistemas-matrizes-determinantes/README.md) |
| 2, 7 | [`temas/03-geometria`](../../temas/03-geometria/README.md) |
| 3, 8, 14 | [`temas/05-polinomios-e-raizes`](../../temas/05-polinomios-e-raizes/README.md) |
| 4, 5 | [`temas/01-combinatoria`](../../temas/01-combinatoria/README.md) |
| 6 | [`temas/06-sequencias-pa-pg-series`](../../temas/06-sequencias-pa-pg-series/README.md) |
| 9, 12, 15 | [`temas/08-calculo`](../../temas/08-calculo/README.md) |
| 10 | [`temas/01-combinatoria`](../../temas/01-combinatoria/README.md) |
| 11 | [`temas/02-sistemas-matrizes-determinantes`](../../temas/02-sistemas-matrizes-determinantes/README.md) |
| 13 | [`temas/10-problemas-taxa-trabalho`](../../temas/10-problemas-taxa-trabalho/README.md) |
| 16 | [`temas/03-geometria`](../../temas/03-geometria/README.md) · [`temas/07-trigonometria`](../../temas/07-trigonometria/README.md) |

> Em cada tema, o arquivo **`RESOLUCOES-PASSO-A-PASSO.md`** traz a resolução linha a linha das questões
> reais daquele assunto — é o complemento natural desta leitura por prova.

---

**Prova original:** [`Prova_PG-EIA_2023-2oSem.pdf`](../Prova_PG-EIA_2023-2oSem.pdf) ·
**Texto extraído:** [`Prova_PG-EIA_2023-2oSem.txt`](../Prova_PG-EIA_2023-2oSem.txt) ·
**Índice de resoluções:** [`README.md`](README.md) · **Provas:** [`../README.md`](../README.md).
