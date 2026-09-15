## 4. Desafio Adicional

Repeti o experimento com um vetor de 1.000 elementos em três situações diferentes. Os resultados (Comparações, Movimentações) foram os seguintes:

*   **Vetor Aleatório:** Bubble (497.355, 246.733) | Insertion (247.725, 247.732) | Selection (499.500, 994) | Quick (10.578, 6.568)
*   **Vetor Já Ordenado:** Bubble (999, 0) | Insertion (999, 999) | Selection (499.500, 0) | Quick (499.500, 500.499)
*   **Vetor Ordem Inversa:** Bubble (499.500, 499.500) | Insertion (499.500, 500.499) | Selection (499.500, 500) | Quick (499.500, 250.499)

**Análise:**

A organização inicial dos dados interfere bastante na quantidade de operações, mas cada algoritmo reage de um jeito diferente.

1. **Vetores já ordenados:** O Bubble e o Insertion Sort percebem que a lista já está ordenada e terminam o trabalho rapidinho, fazendo poucas operações. Ironicamente, esse cenário costuma ser o pior caso para o Quick Sort, fazendo com que ele realize muito mais operações do que o normal.
2. **Vetores em ordem inversa:** Esse é o pior cenário possível para o Bubble e para o Insertion Sort. Como tudo está de trás para frente, eles são obrigados a fazer o número máximo de comparações e trocas.
3. **Selection Sort faz sempre igual:** Ele não liga para a organização inicial dos dados. Seja o vetor aleatório, ordenado ou invertido, o Selection Sort fará exatamente as mesmas 499.500 comparações. A única coisa que muda para ele é a quantidade de trocas.
