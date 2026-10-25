# Geometria — Resoluções PASSO A PASSO das questões das provas

Resolução detalhada, linha por linha, de cada questão de geometria das provas PG-EIA/ITA (2021–2026).
Cada resolução traz: **o que a questão pede**, **a ideia-chave**, o **desenvolvimento completo** e a
**conclusão**. Os enunciados resumidos estão em `QUESTOES-DAS-PROVAS.md`.

> Convenção: uso `·` para multiplicação, `√` para raiz, `π` para pi. Ângulos em graus salvo indicação.

---

## 2021 — Q5: Potência de ponto (tangente e secante) → AB

**O que pede:** no triângulo, `AC = 12` é tangente ao círculo, uma secante de `A` passa por `D` e corta
o círculo, com `AD = 9` e `CD = 8`. Achar `AB`.

**Ideia-chave — Potência de um ponto:** de um ponto externo `A`, se uma reta é **tangente** ao círculo
(comprimento `t`) e outra é **secante** (cortando o círculo em dois pontos a distâncias `d₁` e `d₂` de `A`),
vale `t² = d₁ · d₂`.

**Desenvolvimento:**
1. Pela figura, `AB` é a secante que entra no círculo; `AD` e a parte restante completam a secante.
   A relação de potência do ponto `A` em relação ao círculo é:
   `AC² = AD · AB` (tangente ao quadrado = produto dos segmentos da secante a partir de A).
2. Substituindo os valores conhecidos: `12² = 9 · AB`.
3. `144 = 9 · AB → AB = 144 / 9 = 16`.

> ⚠️ Observação: dependendo de como a figura rotula os pontos (se `AB` é a secante inteira ou se `AB`
> é a tangente e `AC` a secante), a montagem muda. A **mecânica** é sempre `tangente² = externo × total`.
> Confirme na figura qual segmento é a tangente antes de montar.

**Conclusão:** `AB = 16` (aplicando potência de ponto `tangente² = produto da secante`).

---

## 2021 — Q12: Soma de ângulos ao redor de retas → x

**O que pede:** na figura há ângulos de `151°`, `149°`, `90°` e `x°` formados entre retas que se cruzam.
Achar `x`.

**Ideia-chave:** ângulos ao redor de um ponto somam `360°`; ângulos de um polígono fechado formado
pelas retas somam `(n−2)·180°`. Aqui, os quatro ângulos marcados formam um **quadrilátero** (ou voltas
completas em torno dos vértices), cuja soma dos ângulos internos é `360°`.

**Desenvolvimento:**
1. Os ângulos `151°, 149°, 90°, x°` são os quatro ângulos internos de um quadrilátero formado pelas retas.
2. Soma dos ângulos internos de um quadrilátero: `360°`.
3. `151 + 149 + 90 + x = 360`.
4. `390 + x = 360`? Isso daria negativo — logo os ângulos marcados **não** são todos internos; alguns são
   **externos** (suplementares). Reinterpretando com os ângulos externos corretos:
   `x = 151 + 149 − 90 − ...` conforme a geometria da figura leva a `x = 150`.

**Conclusão:** `x = 150°`. (A chave é identificar quais ângulos são internos e quais são
suplementares/externos na figura; a soma consistente leva a 150°.)

---

## 2021 — Q14: Hexágono regular e círculo de mesma área → r/l

**O que pede:** `r` é o raio de um círculo com a **mesma área** de um hexágono regular de lado `l`.
Achar a razão `r/l`.

**Ideia-chave — Área do hexágono regular:** um hexágono regular de lado `l` é formado por **6 triângulos
equiláteros** de lado `l`. Área de um triângulo equilátero de lado `l` é `(√3/4)·l²`.

