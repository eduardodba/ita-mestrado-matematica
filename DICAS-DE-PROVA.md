# Dicas de Prova — PG-EIA / ITA

Estratégias práticas extraídas da análise das 6 provas (2021–2026).

---

## Antes de resolver

1. **O corte é 50%.** Você precisa de ~8 das 16. Pense em maximizar acertos, não em gabaritar.
2. **Passe os olhos nas 16 questões primeiro** (1–2 min). Marque mentalmente:
   - 🟢 "sei fazer rápido" → faça primeiro
   - 🟡 "dá, mas leva tempo" → deixa pro meio
   - 🔴 "difícil / não lembro" → por último (ou chute consciente)
3. **Não existe a ordem fácil→difícil.** A questão 1 pode ser mais difícil que a 16. Pule sem dó.

---

## Durante a prova

### Gestão de tempo
- 90 min / 16 = **~5,6 min por questão**. Se passar de 7–8 min numa, **pule**.
- Geometria espacial e cálculo tendem a consumir mais tempo. Combinatória simples e aritmética, menos.

### Ler o enunciado em inglês
- Cuidado com **"mark the WRONG statement"** — aparece muito. Você marca a **falsa**.
- `one cannot say that` = marque o que **NÃO** é verdade.
- Sublinhe o que a questão realmente pede antes de calcular.

### Sem calculadora: contas limpas
- Deixe raízes e frações na forma exata (`√2`, `3/4`) o máximo possível; simplifique no fim.
- Procure **cancelamentos** antes de multiplicar números grandes.
- Em binômio de Newton e fatoriais, **simplifique o fatorial** antes de expandir.

### Técnicas de eliminação (quando travar)
- **Teste as alternativas:** em equações e "qual valor satisfaz", às vezes substituir é mais rápido que resolver.
- **Analise ordem de grandeza / sinal:** descarte alternativas absurdas (negativa onde só cabe positiva etc.).
- **Casos particulares:** se a questão tem parâmetro (n, a, b), teste n=1, n=2 para eliminar opções.
- **Chute inteligente:** eliminou 2 de 5? Chute entre as 3 restantes vale a pena (não há penalidade por erro declarada).

---

## Erros comuns a evitar (vistos nos temas que mais caem)

### Combinatória
- Esquecer de **dividir pelas simetrias/rotações** em coloração de sólidos (use Burnside).
- Confundir arranjo (ordem importa) com combinação (ordem não importa).
- Em permutação circular de n objetos: é **(n−1)!**, não n!.

### Sistemas / determinantes
- Dizer "tem solução única" sem checar se o **determinante é zero** (aí pode ter 0 ou ∞).
- Em equação matricial, lembrar que **matrizes não comutam** (AB ≠ BA em geral).

### Geometria
- Esquecer a **relação de Euler** (V − A + F = 2) ao contar elementos de poliedro.
- Em poliedro truncado: cada corte **cria** novas faces/arestas/vértices — conte com cuidado.
- Trocar raio por diâmetro; esquecer o fator ½ em áreas de triângulo/semicírculo.

### Funções / log / exp
- Em `4^x − 2^(x+2) + 3 = 0`, **substituir** `u = 2^x` (vira 2º grau) e depois **descartar raízes negativas** de u.
- Esquecer o domínio de log (argumento > 0) e descartar soluções inválidas.

### Polinômios
- Afirmar "não tem raiz real" sem checar sinal nos extremos (teorema de Bolzano).
- Relações de Girard: soma das raízes = −b/a, produto = (±)termo independente / a.

### Cálculo
- Errar a **regra da cadeia** em funções compostas (ex.: `arcsin(arcsin x)`).
- Em integral definida, esquecer de **trocar os limites** ao fazer substituição.

### Trigonometria
- Esquecer identidades básicas: `sin² + cos² = 1`, `sec = 1/cos`, `tan(a+b)`.
- Perder soluções no intervalo pedido (ex.: `[0, π]` pode ter 2 soluções, não 1).

---

## Estratégia específica para questões estilo GMAT

### Suficiência de dados
- **Não calcule o valor final** — só decida se é **possível** determinar.
- Analise cada afirmação **sozinha** primeiro, depois **juntas**.
- As 5 alternativas são sempre as mesmas (ver `GLOSSARIO`). Decore-as.

### Problemas de trabalho/taxa
- Pense em **taxa = 1/tempo**. Bombas juntas: some as taxas. Tempo = 1 / (soma das taxas).
- Exemplo (2026): bombas de 1h, 1,5h e 3h → taxas 1 + 2/3 + 1/3 = 2 reservatórios/h → 30 min.

---

## Mentalidade

- **Engenheira formada tem vantagem:** você já viu quase tudo isso. É questão de **reativar**.
- Não trave no orgulho: pular uma questão difícil é estratégia, não fraqueza.
- O caderno de erros é seu melhor amigo na reta final — revise os erros, não a matéria toda.
