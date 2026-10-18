# Tema 10 — Problemas de Taxa, Trabalho e Velocidade 🟡

**Prioridade: APOIO (mas frequente).** Estilo GMAT clássico: bombas enchendo reservatório,
pessoas realizando tarefas, velocidade média, comissões/porcentagem. São questões de **montar a equação certa** — geralmente rápidas se você acerta o modelo.

---

## 1. Conceitos e teoremas que você precisa saber

### 1.1 Taxa = trabalho / tempo ⭐
A ideia central: **taxa = 1/tempo** (trabalho unitário = 1 tarefa completa).
- Se A faz a tarefa em `t_A` horas, sua taxa é `1/t_A` (tarefas por hora).
- **Trabalho conjunto:** some as taxas. Tempo juntos = `1 / (soma das taxas)`.

> Exemplo (2026 Q2): bombas de 1h, 1,5h e 3h.
> Taxas: `1 + 1/1,5 + 1/3 = 1 + 2/3 + 1/3 = 2` reservatórios/hora.
> Tempo = `1/2` hora = **30 minutos**.

### 1.2 Velocidade
- `velocidade = distância / tempo`.
- **Velocidade média** = distância **total** / tempo **total** (⚠️ NÃO é a média das velocidades!).
  - `v_média = (d₁ + d₂) / (t₁ + t₂)`.
- Velocidades relativas (trem + passageiro): somam se mesmo sentido, subtraem se opostos
  (depende do referencial, como em 2024 Q10).

### 1.3 Porcentagem
- `x% de V = (x/100)·V`.
- Comissão escalonada (2021 Q9): aplique a porcentagem a cada faixa separadamente e some.

### 1.4 Regra de três e proporção
- Grandezas **diretamente** proporcionais: `a/b = c/d`.
- **Inversamente** proporcionais: `a·b = c·d` (ex.: mais máquinas → menos tempo).

### 1.5 Tabela de porcentagens (2022 Q3)
Quando a questão dá porcentagens parciais e pede o total, monte a tabela e use que
**a soma das porcentagens = 100%**.

---

## 2. Resoluções comentadas (questões reais do ITA)

### 📌 2026 — Q2: Três bombas enchendo reservatório
Gabarito: **(c) 30 minutos**.

**Resolução:** taxas `1 + 2/3 + 1/3 = 2` reservatórios/h → tempo `= 1/2 h = 30 min`.
**Lição:** **some as taxas** (não os tempos!). Tempo conjunto = `1/soma`.

### 📌 2023 — Q6: Andy e Robert varrendo
*"Juntos varrem 280 m² em 4h; Robert sozinho leva 7h. Quanto Andy leva p/ varrer 240 m²?"*

**Resolução:** taxa conjunta `= 280/4 = 70 m²/h`. Taxa do Robert `= 280/7 = 40 m²/h`.
Taxa do Andy `= 70 − 40 = 30 m²/h`. Para 240 m²: `240/30 = 8 h`.
**Lição:** **taxa do indivíduo = taxa conjunta − taxa do outro**.

### 📌 2024 — Q9: Velocidade média em dois trechos
*"40 km/h por 3h no 1º trecho; 2h no 2º; média 48 km/h. Velocidade no 2º?"*

**Resolução:** `d₁ = 40·3 = 120 km`. Tempo total `= 5h`. `v_média = d_total/5 = 48 → d_total = 240 km`.
`d₂ = 240 − 120 = 120 km` em 2h → `v₂ = 60 km/h`.
**Lição:** velocidade média usa **distância e tempo TOTAIS**, nunca a média aritmética das velocidades.

### 📌 2024 — Q10: Velocidades relativas no trem
**Resolução:** monte `v_solo1 = V + V₁`, `v_solo2 = V − V₂`, use a relação `v_solo2 = (3/5)v_solo1`
e resolva o sistema para `V`.
**Lição:** escreva cada velocidade **em relação ao solo** e monte a equação da condição dada.

### 📌 2021 — Q9: Comissão escalonada
*"15% dos primeiros $800 + 20% do que exceder; comissão total $320. Vendas?"*

**Resolução:** `0,15·800 = 120`. Falta `320−120 = 200` vindos de `20%` do excedente:
`0,20·x = 200 → x = 1000`. Vendas totais `= 800 + 1000 = 1800`.
**Lição:** aplique cada porcentagem **à sua faixa** e some.

### 📌 2021 — Q13: Três computadores (tarefa de ML) + processos
**Resolução:** taxas `1/48 + 1/24 + 1/16`. Some (MMC 48): `1/48+2/48+3/48 = 6/48 = 1/8` tarefa/h
→ tempo `= 8 h` (respeitando o limite de 96 subprocessos).
**Lição:** mesma lógica de "bombas", agora com computadores.

### 📌 2022 — Q3: Tabela de porcentagens
**Resolução:** use que as porcentagens somam 100% e as quantidades somam o total; preencha os vazios
com regra de três.
**Lição:** **soma das porcentagens = 100%** fecha o sistema.

---

## 3. Exercícios de treino

**E1.** Uma torneira enche um tanque em 6h, outra em 3h. Juntas, em quanto tempo?

**E2.** Um carro faz 100 km a 50 km/h e mais 100 km a 100 km/h. Qual a velocidade média?

**E3.** João faz um trabalho em 10 dias, Maria em 15 dias. Juntos, quantos dias?

**E4.** 30% de um número é 45. Qual o número?

**E5.** Um vendedor ganha 10% sobre os primeiros R$ 2000 e 25% sobre o que exceder.
Se vendeu R$ 5000, qual a comissão?

**E6.** Se 4 operários fazem uma obra em 9 dias, quantos dias levam 6 operários (mesmo ritmo)?

---

## 4. Gabarito e resoluções

**E1.** Taxas `1/6 + 1/3 = 1/6 + 2/6 = 3/6 = 1/2` tanque/h → tempo `= 2 h`.

**E2.** `d_total = 200 km`; tempos `100/50 + 100/100 = 2 + 1 = 3h`; `v_média = 200/3 ≈ 66,7 km/h`.
(Note: NÃO é 75, a média aritmética.)

**E3.** Taxas `1/10 + 1/15 = 3/30 + 2/30 = 5/30 = 1/6` obra/dia → `6 dias`.

**E4.** `0,30·x = 45 → x = 150`.

**E5.** `0,10·2000 = 200`; excedente `= 3000`, `0,25·3000 = 750`. Total `= 200 + 750 = R$ 950`.

**E6.** Inversamente proporcional: `4·9 = 6·d → d = 36/6 = 6 dias`.
