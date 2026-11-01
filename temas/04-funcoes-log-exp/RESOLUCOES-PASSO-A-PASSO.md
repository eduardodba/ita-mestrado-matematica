# Funções, Logaritmos e Exponenciais — Resoluções PASSO A PASSO

Resolução detalhada de cada questão deste tema nas provas PG-EIA/ITA (2021–2026, 1º e 2º semestres).
Estrutura: **o que pede**, **ideia-chave**, **desenvolvimento** e **conclusão**.

---

## 2026/1 — Q4: Equação exponencial 4^x − 2^(x+2) + 3 = 0 → duas soluções

**O que pede:** quantas soluções reais tem a equação.

**Ideia-chave — Substituição `u = 2^x`:** `4^x = (2^x)²` e `2^(x+2) = 4·2^x`, reduzindo a um 2º grau.

**Desenvolvimento:**
1. `4^x = (2^x)² = u²`; `2^(x+2) = 2^x·2² = 4u`.
2. Equação: `u² − 4u + 3 = 0`.
3. Fatorando: `(u−1)(u−3) = 0 → u = 1` ou `u = 3`.
4. Ambos positivos (ok, pois `u = 2^x > 0`):
   - `2^x = 1 → x = 0`.
   - `2^x = 3 → x = log₂3`.
5. Duas soluções reais.

**Conclusão:** duas soluções reais → **alternativa (c)**.
(Chave: `u=2^x`, resolver 2º grau, manter só `u>0`.)

---

## 2026/1 — Q10: Gráfico de y = log₁₀(x) com OA = BC → relação entre a,b,c

**O que pede:** com `OA = BC` no gráfico de `y = log₁₀x`, achar a relação entre `a, b, c`.

**A figura (conferida no PDF):** no eixo x estão `a < b < c`; no eixo y estão as alturas `A, B, C` dos
pontos correspondentes da curva `y = log₁₀x`. Ou seja `A = log a`, `B = log b`, `C = log c`
(com `a < 1 < b < c`, pois `A` é pequeno/negativo e `C` é o maior).

**Ideia-chave — Ler as distâncias no eixo y como valores de log:**
- `OA` = distância da origem até `A` = `log a` (em módulo, a altura do ponto sobre `x=a`).
- `BC` = distância de `B` até `C` no eixo y = `C − B = log c − log b`.

**Desenvolvimento:**
1. Condição do enunciado: `OA = BC`.
2. Traduzindo: `log a = log c − log b`.
3. Passe `log b` para a esquerda: `log a + log b = log c`.
4. Propriedade do produto: `log(ab) = log c`.
5. Como o log é injetivo: `ab = c`.

**Conclusão:** `ab = c` → **alternativa (d)**.
(Chave: distâncias verticais no gráfico de `log` = valores de log; `log a + log b = log(ab)`.)

---

## 2025/1 — Q5: f(x)=arcsin(arcsin x) → afirmação errada

**O que pede:** marcar a afirmação **errada** sobre a função.

**Ideia-chave — Domínio encadeado + regra da cadeia:** para `arcsin(arcsin x)` existir, precisa
`arcsin x ∈ [−1,1]`, o que restringe o domínio; a derivada usa a regra da cadeia.

**Desenvolvimento:**
1. Domínio: `x ∈ [−1,1]` e `arcsin x ∈ [−1,1]`. Como `arcsin x ∈ [−π/2, π/2] ≈ [−1.57,1.57]`, a condição
   `arcsin x ∈ [−1,1]` restringe `x` a `[−sin1, sin1]` — **não** é `(−1,1)` inteiro nem a imagem de arcsin.
2. A afirmação (a) diz que `f` é bijetora com a mesma imagem de `arcsin x` — isso é **falso**, pois a
   composição muda a imagem.
3. A derivada por cadeia: `f'(x) = 1/√(1−arcsin²x) · 1/√(1−x²)` (confere com a opção (d)).

**Conclusão:** a afirmação errada → **alternativa (a)**.
(Chave: domínio da composição de arcsin + derivada por cadeia.)

---

## 2024/1 — Q8: Equação exponencial com x² → classificar raízes

**O que pede:** classificar as raízes de uma equação exponencial do tipo `64·32^x = (1/8)·x²`
(na forma `64/32^x = 1/8^{x²}`).

**Ideia-chave — Igualar potências de 2:** escreva tudo como potência de 2 e iguale expoentes.

**Desenvolvimento:**
1. `64 = 2⁶`, `32 = 2⁵`, `8 = 2³`. Reescreva ambos os lados como `2^(algo)`.
2. Igualando os expoentes, surge uma equação polinomial em `x` (envolvendo `x²`).
3. Resolva o polinômio e classifique as raízes (reais/racionais/inteiras) conforme o enunciado.

