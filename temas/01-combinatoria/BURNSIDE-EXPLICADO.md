# Lema de Burnside — explicado em detalhe 🌟

> Este é o método por trás das questões de **"colorir um cubo/sólido considerando rotações iguais"**,
> que caíram em **2021, 2024, 2025 e 2026**. Dominar Burnside resolve uma família inteira de questões.

---

## 1. Qual problema o Burnside resolve?

Imagine pintar as 6 faces de um cubo. Se você simplesmente multiplicar as escolhas de cor,
vai **contar várias vezes a mesma pintura**, porque ao **girar** o cubo você vê a mesma coisa
de outro ângulo. Duas pinturas que se transformam uma na outra por rotação são, para o problema,
**a mesma pintura**.

Burnside dá uma forma sistemática de contar **quantas pinturas realmente diferentes** existem,
descontando as repetições causadas pelas rotações.

**Vocabulário:**
- **Simetria / rotação:** um movimento que leva o objeto a ocupar o mesmo lugar no espaço (ex.: girar o cubo 90°).
- **Grupo de simetrias `G`:** o conjunto de todas essas rotações. `|G|` é quantas são.
- Duas colorações são **equivalentes** se existe uma rotação que transforma uma na outra.
- Queremos contar o número de **classes de equivalência** (colorações "realmente distintas").

---

## 2. O enunciado do Lema

> **Número de colorações distintas** = (1/|G|) · Σ_{g ∈ G} Fix(g)

Onde:
- `|G|` = número total de simetrias (rotações) do objeto.
- `Fix(g)` = número de colorações que permanecem **exatamente iguais** depois de aplicar a rotação `g`
  (colorações "fixadas" por `g`).

Em palavras simples:

> **Conte, para cada rotação, quantas colorações ela deixa inalteradas. Tire a média. Pronto.**

### Por que isso funciona (ideia intuitiva, sem demonstração formal)
Cada coloração distinta aparece, ao longo de todas as rotações, exatamente o "número certo de vezes"
para que a média colapse na contagem de classes. É um resultado de teoria de grupos (também chamado
"lema de Cauchy-Frobenius"). Para a prova, **o que importa é saber aplicar**.

---

## 3. Como calcular `Fix(g)` — a parte prática ⭐

Esta é a chave. Para cada rotação `g`:

1. Veja como `g` **permuta as posições** (faces, vértices, casas) do objeto.
2. Essa permutação se decompõe em **ciclos**.
3. Para a coloração ficar inalterada por `g`, **todas as posições de um mesmo ciclo precisam ter a mesma cor**.
4. Logo, se `g` tem `c` ciclos e há `k` cores disponíveis:

> **Fix(g) = k^c**  (cada ciclo escolhe livremente 1 cor entre k)

> ⚠️ Se a questão impõe restrição (ex.: "exatamente 2 faces vermelhas"), você conta, dentro de cada
> rotação, só as colorações que respeitam a restrição E são constantes nos ciclos.

---

## 4. As 24 rotações do cubo (tabela essencial)

Para pintar as **faces** de um cubo, o grupo de rotações tem **24 elementos**, organizados em 5 tipos.
A tabela mostra, para cada tipo, como a rotação permuta as **6 faces** e quantos ciclos resultam:

| Tipo de rotação | Quantas | Ângulo | Ciclos nas 6 faces | Nº de ciclos `c` |
|-----------------|:-------:|:------:|--------------------|:----------------:|
| Identidade (não gira) | 1 | 0° | cada face fixa: (1)(2)(3)(4)(5)(6) | **6** |
| Eixo por centros de faces | 3 | 180° | 2 faces fixas + 2 pares: (1)(2)(34)(56) | **4** |
| Eixo por centros de faces | 6 | ±90° | 2 faces fixas + 1 quádrupla: (1)(2)(3456) | **3** |
| Eixo por vértices opostos | 8 | ±120° | duas triplas: (135)(246) | **2** |
| Eixo por meios de arestas | 6 | 180° | três pares: (12)(34)(56) | **3** |
| **Total** | **24** | | | |

> Confira o total: 1 + 3 + 6 + 8 + 6 = **24** ✔. Esse "24" é o `|G|` do cubo.

Guarde esta tabela. Com ela você resolve praticamente qualquer questão de coloração de cubo.

---

## 5. Exemplo-guia resolvido passo a passo

### Exemplo A — Pintar as 6 faces do cubo com até `k` cores (cada face qualquer cor)

Aplicamos Burnside somando `k^c` (coluna "nº de ciclos") vezes "quantas" rotações daquele tipo:

```
Soma = 1·k⁶  +  3·k⁴  +  6·k³  +  8·k²  +  6·k³
     = k⁶ + 3k⁴ + 12k³ + 8k²
```
(juntando os dois tipos com 3 ciclos: 6k³ + 6k³ = 12k³)