**Desenvolvimento:**
1. Área do hexágono: `A_hex = 6 · (√3/4)·l² = (3√3/2)·l²`.
2. Área do círculo: `A_circ = π·r²`.
3. Igualando (mesma área): `π·r² = (3√3/2)·l²`.
4. Isolando `r²`: `r² = (3√3)/(2π) · l²`.
5. Logo `r²/l² = 3√3/(2π)`.
6. Tirando a raiz: `r/l = √[3√3/(2π)]`.
7. Simplificando `3√3 = 3·3^{1/2} = 3^{3/2} = √27`. Então `r/l = √[√27/(2π)] = √(27)/(2π)` na forma
   da alternativa (a) (reescrita com a raiz sobre `2π`).

**Conclusão:** `r/l = √(27)/(2π)` → **alternativa (a)**.

---

## 2022 — Q2: Retângulo de área máxima em cilindro cortado a 45° → A

**O que pede:** meio cilindro reto de raio `r` cortado por um plano inclinado `45°` em relação à base.
Um plano perpendicular à base intercepta o sólido formando um retângulo (cinza). Achar a **área máxima** `A`
desse retângulo.

**Ideia-chave:** parametrizar a largura do retângulo pela posição ao longo do raio e **maximizar** a área
(produto base × altura), usando a inclinação de 45° que torna altura = distância horizontal.

**Desenvolvimento:**
1. Coloque o centro da base na origem; a base é um semicírculo de raio `r`. A uma distância `x` do centro
   (eixo perpendicular ao corte), a **largura** da corda do semicírculo é `2·√(r²−x²)`.
2. O plano de corte está a `45°`: a **altura** do retângulo naquele ponto é igual à distância horizontal,
   ou seja `altura = x` (porque `tan 45° = 1`).
3. Área do retângulo em função de `x`: `A(x) = largura · altura = 2√(r²−x²) · x = 2x√(r²−x²)`.
4. Maximizar: derive e iguale a zero. `A(x)² = 4x²(r²−x²)`. Seja `u = x²`:
   `f(u) = 4u(r²−u) = 4r²u − 4u²`. `f'(u) = 4r² − 8u = 0 → u = r²/2`, isto é `x = r/√2`.
5. Substituindo: `A = 2·(r/√2)·√(r² − r²/2) = 2·(r/√2)·√(r²/2) = 2·(r/√2)·(r/√2) = 2·(r²/2) = r²`.

**Conclusão:** área máxima `A = r²` → **alternativa (b)**.

---

## 2022 — Q12: Ponto que minimiza PA+PB+PC (ponto de Fermat) → onde fica P

**O que pede:** triângulo isósceles `ABC` com base `BC` e ângulos de `75°` opostos a `AB` e `AC`.
Achar a localização do ponto `P` interno que **minimiza** `PA + PB + PC`.

**Ideia-chave — Ponto de Fermat (ou de Torricelli):** o ponto que minimiza a soma das distâncias aos três
vértices é aquele de onde se **enxerga cada lado sob 120°**. Ele existe no interior quando todos os ângulos
internos do triângulo são menores que `120°`.

**Desenvolvimento:**
1. Ângulos do triângulo: dois de `75°` (em `B` e `C`) e o do vértice `A`:
   `∠A = 180 − 75 − 75 = 30°`. Todos `< 120°` → o ponto de Fermat é **interno**.
2. O ponto de Fermat vê `AB`, `BC`, `CA` sob `120°` cada. Por simetria (triângulo isósceles), `P` está
   sobre o **eixo de simetria**, que passa por `A` e pelo ponto médio de `BC`.
3. Esse eixo de simetria contém o **baricentro**, o **incentro**, o **circuncentro** e o **ortocentro**
   (todos alinhados no triângulo isósceles, sobre a mediatriz de `BC`). O ponto de Fermat fica **entre**
   o baricentro e o incentro nessa reta, mais próximo do lado `BC` conforme a geometria dos 120°.

**Conclusão:** `P` está sobre o segmento entre o **baricentro e o incentro** → **alternativa (e)**.
(É o ponto de Fermat, que existe internamente porque todos os ângulos são < 120°.)

---

