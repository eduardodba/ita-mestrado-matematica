# Lema de Burnside — do zero, bem devagar 🌟

> Este é o método das questões de **"colorir um cubo/sólido/figura considerando que girar não cria algo
> novo"** — caiu em 2021, 2024, 2025 e 2026. Aqui vamos construir a ideia **do zero**, com um exemplo
> pequenininho primeiro (dá para desenhar no papel), e só depois chegar na fórmula.

---

## PARTE 1 — Entendendo o problema SEM fórmula nenhuma

### O incômodo central
Suponha que você vai pintar as 3 "contas" de um **colar triangular** (3 posições num triângulo), e tem
**2 cores**: Preto (P) e Branco (B).

Se você contar "na força bruta", cada posição tem 2 escolhas → `2 × 2 × 2 = 8` pinturas:

```
1) PPP      2) PPB      3) PBP      4) BPP
5) PBB      6) BPB      7) BBP      8) BBB
```

Mas um colar pode ser **girado**. Se eu giro o colar, `PPB`, `PBP` e `BPP` são **o mesmo colar** visto de
ângulos diferentes (um P e dois... não — um B e dois P, colocados em rotação). Então, na prática, não são
8 colares distintos. Quantos são **de verdade**?

### Contando "na mão" (agrupando os iguais)
Vamos juntar as 8 pinturas em grupos, onde cada grupo reúne as que viram a mesma coisa ao girar:

- **Grupo 1:** `PPP` — girar não muda nada. (1 pintura)
- **Grupo 2:** `BBB` — idem. (1 pintura)
- **Grupo 3:** `PPB`, `PBP`, `BPP` — são rotações umas das outras (dois P, um B). (3 pinturas → 1 colar)
- **Grupo 4:** `BBP`, `BPB`, `PBB` — rotações umas das outras (dois B, um P). (3 pinturas → 1 colar)

São **4 colares realmente diferentes**: `PPP`, `BBB`, "dois P e um B", "dois B e um P".

> 🎯 **Esse "4" é a resposta.** O Lema de Burnside é só uma **máquina para chegar nesse 4 sem precisar
> listar e agrupar tudo à mão** — o que seria impossível num cubo (com 24 rotações).

---

## PARTE 2 — As três palavras que você precisa

1. **Rotação (ou simetria):** um jeito de girar o objeto deixando-o "no mesmo lugar". O colar triangular
   tem **3 rotações**: girar 0° (não mexer), girar 120° e girar 240°.
2. **Grupo `G`:** o conjunto dessas rotações. Aqui `G = {0°, 120°, 240°}`, então **|G| = 3**.
3. **Coloração fixada por uma rotação `g`** (notação `Fix(g)`): é uma pintura que, **depois** de aplicar
   `g`, fica **idêntica** à de antes. (Como se a rotação não tivesse efeito visível naquela pintura.)

---

## PARTE 3 — O coração do método: contar `Fix(g)` com CICLOS

Toda rotação **embaralha as posições**. A pergunta-chave é: *quais posições trocam de lugar entre si?*
Isso forma os **ciclos**.

### Exemplo no colar triangular (posições 1, 2, 3)
- **Rotação 0° (identidade):** ninguém se move. Ciclos: `(1)(2)(3)` → **3 ciclos**.
- **Rotação 120°:** a posição 1 vai para onde estava a 2, a 2 para a 3, a 3 para a 1. Ciclo: `(1 2 3)`
  → **1 ciclo** (um único ciclo com as 3 posições).
- **Rotação 240°:** 1→3→2→1. Ciclo: `(1 3 2)` → **1 ciclo**.

### A regra de ouro
> Para uma pintura ficar **inalterada** por uma rotação, **todas as posições de um mesmo ciclo têm que
> ter a MESMA cor** (senão, ao girar, uma cor apareceria onde estava outra, e a figura mudaria).

Então, se a rotação tem `c` ciclos e você tem `k` cores:
> **Fix(g) = k^c** — cada ciclo escolhe livremente 1 cor (k opções), e são `c` ciclos independentes.

### Aplicando no colar (k = 2 cores):
| Rotação | Ciclos | Nº de ciclos `c` | Fix = `2^c` |
|---------|--------|:----------------:|:-----------:|
| 0° | (1)(2)(3) | 3 | `2³ = 8` |
| 120° | (1 2 3) | 1 | `2¹ = 2` |
| 240° | (1 3 2) | 1 | `2¹ = 2` |

