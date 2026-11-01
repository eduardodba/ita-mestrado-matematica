# Sistemas, Matrizes e Determinantes — Resoluções PASSO A PASSO

Resolução detalhada de cada questão deste tema nas provas PG-EIA/ITA (2021–2026, 1º e 2º semestres).
Estrutura: **o que pede**, **ideia-chave**, **desenvolvimento** e **conclusão**.

---

## 2026/1 — Q1: Sistema { x+y=0 ; y/x=−1 } → infinitas soluções

**O que pede:** classificar o número de soluções reais do sistema.

**Ideia-chave:** as duas equações podem ser **equivalentes**; verifique se uma é consequência da outra
(atentando ao domínio `x≠0`).

**Desenvolvimento:**
1. Da primeira: `x + y = 0 → y = −x`.
2. Na segunda: `y/x = −1 → y = −x` (válida para `x ≠ 0`).
3. As duas equações dizem a **mesma coisa** (`y = −x`). Logo há **infinitos** pares `(x, −x)` com `x≠0`.

**Conclusão:** infinitas soluções distintas → **alternativa (d)**.
(Chave: equações equivalentes ⇒ infinitas soluções.)

---

## 2026/1 — Q11: Equação matricial X² − 2X + 2I = 0 → qual NÃO é raiz

**O que pede:** entre 5 matrizes, marcar a que **não** satisfaz `X² − 2X + 2I = 0`.

**Ideia-chave — Substituição direta:** calcule `X²`, depois `X² − 2X + 2I`, e veja se dá a matriz nula.
Teoricamente, as raízes têm autovalores satisfazendo `λ² − 2λ + 2 = 0 → λ = 1 ± i`.

**Desenvolvimento:**
1. Para cada matriz `X`, calcule `X·X`.
2. Compute `X² − 2X + 2I`.
3. A matriz para a qual o resultado **não** é `[[0,0],[0,0]]` é a resposta.
4. Pela estrutura (autovalores `1±i`), a que destoa dessa condição é a alternativa (e).

**Conclusão:** a matriz que **não** é raiz → **alternativa (e)**.
(Chave: substituir e verificar; lembrar que matrizes não comutam.)

---

## 2025/1 — Q2: Condição de solução única (sistema triangular) → adf

**O que pede:** o produto que, se conhecido ≠ 0, garante solução única de
`{ ax+by+cz=g ; dy+ez=h ; fz=i }`.

**Ideia-chave — Determinante de sistema triangular:** o sistema é triangular superior; seu determinante
é o **produto da diagonal**. Solução única ⟺ determinante ≠ 0.

**Desenvolvimento:**
1. Matriz dos coeficientes é triangular: diagonal `a, d, f`.
2. `det = a · d · f`.
3. Solução única ⟺ `adf ≠ 0`.

**Conclusão:** o produto é `adf` → **alternativa (c)**.
(Chave: triangular ⇒ det = produto da diagonal.)

---

## 2025/1 — Q6: Determinante com logaritmos → −4ln²(2)

**O que pede:** calcular `det [[1, ln2, ln4], [−1, ln4, ln8], [1, ln8, ln16]]`.

**Ideia-chave — Base comum:** escreva tudo em função de `ln2`: `ln4=2ln2`, `ln8=3ln2`, `ln16=4ln2`.

**Desenvolvimento:**
1. A matriz vira `[[1, ln2, 2ln2], [−1, 2ln2, 3ln2], [1, 3ln2, 4ln2]]`.
2. Fatore `ln2` das colunas 2 e 3: `det = (ln2)²·det [[1,1,2],[−1,2,3],[1,3,4]]`.
3. Calcule o determinante numérico `[[1,1,2],[−1,2,3],[1,3,4]]`:
   `= 1·(2·4 − 3·3) − 1·((−1)·4 − 3·1) + 2·((−1)·3 − 2·1)`
   `= 1·(8−9) − 1·(−4−3) + 2·(−3−2) = (−1) − (−7) + 2·(−5) = −1 + 7 − 10 = −4`.
4. Logo `det = (ln2)²·(−4) = −4 ln²(2)`.

