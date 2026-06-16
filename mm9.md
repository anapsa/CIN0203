# Capítulo 7 — Computational Geometry

Geometria em CP exige cuidado com precisão, colinearidade e casos degenerados. Usar EPS, evitar comparar double com ==.


## 7.2 — Objetos básicos
**Point**
- Operações: distância, vetor, rotação, produto escalar, produto vetorial.
- cross > 0: esquerda/ccw.
- cross < 0: direita/cw.
- cross = 0: colinear.

**Line/Segment**
- Saber: reta por dois pontos, distância ponto-reta, distância ponto-segmento, interseção.
- Cuidado com paralelas, coincidentes, endpoints e colinearidade.

**Circle**
- Saber: área, circunferência, ponto dentro/fora, interseção reta-círculo e círculo-círculo.

**Triangle/Quadrilateral**
- Normalmente aparece como fórmula ou subparte: área, perímetro, altura, incírculo/circuncírculo.

## 7.3 — Polígonos
Representação comum: vector<Point> polygon.

Saber implementar:
- perímetro;
- área por Shoelace;
- testar convexidade;
- ponto dentro do polígono;
- cortar polígono por reta;
- convex hull.

Área:
area = abs(sum(cross(p[i], p[i+1]))) / 2

## Convex Hull
Algoritmo padrão: Andrew's Monotone Chain.
- Complexidade: O(n $log n$).
- Cuidado principal: o problema quer manter ou remover pontos colineares na borda?

## 7.4 — 3D Geometry
Geralmente envolve pontos 3D, distância, vetores, produto escalar/vetorial e planos. Muitas vezes dá para reduzir para fórmula ou para 2D.

## Checklist de geometria
1. Usei EPS?
2. Tratei pontos repetidos?
3. Tratei colinearidade?
4. Tratei segmento que só encosta?
5. A borda conta como dentro?
6. A área pode sair negativa?
7. A ordem dos pontos importa?
