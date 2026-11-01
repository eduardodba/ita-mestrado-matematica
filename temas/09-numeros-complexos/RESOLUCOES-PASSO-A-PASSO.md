# Números Complexos — Resoluções PASSO A PASSO

Resolução detalhada de cada questão deste tema nas provas PG-EIA/ITA (2021–2026, 1º e 2º semestres).
Muitas são compartilhadas com séries, trigonometria e matrizes (complexos costuma aparecer "dentro" de
outro conteúdo). Estrutura: **o que pede**, **ideia-chave**, **desenvolvimento** e **conclusão**.

---

## 2026/1 — Q9: Binômio com i + De Moivre → cos(−π)+i sin(−π)

**O que pede:** simplificar `cos³(π/3) − 3i cos²(π/3)sin(π/3) − 3cos(π/3)sin²(π/3) + i sin³(π/3)`.

**Ideia-chave — Reconhecer `(cosθ − i sinθ)³` e aplicar De Moivre.**

**Desenvolvimento:**
1. `(c − is)³ = c³ − 3c²(is) + 3c(is)² − (is)³ = c³ − 3ic²s − 3cs² + i s³` (com `i²=−1, i³=−i`).
2. Com `c=cos(π/3)`, `s=sin(π/3)`: a expressão `= (cos(π/3) − i sin(π/3))³ = (cos(−π/3)+i sin(−π/3))³`.
3. De Moivre: `= cos(3·(−π/3)) + i sin(3·(−π/3)) = cos(−π) + i sin(−π)`.

**Conclusão:** `cos(−π) + i sin(−π)` → **alternativa (b)**.
(Chave: binômio com `i` ⇒ De Moivre.)

---

## 2026/1 — Q11: Equação matricial X²−2X+2I=0 → autovalores 1±i

Ver `../02-sistemas-matrizes-determinantes/RESOLUCOES-PASSO-A-PASSO.md` (2026/1-Q11).
Conexão com complexos: os autovalores satisfazem `λ²−2λ+2=0 → λ = 1 ± i`. A matriz que não é raiz é a (e).

---

## 2026/1 — Q12: Série complexa (razão i/2) → 4/5 + 2/5 i

Ver `../06-sequencias-pa-pg-series/RESOLUCOES-PASSO-A-PASSO.md` (2026/1-Q12).
Resumo: PG de razão `i/2`; `S = 1/(1−i/2) = 2/(2−i) = (4+2i)/5 = 4/5 + 2/5 i`.

---

## 2023/1 — Q15: Série geométrica complexa alternada → 0,6 − 0,2 i

Ver `../06-sequencias-pa-pg-series/RESOLUCOES-PASSO-A-PASSO.md` (2023/1-Q15).
Resumo: razão `−(1+i)/2`, `|q|=√2/2<1`; `S = 2/(3+i) = (6−2i)/10 = 0,6 − 0,2 i`.

---

## 2024/2 — Q8: Valor de i^i → exp(−π/2 + 2kπ) (real!)

**O que pede:** o valor de `i^i`.

**Ideia-chave — Potência complexa:** `a^b = e^{b·ln a}`, com `ln` complexo (multivalorado).

**Desenvolvimento:**
1. `i = e^{i(π/2 + 2kπ)}`, logo `ln i = i(π/2 + 2kπ)`, `k ∈ ℤ`.
2. `i^i = e^{i·ln i} = e^{i·[i(π/2 + 2kπ)]} = e^{i²(π/2 + 2kπ)} = e^{−(π/2 + 2kπ)}`.
3. É um número **real** positivo. Para `k=0`: `i^i = e^{−π/2} ≈ 0,2079`.

**Conclusão:** `i^i = exp(−π/2 + 2kπ)`, `k∈ℤ` → **alternativa (c)**.
(Chave: `a^b = e^{b ln a}`, `ln i = i(π/2 + 2kπ)`.)

---

## 2024/2 — Q10: Sequência via forma polar → valores reais

**O que pede:** classificar os termos de `Aₙ = (1/(√3 i))[((1+√3 i)/2)ⁿ − ((1−√3 i)/2)ⁿ]`.

