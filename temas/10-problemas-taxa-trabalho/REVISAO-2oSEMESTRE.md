# Revisão das provas de 2º SEMESTRE — Problemas de Taxa, Trabalho e Velocidade

Revisão completa das **5 provas de 2º semestre (2021 a 2025)** para este tema.
Gabaritos oficiais: 2022-2ºSem e 2025-2ºSem.

> Tema **muito frequente** nos 2ºs semestres (estilo GMAT): bombas/reservatórios, trabalho conjunto,
> velocidade, proporção, porcentagem. Geralmente rápidas se você montar a equação certa.

---

### 2025/2º — Q9: Produtividade (artesãos)
3 professionals make 24 pieces in 2 h; 4 apprentices make 16 pieces in 3 h. How long for 2 professionals
+ 3 apprentices to make 48 pieces?
(a) 2 · (b) 3 · (c) 4 · (d) 5 · (e) 6 hours
**Gabarito: (c)** — taxa profissional `=24/(3·2)=4 peças/h`; aprendiz `=16/(4·3)=4/3 peças/h`.
Juntos: `2·4 + 3·(4/3) = 8+4 = 12 peças/h` → `48/12 = 4 h`.
**Lição:** **taxa por indivíduo = peças/(nº·horas)**; some as taxas da equipe.

### 2025/2º — Q14: Porcentagem (eleição)
A received 1/3 more votes than B; B received 1/4 fewer than C; C=12000. Votes of A?
(a) 9000 · (b) 11000 · (c) 12000 · (d) 13000 · (e) 16000
**Gabarito: (c)** — `B = C·(3/4) = 9000`; `A = B·(4/3) = 12000`.

---

### 2024/2º — Q1: Reservatório com entrada e saída
Floodgates open: dump full reservoir in 24 days. Closed, river fills empty reservoir in 12 days.
Full, gates open but river diverted: how many days to dump?
(a) 6 · (b) 8 · (c) 12 · (d) 15 · (e) 18 days
→ Taxa de **saída** (comportas) e de **entrada** (rio) combinam. Quando as comportas abertas levam 24 dias
para esvaziar com o rio entrando, e o rio sozinho enche em 12 dias: monte `saída − entrada`. Isole a
taxa de saída pura e calcule o tempo de esvaziamento sem o rio.
**Lição:** tanque com **entrada e saída simultâneas** → subtraia as taxas.

---

### 2023/2º — Q13: Aumento e desconto de 20% (porcentagem)
Shirt R$150, raised by 20%, then reduced by 20%. New price?
(a) 120 · (b) 139 · (c) 150 · (d) 144 · (e) none
**Gabarito: (d)** — `150·1,2·0,8 = 150·0,96 = 144`.
**Lição:** +20% depois −20% **não** volta ao original (dá 0,96× = −4%).

---

### 2022/2º — Q3: Três reservatórios drenando (taxas)
A (180 L, 3 L/s), B (100 L, 2 L/s) drenam para C (200 L, cap. 250 L, dreno 4 L/s). Mark the WRONG
statement (tempos de encher/esvaziar C, A, B).
**Gabarito: (e) B empty in 50 s** (verifique: `100/2 = 50 s` — então essa estaria certa; o erro está
em outra opção — refaça as contas de fluxo de C). Monte o balanço de vazões de C ao longo do tempo.

### 2022/2º — Q10: Preço por garrafa (proporção)
5 bottles X cost $64; 7 bottles Y cost $163.80. Cost of 3 X + 2 Y?
(a) 36.2 · (b) 85.2 · (c) 94.9 · (d) 95.8 · (e) 98.8
**Gabarito: (b)** — `X=64/5=12,8`; `Y=163,80/7=23,4`; `3·12,8 + 2·23,4 = 38,4+46,8 = 85,2`.

### 2022/2º — Q12: Trabalho conjunto (Alice e Bob)
Alice sozinha 18 h; Alice+Bob 12 h. Bob sozinho?
(a) 36 · (b) 24 · (c) 18 · (d) 12 · (e) 6 hours
**Gabarito: (a)** — `1/18 + 1/Bob = 1/12 → 1/Bob = 1/12−1/18 = 1/36 → Bob=36 h`.

### 2022/2º — Q14: Encontro de caminhantes (velocidade)
Yasmim A→B (22.5 km) a 1.5 km/h; 1 h depois Julia B→A a 2 km/h. Km que Julia andou no encontro?
(a) 12 · (b) 11.5 · (c) 11 · (d) 10.5 · (e) 9.75
**Gabarito: (a)** — monte posições vs tempo; Yasmim já andou 1,5 km na 1ª hora; resolva o encontro.

