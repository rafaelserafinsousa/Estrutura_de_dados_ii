# ATIVIDADE PRÁTICA – ANÁLISE DE ALGORITMOS DE ORDENAÇÃO

## 1. Código Fonte (Etapas 1 e 2)
O experimento foi desenvolvido em Python. Foi utilizada uma *seed* fixa (`random.seed(42)`) para garantir que os testes fossem reprodutíveis e que todos os algoritmos recebessem exatamente os mesmos dados iniciais em cada tamanho de vetor.

```python
import random
import sys

# Aumentando o limite de recursão para o Quick Sort no pior caso
sys.setrecursionlimit(2000)

def bubble_sort(arr):
    n = len(arr)
    comps = swaps = 0
    for i in range(n):
        swapped = False
        for j in range(0, n-i-1):
            comps += 1
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
                swaps += 1
                swapped = True
        if not swapped: break
    return comps, swaps

def insertion_sort(arr):
    comps = movs = 0
    for i in range(1, len(arr)):
        key = arr[i]
        j = i - 1
        while j >= 0:
            comps += 1
            if arr[j] > key:
                arr[j + 1] = arr[j]
                movs += 1
                j -= 1
            else:
                break
        arr[j + 1] = key
        movs += 1
    return comps, movs

def selection_sort(arr):
    n = len(arr)
    comps = swaps = 0
    for i in range(n):
        min_idx = i
        for j in range(i+1, n):
            comps += 1
            if arr[j] < arr[min_idx]:
                min_idx = j
        if min_idx != i:
            arr[i], arr[min_idx] = arr[min_idx], arr[i]
            swaps += 1
    return comps, swaps

def quick_sort(arr):
    comps = [0]
    swaps = [0]
    def partition(low, high):
        pivot = arr[high]
        i = low - 1
        for j in range(low, high):
            comps[0] += 1
            if arr[j] <= pivot:
                i += 1
                arr[i], arr[j] = arr[j], arr[i]
                swaps[0] += 1
        arr[i + 1], arr[high] = arr[high], arr[i + 1]
        swaps[0] += 1
        return i + 1

    def qs(low, high):
        if low < high:
            pi = partition(low, high)
            qs(low, pi - 1)
            qs(pi + 1, high)
            
    qs(0, len(arr) - 1)
    return comps[0], swaps[0]