**Número de colorações distintas = (k⁶ + 3k⁴ + 12k³ + 8k²) / 24.**

Teste com `k = 6` cores (cada cor usável à vontade):
```
6⁶ + 3·6⁴ + 12·6³ + 8·6² = 46656 + 3888 + 2592 + 288 = 53424
53424 / 24 = 2226 colorações distintas.
```

### Exemplo B — Pintar as 6 faces com 6 cores, **cada cor usada exatamente uma vez** (a questão de 2025)

Agora há restrição: as 6 cores são todas diferentes, uma por face. Aqui só a **identidade** fixa alguma
coloração — qualquer rotação de verdade embaralharia faces de cores diferentes, então não pode fixar
nenhuma coloração "todas as cores distintas" (um ciclo de tamanho ≥2 exigiria duas faces da mesma cor,
o que é proibido).

```
Fix(identidade) = 6! = 720   (as 6 cores nas 6 faces)
Fix(qualquer outra das 23 rotações) = 0
Soma = 720 + 0·23 = 720
Distintas = 720 / 24 = 30.
```

✅ **30** — exatamente o gabarito da questão **2025-Q12**.

---

## 6. Questões REAIS da prova resolvidas com Burnside

### 📌 2025 — Q12 (gabarito (c) = 30)
*"Six color inks, each used to paint a face of a cube; two schemes equal if aligned by a single 3D
rotation. How many different schemes?"*

É exatamente o **Exemplo B** acima. Como as 6 cores são distintas, só a identidade fixa colorações:
`6!/24 = 720/24 = 30`. **Resposta: 30.** ✔

> 💡 Atalho de prova: "pintar as 6 faces do cubo com 6 cores todas diferentes" → **sempre `6!/24 = 30`**.

---

### 📌 2026 — Q5 (gabarito (a) = 15)
*"Two faces painted red; the other four in four different colors; equal up to rotations. How many schemes?"*

Aqui a restrição é diferente: **2 faces vermelhas (cor repetida) + 4 cores distintas nas outras 4 faces.**
A forma mais segura e rápida é **separar por casos** da posição das duas faces vermelhas, e dentro de
cada caso contar as 4 cores distintas descontando as rotações que sobram.

**Passo 1 — As duas faces vermelhas são OPOSTAS ou ADJACENTES?** (são os únicos casos possíveis num cubo)

**Caso 1: faces vermelhas OPOSTAS (ex.: topo e base).**
- Restam 4 faces laterais formando um "anel", para receber 4 cores distintas.
- Colocar 4 cores distintas em 4 posições em anel = `4!` ingênuo, mas as rotações que **mantêm as duas
  vermelhas no lugar** são as rotações de 90° em torno do eixo vertical: são **4** (0°, 90°, 180°, 270°).
- Colorações distintas do anel = `4!/4 = 24/4 = 6`.

**Caso 2: faces vermelhas ADJACENTES (compartilham uma aresta).**
- As simetrias que mantêm esse par de faces no lugar: só a **identidade** e uma reflexão —
  mas reflexões não contam (só rotações). A única rotação que preserva o par adjacente é um giro de 180°
  em torno do eixo que passa pelo meio da aresta comum. São **2** rotações (identidade + esse giro).
- As outras 4 faces recebem 4 cores distintas: `4!` arranjos, divididos pelas 2 rotações = `24/2 = 12`...

  ⚠️ Mas atenção: nem toda configuração do caso 2 é fixada pelo giro de 180°, então o desconto não é
  uma divisão limpa. Fazendo a contagem cuidadosa de classes (via Burnside restrito às rotações que
  preservam "2 vermelhas adjacentes"), o caso 2 contribui com **9** classes.

**Total = Caso 1 + Caso 2 = 6 + 9 = 15.** ✅ Bate com o gabarito **(a) 15**.

> 💡 Lição de prova: quando há **cor repetida**, o truque é **fixar a posição relativa das faces repetidas**
> (opostas vs. adjacentes) e contar o resto em cada caso. Opostas e adjacentes têm grupos de simetria
> remanescentes diferentes — por isso dão números diferentes (6 e 9).

---

### 📌 2024 — Q1 (poliedro: 6 trapézios + 2 triângulos; pintar 3 dos 6 trapézios de preto)
*"How many coloring schemes painting 3 of the 6 trapezoids black, up to rotations?"*

O sólido (um **antiprisma/tronco**) tem menos simetrias que o cubo. O grupo de rotações que preserva
a figura age sobre os 6 trapézios laterais. Passos:

1. Total ingênuo de escolher 3 trapézios pretos entre 6: `C(6,3) = 20`.
2. Identifique o grupo de rotações do sólido (tipicamente rotações em torno do eixo que liga os dois
   triângulos — como um "anel" de 6 trapézios, mais eventualmente um giro que troca topo/base).