**Lendo a tabela:**
- Em 0°, qualquer uma das 8 pinturas fica igual (a identidade nunca muda nada) → `Fix = 8`.
- Em 120°, para a pintura não mudar, as 3 posições (que estão todas no mesmo ciclo) precisam da mesma cor
  → só `PPP` e `BBB` servem → `Fix = 2`.
- Em 240°, mesma coisa → `Fix = 2`.

---

## PARTE 4 — A fórmula do Lema de Burnside (finalmente)

> **Número de colorações distintas = (soma de todos os `Fix(g)`) ÷ (número de rotações `|G|`)**
>
> Ou seja: é a **média** de `Fix(g)` sobre todas as rotações.

### No nosso colar:
```
soma dos Fix = 8 + 2 + 2 = 12
|G| = 3
distintas = 12 / 3 = 4   ✅
```

**Deu 4** — exatamente o que contamos na mão na Parte 1! A fórmula funciona, e agora podemos usá-la em
objetos onde contar à mão seria inviável.

### Por que dividir pela média funciona? (intuição)
Pense assim: cada colar **realmente distinto** é "visto" várias vezes quando você soma os `Fix`. A soma
conta cada pintura uma vez para cada rotação que a deixa parada. Quando você divide pelo total de
rotações, esses excessos se cancelam **na média exata**, sobrando o número de classes. (É um teorema
demonstrado — para a prova, basta confiar e aplicar.)

---

## PARTE 5 — Exemplo médio: quadrado com 2 cores (caiu em 2021!)

Pintar as **4 casas de um quadrado** com 2 cores, considerando iguais as que são rotação uma da outra.
O quadrado tem **4 rotações**: 0°, 90°, 180°, 270° → `|G| = 4`.

**Como cada rotação embaralha as 4 casas** (numere-as 1,2,3,4 em volta):
| Rotação | O que faz | Ciclos | `c` | Fix = `2^c` |
|---------|-----------|--------|:---:|:-----------:|
| 0° | nada | (1)(2)(3)(4) | 4 | `2⁴ = 16` |
| 90° | 1→2→3→4→1 | (1 2 3 4) | 1 | `2¹ = 2` |
| 180° | 1↔3, 2↔4 | (1 3)(2 4) | 2 | `2² = 4` |
| 270° | 1→4→3→2→1 | (1 4 3 2) | 1 | `2¹ = 2` |

```
soma dos Fix = 16 + 2 + 4 + 2 = 24
|G| = 4
distintas = 24 / 4 = 6
```

**São 6 pinturas distintas do quadrado.** (Confere com a questão 2021/1-Q11.)

> 💡 Repare no padrão: a **identidade** sempre dá `k^(nº de posições)` (aqui `2⁴`), e é o maior termo.
> As outras rotações têm menos ciclos, logo contribuem menos.

---

## PARTE 6 — O CUBO (o caso que mais cai)

Pintar as **6 faces** de um cubo. O grupo de rotações do cubo tem **24 rotações**, de 5 tipos.
Esta é a tabela que vale a pena ter em mente — mostra como cada tipo de rotação embaralha as **6 faces**:

| Tipo de rotação | Quantas | Como age nas 6 faces | Nº de ciclos `c` |
|-----------------|:-------:|----------------------|:----------------:|
| Identidade (0°) | 1 | cada face parada: (1)(2)(3)(4)(5)(6) | **6** |
| Eixo por centros de faces, 90° e 270° | 6 | 2 faces paradas + 4 girando juntas: (1)(2)(3 4 5 6) | **3** |
| Eixo por centros de faces, 180° | 3 | 2 paradas + 2 pares: (1)(2)(3 5)(4 6) | **4** |
| Eixo por 2 vértices opostos, ±120° | 8 | duas triplas de faces: (1 2 3)(4 5 6) | **2** |
| Eixo por meios de arestas opostas, 180° | 6 | três pares: (1 2)(3 4)(5 6) | **3** |
| **Total** | **24** | | |

Confira o total: `1 + 6 + 3 + 8 + 6 = 24` ✔.

### Exemplo A — 6 faces com `k` cores livres (cada face qualquer cor)
Some `(quantas rotações) × k^(ciclos)` por tipo:
```
Fix total = 1·k⁶  +  6·k³  +  3·k⁴  +  8·k²  +  6·k³
          = k⁶ + 3k⁴ + 12k³ + 8k²        (juntando 6k³ + 6k³ = 12k³)
distintas = (k⁶ + 3k⁴ + 12k³ + 8k²) / 24
```
Com `k = 2` (preto/branco): `(64 + 48 + 96 + 32)/24 = 240/24 = `**10** colorações distintas do cubo.