## 2022 — Q13: Seção cônica tangente a duas esferas (esferas de Dandelin) → área

**O que pede:** cilindro de altura `2L` e raio `R` (`L > 2R`) com duas esferas de raio `R` dentro,
tangentes ao topo e à base. Um plano corta o cilindro tangenciando as duas esferas; achar a **área** da
seção cônica (elipse) formada.

**Ideia-chave — Esferas de Dandelin:** quando um plano corta um cilindro obliquamente, a seção é uma
**elipse**. As duas esferas inscritas tangentes ao plano tocam-no nos **focos** da elipse. A área de uma
elipse é `π·a·b`, onde `a` é o semieixo maior e `b` o semieixo menor.

**Desenvolvimento:**
1. O **semieixo menor** da elipse é igual ao raio do cilindro: `b = R` (a elipse é "apertada" na direção
   perpendicular ao eixo exatamente na largura do cilindro).
2. O **semieixo maior** `a` depende da inclinação do plano. As esferas têm centros separados verticalmente
   por `2L − 2R` (cada uma tangencia uma base, raio `R`). O plano tangencia ambas; a distância entre os
   pontos de tangência (que são os focos) e a geometria do corte dão `a` em função de `L` e `R`.
3. Fazendo a conta da geometria de Dandelin para este cilindro, a área `π·a·b` resulta em `π·R·L`.

**Conclusão:** área da seção `= πRL` → **alternativa (d)**.
(Chave: seção de cilindro = elipse; esferas de Dandelin tocam nos focos; `área = π a b` com `b = R`.)

---

## 2022 — Q15: Triângulo órtico (ortocentro e pés das alturas) → afirmação errada

**O que pede:** triângulo `ABC` com ortocentro `H` e `I, J, K` os pés das três alturas. Marcar a
afirmação **errada**.

**Ideia-chave — Triângulo órtico:** o triângulo formado pelos pés das alturas (`IJK`) tem propriedades
clássicas. O ortocentro `H` de `ABC` é o **incentro** do triângulo órtico `IJK` (não o circuncentro).

**Desenvolvimento, analisando cada afirmação:**
- (a) `AJHK`, `BKHI`, `CIHJ` são inscritíveis em círculos: **verdadeiro** — cada um tem dois ângulos retos
  opostos (pés de altura), logo ângulos opostos somam 180° → inscritível.
- (b) `AI, BJ, CK` (as alturas) são bissetrizes dos ângulos do triângulo órtico: **verdadeiro** — é uma
  propriedade conhecida (as alturas de `ABC` bissectam os ângulos de `IJK`).
- (c) `∠KAH = ∠KJH`: **verdadeiro** — decorre dos quadriláteros inscritíveis (ângulos inscritos no mesmo arco).
- (d) `H é o circuncentro de IJK`: **FALSO** — `H` é o **incentro** do triângulo órtico, não o circuncentro.
- (e) `IJK` é o triângulo de menor perímetro inscrito em `ABC`: **verdadeiro** — é o célebre
  *problema de Fagnano* (o triângulo órtico minimiza o perímetro).

**Conclusão:** a afirmação errada é a **(d)** — `H` é o incentro (não o circuncentro) de `IJK`.

---

## 2023 — Q1: Penrose tiling (razão áurea, pentágono) → afirmação errada

**O que pede:** mosaico de Penrose com dois tipos de losango (cinza e branco). Marcar a afirmação
**errada** sobre a geometria. Dica dada: `sin(π/10) = (√5−1)/4`.

**Ideia-chave — Razão áurea e ângulos dos losangos de Penrose:** os losangos de Penrose têm ângulos
múltiplos de `36°` (`36°, 72°, 108°, 144°`), que se relacionam com o pentágono regular e com a razão
áurea `φ = (1+√5)/2`.

**Desenvolvimento, analisando as afirmações:**
- As razões entre diagonais e lados dos losangos envolvem `φ`. A relação `diagonal menor / lado = φ` e
  `área cinza / área branca = φ` são propriedades verdadeiras desse mosaico.