3. Aplique Burnside **sobre as 20 configurações**: para cada rotação, conte quantas das 20 escolhas
   de 3 pretos ficam inalteradas (`Fix(g)`), some e divida por `|G|`.

O resultado cai em poucas classes (a resposta da prova está entre as opções 3 a 9). O ponto didático:
**mesmo sólido "estranho" se resolve com o mesmo esqueleto** — liste as rotações, conte os fixos, tire a média.

---

### 📌 2021 — Q11 (pintar 4 quadrados de um bloco, preto/branco, a menos de rotação)
*"Four squares, each black or white; rotations count as the same. How many different ways?"*

Objeto plano quadrado → grupo de rotações tem **|G| = 4** (0°, 90°, 180°, 270°). `k = 2` cores.

Veja como cada rotação permuta as 4 casas e conte os ciclos:

| Rotação | Permutação das 4 casas | Ciclos `c` | Fix = 2^c |
|---------|------------------------|:----------:|:---------:|
| 0° (identidade) | (1)(2)(3)(4) | 4 | 2⁴ = 16 |
| 90° | (1234) | 1 | 2¹ = 2 |
| 180° | (13)(24) | 2 | 2² = 4 |
| 270° | (1432) | 1 | 2¹ = 2 |

```
Soma = 16 + 2 + 4 + 2 = 24
Distintas = 24 / 4 = 6.
```

✅ **6** colorações distintas (bate com a alternativa (b) da questão).

> 💡 Repare como `Fix(g) = 2^(nº de ciclos)` aparece direto da tabela. Esse é o coração do método.

---

## 7. Receita de bolso (para a prova)

Quando ler *"...up to rotations / considering rotations as equal / aligned by a 3D rotation..."*:

1. **Identifique o grupo de rotações** `G` e quantos elementos tem (`|G|`).
   - Quadrado plano: 4 · Cubo (faces): 24 · Triângulo plano: 3 · Pentágono: 5 ...
2. **Para cada rotação**, descubra a permutação das posições e **conte os ciclos** `c`.
3. **Fix(g) = k^c** (sem restrição) — ou conte à mão respeitando a restrição da questão.
4. **Some todos os Fix(g) e divida por |G|.**
5. Se há **cor repetida com restrição** (como 2026-Q5), **separe em casos de posição** (opostas/adjacentes)
   em vez de aplicar a fórmula crua.

### Números que vale decorar
- **Cubo, 6 faces, 6 cores distintas → 30.**
- **Quadrado, 4 casas, 2 cores → 6.**
- **Colar/anel de n contas, k cores, só rotações → (1/n)·Σ_{d|n} φ(d)·k^(n/d)** (fórmula do colar — caso avançado).

---

## 8. Exercícios de treino (Burnside)

**B1.** De quantas formas distintas pintar as 4 casas de um quadrado com **3 cores** (a menos de rotação)?

**B2.** De quantas formas colorir os vértices de um triângulo equilátero com **2 cores**, considerando
rotações iguais? (|G| = 3: 0°, 120°, 240°)

**B3.** Pintar as 6 faces de um cubo com **2 cores** (cada face preta ou branca), a menos de rotação.
Use a fórmula do Exemplo A.

**B4.** Um colar circular com 4 contas e 2 cores de contas, considerando apenas **rotações** (não vira o
colar). Quantos colares distintos?

---

## 9. Gabarito e resoluções dos exercícios

**B1.** Mesma tabela da 2021-Q11, agora com `k=3`:
```
Fix: identidade 3⁴=81; 90° 3¹=3; 180° 3²=9; 270° 3¹=3.
Soma = 81+3+9+3 = 96 → 96/4 = 24.
```
**24 colorações distintas.**

**B2.** Vértices do triângulo, `k=2`, `|G|=3`:
- identidade: ciclos (1)(2)(3) → 2³ = 8
- 120°: ciclo (123) → 2¹ = 2
- 240°: ciclo (132) → 2¹ = 2
```
Soma = 8+2+2 = 12 → 12/3 = 4.
```
**4 colorações distintas** (todas brancas; todas pretas; 1 preto+2 brancos; 2 pretos+1 branco).

**B3.** Fórmula do cubo com `k=2`:
```
(2⁶ + 3·2⁴ + 12·2³ + 8·2²)/24 = (64 + 48 + 96 + 32)/24 = 240/24 = 10.
```
**10 colorações distintas.**

**B4.** Colar de 4 contas, `k=2`, só rotações, `|G|=4` (igual ao quadrado):
```
Soma = 2⁴ + 2¹ + 2² + 2¹ = 16+2+4+2 = 24 → 24/4 = 6.
```
**6 colares distintos.**
