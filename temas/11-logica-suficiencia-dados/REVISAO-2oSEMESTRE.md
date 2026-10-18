# Revisão das provas de 2º SEMESTRE — Lógica, Suficiência de Dados e Teoria dos Números

Revisão completa das **5 provas de 2º semestre (2021 a 2025)** para este tema.
Gabaritos oficiais: 2022-2ºSem e 2025-2ºSem.

> Os 2ºs semestres trouxeram **mais suficiência de dados** (estilo GMAT) e também
> **teoria dos números** (divisibilidade, primos, quadrados/cubos perfeitos). Agrupei aqui.

As 5 alternativas de suficiência são sempre as mesmas (ver `README.md`, seção 1.1).

---

### 2025/2º — Q6: Suficiência (expressão algébrica)
I. xy/(x−y)=5 ; II. xy/(x+y)=1. Determinar (x²−y²)/(x²y²) + 2/(xy).
(a)...(e) suficiência padrão.
**Gabarito: (c)** — a expressão pedida se escreve em função de `1/(x−y)` e `1/(x+y)`; precisa das duas.

### 2025/2º — Q12: Teoria dos números (dígitos invertidos)
How many integers n (10<n<100) are there such that reversing the digits gives n+9?
(a) 5 · (b) 6 · (c) 7 · (d) 8 · (e) 9
**Gabarito: (d)** — `n=10a+b`, invertido `10b+a`. `10b+a = 10a+b+9 → 9(b−a)=9 → b=a+1`.
Pares `(a,b)`: a=1..8 → **8** números.

### 2025/2º — Q13: Suficiência (geometria — ceviana)
Triangle with a cevian, ângulos 2α,2α,α. Determinar BC. I. AD=6 ; II. α=36°.
**Gabarito: (a)** — statement I alone sufficient (a geometria já fixa as proporções; falta uma medida).

---

### 2024/2º — (ver teoria dos números em tema 05-Q8; demais em outros temas)

---

### 2023/2º — Q5: Lógica/estado (travessia do rio) — ver tema 01
Problema de planejamento (3 casais). Resposta: 11 travessias.

### 2023/2º — Q8: Teoria dos números (fórmula inteira?) — ver tema 05
`(n³+n)/6` pode não ser inteiro. Teste pequenos n.

---

### 2022/2º — Q6: Suficiência (eventos independentes)
A, B independentes; diagrama de Euler com x, y (x·y≠0). O que se pode determinar?
**Gabarito: (b)** — independência dá `P(A∩B)=P(A)P(B)`, o que fixa uma relação; só uma variável sai.

### 2022/2º — Q8: Suficiência (aluguel de carro)
Tabela de tarifas; determinar o tipo de carro da Maria. I. total $92 ; II. 10 dias.
**Gabarito: (a)** — statement I alone sufficient.

---

### 2021/2º — Q4: Suficiência (três números)
I. 1/x+1/y+1/z=3 ; II. 1/(xy)+1/(yz)+1/(xz)=5. Determinar (x+y+z)/(xy+yz+zx).
→ Note que `(x+y+z)/(xyz) = I` e `(xy+yz+zx)/(xyz)=? ` — reescreva a expressão pedida em função de I e II.

### 2021/2º — Q6: Suficiência (luzes alternadas azul/verde)
I. 51 luzes ; II. removendo as pontas restam 24 verdes e 25 azuis. Determinar quantas verdes.
→ Cores alternam → padrão fixo; combine as informações.

### 2021/2º — Q8: Suficiência (três máquinas)
I. A sozinha 20 h ; II. B = metade do tempo de C. Determinar tempo das três juntas.
→ Falta informação sobre C em termos absolutos → provavelmente **(e)** insuficiente.

### 2021/2º — Q10: Teoria dos números (1003003001)
Sobre 1003003001: mark the correct statement (divisível por 7? por 11? quadrado? cubo perfeito?).
→ Note `1003003001 = 1001³` (pois `1001³ = 1.003.003.001`). Logo é **cubo perfeito**; `1001=7·11·13`.

### 2021/2º — Q11: Teoria dos números (expressões sempre inteiras/perfeitas)
Sobre expressões em n inteiro, "one cannot say that...". Teste divisibilidade e padrões
(`n⁴−4n³+6n²−4n+1=(n−1)⁴` é quadrado perfeito, etc.).