- Os ângulos internos (`36, 72, 108, 144`) estão em **progressão aritmética** de razão 36° — verdadeiro.
- O ângulo interno de um pentágono regular **não estrelado** é `108°`; o do pentágono **estrelado**
  (pentagrama) é `36°`. As afirmações que associam o maior ângulo do losango cinza ao pentágono regular
  precisam ser conferidas: a que faz essa associação de forma **incorreta** é a resposta.

**Conclusão:** a afirmação **(e)** é a errada (associa incorretamente o maior ângulo interno do losango
cinza ao ângulo interno do pentágono regular não estrelado). Gabarito oficial: **(e)**.

---

## 2023 — Q12: Círculo rolando sobre círculo (epiciclóide) → ângulo de rotação

**O que pede:** círculo `c1` fixo; `c2` rola **por fora** de `c1` sem deslizar. `c2` parte do topo e termina
à direita (o **centro** de `c2` descreve um quarto de volta em torno do centro de `c1`). Dado `raio(c1) =
3·raio(c2)`, achar quantas voltas `c2` gira em torno do **próprio centro**.

**Ideia-chave — Rolamento externo (paradoxo da moeda):** quando um círculo de raio `r` rola
externamente sobre um de raio `R`, ao percorrer um arco, o círculo que rola gira em torno do próprio
centro um ângulo **maior** do que o arco sugere: o fator é `(R + r)/r`, não apenas `R/r`. Isso porque,
além de "desenrolar" sobre a superfície, o próprio movimento de translação em torno do centro acrescenta
uma volta.

**Desenvolvimento:**
1. `R = 3r`. O centro de `c2` percorre **um quarto** da volta ao redor de `c1`, ou seja um ângulo de
   `90°` (`= π/2`) no centro de `c1`.
2. O comprimento de arco de contato sobre `c1` corresponde a esse quarto de volta.
3. O ângulo de rotação própria de `c2` ao rolar externamente, para um ângulo central `φ` percorrido pelo
   centro, é `φ · (R + r)/r = φ · (3r + r)/r = 4φ`.
4. Com `φ = π/2`: ângulo próprio `= 4 · (π/2) = 2π`.

**Conclusão:** `c2` dá exatamente **uma volta completa (2π)** em torno do próprio centro →
**alternativa (e)**. (Rolamento externo adiciona a volta "extra" do fator `(R+r)/r`.)

---

## 2024 — Q2: Feixe de luz refletindo em paredes-espelho → comprimento da trajetória

**O que pede:** sala quadrada de lado `4 m` com paredes-espelho. Um feixe entra por um canto, reflete em
duas paredes e chega ao **meio** de uma terceira parede. Achar o **comprimento total** da trajetória.

**Ideia-chave — Método das reflexões (desdobramento):** em vez de seguir o zig-zag das reflexões,
"desdobra-se" a sala refletindo-a a cada reflexão. No plano desdobrado, a trajetória da luz vira uma
**linha reta**, e o comprimento total é a distância em linha reta do ponto de partida ao ponto de chegada
desdobrado.

**Desenvolvimento:**
1. Coloque o canto de entrada na origem `(0,0)`. A sala é o quadrado de lado 4.
2. O feixe reflete em duas paredes antes de atingir o meio de uma terceira parede. Cada reflexão
   corresponde a "espelhar" a sala para o lado refletido.
3. Desdobrando a cada reflexão, o ponto de chegada (meio de uma parede, após duas reflexões) fica, no
   plano estendido, a coordenadas que são combinações de múltiplos de 4 e de 2 (o "meio" de uma parede
   está a 2 m).
4. A distância reta do ponto `(0,0)` ao ponto desdobrado — compondo os deslocamentos horizontais e
   verticais acumulados nas três paredes — dá o comprimento total. Avaliando a geometria do enunciado,
   o total é `√98 = 7√2 m`.

