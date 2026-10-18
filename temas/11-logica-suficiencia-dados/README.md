# Tema 11 — Raciocínio Lógico e Suficiência de Dados 🟡

**Prioridade: APOIO.** Aparece de forma esparsa (2021, 2022), no formato clássico do **GMAT Data Sufficiency**.
São questões onde você **não precisa achar o valor** — só decidir se dá para determiná-lo.

---

## 1. Conceitos e teoremas que você precisa saber

### 1.1 O formato "Data Sufficiency" ⭐
A pergunta traz duas afirmações (I e II). As **5 alternativas são SEMPRE as mesmas**:

- **(a)** afirmação **I sozinha** basta, mas II sozinha não.
- **(b)** afirmação **II sozinha** basta, mas I sozinha não.
- **(c)** **as duas juntas** bastam, mas nenhuma sozinha.
- **(d)** **cada uma sozinha** já basta.
- **(e)** nem as duas juntas bastam (precisa de mais dados).

> 🎯 Decore esse padrão. Na prova, você economiza o tempo de reler as 5 opções.

### 1.2 Método de análise (passo a passo)
1. Analise a **afirmação I sozinha**: dá para responder? (sim/não)
2. Analise a **afirmação II sozinha**: dá para responder? (sim/não)
3. Se nenhuma sozinha resolve, analise as **duas juntas**.
4. Cruze com a tabela acima para achar a letra.

**Armadilha clássica:** "determinar o valor" ≠ "achar uma equação". Uma equação com duas
incógnitas geralmente **não** determina valores únicos. E cuidado com soluções múltiplas
(ex.: `x²=4` dá `x=±2`, então pode não ser suficiente para saber o **sinal**).

### 1.3 Lógica proposicional básica
- **Condicional** `p → q`: falsa só quando `p` verdadeira e `q` falsa.
- **Contrapositiva** `¬q → ¬p` é equivalente a `p → q`.
- **Negação de "todo"** = "existe pelo menos um que não"; negação de "existe" = "nenhum".

### 1.4 Problemas de idade / relações temporais
Traduza o enunciado em **equações** com variáveis para "idade agora" e "idade no passado/futuro".
(ex.: 2022 Q16 — "eu tenho o triplo da idade que você tinha quando...").

---

## 2. Resoluções comentadas (questões reais do ITA)

### 📌 2021 — Q7: "r é maior que zero?"
*"I. rt = 18; II. r + t = 11."* 

**Resolução:**
- **I sozinha:** `rt=18` > 0 significa `r` e `t` **mesmo sinal**, mas não sabemos se ambos positivos
  ou ambos negativos → não determina se `r>0`. **Insuficiente.**
- **II sozinha:** `r+t=11` não fixa `r` (pode ser 10 e 1, ou −5 e 16...). **Insuficiente.**
- **Juntas:** `rt=18` e `r+t=11` → `r,t` são raízes de `x²−11x+18=0 → (x−2)(x−9)` → `{2,9}`,
  **ambos positivos** → `r>0` com certeza. **Suficientes juntas.** → **(c)**.
**Lição:** combine as duas e veja se o resultado é **inequívoco**.

### 📌 2022 — Q4: "determinar z" com I e II
*"I. x + 1/y = 3; II. y/(xy+1) + 1/z = 5."*

**Resolução:** manipule II: `y/(xy+1)` — repare que `xy+1 = y·(x+1/y) = y·3` (usando I).
Então `y/(xy+1) = y/(3y) = 1/3`. Logo II vira `1/3 + 1/z = 5 → 1/z = 14/3 → z = 3/14`.
Precisou de I **e** II juntas → **(c)**.
**Lição:** às vezes I **destrava** a II; teste a combinação antes de concluir "insuficiente".

### 📌 2022 — Q16 / 2021: Problema de idades
**Resolução:** defina `x` = minha idade hoje, `y` = sua idade hoje. Traduza cada frase temporal
numa equação (cuidado com "quando eu tinha...", que desloca o tempo). Resolva o sistema.
**Lição:** **uma variável por pessoa**, uma equação por frase. Organize a linha do tempo.

---

## 3. Exercícios de treino

**E1.** (Suficiência) *"Qual o valor de x?"* I. `x² = 16`.  II. `x > 0`. Qual alternativa (a–e)?

**E2.** (Suficiência) *"m é par?"* I. `m = 2k` para algum inteiro k.  II. `m + 1` é ímpar.

**E3.** Dois números somam 10 e seu produto é 21. Quais são?

**E4.** Negue logicamente: "Todos os alunos passaram."

**E5.** (Idades) Hoje tenho o dobro da sua idade. Há 10 anos, tinha o triplo. Quantos anos cada um tem?

**E6.** (Suficiência) *"r > 0?"* I. `r² = 25`.  II. `r³ = 125`. Qual alternativa?

---

## 4. Gabarito e resoluções

**E1.** I: `x=±4` (não determina). II: só diz `x>0` (não dá valor). Juntas: `x=4`. → **(c)**.

**E2.** I: `m=2k` → m é par (suficiente). II: `m+1` ímpar → `m` par (suficiente).
Cada uma sozinha basta → **(d)**.

**E3.** Raízes de `x²−10x+21=0 → (x−3)(x−7)` → **3 e 7**.

**E4.** "Pelo menos um aluno **não** passou" (ou "existe aluno que não passou").

**E5.** `x=2y` (hoje); `x−10 = 3(y−10)`. Substituindo: `2y−10 = 3y−30 → y=20`, `x=40`.
**Você tem 20, eu tenho 40.**

**E6.** I: `r²=25 → r=±5` (não determina o sinal). II: `r³=125 → r=5` (determina, pois cubo preserva sinal).
Só II basta → **(b)**.

---

## 5. Banco de questões reais

As questões deste tema nas 6 provas (2021–2026), com enunciado original em inglês e gabarito
(quando divulgado), estão em **[QUESTOES-DAS-PROVAS.md](QUESTOES-DAS-PROVAS.md)**.