**Conclusão:** a natureza das raízes sai ao igualar os expoentes de base 2 e resolver o polinômio.
(Chave: mesma base ⇒ igualar expoentes.)

---

## 2023/1 — Q9: Simplificar log_a(√(a³/b)) → nenhuma vale sempre

**O que pede:** qual expressão é igual a `log_a(√(a³/b))` para todos `a,b>0`.

**Ideia-chave — Propriedades do log:** `log(√X) = ½ log X`; `log_a(a³) = 3`.

**Desenvolvimento:**
1. `log_a(√(a³/b)) = ½ · log_a(a³/b) = ½ (log_a a³ − log_a b) = ½ (3 − log_a b)`.
2. Compare com as opções: as que usam `ln(3)` ou `log_b(a)` de forma incorreta não equivalem a
   `½(3 − log_a b)` para todos `a,b`.
3. Nenhuma alternativa reproduz exatamente `½(3 − log_a b)` universalmente.

**Conclusão:** nenhuma vale para todos `a,b` → **alternativa (e)**.
(Chave: `log√X = ½logX`, `log_a a³ = 3`.)

---

## 2022/1 — Q7: Qual expressão / ln(x+1) é racional → fatorar o argumento

**O que pede:** qual expressão, dividida por `ln(x+1)`, dá número racional para todo `x>1`.

**Ideia-chave — Fatorar o argumento do log** para revelar `ln(x+1)` como fator.

**Desenvolvimento:**
1. `ln(x⁴−4x³+6x²−4x+1) = ln((x−1)⁴) = 4ln(x−1)` — dá `ln(x−1)`, não `ln(x+1)`.
2. Teste cada opção fatorando: procure aquela cujo log seja **múltiplo** de `ln(x+1)`.
3. Por exemplo, uma opção com argumento contendo `(x+1)` como fator (via diferença/soma de potências)
   produzirá `k·ln(x+1)`, cujo quociente por `ln(x+1)` é `k` (racional).

**Conclusão:** a opção cujo argumento fatora em potência de `(x+1)` → quociente racional.
(Chave: fatorar o argumento para isolar `ln(x+1)`.)

---

## 2021/1 — Q4: Equação 1 / x^(ln x + 2) = e → x = 1/e

**O que pede:** resolver `1 / x^(ln x + 2) = e`.

**Ideia-chave — Tomar `ln` dos dois lados** e substituir `t = ln x`.

**Desenvolvimento:**
1. `1 / x^(ln x + 2) = e` ⇒ `x^(−(ln x + 2)) = e`.
2. Tome `ln`: `−(ln x + 2)·ln x = ln e = 1`.
3. Seja `t = ln x`: `−(t+2)t = 1 → −t² − 2t = 1 → t² + 2t + 1 = 0 → (t+1)² = 0 → t = −1`.
4. `ln x = −1 → x = e^{−1} = 1/e`.

**Conclusão:** `x = 1/e` → **alternativa (a)**.
(Chave: `ln` dos dois lados + `t = ln x` vira quadrado perfeito.)

---

## 2025/2 — Q7: Equação logarítmica encaixada → intervalo de x

**O que pede:** localizar o intervalo que contém a solução `x` de uma equação com vários logaritmos.

**Ideia-chave — Mudança de base:** reduza tudo a `log₃` para simplificar.

**Desenvolvimento:**
1. Converta `logₓ₊₂(x)`, `logₓ(x+2)`, `log₃(x)` para uma base comum (base 3 ou natural).
2. Simplifique a equação até isolar `log₃x` (ou `x`).
3. Resolva e verifique em qual intervalo das opções `x` cai (respeitando `x>0, x≠1, x≠1/3`).

**Conclusão:** a solução cai no intervalo `(1/81, 1/3)` → **alternativa (b)**.
(Chave: mudança de base unifica os logs.)

---

## 2025/2 — Q15: Isolar m em (m+a)/(m+b) = 3a/b → 2ab/(b−3a)

**O que pede:** com `a,b,m>0` e `(m+a)/(m+b) = 3a/b`, achar `m`.

**Ideia-chave — Multiplicar cruzado e isolar m.**

**Desenvolvimento:**
1. `b(m+a) = 3a(m+b)`.
2. `bm + ab = 3am + 3ab`.
3. `bm − 3am = 3ab − ab = 2ab`.
4. `m(b − 3a) = 2ab → m = 2ab/(b − 3a)`.

**Conclusão:** `m = 2ab/(b−3a)` → **alternativa (a)**. (Chave: multiplicação cruzada + fatorar `m`.)

---

## 2024/2 — Q11: Ordenar p=log₃2, q=log_{√3}4, r=log_{1/3}√2

**O que pede:** ordenar os três logaritmos.

