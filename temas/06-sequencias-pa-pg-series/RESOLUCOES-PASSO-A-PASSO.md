# Sequências, PA/PG e Séries — Resoluções PASSO A PASSO

Resolução detalhada de cada questão deste tema nas provas PG-EIA/ITA (2021–2026, 1º e 2º semestres).
Estrutura: **o que pede**, **ideia-chave**, **desenvolvimento** e **conclusão**.

---

## 2026/1 — Q12: Série complexa 1 + (1/2)i − 1/4 − (1/8)i + ... → 4/5 + 2/5 i

**O que pede:** somar a série infinita.

**Ideia-chave — É uma PG (progressão geométrica), só que a razão é um número complexo.** A fórmula da
soma infinita `S = a₁/(1 − q)` vale igualzinho para razão complexa, desde que `|q| < 1` (módulo menor
que 1, para a série convergir).

**Desenvolvimento:**
1. **Descobrir a razão `q`** (cada termo dividido pelo anterior deve dar o mesmo valor):
   - termos: `1, (1/2)i, −1/4, −(1/8)i, 1/16, ...`
   - `(1/2)i ÷ 1 = i/2`. Confirme no próximo: `(i/2)·(i/2) = i²/4 = −1/4` ✔ (bate com o 3º termo);
     `(−1/4)·(i/2) = −i/8` ✔. Então a razão é `q = i/2`.
2. **Checar convergência:** `|q| = |i/2| = 1/2 < 1` ✔ → a série converge e podemos usar a fórmula.
3. **Aplicar a fórmula** com `a₁ = 1`:
   `S = a₁/(1 − q) = 1/(1 − i/2)`.
   Primeiro junte o denominador: `1 − i/2 = (2 − i)/2`. Dividir por uma fração é multiplicar pelo inverso:
   `S = 1 ÷ (2−i)/2 = 2/(2 − i)`.
4. **Racionalizar** (tirar o `i` do denominador): multiplique em cima e embaixo pelo **conjugado** do
   denominador. O conjugado de `2 − i` é `2 + i`.
   - Embaixo: `(2 − i)(2 + i) = 2² − i² = 4 − (−1) = 5` (usa o produto `(a−b)(a+b) = a² − b²`, e `i² = −1`).
   - Em cima: `2·(2 + i) = 4 + 2i`.
   - Logo `S = (4 + 2i)/5`.
5. Separe parte real e imaginária: `S = 4/5 + (2/5)i`.

**Conclusão:** `S = 4/5 + 2/5 i` → **alternativa (b)**.
(Chave: reconhecer a PG de razão complexa `q = i/2`; aplicar `S = a₁/(1−q)`; **racionalizar** pelo
conjugado — lembrando que `(2−i)(2+i) = 4 + 1 = 5`.)

---

## 2026/1 — Q13: Integral de radical infinito aninhado → 2/3

**O que pede:** `∫₀¹ ∛(x·∛(x·∛(x·...))) dx`.

**Ideia-chave — A torre é infinita, então ela "se contém".** Primeiro simplificamos a função dentro da
integral; depois integramos. O truque para a torre infinita: dê um nome `y` a ela e observe que, por ser
**infinita**, o que está "dentro do primeiro radical" é idêntico à torre toda de novo.

**Desenvolvimento:**
1. Defina `y = ∛(x·∛(x·∛(x·...)))`. Como a torre é infinita, tudo o que está debaixo do primeiro `∛`
   depois do primeiro `x` é a **mesma** torre `y`. Ou seja, dentro do primeiro radical temos `x·y`:
   `y = ∛(x·y)`.
2. Eleve os dois lados ao cubo para tirar a raiz cúbica: `y³ = x·y`.
3. Resolva para `y` (descartando a solução trivial `y = 0`, que não corresponde à torre): divida por `y`:
   `y² = x → y = √x` (a raiz positiva, pois a torre é positiva para `x ∈ (0,1]`).