---

### 2021/2º — Q1: Alocar operários (montagem + pintura em série)
6 workers; montar 1 carro = 4 semanas/trabalhador, pintar = 1 semana/trabalhador; tarefas escaláveis e
**sequenciais**. Qual divisão produz cada carro no menor tempo?
(a) 1 e 5 · (b) 2 e 4 · (c) 3 e 3 · (d) 4 e 2 · (e) 5 e 1
→ Tarefas em série viram gargalo: equilibre os tempos das duas etapas (minimize o máximo).

---

## Observação sobre frequência (2º sem)
Este é um dos temas **mais frequentes** nos 2ºs semestres (apareceu em todas, às vezes 2–3 vezes).
Padrões: **trabalho conjunto** (2022/2, 2025/2), **reservatório entrada/saída** (2024/2, 2022/2),
**porcentagem** (2023/2, 2025/2), **velocidade/encontro** (2022/2). São pontos "fáceis" de garantir —
treine para fazê-las rápido.

---

## Conceitos-chave reforçados (2º sem)

### Trabalho conjunto (a fórmula mestra)
Taxa = trabalho/tempo. Juntos: **some as taxas**; tempo = 1/(soma das taxas).
- Um indivíduo que faz em `t` horas tem taxa `1/t`.
- Grupo: `taxa_total = n₁·r₁ + n₂·r₂ + …`.

### Tanque com entrada E saída simultâneas
Taxa líquida = `taxa_entrada − taxa_saída`. Se esvazia, a saída domina; se enche, a entrada domina.
Isole a taxa "pura" combinando os cenários dados.

### Porcentagem encadeada
+p% depois −p% **não** retorna ao valor inicial: o fator é `(1+p)(1−p) = 1−p²`.
Ex.: +20% e −20% → `0,96×` (perda de 4%).

### Proporção direta (preço por unidade)
Ache o **valor unitário** primeiro, depois escale.

---

## Resoluções detalhadas

### 2024/2 — Q1 (reservatório entrada/saída)
Comportas abertas esvaziam o cheio em 24 dias **com o rio entrando**: taxa líquida de saída = `V/24`.
Rio sozinho enche o vazio em 12 dias: taxa de entrada = `V/12`.
Logo taxa de saída pura `S` satisfaz `S − V/12 = V/24` → `S = V/24 + V/12 = V/24 + 2V/24 = 3V/24 = V/8`.
Sem o rio, esvaziar o cheio leva `V / (V/8) = 8 dias`. **Resposta (b).**

### 2022/2 — Q12 (Alice e Bob → 36 h)
`1/18 + 1/B = 1/12`. `1/B = 1/12 − 1/18 = 3/36 − 2/36 = 1/36` → `B = 36 h`. **Resposta (a).**

### 2025/2 — Q9 (artesãos → 4 h)
Profissional: `24/(3·2) = 4` peças/h cada. Aprendiz: `16/(4·3) = 4/3` peças/h cada.
2 prof + 3 aprend: `2·4 + 3·(4/3) = 8 + 4 = 12` peças/h. Para 48: `48/12 = 4 h`. **Resposta (c).**

### 2023/2 — Q13 (camisa +20% −20% → 144)
`150 · 1,20 · 0,80 = 150 · 0,96 = 144`. **Resposta (d).**

---

## Exercícios de treino (2º sem)

**T1.** Duas bombas enchem um tanque em 4 h e 6 h sozinhas. Juntas, quanto tempo?

**T2.** Um preço sobe 25% e depois cai 25%. Qual a variação percentual total?

**T3.** 3 impressoras imprimem 900 páginas em 2 h. Quantas páginas 5 impressoras (mesmo ritmo)
imprimem em 3 h?

**T4.** Um tanque enche em 3 h por uma torneira, mas um furo o esvazia em 6 h. Com torneira aberta e
furo presente, em quanto tempo enche?

---

## Gabarito dos exercícios (2º sem)

**T1.** `1/4 + 1/6 = 3/12 + 2/12 = 5/12` tanque/h → `12/5 = 2,4 h` (2 h 24 min).

**T2.** Fator `1,25 · 0,75 = 0,9375` → variação **−6,25%**.

**T3.** Taxa = `900/(3·2) = 150` pág/h por impressora. 5 impressoras × 3 h: `5·150·3 = 2250` páginas.

**T4.** Taxa líquida `= 1/3 − 1/6 = 1/6` tanque/h → `6 h`.
