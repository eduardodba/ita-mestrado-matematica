# Revisão das provas de 2º SEMESTRE — Sistemas, Matrizes e Determinantes

Revisão completa das **5 provas de 2º semestre (2021 a 2025)** para este tema.
Gabaritos oficiais: 2022-2ºSem e 2025-2ºSem.

---

### 2025/2º — Q10: Determinante de matriz bloco-triangular
Given A = [[a,c,e,e],[0,a,e,e],[0,0,b,d],[0,0,0,b]], which option ensures det(A) > 0?
(a) c⁴de>0 · (b) a+b>0 · (c) a²+b²>0 · (d) ab≠0 · (e) cde≠0
**Gabarito: (d)** — matriz triangular em blocos: `det = a·a·b·b = a²b²`. Para `>0` basta `ab≠0`
(ou seja, `a≠0` e `b≠0`), pois `a²b²>0`.
**Lição:** determinante de **matriz triangular = produto da diagonal**; aqui `(a²)(b²)`.

---

### 2024/2º — Q5: Sistema não linear
{ x²−xy+y² = 7 ; x³+y³ = 35 }. How many solutions?
(a) no real · (b) 1 · (c) 2 · (d) 3 · (e) 6 real solutions
→ Use `x³+y³ = (x+y)(x²−xy+y²)` → `(x+y)·7 = 35 → x+y=5`. Depois resolva com `x²−xy+y²=7`.

### 2024/2º — Q6: Autovetores
For M = [[1,−0.3,0],[−0.3,1,0],[0,0,1.3]], mark the option that is NOT an eigenvector:
(a) {√2/2,−√2/2,0} · (b) {0,0,1} · (c) {√3/3,−√3/3,√3/3} · (d) {1,1,0} · (e) {√3/3,√3/3,√3/3}
→ Teste `M·v = λv` para cada vetor. Os que **não** mantêm a direção não são autovetores.
**Conceito novo deste tema:** autovalores/autovetores (`[M]{v}=λ{v}`).

---

### 2023/2º — Q1: Raiz quadrada de matriz
If [A]² = [[4,10],[0,9]], one can say that
(a) only one matrix A · (b) only two · (c) only three · (d) only four · (e) no matrix A satisfies it
→ Procure matrizes `A` cujo quadrado dá a matriz dada (há múltiplas "raízes quadradas" de matriz).

### 2023/2º — Q11: Discussão de sistema 3×3
{ x−y−z=3 ; −x+y−z=4 ; x−y+z=5 } one can say that
(a) no real solutions · (b) one real solution · (c) two · (d) more than two · (e) more info needed
→ Some/subtraia as equações: some (1) e (3) → `2(x−y)=8`? Resolva; o determinante define a natureza.

---

### 2022/2º — Q5: Sistema com potências (substituição)
{ x−y²+z³=−2 ; x+y²−z³=8 ; x−y²−z³=0 } one can say that it has
(a) 6 · (b) 3 · (c) 2 · (d) 1 · (e) 0 sets of real roots
**Gabarito: (c)** — trate `u=y²`, `w=z³` (lineares em x,u,w); ache `x,u,w`, depois volte a `y=±√u`.
Como `y²` dá dois sinais de y mas `z³` dá um único z, conte os conjuntos reais.

### 2022/2º — Q7: Qual matriz tem determinante 1
Which matrix has determinant equal to 1? (opções com entradas √2/2, complexas i...)
**Gabarito: (e)** — None of them. Calcule `det 2×2 = ad−bc` de cada; nenhuma dá exatamente 1.

---

### 2021/2º — Q2: Sistema triangular "soma acumulada"
System x₁=1; x₁+x₂=3; x₁+x₂+x₃=7; ...; x₁+...+xₙ=2ⁿ−1. Find x₁₀.
(a) 255 · (b) 333 · (c) 512 · (d) 1024 · (e) none
→ Cada `xₖ = (2ᵏ−1) − (2^{k−1}−1) = 2^{k−1}`. Logo `x₁₀ = 2⁹ = 512`. Resposta **(c)**.
**Lição:** a k-ésima equação menos a anterior isola `xₖ` (sistema triangular).

---

## Observação sobre frequência (2º sem)
O tema apareceu em **todas** as 5 provas de 2º semestre. Destaques:
- **Discussão de sistema** (2021/2, 2022/2, 2023/2) — o mesmo padrão dos 1ºs semestres.
- **Determinante** por triangularização (2025/2, 2022/2).
- **Conceito novo que vale revisar:** autovalores/autovetores (2024/2-Q6) e raiz quadrada de matriz
  (2023/2-Q1). Confirma prioridade ALTA.

