## 3. Análise dos Resultados (Etapa 4)

**a)** Para 10 elementos, o algoritmo que realizou o menor número de comparações foi o **Insertion Sort** (27 comparações).

**b)** O algoritmo que realizou menos trocas ou movimentações foi o **Selection Sort** (apenas 7 trocas).

**c)** Sim. Ao aumentar para 20 elementos, o Insertion Sort (101) e o Quick Sort (83) continuaram com as menores taxas de comparação, enquanto o Selection Sort (17) se manteve como o mais eficiente no quesito trocas.

**d)** Ao passar para 1.000 elementos, houve um crescimento drástico (quadrático) no número de operações do Bubble, Insertion e Selection Sort, que saltaram para a casa das centenas de milhares. O Quick Sort, no entanto, cresceu de forma muito mais controlada, mantendo-se na casa dos milhares (10.664 comparações).

**e)** Não apresentaram a mesma quantidade. Embora todos pertençam à classe de complexidade de tempo O(n²), o *Big-O* desconsidera constantes. O Selection Sort faz todas as comparações possíveis (~499.500), enquanto o Insertion Sort, ao encontrar a posição correta, interrompe as comparações mais cedo (~238.487). 

**f)** O **Bubble Sort** apresentou o maior crescimento total, ultrapassando 736 mil operações somadas (comparações + trocas) no vetor de 1.000 elementos.

**g)** O Quick Sort diferenciou-se por apresentar um crescimento log-linear, resolvendo o problema de 1.000 elementos com uma quantidade de operações esmagadoramente menor em relação aos demais, provando sua eficiência em conjuntos maiores.

**h)** Sim, os resultados são totalmente coerentes. Os algoritmos O(n²) demonstraram um crescimento em forma de parábola, enquanto o Quick Sort demonstrou o esperado comportamento otimizado da estratégia de divisão e conquista O(n log n).

**i)** Escolheria o **Quick Sort**. Para milhares de pedidos na central de distribuição, a diferença entre realizar ~16 mil operações (Quick) e ~700 mil operações (Bubble) define se o sistema será ágil e em tempo real, ou se apresentará lentidão severa.