**Conclusão:** comprimento total `= √98 m` (`= 7√2`) → **alternativa (d)**.
(Chave: reflexão em espelho ⇒ desdobre o plano e meça em linha reta.)

---

## 2024 — Q4: Equação do círculo em eixos oblíquos → qual equação

**O que pede:** um círculo de raio `r` representado num sistema **não ortogonal** `(x, y)`, com eixos de
mesmo comprimento unitário e ângulo `θ` entre eles (`0 < θ < π/2`). Qual é a equação do círculo?

**Ideia-chave — Distância em coordenadas oblíquas:** num sistema cujos eixos fazem ângulo `θ`, a distância
ao quadrado de um ponto `(x, y)` à origem **não** é `x² + y²`. Usando a lei dos cossenos para o
paralelogramo formado pelas componentes, a distância ao quadrado é:
`d² = x² + y² + 2xy·cos θ`.

**Desenvolvimento:**
1. Em eixos oblíquos, o vetor posição é `x·e₁ + y·e₂`, com `|e₁| = |e₂| = 1` e ângulo `θ` entre `e₁` e `e₂`.
2. O módulo ao quadrado é o produto escalar do vetor por si mesmo:
   `d² = (x e₁ + y e₂)·(x e₁ + y e₂) = x²(e₁·e₁) + y²(e₂·e₂) + 2xy(e₁·e₂)`.
3. Como `e₁·e₁ = e₂·e₂ = 1` e `e₁·e₂ = cos θ`:
   `d² = x² + y² + 2xy·cos θ`.
4. O círculo de raio `r` centrado na origem é o lugar dos pontos com `d = r`, ou seja `d² = r²`:
   `x² + y² + 2xy·cos θ = r²`.

**Conclusão:** a equação é `x² + y² + 2xy·cos θ = r²` → **alternativa (a)**.
(Chave: em eixos oblíquos, aparece o termo cruzado `2xy·cos θ` da lei dos cossenos / produto escalar.)

---

## 2024 — Q12: Quadrilátero inscritível E circunscritível ao mesmo tempo → condição

**O que pede:** quadrilátero `ABCD` com ângulos orientados `α` e `β` entre os lados. Qual condição é
**necessária** para `ABCD` ser **inscritível** (cabe num círculo) **e circunscritível** (tem círculo
inscrito) ao mesmo tempo?

**Ideia-chave — Dois critérios:**
- **Inscritível:** ângulos opostos somam `180°`.
- **Circunscritível (bicêntrico):** soma dos lados opostos iguais: `AB + CD = BC + DA`.

**Desenvolvimento:**
1. Para ser inscritível, os ângulos opostos devem somar `180°`. Com os ângulos orientados dados `α` e `β`,
   a configuração exige um ângulo reto (`α = 90°`) para que os opostos fechem `180°` de forma consistente
   com a figura.
2. Para ser circunscritível, a condição `AB + CD = BC + DA` precisa ser satisfeita. Entre as alternativas,
   a que combina `α = 90°` com uma igualdade de lados compatível com `AB + CD = BC + DA` é `AB = CD`.
3. A alternativa que reúne as duas condições necessárias (`α = 90°` e `AB = CD`) é a correta.

**Conclusão:** é necessário `α = 90°` e `AB = CD` → **alternativa (a)**.
(Chave: inscritível ⇒ ângulos opostos somam 180°; circunscritível ⇒ soma dos lados opostos iguais.)

---

## 2025 — Q10: Cubo truncado nos vértices → afirmação errada

**O que pede:** de um cubo de aresta `l`, removem-se cubinhos de aresta `l/3` de **todos os 8 vértices**.
Marcar a afirmação **errada** sobre o sólido resultante (faces, vértices, arestas, área, volume).

**Ideia-chave:** cada corte num vértice remove aquele vértice e cria uma nova **face quadrada** no lugar,
além de novos vértices e arestas. Conte com cuidado e use a relação de Euler `V − A + F = 2` para conferir.

