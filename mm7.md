# Capítulo 5 — Mathematics

## Ideia geral
Reconhecer padrão, fórmula, propriedade de números ou recorrência. A habilidade principal é evitar simular quando existe uma expressão direta.

## 5.2 — Ad Hoc Matemático
**Fórmula/padrão**
- Testar casos pequenos e procurar PA, PG, paridade, tabuleiro, diagonal, soma ou simetria.
- Trocar simulação grande por fórmula O(1) ou O($log n$).

**Base, log e potência**
- Converter base usando decimal como intermediário quando couber.
- Usar log para dígitos e ordem de grandeza.
- Usar fast exponentiation para potência com módulo.

**Frações/polinômios**
- Reduzir frações com gcd.
- Avaliar polinômios com Horner.
- Cuidar de overflow e precisão.

## 5.3 — Number Theory
**Primos/fatoração**
- Usar crivo para muitas consultas até N.
- Usar trial division até sqrt(n) para fatorar um número.
- Usar fatoração para quantidade/soma de divisores e Euler Phi.

**GCD/LCM**
- Usar em frações, divisibilidade, ciclos e periodicidade.
- Calcular a/gcd(a,b)*b para reduzir risco de overflow.

**Modular arithmetic**
- Usar inverso modular para divisão.
- Usar a^(MOD-2) quando MOD é primo.
- Usar Euclides estendido quando MOD não é primo e gcd(a,m)=1.

## 5.4 — Combinatorics
**Reconhecer**
- Fibonacci: recorrência simples.
- Binomial C(n,k): escolher subconjuntos.
- Catalan: parênteses, árvores binárias, triangulações, caminhos válidos.

**Escolher técnica**
- Usar Pascal para n pequeno.
- Usar factorial + inverso modular para muitas queries com MOD primo.
- Usar matrix power/fast doubling para Fibonacci com n grande.

## 5.5 — Probability
Usar quando aparecer chance, expectativa ou contagem de eventos.

**Caminhos comuns**
- Derivar fórmula fechada.
- Contar favoráveis / totais.
- Usar DP quando a probabilidade depende de estado.

**Armadilhas**
- Confundir eventos dependentes e independentes.
- Esquecer complemento.
- Errar formato/precisão da saída.

## 5.6 — Cycle Finding
Usar quando uma sequência gerada por função pode repetir.

**Opções**
- Guardar visited[value] se o estado cabe.
- Usar Floyd se quiser memória O(1).

slow = f(slow)
fast = f(fast)

## 5.7 — Game Theory básico
Usar quando dois jogadores jogam alternadamente e ambos jogam perfeito.

estado vencedor = existir movimento para estado perdedor
estado perdedor = todos os movimentos irem para estados vencedores

**Reconhecer**
- Nim: usar XOR.
- Jogos pequenos: usar DP de vencedor/perdedor.
- Jogos com estado grande: procurar padrão matemático.

## 5.8 — Matrix Power
Usar quando houver recorrência linear e n grande.

estado(n) = M * estado(n-1)
resposta = M^n * estado inicial
complexidade = O(k^3 log n)

Bom para Fibonacci grande, contagem de caminhos com tamanho fixo e DP linear recorrente.