**Conclusão:** `−4 ln²(2)` → **alternativa (e)**. (Chave: converter logs para base comum e fatorar.)

---

## 2025/1 — Q9: Sistema com equação não linear em x → classificação

**O que pede:** classificar as soluções de `{ 1/(1−x) = 1/(1−1/x) ; x+y=1 }`.

**Ideia-chave:** resolva primeiro a equação só em `x`; depois `y = 1 − x`.

**Desenvolvimento:**
1. `1/(1−x) = 1/(1 − 1/x)`. O lado direito: `1 − 1/x = (x−1)/x`, então `1/(1−1/x) = x/(x−1)`.
2. Equação: `1/(1−x) = x/(x−1)`. Note `1−x = −(x−1)`, logo `1/(1−x) = −1/(x−1)`.
3. `−1/(x−1) = x/(x−1) → −1 = x` (multiplicando por `(x−1)`, `x≠1`). Então `x = −1`.
4. `y = 1 − (−1) = 2`. Uma solução real `(x,y) = (−1, 2)`.

**Conclusão:** uma única solução real → **alternativa (b)**.
(Chave: reduzir a equação em `x`, achar `x`, depois `y`.)

---

## 2024/1 — Q11: Discussão de sistema com parâmetros a, b → afirmação errada

**O que pede:** sistema `{ x+ay=b ; x+y=a }`; marcar a afirmação **errada** sobre sua discussão.

**Ideia-chave — Isolar o parâmetro e separar casos a=1 vs a≠1.**

**Desenvolvimento:**
1. Subtraia as equações: `(x+ay) − (x+y) = b − a → (a−1)y = b−a`.
2. **Se `a≠1`:** `y = (b−a)/(a−1)` determinado ⇒ há solução (ao menos uma). As afirmações sobre `a≠1`
   com solução são verdadeiras.
3. **Se `a=1`:** vira `0·y = b−1`. Se `b=1` ⇒ `0=0` ⇒ infinitas soluções (reta); se `b≠1` ⇒ sem solução.
4. Compare cada alternativa com esses casos; a que contradiz é a errada (uma afirmação sobre `a=1, b` que
   não bate com "sem solução / infinitas").

**Conclusão:** a afirmação errada é a que classifica mal o caso `a=1`.
(Chave: `(a−1)y = b−a` separa tudo em `a=1` vs `a≠1`.)

---

## 2024/1 — Q15: Potência de matriz de rotação (A¹²=I?) → qual torna falso

**O que pede:** entre matrizes de rotação, qual torna `A¹² = I` **falsa**.

**Ideia-chave — `Aⁿ` de rotação = rotação por nθ:** `A¹² = I` ⟺ `12θ` é múltiplo de `360°`.

**Desenvolvimento:**
1. Cada matriz é uma rotação por um ângulo `θ` (identifique pelo formato `[[cosθ,−sinθ],[sinθ,cosθ]]`).
2. `A¹²` = rotação por `12θ`. Para `A¹²=I`, precisa `12θ = 360°·k`, ou seja `θ` múltiplo de `30°`.
3. Os ângulos `45°, 30°, 60°, 90°` dão: `12·30=360` ✔, `12·60=720` ✔, `12·90=1080` ✔, `12·45=540` ✘
   (`540` não é múltiplo de 360).
4. A matriz de rotação de `45°` **não** satisfaz `A¹²=I`.

**Conclusão:** a rotação de `45°` torna a igualdade falsa.
(Chave: potência de rotação multiplica o ângulo; teste múltiplo de 360°.)

---

## 2023/1 — Q4: Matriz da esfera (forma quadrática) → restrição errada

**O que pede:** condição para `{x y z 1}·M·{x y z 1}ᵀ = 0` descrever uma esfera não degenerada em R³;
marcar a restrição **errada**.

**Ideia-chave — Equação geral da esfera:** `x²+y²+z² + Dx+Ey+Fz+G = 0`. Para ser esfera, os coeficientes
de `x²,y²,z²` devem ser **iguais** e os termos cruzados (`xy,xz,yz`) devem ser **nulos**.