**Ideia-chave — Converter todos para a mesma base (3) em função de `p = log₃2`.**

**Desenvolvimento:**
1. `p = log₃2`.
2. `q = log_{√3}4 = ln4/ln√3 = (2ln2)/((1/2)ln3) = 4·(ln2/ln3) = 4p`.
3. `r = log_{1/3}√2 = ln√2/ln(1/3) = ((1/2)ln2)/(−ln3) = −(1/2)·(ln2/ln3) = −p/2`.
4. Como `p > 0`: `r = −p/2 < 0 < p < 4p = q`.
5. Ordem: `r < p < q`.

**Conclusão:** `r < p < q` → **alternativa (e)**.
(Chave: tudo em base 3; `q=4p`, `r=−p/2`.)

---

## 2022/2 — Q11: −log_{1/√e}(x) = ln(4x−3) → duas raízes

**O que pede:** classificar as raízes reais.

**Ideia-chave — Converter o log de base `1/√e` para `ln`.**

**Desenvolvimento:**
1. `log_{1/√e}(x) = ln x / ln(e^{−1/2}) = ln x / (−1/2) = −2 ln x`.
2. A equação `−log_{1/√e}(x) = ln(4x−3)` vira `2 ln x = ln(4x−3)`.
3. `ln(x²) = ln(4x−3) → x² = 4x − 3 → x² − 4x + 3 = 0 → (x−1)(x−3) = 0`.
4. `x = 1` ou `x = 3`; ambos com `4x−3 > 0` ✔ e `x>0` ✔.

**Conclusão:** duas raízes reais distintas → **alternativa (d)**.
(Chave: converter base do log; vira 2º grau.)

---

## 2021/2 — Q3: ln x + ln(4−x) = 1 → raízes reais irracionais

**O que pede:** classificar as raízes.

**Ideia-chave — Juntar os logs e exponenciar.**

**Desenvolvimento:**
1. `ln x + ln(4−x) = ln[x(4−x)] = 1`.
2. `x(4−x) = e^1 = e`.
3. `4x − x² = e → x² − 4x + e = 0`.
4. `Δ = 16 − 4e ≈ 16 − 10,87 = 5,13 > 0` ⇒ duas raízes reais.
5. As raízes `x = (4 ± √(16−4e))/2 = 2 ± √(4−e)` são **irracionais** (e dentro de `(0,4)`, domínio válido).

**Conclusão:** raízes reais **irracionais** (não inteiras nem racionais).
(Chave: `ln A + ln B = ln(AB)`, exponenciar, resolver 2º grau.)

---

## 2021/2 — Q12: b'/a' com a,b,a',b' em x,y → simplificação

**O que pede:** com `a=(x+y)/2`, `b=(x−y)/2`, `a'=(x+2y)/3`, `b'=x−y`, achar `b'/a'`.

**Ideia-chave — Escrever `x` e `y` em função de `a` e `b`, depois montar `b'/a'`.**

**Desenvolvimento:**
1. De `a = (x+y)/2` e `b = (x−y)/2`: somando, `a + b = x`; subtraindo, `a − b = y`.
   Ou seja `x = a+b` e `y = a−b`.
2. `b' = x − y = (a+b) − (a−b) = 2b`.
3. `a' = (x + 2y)/3 = [(a+b) + 2(a−b)]/3 = (a + b + 2a − 2b)/3 = (3a − b)/3`.
4. `b'/a' = 2b ÷ [(3a − b)/3] = 2b · 3/(3a − b) = 6b/(3a − b)`.

**Conclusão:** `b'/a' = 6b/(3a − b)` → **alternativa (e)**.
(Chave: inverter `a=(x+y)/2, b=(x−y)/2` para `x=a+b, y=a−b` e substituir.)

---

## Mapa rápido: qual ferramenta usar

| Questão | Ferramenta central |
|---------|--------------------|
| 2021/1-Q4 | ln dos dois lados + t=lnx |
| 2022/1-Q7 | Fatorar argumento do log |
| 2023/1-Q9 | `log√X=½logX`, `log_a a³=3` |
| 2024/1-Q8 | Igualar potências de base 2 |
| 2025/1-Q5 | Domínio encadeado + regra da cadeia |
| 2026/1-Q4 | Substituição `u=2^x` (2º grau) |
| 2026/1-Q10 | Distâncias no gráfico ⇒ equações de log |
| 2021/2-Q3 | `lnA+lnB=ln(AB)` + 2º grau |
| 2021/2-Q12 | Substituição algébrica |
| 2022/2-Q11 | Mudar base do log ⇒ 2º grau |
| 2024/2-Q11 | Base comum (q=4p, r=−p/2) |
| 2025/2-Q7 | Mudança de base |
| 2025/2-Q15 | Multiplicação cruzada + isolar m |
