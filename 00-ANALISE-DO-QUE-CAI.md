# Análise — O que mais cai na prova PG-EIA / ITA

Análise das **6 provas reais de 2021 a 2026** (96 questões no total, 16 por prova).
Cada prova tem 16 questões de múltipla escolha, em inglês, 90 min, sem calculadora.

---

## Mapa de frequência (tema × ano)

Cada questão foi classificada pelo conteúdo **dominante**. Algumas tocam mais de um tema.

| Tema | 2021 | 2022 | 2023 | 2024 | 2025 | 2026 | Total aprox. |
|------|:----:|:----:|:----:|:----:|:----:|:----:|:----:|
| **Combinatória / Contagem** | ●● | ● | ●● | ●● | ●●● | ●● | **~12** |
| **Sistemas / Matrizes / Determinantes** | ● | ● | ●● | ●● | ●●● | ●● | **~11** |
| **Geometria plana e espacial** | ●●● | ●●● | ●●● | ●● | ●●● | ●●●● | **~18** |
| **Funções / Log / Exp** | ●● | ● | ●● | ● | ● | ●● | **~9** |
| **Polinômios e raízes** | ●● | ● | ●● | ●● | ●● | ●● | **~11** |
| **Sequências / PA / PG / Séries** | ● | ● | ● | — | — | ●● | **~5** |
| **Trigonometria** | ● | ●●● | ● | ● | ● | ● | **~8** |
| **Cálculo (deriv./integr./taxa)** | — | ● | ●● | ●● | ●●● | ●● | **~10** |
| **Números complexos** | — | ● | ● | — | — | ●● | **~4** |
| **Problemas taxa/trabalho/velocidade** | ●● | ● | ● | ●● | ● | ● | **~8** |
| **Lógica / Suficiência de dados** | ● | ● | — | — | — | — | **~2** |

> ● = aproximadamente uma questão. A soma passa de 96 porque questões híbridas contam em mais de um tema.

---

## Leitura dos dados

### 🔴 Os três pilares (caem SEMPRE)
1. **Geometria (plana + espacial)** é o tema mais pesado: 2 a 4 questões por prova.
   Recorrentes: círculos inscritos/tangentes, poliedros (cubo truncado, tetraedro, nonágono),
   áreas e volumes, triângulos (ortocentro, incentro), sólidos de revolução.
2. **Combinatória / contagem**: permutações (circular, com repetição), caminhos em grade,
   **coloração de sólidos com rotações** (Burnside) — esse último apareceu em 2021, 2024, 2025 e 2026.
3. **Sistemas lineares / matrizes / determinantes**: discussão de sistemas (quando tem 0, 1 ou ∞ soluções),
   cálculo de determinantes, equações matriciais (ex.: X² − 2X + 2I = 0).

### 🟠 Os temas de reforço (caem quase sempre)
4. **Polinômios e raízes**: natureza das raízes (reais/irracionais/inteiras), coeficientes de expansão binomial.
5. **Funções / log / exp**: equações exponenciais tipo `4^x − 2^(x+2) + 3 = 0`, propriedades de log, gráficos.
6. **Trigonometria**: identidades (sec, tan de soma), equações trigonométricas no intervalo.
7. **Sequências e séries**: PG infinita (inclusive com números complexos), somatórios.

### 🟡 Apoio (aparecem, mas em menor dose)
8. **Cálculo**: derivada como taxa de variação, integrais definidas com substituição,
   derivada de funções compostas (a famosa **regra da cadeia**), coordenadas polares. Tem crescido nos anos recentes.
9. **Números complexos**: forma polar, De Moivre, séries geométricas complexas.
10. **Problemas de taxa/trabalho**: bombas enchendo reservatório, pessoas varrendo, velocidade média.
11. **Lógica / suficiência de dados** (estilo GMAT clássico: "a afirmação I sozinha basta?").

---

## Padrões recorrentes dignos de atenção especial

Estes aparecem com frequência quase literal, ano após ano — **vale dominar o método**:

| Padrão | Anos em que apareceu | Onde estudar |
|--------|----------------------|--------------|
| **Coloração de cubo/sólido com rotações** (Burnside) | 2021, 2024, 2025, 2026 | `temas/01-combinatoria` |
| **Caminhos numa grade / quadrado** (contagem de trajetos) | 2024, 2025 | `temas/01-combinatoria` |
| **Discussão de sistema linear** (0, 1 ou ∞ soluções) | 2021, 2024, 2025, 2026 | `temas/02-sistemas-matrizes-determinantes` |
| **Natureza das raízes de polinômio** | todos | `temas/05-polinomios-e-raizes` |
| **Círculo inscrito/tangente em polígono** | 2021, 2023, 2026 | `temas/03-geometria` |
| **Poliedro: contar faces/vértices/arestas, área, volume** | 2023, 2024, 2025, 2026 | `temas/03-geometria` |
| **PG infinita (real ou complexa)** | 2021, 2023, 2026 | `temas/06-sequencias-pa-pg-series` |
| **Problema de trabalho conjunto** (bombas/pessoas) | 2022, 2023, 2026 | `temas/10-problemas-taxa-trabalho` |
| **Equação exponencial redutível a 2º grau** | 2024, 2026 | `temas/04-funcoes-log-exp` |

---

## Conclusão prática

Se o tempo for curto, concentre-se nesta ordem:

1. **Geometria** (maior peso absoluto)
2. **Combinatória** (padrão de coloração/caminhos se repete)
3. **Sistemas / matrizes / determinantes**
4. **Polinômios + Funções/log/exp**
5. **Trigonometria + Sequências/séries**
6. **Cálculo + Complexos + Problemas de taxa + Lógica** (apoio)

Dominando os 5 primeiros blocos, você cobre com folga as ~8 questões necessárias para o corte.