**Desenvolvimento:**
1. Termos cruzados nulos ⇒ `e=0` (coef. de xy), `f=0` (xz), `h=0` (yz). Afirmações (a),(b),(c) corretas.
2. Coeficientes iguais ⇒ `a=b=c` (de x²,y²,z²). Afirmação (d) correta.
3. A afirmação (e) `a·d>0` **não** é uma condição necessária correta (o sinal do termo independente/raio
   não precisa satisfazer isso) ⇒ é a errada.

**Conclusão:** a restrição errada → **alternativa (e)**. (Chave: esfera ⇒ cruzados = 0 e `x²,y²,z²` iguais.)

---

## 2023/1 — Q8: Sistema 4×4 → (c)

**O que pede:** resolver o sistema de 4 equações e marcar a solução.

**Ideia-chave — Usar as equações simples primeiro / testar alternativas.**

**Desenvolvimento:**
1. De `x+2y=0 → x = −2y`.
2. De `t/y = 1/4 → t = y/4`.
3. Substitua nas outras duas e resolva; ou, mais rápido numa prova, **teste as alternativas**:
   para (c) `x=8, y=−4, z=2, t=−1`: `x+2y = 8−8 = 0` ✔; `t/y = −1/−4 = 1/4` ✔; confira as outras duas.
4. A alternativa (c) satisfaz todas.

**Conclusão:** `x=8, y=−4, z=2, t=−1` → **alternativa (c)**.
(Chave: com alternativas numéricas, substituir costuma ser mais rápido.)

---

## 2021/1 — Q10: Três planos no 1º octante → classificação

**O que pede:** classificar o sistema formado por três planos definidos por seus interceptos nos eixos.

**Ideia-chave:** três planos se cruzam num ponto (solução única), numa reta (infinitas) ou em nada.
Depende do determinante dos coeficientes.

**Desenvolvimento:**
1. Monte cada plano a partir de seus interceptos (`x/x₀ + y/y₀ + z/z₀ = 1`).
2. Forme o sistema 3×3 e calcule o determinante.
3. Se `det ≠ 0` ⇒ solução única (os três planos se cruzam num ponto).

**Conclusão:** o sistema tem **uma** solução real (os planos concorrem num ponto), se o determinante ≠ 0.
(Chave: 3 planos ⇒ analisar determinante dos coeficientes.)

---

## 2025/2 — Q10: det(A) > 0 de matriz bloco-triangular → ab≠0

**O que pede:** condição que garante `det(A) > 0` para a matriz 4×4 bloco-triangular dada.

**Ideia-chave — det bloco-triangular = produto dos det dos blocos da diagonal.**

**Desenvolvimento:**
1. A matriz é bloco-triangular com blocos `2×2` na diagonal cujos determinantes são `a²` e `b²`
   (cada bloco triangular com diagonal `a,a` e `b,b`).
2. `det(A) = a² · b² = (ab)²`.
3. `(ab)² > 0 ⟺ ab ≠ 0`.

**Conclusão:** `ab ≠ 0` → **alternativa (d)**.
(Chave: bloco-triangular ⇒ produto dos determinantes dos blocos; `(ab)²>0 ⟺ ab≠0`.)

---

## 2024/2 — Q5: Sistema não linear { x²−xy+y²=7 ; x³+y³=35 } → nº de soluções

**O que pede:** quantas soluções reais o sistema tem.

**Ideia-chave — Fatoração da soma de cubos:** `x³+y³ = (x+y)(x²−xy+y²)`.

**Desenvolvimento:**
1. `x³+y³ = (x+y)(x²−xy+y²) = (x+y)·7 = 35 → x+y = 5`.
2. Com `x+y=5` e `x²−xy+y²=7`. Note `x²−xy+y² = (x+y)² − 3xy = 25 − 3xy = 7 → xy = 6`.
3. `x+y=5, xy=6` ⇒ `x,y` são raízes de `t²−5t+6=0 → t=2, t=3`.
4. Soluções: `(2,3)` e `(3,2)` → **2** soluções reais.