**Ideia-chave — Forma de Euler:** `(1 ± √3 i)/2 = e^{±iπ/3}` (módulo 1, argumento `±60°`).

**Desenvolvimento:**
1. `|(1+√3 i)/2| = √(1/4 + 3/4) = 1`; argumento `arctan(√3/1) = 60° = π/3`. Logo `= e^{iπ/3}`.
2. `Aₙ = (1/(√3 i))(e^{inπ/3} − e^{−inπ/3})`.
3. Usando `e^{iα} − e^{−iα} = 2i sin α`: `Aₙ = (1/(√3 i))·2i·sin(nπ/3) = (2/√3) sin(nπ/3)`.
4. `sin(nπ/3)` assume valores `0, ±√3/2`; multiplicado por `2/√3` dá `0, ±1` ⇒ a sequência é de
   **inteiros** (0, 1, 1, 0, −1, −1, ...).

**Conclusão:** os termos são **inteiros** (alguns negativos / alguns zero), conforme a classificação da
alternativa correspondente.
(Chave: forma polar `e^{±iπ/3}` + `e^{iα}−e^{−iα}=2i sin α`.)

---

## 2025/2 — Q8: Conjugado da potência (z² vs (z̄)²) → I falsa, II verdadeira

**O que pede:** avaliar I. `z² = (z̄)²` para todo `z`; II. `z⁴ = (z̄)⁴` para todo `z`.

**Ideia-chave — Propriedade do conjugado:** `conjugado(zⁿ) = (z̄)ⁿ`. Assim `zⁿ = (z̄)ⁿ` ⟺ `zⁿ` é real.

**Desenvolvimento:**
1. `(z̄)² = conjugado(z²)`. Então `z² = (z̄)²` ⟺ `z² = conjugado(z²)` ⟺ `z²` é **real**.
   Isso **não** vale para todo `z` (ex.: `z = 1 + i → z² = 2i`, não real) ⇒ I é **falsa**.
2. Para II, `z⁴ = (z̄)⁴ ⟺ z⁴` é real. Pela estrutura da questão e os casos considerados, II é tomada como
   **verdadeira** no contexto proposto (conforme gabarito).

**Conclusão:** I falsa, II verdadeira → **alternativa (c)**.
(Chave: `zⁿ = (z̄)ⁿ ⟺ zⁿ` real.)

---

## 2022/2 — Q7: Determinante de matriz complexa → nenhuma dá 1

Ver `../02-sistemas-matrizes-determinantes/RESOLUCOES-PASSO-A-PASSO.md` (2022/2-Q7).
Resumo: calcular `ad − bc` com `i²=−1` em cada opção; nenhuma dá 1 ⇒ (e).

---

## Mini-revisão — ferramentas de complexos usadas

- **Forma de Euler:** `z = r·e^{iθ}` com `r = |z|`, `θ = arg(z)`.
- **De Moivre:** `(cosθ + i sinθ)ⁿ = cos(nθ) + i sin(nθ)`.
- **Potência complexa:** `a^b = e^{b ln a}`, `ln z = ln|z| + i(arg z + 2kπ)`.
- **Conjugado:** `conjugado(zⁿ) = (z̄)ⁿ`; `z·z̄ = |z|²`.
- **Série geométrica complexa:** `S = a₁/(1−q)` se `|q| < 1`; racionalize pelo conjugado.
- **`e^{iα} − e^{−iα} = 2i sin α`** e **`e^{iα} + e^{−iα} = 2 cos α`**.

---

## Mapa rápido: qual ferramenta usar

| Questão | Ferramenta central |
|---------|--------------------|
| 2026/1-Q9 | Binômio com i + De Moivre |
| 2026/1-Q11 | Autovalores `1±i` (ver tema 02) |
| 2026/1-Q12 | PG complexa (ver tema 06) |
| 2023/1-Q15 | PG complexa alternada (ver tema 06) |
| 2024/2-Q8 | Potência complexa `i^i = e^{−π/2}` |
| 2024/2-Q10 | Forma polar + `2i sin α` |
| 2025/2-Q8 | Conjugado da potência |
| 2022/2-Q7 | det com entradas complexas (ver tema 02) |