---

## Conceitos novos que os 2ºs semestres cobraram (revisão)

### Autovalores e autovetores ⭐ (2024/2-Q6)
`[M]{v} = λ{v}`: `v` (não nulo) é **autovetor** e `λ` o **autovalor** associado.
- Para testar se `v` é autovetor: calcule `M·v` e veja se o resultado é **múltiplo** de `v`
  (mesma direção). Se for `λv`, é autovetor com autovalor `λ`.
- Autovalores saem de `det(M − λI) = 0` (polinômio característico).
- Matriz simétrica tem autovetores ortogonais entre si.

### Raiz quadrada de matriz (2023/2-Q1)
`A² = B` pode ter **várias** soluções `A` (0, 2, 4...), diferente de números reais.
Para `B` diagonal/triangular, monte `A = [[p,q],[r,s]]`, eleve ao quadrado e resolva o sistema.

### Determinante de matriz triangular e bloco-triangular
- Triangular (superior ou inferior): `det = produto da diagonal`.
- Bloco-triangular: `det = produto dos determinantes dos blocos da diagonal`.
  Em 2025/2-Q10, a matriz 4×4 tem blocos 2×2 → `det = (a·a)·(b·b) = a²b²`.

### Sistema triangular por "diferença de equações" (2021/2-Q2)
Quando as equações são somas parciais acumuladas, **cada equação menos a anterior** isola uma incógnita.

---

## Resoluções detalhadas

### 2025/2 — Q10 (det > 0 → ab≠0)
A é bloco-triangular com blocos `[[a,c],[0,a]]` e `[[b,d],[0,b]]` na diagonal (olhando a estrutura).
`det = a²·b²`, sempre ≥ 0. Para ser **estritamente** positivo, basta `a≠0` e `b≠0`, ou seja `ab≠0`.
**Resposta (d).**

### 2024/2 — Q6 (não é autovetor)
`M = [[1,−0.3,0],[−0.3,1,0],[0,0,1.3]]`. Teste cada vetor:
- `{√2/2,−√2/2,0}`: `M·v` nas 2 primeiras coords dá `(1+0.3, −1−0.3, 0)·(√2/2)` → múltiplo (λ=1.3). ✔
- `{0,0,1}`: `M·v = (0,0,1.3)` = 1.3·v. ✔
- `{1,1,0}`: `M·v = (1−0.3, −0.3+1, 0) = (0.7,0.7,0)` = 0.7·v. ✔
- `{√3/3,√3/3,√3/3}`: 3ª coord vira 1.3·(√3/3), mas 1ª/2ª viram 0.7·(√3/3) → **não é múltiplo** (direção muda).
→ o vetor que **não** mantém a direção é o que **não** é autovetor. Verifique entre (c) e (e).

### 2021/2 — Q2 (x₁₀ = 512)
A k-ésima equação é `x₁+…+xₖ = 2ᵏ−1`. Subtraindo a anterior: `xₖ = (2ᵏ−1)−(2^{k−1}−1) = 2^{k−1}`.
`x₁₀ = 2⁹ = 512`. **Resposta (c).**

---

## Exercícios de treino (2º sem)

**T1.** `v = (1,1)` é autovetor de `M = [[2,1],[1,2]]`? Se sim, qual o autovalor?

**T2.** Calcule o determinante de `[[3,5,7],[0,2,9],[0,0,4]]`.

**T3.** Quantas matrizes reais 2×2 diagonais `A` satisfazem `A² = [[9,0],[0,4]]`?

**T4.** No sistema `x₁=2; x₁+x₂=6; x₁+x₂+x₃=12;…; x₁+…+xₙ=n²+n`, ache `x₅`.

---

## Gabarito dos exercícios (2º sem)

**T1.** `M·(1,1) = (3,3) = 3·(1,1)`. Sim, autovetor com **autovalor 3**.

**T2.** Triangular → produto da diagonal `= 3·2·4 = 24`.

**T3.** `A` diagonal `[[p,0],[0,s]]` com `p²=9, s²=4` → `p=±3`, `s=±2` → `2×2 = 4` matrizes.

**T4.** `xₖ = (k²+k) − ((k−1)²+(k−1)) = 2k`. Logo `x₅ = 10`.
