# Capítulo 6 — String Processing

A primeira decisão em strings é separar substring de subsequência.

- substring = contínua
- subsequence = pode pular caracteres

## 6.2 — Ad Hoc String
Usar quando o problema é manipulação cuidadosa.

**Observar**
- parsing, frequência, espaços, pontuação, case-sensitive, ordenação customizada.
- entrada com linha vazia.
- caracteres fora de a-z.

## 6.3 — String com DP
**Edit Distance**
- Usar para transformar uma string em outra.
- Estado comum: dp[i][j] = custo nos prefixos A[0..i), B[0..j).
- Operações: inserir, deletar, substituir.

**LCS**
- Usar quando a pergunta fala em subsequência comum.
- Estado comum: dp[i][j] = LCS dos prefixos.

**Dica**
- Se for substring, pensar em matching, hashing ou suffix array.
- Se for subsequência, pensar em DP.

## 6.4 — String Matching
Usar quando for preciso encontrar padrão P em texto T.

**Escolher técnica**
- Usar find para caso simples.
- Usar KMP para O(n+m) com controle total.
- Usar Rabin-Karp/hashing para muitas comparações.

**KMP**
pi/lps[i] = tamanho do maior prefixo que também é sufixo
complexidade = O(n+m)

**Grid 2D**
- Transformar cada direção em busca linear.
- Cuidar dos limites da matriz.

## 6.5 — Suffix Trie / Tree / Array
Usar quando houver muitas perguntas sobre substrings da mesma string.

**Suffix Array**
- Ordenar todos os sufixos.
- Buscar padrão com binary search.
- Contar substrings distintas.
- Achar longest repeated/common substring.

**LCP**

LCP[i] = maior prefixo comum entre suffixArray[i] e suffixArray[i-1]

Evitar implementar suffix tree em contest se não estiver muito treinado.

## 6.6 — String Hashing
Usar para comparar substrings rápido.

hash(l,r) em O(1) após prefix hash

**Cuidados**
- Usar módulo grande, long long ou double hash.
- Normalizar hash antes de comparar.
- Lembrar que colisão existe.

## 6.7 — Anagram and Palindrome
**Anagrama**
- Comparar frequência de caracteres.
- Ordenar string se for simples.

**Palíndromo**
- Usar dois ponteiros para teste único.
- Usar DP ou hashing para muitas consultas.
- Lembrar que bordas e tamanho par/ímpar importam.