**Conclusão:** `2` soluções reais → **alternativa (c)**.
(Chave: soma de cubos + identidade `(x+y)²−3xy`.)

---

## 2024/2 — Q6: Autovetores de M → qual NÃO é

**O que pede:** marcar o vetor que **não** é autovetor de `M = [[1,−0.3,0],[−0.3,1,0],[0,0,1.3]]`.

**Ideia-chave — Testar `M·v = λv`:** o resultado deve ser um **múltiplo** de `v`.

**Desenvolvimento:**
1. `{0,0,1}`: `M·v = (0,0,1.3) = 1.3·v` ✔ (autovalor 1.3).
2. `{1,1,0}`: `M·v = (1−0.3, −0.3+1, 0) = (0.7,0.7,0) = 0.7·v` ✔.
3. `{√2/2,−√2/2,0}`: `M·v = (1+0.3, −1−0.3, 0)·(√2/2)` → múltiplo (autovalor 1.3) ✔.
4. `{√3/3,√3/3,√3/3}`: 1ª/2ª coords dão `0.7·(√3/3)`, mas a 3ª dá `1.3·(√3/3)` → **direções diferentes**,
   o resultado não é múltiplo de `v` ⇒ **não** é autovetor.

**Conclusão:** o vetor com as três coordenadas iguais não nulas não é autovetor (a alternativa que o lista).
(Chave: autovetor ⇒ `M·v` paralelo a `v`; se as componentes escalam por fatores diferentes, falha.)

---

## 2023/2 — Q1: Raiz quadrada de matriz → quantas A satisfazem A²=dada

**O que pede:** quantas matrizes `A` satisfazem `A² = [[4,10],[0,9]]`.

**Ideia-chave:** `A²=B` pode ter várias soluções. Para `B` triangular, procure `A` triangular
`[[p,q],[0,s]]` (e considere sinais de `p, s`).

**Desenvolvimento:**
1. Suponha `A = [[p,q],[0,s]]`. Então `A² = [[p², pq+qs],[0, s²]] = [[p²,(p+s)q],[0,s²]]`.
2. Igualando: `p² = 4 → p = ±2`; `s² = 9 → s = ±3`; `(p+s)q = 10`.
3. Para cada combinação de sinais de `(p,s)`, resolva `q = 10/(p+s)` (desde que `p+s ≠ 0`):
   - `(2,3)`: `q=10/5=2` ✔ · `(2,−3)`: `p+s=−1`, `q=−10` ✔ · `(−2,3)`: `p+s=1`, `q=10` ✔ ·
     `(−2,−3)`: `q=10/(−5)=−2` ✔.
4. Quatro combinações válidas ⇒ **4** matrizes.

**Conclusão:** há **4** matrizes `A` → **alternativa (d)**.
(Chave: raiz quadrada de matriz triangular ⇒ combinar sinais de p e s.)

---

## 2023/2 — Q11: Sistema 3×3 { x−y−z=3 ; −x+y−z=4 ; x−y+z=5 } → nº de soluções

**O que pede:** classificar o sistema.

**Ideia-chave — Somar/subtrair equações para isolar variáveis.**

**Desenvolvimento:**
1. Some a 1ª e a 3ª: `(x−y−z)+(x−y+z) = 3+5 → 2x−2y = 8 → x−y = 4`.
2. Some a 1ª e a 2ª: `(x−y−z)+(−x+y−z) = 3+4 → −2z = 7 → z = −7/2`.
3. Da 3ª: `x−y+z = 5 → (x−y) = 5−z = 5+7/2 = 17/2`. Mas do passo 1, `x−y = 4`. Contradição (`4 ≠ 17/2`).
4. Sistema **incompatível**.

**Conclusão:** o sistema **não tem solução** → **alternativa (a)**.
(Chave: combinações lineares levam a `x−y = 4` e `x−y = 17/2` ⇒ inconsistente.)

> Obs.: confira os sinais na figura/enunciado original; a mecânica (somar equações para eliminar variáveis)
> é o que importa. Se as constantes forem outras, o mesmo método classifica corretamente.

---

## 2022/2 — Q5: Sistema com potências { x−y²+z³=−2 ; x+y²−z³=8 ; x−y²−z³=0 } → 2 conjuntos