4. Então a função dentro da integral é simplesmente `√x`. A integral vira:
   `∫₀¹ √x dx = ∫₀¹ x^{1/2} dx`.
5. Integre pela regra `∫ x^n dx = x^{n+1}/(n+1)`, com `n = 1/2`:
   `= [x^{3/2} / (3/2)]₀¹ = [(2/3)·x^{3/2}]₀¹ = (2/3)·1 − 0 = 2/3`.

**Conclusão:** `2/3` → **alternativa (b)**.
(Chave: torre infinita ⇒ ela se repete dentro de si ⇒ `y = ∛(x·y)` ⇒ `y = √x`; depois é uma integral
simples de potência.)

---

## 2026/1 — Q14: 1+2+...+n = 105 → n = 14

**O que pede:** achar `n`.

**Ideia-chave — Soma de Gauss:** `n(n+1)/2 = 105`.

**Desenvolvimento:**
1. `n(n+1) = 210`.
2. `14·15 = 210` ⇒ `n = 14`.

**Conclusão:** `n = 14` → **alternativa (b)**.

---

## 2023/1 — Q15: Série geométrica complexa alternada → 0,6 − 0,2 i

**O que pede:** somar `S = Σ_{k≥0} (−1)^k ((1+i)/2)^k`.

**Ideia-chave — PG de razão `q = −(1+i)/2`:** converge se `|q|<1`.

**Desenvolvimento:**
1. Razão `q = −(1+i)/2`. `|q| = |1+i|/2 = √2/2 < 1` ⇒ converge.
2. `S = 1/(1−q) = 1/(1 + (1+i)/2) = 1/((2+1+i)/2) = 2/(3+i)`.
3. Racionalize: `2(3−i)/((3+i)(3−i)) = (6−2i)/(9+1) = (6−2i)/10 = 0,6 − 0,2 i`.

**Conclusão:** `0,6 − 0,2 i` → **alternativa (b)**.
(Chave: identificar razão complexa, checar `|q|`, racionalizar.)

---

## 2021/1 — Q6: Soma alternada de PG 4,1,1/4,... → 16/5

**O que pede:** `a₀ − a₁ + a₂ − a₃ + ...` com PG `4, 1, 1/4, 1/16, ...`.

**Ideia-chave — Soma alternada = PG de razão −q.**

**Desenvolvimento:**
1. PG original: `a₀=4`, razão `q=1/4`.
2. Soma alternada: termos `4, −1, 1/4, −1/16, ...` ⇒ razão efetiva `−1/4`.
3. `S = a₀/(1−(−1/4)) = 4/(1+1/4) = 4/(5/4) = 16/5`.

**Conclusão:** `16/5` → **alternativa (a)**.
(Chave: alternar sinais ⇒ razão vira `−q`.)

---

## 2022/1 — Q1: Recorrência acoplada (rotação) → afirmação errada

**O que pede:** sequências `a_{i+1}=(4/5)aᵢ−(3/5)bᵢ`, `b_{i+1}=(3/5)aᵢ+(4/5)bᵢ`, `a₀=1,b₀=0`;
marcar a afirmação **errada**.

**Ideia-chave — Reconhecer matriz de rotação:** `cosθ=4/5`, `sinθ=3/5`; cada passo gira `(aᵢ,bᵢ)` por `θ`.

**Desenvolvimento:**
1. A transformação é `[[4/5,−3/5],[3/5,4/5]]`, uma **rotação** por `θ` com `cosθ=4/5, sinθ=3/5`.
2. `(aᵢ,bᵢ)` fica sobre o **círculo unitário** para todo `i` (raio preservado = 1). Logo é **limitada** ✔.
3. Verifique cada afirmação usando que a sequência é rotação:
   - "bᵢ negativo para algum i" ✔ (ao girar, b passa por valores negativos).
   - "aᵢ=1, bᵢ=0 para algum i>0" — só se `iθ` for múltiplo de `2π`; como `θ=arccos(4/5)` é irracional em
     relação a `2π`, isso **nunca** ocorre ⇒ essa afirmação é **falsa**.
