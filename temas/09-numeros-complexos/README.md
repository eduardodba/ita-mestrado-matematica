# Tema 09 — Números Complexos 🟡

**Prioridade: APOIO.** Alterna entre os anos (forte em 2026 e 2023). Muitas vezes aparece
**dentro** de outro tema (séries complexas, De Moivre em trigonometria, autovalores em matrizes).

---

## 1. Conceitos e teoremas que você precisa saber

### 1.1 Forma algébrica
- `z = a + bi`, com `i² = −1`. Parte real `a`, imaginária `b`.
- **Conjugado:** `z̄ = a − bi`. `z·z̄ = a² + b² = |z|²`.
- **Módulo:** `|z| = √(a²+b²)`.
- **Divisão:** multiplique numerador e denominador pelo **conjugado** do denominador:
  `1/(a+bi) = (a−bi)/(a²+b²)`.

### 1.2 Forma polar (trigonométrica)
- `z = |z|·(cosθ + i sinθ)`, onde `θ = arg(z) = arctan(b/a)` (ajustando o quadrante).
- Multiplicação: **módulos multiplicam, argumentos somam**.

### 1.3 Fórmula de De Moivre ⭐
> `(cosθ + i sinθ)ⁿ = cos(nθ) + i sin(nθ)`

Usada para **potências** e **raízes** de complexos.
- Raízes n-ésimas de `z`: `n` soluções distribuídas igualmente no círculo de raio `|z|^(1/n)`,
  com argumentos `(θ + 2kπ)/n`, `k=0..n−1`.

### 1.4 Séries geométricas complexas
A fórmula `S = a₁/(1−q)` vale para razão complexa com `|q| < 1`. (ver tema 06)

### 1.5 Conexão com matrizes
Equações matriciais `X²−2X+2I=0` têm "autovalores" `λ=1±i` (raízes de `λ²−2λ+2=0`). (ver tema 02)

---

## 2. Resoluções comentadas (questões reais do ITA)

### 📌 2026 — Q9: `cos³ − 3i cos²sin − 3cos sin² + i sin³` (De Moivre)
Gabarito: **(b) cos(−π) + i sin(−π)**.

**Resolução:** os coeficientes `1, −3i, −3, +i` são a expansão de `(cosθ − i sinθ)³`:
`(c − is)³ = c³ − 3c²(is) + 3c(is)² − (is)³ = c³ − 3ic²s − 3cs² + i s³` ✔.
Então a expressão `= (cos(π/3) − i sin(π/3))³ = cos(−π/3)³`... aplique De Moivre:
`= cos(3·(−π/3)) + i sin(3·(−π/3)) = cos(−π) + i sin(−π)`.
**Lição:** reconheça o **binômio com `i`** e aplique **De Moivre** direto.

### 📌 2026 — Q12: Série complexa (ver também tema 06)
Razão `i/2`, `S = 4/5 + 2/5 i`. **Lição:** `S=a₁/(1−q)` + conjugado para racionalizar.

### 📌 2026 — Q11: Equação matricial com autovalores complexos (ver tema 02)
`X²−2X+2I=0` ⟹ `λ=1±i`. **Lição:** complexos aparecem como autovalores.

### 📌 2023 — Q15: Série geométrica complexa alternada
`S = 0,6 − 0,2 i`. **Lição:** razão `−(1+i)/2`, `|q|=√2/2<1` converge; racionalize.

---

## 3. Exercícios de treino

**E1.** Calcule `(1 + i)²`.

**E2.** Qual o módulo de `z = 3 + 4i`?

**E3.** Escreva `1/(2 − i)` na forma `a + bi`.

**E4.** Use De Moivre para calcular `(1 + i)⁸`. *(dica: `1+i = √2·(cos45° + i sin45°)`)*

**E5.** Some a série `1 + (i/3) + (i/3)² + (i/3)³ + …`.

**E6.** Quais são as raízes quadradas de `i`?

---

## 4. Gabarito e resoluções

**E1.** `(1+i)² = 1 + 2i + i² = 1 + 2i − 1 = 2i`.

**E2.** `|z| = √(3²+4²) = √25 = 5`.

**E3.** `1/(2−i) = (2+i)/((2−i)(2+i)) = (2+i)/5 = 2/5 + (1/5)i`.

**E4.** `|1+i|=√2`, arg `45°`. `(1+i)⁸ = (√2)⁸·(cos(8·45°)+i sin(8·45°)) = 16·(cos360°+i sin360°) = 16·1 = 16`.

**E5.** Razão `q=i/3`, `|q|=1/3<1`: `S = 1/(1−i/3) = 3/(3−i) = 3(3+i)/10 = 9/10 + (3/10)i`.

**E6.** `i = cos90° + i sin90°`. Raízes: `cos45°+i sin45° = (√2/2)(1+i)` e `cos225°+i sin225° = −(√2/2)(1+i)`.
Ou seja `±(√2/2)(1+i)`.

---

## 5. Banco de questões reais

As questões deste tema nas 6 provas (2021–2026), com enunciado original em inglês e gabarito
(quando divulgado), estão em **[QUESTOES-DAS-PROVAS.md](QUESTOES-DAS-PROVAS.md)**.