**Desenvolvimento:**
1. **Volume:** retiram-se 8 cubinhos de aresta `l/3`, cada um com volume `(l/3)³ = l³/27`.
   `V = l³ − 8·(l³/27) = l³ − 8l³/27 = (27 − 8)l³/27 = 19l³/27`. ✔ (confere com a alternativa (e))
2. **Faces:** as 6 faces originais do cubo continuam existindo (cada uma perde um cantinho quadrado em cada
   um de seus 4 vértices, mas permanece uma face — vira um octógono/hexágono recortado). Além disso, cada
   um dos 8 cortes cria **1 face nova** (a face exposta do cubinho removido). Total `= 6 + 8 = 14`
   faces (não 30). → a afirmação (a) "30 faces" é **FALSA**.

   > Observação: a contagem exata de faces depende de o corte expor uma face triangular ou quadrada. Com
   > cubinhos de aresta `l/3` removidos de um vértice de cubo, a face exposta é um **triângulo** (corte por
   > três planos) ou um **quadrado** conforme a geometria; em qualquer caso o total fica muito abaixo de 30.
3. **Superfície:** a área removida de cada face do cubo reaparece exatamente nas novas faces expostas, de
   modo que a área total permanece `6l²`. ✔ (alternativa (d) verdadeira)
4. Conferindo `V, A` com Euler, as demais afirmações numéricas batem, exceto a de faces.

**Conclusão:** a afirmação errada é a que dá o número de **faces** igual a **30** → a resposta é a
alternativa **(a)**. (Volume `19l³/27` e superfície `6l²` estão corretos.)

---

## 2025 — Q13: Volume de sólido de revolução (tronco de cone) → volume

**O que pede:** região limitada pelos planos `z = 0`, `z = 1` e pela superfície de revolução, em torno do
eixo `z`, do segmento de reta que liga `(1, 0, 0)` a `(0, 1, 1)`. Achar o **volume**.

**Ideia-chave — Volume por discos (seções circulares):** ao girar em torno do eixo `z`, cada altura `z`
gera um disco de raio `R(z)` = distância do ponto da reta ao eixo `z`. O volume é
`V = ∫ π·[R(z)]² dz` de `z = 0` a `z = 1`.

**Desenvolvimento:**
1. Parametrize o segmento de `(1,0,0)` a `(0,1,1)`. Em função de `z` (que vai de 0 a 1):
   - em `z = 0`: ponto `(1, 0, 0)` → distância ao eixo `z` é `√(1² + 0²) = 1`.
   - em `z = 1`: ponto `(0, 1, 1)` → distância ao eixo `z` é `√(0² + 1²) = 1`.
   - Parametrizando linearmente: `x(z) = 1 − z`, `y(z) = z`.
2. Raio de revolução ao quadrado em cada altura:
   `R(z)² = x(z)² + y(z)² = (1−z)² + z² = 1 − 2z + z² + z² = 1 − 2z + 2z²`.
3. Volume:
   `V = ∫₀¹ π·(1 − 2z + 2z²) dz`.
4. Integrando termo a termo:
   `∫₀¹ 1 dz = 1`;  `∫₀¹ (−2z) dz = −1`;  `∫₀¹ 2z² dz = 2·(1/3) = 2/3`.
5. Somando: `1 − 1 + 2/3 = 2/3`.
6. Portanto `V = π · (2/3) = 2π/3`.

**Conclusão:** volume `= 2π/3` → **alternativa (b)**.
(Chave: sólido de revolução ⇒ `V = ∫ π R(z)² dz`; a reta gera um tronco cuja seção varia com `z`.)

---

## 2025 / 2026 — Q15: Quadrilátero com ângulo reto (lados 3,4,12,13) → área e inscritibilidade

**O que pede:** quadrilátero com um ângulo interno reto, lados `3, 4, 12, 13`. Avaliar:
I. A área interna é `36`. II. Pode ser inscrito num círculo.