---

## Observação sobre frequência (2º sem)
Suficiência de dados apareceu **mais** nos 2ºs semestres (2021/2 teve 3–4!) e teoria dos números
ganhou espaço (2021/2, 2023/2, 2025/2). Dicas:
- **Suficiência:** decore o padrão das 5 alternativas; analise I e II separadamente antes de juntar.
- **Teoria dos números:** reconheça fatorações notáveis (`1001³`, `(n−1)⁴`), teste divisibilidade por
  7/11/13, e lembre dos critérios de quadrado/cubo perfeito.

---

## Conceitos-chave reforçados (2º sem)

### Teoria dos números — ferramentas que caíram
- **Critérios de divisibilidade:** por 3 (soma dos dígitos), por 9 (idem), por 11 (soma alternada),
  por 7/13 (agrupar de 3 em 3 dígitos — ligado a `1001 = 7·11·13`).
- **Quadrado/cubo perfeito:** reconhecer fatorações notáveis. `(n−1)⁴` é quadrado perfeito sempre;
  `1003003001 = 1001³` é cubo perfeito.
- **Número de 2 dígitos:** `n = 10a + b`; invertido `10b + a`. Diferença `= 9(a−b)`.
- **Soma de inteiros consecutivos / combinatórios sempre inteiros:** `(n²±n)/2 = C(n±...)`.

### Suficiência de dados — método (relembrando)
1. Analise **I sozinha**. 2. Analise **II sozinha**. 3. Se nenhuma basta, analise **juntas**.
4. Cruze com as 5 alternativas padrão. Nunca calcule o valor final se só precisa decidir suficiência.

---

## Resoluções detalhadas

### 2025/2 — Q12 (dígitos invertidos → 8 números)
`n = 10a+b`, invertido `10b+a`. Condição `10b+a = (10a+b)+9` → `9b−9a = 9` → `b = a+1`.
Com `10<n<100`: `a ∈ {1,…,8}` (e `b=a+1 ≤ 9`). São **8** valores. **Resposta (d).**

### 2021/2 — Q10 (1003003001 é cubo perfeito)
`1001³ = (1000+1)³ = 1000000000 + 3·1000000 + 3·1000 + 1 = 1.003.003.001`. Logo é **cubo perfeito**,
e `1001 = 7·11·13` (divisível por 7 e 11). A opção correta reflete isso.

### 2021/2 — Q4 (suficiência, três números)
Expressão pedida `(x+y+z)/(xy+yz+zx)`. Note: `I = 1/x+1/y+1/z = (xy+yz+zx)/(xyz)`;
`II = 1/(xy)+1/(yz)+1/(zx) = (x+y+z)/(xyz)`. Então a razão pedida `= II/I = 5/3`.
Precisa das **duas** → **(c)**.

### 2022/2 — Q6 (eventos independentes)
Independência: `P(A∩B) = P(A)·P(B)`. Isso impõe **uma equação** entre `x` e `y`, permitindo achar uma
em função da outra, mas não ambas isoladamente sem mais dados.

---

## Exercícios de treino (2º sem)

**T1.** (Suficiência) "Qual é x?" I. `x² = 9`. II. `x < 0`. Qual alternativa (a–e)?

**T2.** `11³` é igual a quanto? É quadrado ou cubo perfeito?

**T3.** Quantos números de 2 dígitos têm a soma dos dígitos igual a 10?

**T4.** `n⁴ − 4n³ + 6n² − 4n + 1` é sempre que tipo de número para n inteiro? (fatore)

---

## Gabarito dos exercícios (2º sem)

**T1.** I: `x=±3` (não decide). II: só sinal. Juntas: `x=−3`. → **(c)**.

**T2.** `11³ = 1331`. É **cubo perfeito** (`11³`), não quadrado.

**T3.** Pares `(a,b)` com `a+b=10`, `a∈{1..9}`: `(1,9),(2,8),…,(9,1)` = **9** números.

**T4.** `(n−1)⁴` → é um **quadrado perfeito** (de fato `[(n−1)²]²`), sempre.