4. A afirmação sobre voltar a `(1,0)` é a errada.

**Conclusão:** a afirmação errada é a que diz que a sequência retorna a `aᵢ=1, bᵢ=0` para algum `i>0`.
(Chave: coeficientes cos/sin ⇒ rotação; retorno exige ângulo comensurável com 2π.)

---

## 2024/2 — Q13: PG com incógnita 2 + 4/m + 8/m² + ... = 7 → m

**O que pede:** achar `m` tal que a série vale `14/2 = 7`.

**Ideia-chave — PG infinita de razão 2/m:** `S = a₁/(1−q)` com `a₁=2`, `q=2/m`.

**Desenvolvimento:**
1. `S = 2/(1 − 2/m) = 2/((m−2)/m) = 2m/(m−2)`.
2. Iguale a 7: `2m/(m−2) = 7 → 2m = 7(m−2) → 2m = 7m − 14 → 14 = 5m → m = 14/5`.
3. `14/5` não é inteiro ⇒ não está entre (a)–(d).

**Conclusão:** nenhuma das opções inteiras → **alternativa (e)**.
(Chave: `S=a₁/(1−q)`; resolver para m e checar convergência `|2/m|<1`.)

---

## 2023/2 — Q6: Série alternada Σ(−1)^i √(2^{i−1}) → sem limite

**O que pede:** `lim Sₙ` de `Sₙ = −1 + √2 − 2 + 2√2 − 4 + 4√2 − ...`.

**Ideia-chave — Teste do termo geral:** se os termos não tendem a 0, a série **não** converge.

**Desenvolvimento:**
1. O termo geral em módulo é `√(2^{i−1}) = (√2)^{i−1}`, que **cresce** sem limite (razão `√2 > 1`).
2. Como o termo não tende a zero, a série **diverge** / não tem limite definido.

**Conclusão:** não há limite definido → **alternativa (e)**.
(Chave: termos crescentes ⇒ série diverge.)

---

## 2022/2 — Q15: Convergência de aₙ = cos^{n+1}(nθ) → todas verdadeiras

**O que pede:** marcar a afirmação correta sobre convergência.

**Ideia-chave — `|cos| ≤ 1` elevado a potência crescente.**

**Desenvolvimento:**
1. Se `|cos(nθ)| < 1`, então `cos^{n+1}(nθ) → 0` quando `n → ∞`.
2. Nos casos `θ = π` e `θ = 2π`, `cos(nθ) = ±1`, e a potência estabiliza (converge).
3. Analisando cada intervalo proposto, **todas** as afirmações de convergência se verificam.

**Conclusão:** todas as afirmações são verdadeiras → **alternativa (e)**.
(Chave: potência alta de algo com módulo ≤ 1 tende a 0.)

---

## 2021/2 — Q2: Sequência por somas parciais → x₁₀ = 512

Ver `../02-sistemas-matrizes-determinantes/RESOLUCOES-PASSO-A-PASSO.md` (2021/2-Q2).
Resumo: `xₖ = (2ᵏ−1) − (2^{k−1}−1) = 2^{k−1}`; `x₁₀ = 2⁹ = 512`.

---

## Mapa rápido: qual ferramenta usar

| Questão | Ferramenta central |
|---------|--------------------|
| 2021/1-Q6 | Soma alternada (razão −q) |
| 2022/1-Q1 | Recorrência = rotação |
| 2023/1-Q15 | PG complexa + racionalizar |
| 2026/1-Q12 | PG complexa (razão i/2) |
| 2026/1-Q13 | Radical infinito (ponto fixo) + integral |
| 2026/1-Q14 | Soma de Gauss |
| 2021/2-Q2 | Somas parciais |
| 2022/2-Q15 | Potência de |cos| ≤ 1 |
| 2023/2-Q6 | Teste do termo geral (diverge) |
| 2024/2-Q13 | PG infinita com incógnita |