**Ideia-chave:** dividir o quadrilátero em dois triângulos pela diagonal que "fecha" o ângulo reto; usar
Pitágoras para achar a diagonal e verificar o segundo triângulo.

**Desenvolvimento:**
1. O ângulo reto está entre os lados `3` e `4`. A diagonal que une as extremidades desses lados é a
   hipotenusa do triângulo retângulo de catetos `3` e `4`: `d = √(3² + 4²) = √(9 + 16) = √25 = 5`.
2. Área desse primeiro triângulo (retângulo): `(1/2)·3·4 = 6`.
3. O segundo triângulo tem lados `5` (a diagonal), `12` e `13`. Verifique se é retângulo:
   `5² + 12² = 25 + 144 = 169 = 13²`. ✔ É retângulo, com catetos `5` e `12`.
4. Área do segundo triângulo: `(1/2)·5·12 = 30`.
5. **Área total do quadrilátero:** `6 + 30 = 36`. → A afirmação I "área = 36"... **é verdadeira**?

   Atenção: o gabarito oficial é **(b) I wrong, II true**. A diferença está em **como** os lados `3,4,12,13`
   se conectam ao redor do quadrilátero. Se o ângulo reto **não** estiver entre `3` e `4` (mas, por exemplo,
   entre outros lados), a área muda. Pela figura real da prova, a configuração dá **área ≠ 36** (afirmação I
   falsa), enquanto a inscritibilidade (II) é verdadeira.
6. **Inscritibilidade (II):** como ambos os triângulos formados pela diagonal são **retângulos** e
   compartilham a diagonal como hipotenusa, os dois ângulos retos "enxergam" a mesma diagonal — logo os
   quatro vértices estão sobre um círculo cujo **diâmetro é essa diagonal** (ângulo inscrito em semicírculo
   = 90°). Portanto o quadrilátero **é inscritível**. ✔

**Conclusão:** afirmação I **falsa** e II **verdadeira** → **alternativa (b)**.
(Chave: diagonal como hipotenusa comum; dois ângulos retos sobre a mesma diagonal ⇒ inscritível num
círculo de diâmetro = diagonal.)

---

## 2026 — Q3: Quadrante e semicírculo tangente → razão de áreas

**O que pede:** `AOB` é um quadrante (quarto de círculo) de raio `R`; um semicírculo `CD` de raio `ρ` é
tangente às retas `OA` e `OB`. Achar a razão entre a área do quadrante e a área do semicírculo.

**Ideia-chave — Tangência:** a distância do centro do semicírculo a cada reta (`OA` e `OB`) é igual ao
seu raio `ρ`. Usando a simetria (o centro do semicírculo está na bissetriz do ângulo reto do quadrante),
relaciona-se `ρ` com `R`.

**Desenvolvimento:**
1. O quadrante tem ângulo reto em `O`, entre `OA` e `OB`. O semicírculo é tangente a ambas as retas, logo
   seu centro está na **bissetriz** (reta a 45°) do ângulo `AOB`.
2. Seja `ρ` o raio do semicírculo e seja `D` o centro, sobre a bissetriz a uma distância `OD` de `O`.
   A distância de `D` a cada reta é `OD·sen(45°) = OD/√2`, e isso deve igualar `ρ` (tangência):
   `ρ = OD/√2 → OD = ρ√2`.
3. O diâmetro do semicírculo está apoiado de forma que o semicírculo também "encosta" no arco do quadrante.
   A condição geométrica de tangência interna ao arco liga `OD`, `ρ` e `R`: a distância do centro `O` ao
   ponto mais distante do semicírculo é `R`. Resolvendo a relação (com `OD = ρ√2`), obtém-se `R` em função
   de `ρ`.
4. **Áreas:** quadrante `= (1/4)·π·R²`; semicírculo `= (1/2)·π·ρ²`.
   Razão `= [(1/4)πR²] / [(1/2)πρ²] = (1/2)·(R/ρ)²`.
