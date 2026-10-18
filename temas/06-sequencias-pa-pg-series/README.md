# Tema 06 — Sequências, PA/PG e Séries 🟠

**Prioridade: MÉDIA.** Aparece com frequência, principalmente **PG infinita**
(inclusive com termos complexos) e **somatórios**.

---

## 1. Conceitos e teoremas que você precisa saber

### 1.1 Progressão Aritmética (PA)
- Termo geral: `aₙ = a₁ + (n−1)·r`.
- Soma dos n primeiros: `Sₙ = (a₁+aₙ)·n/2`.
- **Soma de Gauss:** `1+2+…+n = n(n+1)/2`.

### 1.2 Progressão Geométrica (PG)
- Termo geral: `aₙ = a₁·q^(n−1)`.
- Soma finita: `Sₙ = a₁·(qⁿ−1)/(q−1)`, `q≠1`.
- **PG infinita** (converge se `|q|<1`): `S = a₁/(1−q)`. ⭐ a mais cobrada.

### 1.3 Séries alternadas e complexas
- A fórmula `S = a₁/(1−q)` vale também para **razão complexa** com `|q|<1`
  (módulo do complexo menor que 1).
- Séries com `(−1)ᵏ`: identifique `q` (pode ser negativo ou complexo) e aplique a mesma fórmula.

### 1.4 Relações de recorrência
- `a_{n+1} = f(aₙ)`: às vezes a sequência é periódica ou converge.
- Recorrências lineares acopladas (ex.: 2022 Q1) podem representar **rotações** no plano
  (matriz de rotação aplicada repetidamente → sequência limitada e periódica).

### 1.5 Somatórios úteis
- `Σ k = n(n+1)/2`
- `Σ k² = n(n+1)(2n+1)/6`
- `Σ k³ = [n(n+1)/2]²`

---

## 2. Resoluções comentadas (questões reais do ITA)

### 📌 2026 — Q14: `1 + 2 + 3 + … + n = 105`, achar n
Gabarito: **(b) 14**.

**Resolução:** Gauss: `n(n+1)/2 = 105 → n(n+1)=210 → n=14` (pois `14·15=210`).
**Lição:** reconheça a **soma de Gauss**; resolva `n(n+1)=2·soma` por tentativa.

### 📌 2026 — Q12: Série complexa `1 + (1/2)i − 1/4 − (1/8)i + 1/16 + …`
Gabarito: **(b) 4/5 + 2/5 i**.

**Resolução:** é uma PG de razão `q = i/2` (cada termo multiplica por `i/2`:
`1·(i/2)=i/2`, `(i/2)²=−1/4`, …). `|q|=1/2<1` → converge.
`S = 1/(1−i/2) = 1/((2−i)/2) = 2/(2−i) = 2(2+i)/((2−i)(2+i)) = (4+2i)/5 = 4/5 + 2/5 i`.
**Lição:** identifique a **razão complexa** e aplique `S=a₁/(1−q)`; racionalize multiplicando pelo conjugado.

### 📌 2026 — Q13: Integral de radical infinito aninhado
*"∫₀¹ (x^(1/3) de x^(1/3) de ... )dx"* — a torre de raízes cúbicas.
**Resolução:** seja `y = ∛(x·∛(x·∛(x…)))`. Então `y³ = x·y` → `y² = x` → `y = √x = x^(1/2)`.
`∫₀¹ x^(1/2) dx = [x^(3/2)·(2/3)]₀¹ = 2/3`.
**Lição:** radical **infinito aninhado** → monte equação `y = f(x,y)` e resolva para `y`.

### 📌 2023 — Q15: Série geométrica complexa alternada
`S = Σ (−1)ᵏ·((1+i)/2)ᵏ` Gabarito: **(b) 0,6 − 0,2 i**.

**Resolução:** razão `q = −(1+i)/2`, `|q| = √2/2 < 1`. `S = 1/(1−q) = 1/(1+(1+i)/2) = 2/(3+i)`
`= 2(3−i)/10 = (6−2i)/10 = 0,6 − 0,2 i`.
**Lição:** mesma fórmula, razão complexa; cheque convergência pelo **módulo**.

### 📌 2021 — Q6: Soma alternada de PG `a₀ − a₁ + a₂ − …`
PG `4, 1, 1/4, 1/16, …` razão `1/4`. Soma alternada → razão efetiva `−1/4`.
`S = 4/(1−(−1/4)) = 4/(5/4) = 16/5`.
**Lição:** soma alternada de PG = PG de razão `−q`.

### 📌 2022 — Q1: Recorrência acoplada (rotação disfarçada)
`a_{i+1}=(4/5)aᵢ−(3/5)bᵢ`, `b_{i+1}=(3/5)aᵢ+(4/5)bᵢ`.
**Resolução:** é a aplicação de uma **matriz de rotação** (cos θ=4/5, sin θ=3/5) a cada passo.
Logo `(aᵢ,bᵢ)` gira num círculo de raio 1 → **limitada** para todo i. Analise as afirmações com isso.
**Lição:** coeficientes `cos/sin` em recorrência = **rotação** → sequência limitada/periódica.

---

## 3. Exercícios de treino

**E1.** Soma `1 + 2 + … + 100`.

**E2.** Qual a soma da PG infinita `3 + 1 + 1/3 + 1/9 + …`?

**E3.** Numa PA, `a₁=5` e `a₁₀=32`. Qual a razão?

**E4.** Soma da série `1 − 1/2 + 1/4 − 1/8 + …`.

**E5.** Resolva para `n`: `1+2+…+n = 55`.

**E6.** Avalie `x = √(2·√(2·√(2·…)))` (radical infinito).

---

## 4. Gabarito e resoluções

**E1.** `100·101/2 = **5050**`.

**E2.** Razão `1/3`, `|q|<1`: `S = 3/(1−1/3) = 3/(2/3) = **9/2 = 4,5**`.

**E3.** `a₁₀ = a₁+9r → 32 = 5+9r → r = 27/9 = **3**`.

**E4.** PG razão `−1/2`: `S = 1/(1−(−1/2)) = 1/(3/2) = **2/3**`.

**E5.** `n(n+1)/2 = 55 → n(n+1)=110 → n=10` (`10·11=110`). **n=10**.

**E6.** `x=√(2x) → x²=2x → x=2` (descartando x=0). **x=2**.