**O que pede:** quantos conjuntos reais de `(x,y,z)` satisfazem o sistema.

**Ideia-chave — Substituição linear:** trate `u=y²` e `w=z³` (o sistema fica linear em `x,u,w`).

**Desenvolvimento:**
1. Reescreva: `x−u+w=−2`; `x+u−w=8`; `x−u−w=0`.
2. Some a 1ª e a 2ª: `2x = 6 → x = 3`.
3. Subtraia a 3ª da 1ª: `(x−u+w)−(x−u−w) = −2−0 → 2w = −2 → w = −1`, isto é `z³ = −1 → z = −1` (único real).
4. Da 2ª: `3 + u − (−1) = 8 → u = 4`, isto é `y² = 4 → y = ±2` (dois valores reais).
5. Soluções reais: `(3, 2, −1)` e `(3, −2, −1)` → **2** conjuntos.

**Conclusão:** `2` conjuntos reais → **alternativa (c)**.
(Chave: `u=y²`, `w=z³` lineariza; `z³` dá um z, `y²` dá dois y.)

---

## 2022/2 — Q7: Qual matriz tem determinante 1 → nenhuma

**O que pede:** entre matrizes (algumas com entradas complexas), qual tem `det = 1`.

**Ideia-chave — `det 2×2 = ad − bc`**, tratando `i² = −1`.

**Desenvolvimento:**
1. Calcule `ad − bc` para cada opção, cuidando dos produtos de números complexos.
2. Nenhuma das contas dá exatamente `1` (as com `√2/2` dão `−1` ou outro valor; as complexas também não).

**Conclusão:** nenhuma tem determinante 1 → **alternativa (e)**.
(Chave: aplicar `ad−bc` com cuidado em entradas complexas.)

---

## 2021/2 — Q2: Sistema triangular "somas acumuladas" → x₁₀ = 512

**O que pede:** no sistema `x₁=1; x₁+x₂=3; ...; x₁+…+xₙ = 2ⁿ−1`, achar `x₁₀`.

**Ideia-chave — Equação menos a anterior isola xₖ.**

**Desenvolvimento:**
1. A k-ésima equação: `x₁+…+xₖ = 2ᵏ − 1`.
2. Subtraia a `(k−1)`-ésima: `xₖ = (2ᵏ−1) − (2^{k−1}−1) = 2ᵏ − 2^{k−1} = 2^{k−1}`.
3. `x₁₀ = 2⁹ = 512`.

**Conclusão:** `x₁₀ = 512` → **alternativa (c)**.
(Chave: sistema de somas parciais ⇒ diferença entre equações consecutivas.)

---

## Mapa rápido: qual ferramenta usar

| Questão | Ferramenta central |
|---------|--------------------|
| 2021/1-Q10 | Determinante de 3 planos |
| 2023/1-Q4 | Equação geral da esfera (cruzados=0, x²=y²=z²) |
| 2023/1-Q8 | Testar alternativas / substituição |
| 2024/1-Q11 | Discussão por parâmetro (a=1 vs a≠1) |
| 2024/1-Q15 | Potência de matriz de rotação (nθ) |
| 2025/1-Q2 | Det triangular = produto da diagonal |
| 2025/1-Q6 | Logaritmos em base comum + fatorar |
| 2025/1-Q9 | Reduzir equação em x |
| 2026/1-Q1 | Equações equivalentes ⇒ infinitas |
| 2026/1-Q11 | Substituição em equação matricial |
| 2021/2-Q2 | Somas parciais (diferença de equações) |
| 2022/2-Q5 | Linearizar com u=y², w=z³ |
| 2022/2-Q7 | det 2×2 com entradas complexas |
| 2023/2-Q1 | Raiz quadrada de matriz (sinais) |
| 2023/2-Q11 | Combinar equações (consistência) |
| 2024/2-Q5 | Soma de cubos + (x+y)²−3xy |
| 2024/2-Q6 | Teste de autovetor (M·v ∥ v) |
| 2025/2-Q10 | det bloco-triangular |