### Exemplo B — 6 cores TODAS diferentes, uma por face (caiu em 2025!)
Aqui vem o atalho mais útil da prova. Se as 6 cores são **todas distintas**, uma rotação de verdade
**sempre** embaralha faces de cores diferentes → nenhuma pintura fica parada, exceto na identidade:
```
Fix(identidade) = 6! = 720   (as 6 cores nas 6 posições)
Fix(qualquer outra das 23)   = 0
distintas = (720 + 0) / 24 = 30
```
> 🎯 **Decore:** cubo + 6 cores distintas (uma por face) → sempre `6!/24 = 30`.

---

## PARTE 7 — Quando há restrição (ex.: "exatamente 2 faces vermelhas")

Quando a questão **limita** as cores (ex.: 2026/1-Q5: "2 faces vermelhas + 4 cores diferentes"), a
fórmula `k^c` não serve direto, porque nem toda cor é livre. Dois caminhos:

**Caminho 1 (Burnside restrito):** para cada rotação, conte quantas pinturas **que respeitam a restrição**
ficam paradas. Some e divida por `|G|`.

**Caminho 2 (separar em casos — costuma ser mais rápido numa prova):** fixe a posição relativa das peças
repetidas. No caso "2 faces vermelhas", elas só podem estar **opostas** ou **adjacentes**:
- **Opostas** (topo/base): sobram 4 faces em anel para 4 cores distintas; as rotações que mantêm as
  vermelhas no lugar são os 4 giros em torno do eixo vertical → `4!/4 = 6` pinturas.
- **Adjacentes** (compartilham aresta): o grupo que preserva essa configuração é menor; a contagem dá
  `9` pinturas.
- Total: `6 + 9 = 15`. (É a resposta da 2026/1-Q5.)

---

## PARTE 8 — Receita de bolso para a prova

Quando ler *"...up to rotations / considering rotations as equal / aligned by a 3D rotation..."*:

1. **Conte as rotações** do objeto → isso é `|G|`.
   - triângulo plano: 3 · quadrado: 4 · pentágono: 5 · cubo (faces): 24 · tetraedro: 12.
2. Para **cada** rotação, descubra os **ciclos** das posições e conte quantos são (`c`).
3. `Fix = k^c` (sem restrição). Com restrição, conte à mão as pinturas válidas que ficam paradas.
4. **Some tudo e divida por `|G|`.**
5. Com cores todas distintas: só a identidade conta → resposta `= (nº posições)! / |G|`.

---

## PARTE 9 — Exercícios (resolvidos ao final)

**B1.** Colar triangular (3 contas) com **3 cores**, só rotações. Quantos colares distintos?

**B2.** Quadrado (4 casas) com **3 cores**, só rotações. Quantos?

**B3.** Cubo, 6 faces, **2 cores** (cada face preta ou branca). Quantos? (use o Exemplo A)

**B4.** Colar de **4 contas** com 2 cores, só rotações. Quantos?

**B5.** Pentágono (5 vértices) com 2 cores, só rotações (|G|=5). Quantos?

---

## PARTE 10 — Gabarito dos exercícios (com a conta)

**B1.** `|G|=3`, `k=3`.
```
0°:  (1)(2)(3)  → 3 ciclos → 3³ = 27
120°:(1 2 3)    → 1 ciclo  → 3¹ = 3
240°:(1 3 2)    → 1 ciclo  → 3¹ = 3
soma = 27+3+3 = 33 → 33/3 = 11 colares.
```

**B2.** `|G|=4`, `k=3` (mesma estrutura do quadrado da Parte 5):
```
0°: 3⁴=81 · 90°: 3¹=3 · 180°: 3²=9 · 270°: 3¹=3
soma = 81+3+9+3 = 96 → 96/4 = 24.
```

**B3.** Fórmula do cubo com `k=2`: `(2⁶ + 3·2⁴ + 12·2³ + 8·2²)/24 = (64+48+96+32)/24 = 240/24 = 10`.

**B4.** Colar de 4 contas = mesma estrutura do quadrado, `k=2`: `(16+2+4+2)/4 = 24/4 = 6`.

**B5.** Pentágono, `|G|=5`, `k=2`. A identidade dá `2⁵=32`; cada uma das 4 rotações próprias é um único
ciclo de 5 posições → `2¹=2` cada:
```
soma = 32 + 2 + 2 + 2 + 2 = 40 → 40/5 = 8 colares.
```

---

### Resumo de uma linha
> **Burnside = média, sobre todas as rotações, de "quantas pinturas aquela rotação não muda".**
> E "quantas não muda" = `k^(número de ciclos da rotação)`.