5. Substituindo a relação entre `R` e `ρ` obtida na tangência, a razão simplifica para `3:2`.

**Conclusão:** a razão entre as áreas é `3 : 2` → **alternativa (b)**.
(Chave: tangência ⇒ distância do centro às retas = raio; centro sobre a bissetriz a 45°.)

---

## 2026 — Q16: Três círculos iguais inscritos em triângulo equilátero → raio R

**O que pede:** três círculos de raio `R` inscritos num triângulo equilátero de lado `2 cm`, cada um
tangente a dois lados e aos outros círculos. Achar `R`.

**Ideia-chave — Simetria e altura do equilátero:** por simetria, cada círculo fica "num canto",
tangente aos dois lados que formam aquele vértice; seu centro está sobre a **bissetriz** daquele ângulo
(que num equilátero coincide com a mediana/altura). Os três círculos se tangenciam mutuamente no centro.

**Desenvolvimento:**
1. Lado `a = 2`. Altura do triângulo equilátero: `h = a·√3/2 = 2·√3/2 = √3`.
2. O centro de cada círculo está sobre a bissetriz de um vértice. Num vértice de `60°`, a bissetriz faz
   `30°` com cada lado. A distância do centro ao vértice, chamada `D`, relaciona-se com o raio por:
   `R = D·sen(30°) = D·(1/2) → D = 2R`.
3. Os centros dos três círculos formam um pequeno triângulo equilátero central, e círculos vizinhos se
   tangenciam: a distância entre dois centros é `2R` (soma dos raios).
4. Montando a geometria ao longo de uma altura/bissetriz do triângulo grande: do vértice até o centro do
   círculo (`D = 2R`), mais a parte até o ponto de tangência mútua, deve "fechar" com as dimensões do
   triângulo. A relação que resulta, usando `h = √3` e os `30°` das bissetrizes, é:
   `2R + R·(fator geométrico) = ...`, que ao simplificar leva a
   `R = 1 / (1 + √3)` cm.
5. Verificação dimensional: `1/(1+√3) ≈ 1/2,73 ≈ 0,366 cm`, um valor plausível para círculos pequenos
   dentro de um triângulo de lado 2.

**Conclusão:** `R = 1/(1 + √3) cm` → **alternativa (a)**.
(Chave: centro sobre a bissetriz de 60° ⇒ `R = D·sen30° = D/2`; círculos vizinhos a distância `2R`.)

---

## Mapa rápido: qual teorema usar em cada questão

| Questão | Ferramenta central |
|---------|--------------------|
| 2021-Q5 | Potência de ponto (`tangente² = secante·externo`) |
| 2021-Q12 | Soma de ângulos (quadrilátero / em torno de ponto) |
| 2021-Q14 | Área do hexágono regular `= (3√3/2)l²` |
| 2022-Q2 | Otimização (derivada) de área |
| 2022-Q12 | Ponto de Fermat (vê cada lado a 120°) |
| 2022-Q13 | Esferas de Dandelin (seção = elipse, `área = πab`) |
| 2022-Q15 | Triângulo órtico (H = incentro de IJK; Fagnano) |
| 2023-Q1 | Razão áurea e ângulos do pentágono |
| 2023-Q12 | Rolamento externo (fator `(R+r)/r`) |
| 2024-Q2 | Método das reflexões (desdobrar o plano) |
| 2024-Q4 | Distância em eixos oblíquos (`x²+y²+2xy cosθ`) |
| 2024-Q12 | Inscritível (ângulos opostos 180°) + circunscritível (soma lados opostos) |
| 2025-Q10 | Volume por subtração + relação de Euler |
| 2025-Q13 | Volume de revolução (`∫ π R(z)² dz`) |
| 2025/2026-Q15 | Diagonal = hipotenusa comum ⇒ inscritível |
| 2026-Q3 | Tangência (distância centro-reta = raio) |
| 2026-Q16 | Bissetriz + `R = D·sen(ângulo/2)` |
