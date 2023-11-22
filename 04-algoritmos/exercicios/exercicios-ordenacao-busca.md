# Exercícios: Algoritmos de Ordenação e Busca

## Exercício 1: Bubble Sort

Implemente uma função chamada `bubble_sort` que utilize o algoritmo de ordenação Bubble Sort para ordenar uma lista de elementos.

#### Exemplo de Código:

```python
def bubble_sort(lista):
    n = len(lista)
    
    for i in range(n):
        for j in range(0, n-i-1):
            if lista[j] > lista[j+1]:
                lista[j], lista[j+1] = lista[j+1], lista[j]

# Exemplo de Uso
numeros = [64, 34, 25, 12, 22, 11, 90]
bubble_sort(numeros)
print("Lista Ordenada:", numeros)
```

## Exercício 2: Busca Binária

Implemente uma função chamada `busca_binaria` que utilize o algoritmo de busca binária para encontrar a posição de um elemento em uma lista ordenada.

#### Exemplo de Código:

```python
def busca_binaria(lista, alvo):
    inicio, fim = 0, len(lista) - 1

    while inicio <= fim:
        meio = (inicio + fim) // 2
        if lista[meio] == alvo:
            return meio
        elif lista[meio] < alvo:
            inicio = meio + 1
        else:
            fim = meio - 1

    return -1

# Exemplo de Uso
numeros_ordenados = [11, 12, 22, 25, 34, 64, 90]
alvo = 22
posicao = busca_binaria(numeros_ordenados, alvo)

if posicao != -1:
    print(f"O elemento {alvo} foi encontrado na posição {posicao}.")
else:
    print(f"O elemento {alvo} não foi encontrado na lista.")
```

## Exercício 3: Quick Sort

Implemente uma função chamada `quick_sort` que utilize o algoritmo de ordenação Quick Sort para ordenar uma lista de elementos.

#### Exemplo de Código:

```python
def quick_sort(lista):
    if len(lista) <= 1:
        return lista
    else:
        pivo = lista[0]
        menores = [elemento for elemento in lista[1:] if elemento <= pivo]
        maiores = [elemento for elemento in lista[1:] if elemento > pivo]
        return quick_sort(menores) + [pivo] + quick_sort(maiores)

# Exemplo de Uso
numeros = [64, 34, 25, 12, 22, 11, 90]
numeros_ordenados = quick_sort(numeros)
print("Lista Ordenada:", numeros_ordenados)
```

## Exercício 4: Busca Sequencial Recursiva

Implemente uma função chamada `busca_sequencial_recursiva` que realize uma busca sequencial de forma recursiva em uma lista.

#### Exemplo de Código:

```python
def busca_sequencial_recursiva(lista, alvo, inicio=0):
    if inicio < len(lista):
        if lista[inicio] == alvo:
            return inicio
        else:
            return busca_sequencial_recursiva(lista, alvo, inicio + 1)
    else:
        return -1

# Exemplo de Uso
numeros = [64, 34, 25, 12, 22, 11, 90]
alvo = 12
posicao = busca_sequencial_recursiva(numeros, alvo)

if posicao != -1:
    print(f"O elemento {alvo} foi encontrado na posição {posicao}.")
else:
    print(f"O elemento {alvo} não foi encontrado na lista.")
```

---

Esses exercícios proporcionam a oportunidade de praticar a implementação e compreensão de algoritmos de ordenação e busca. Experimente resolver cada exercício para aprimorar suas habilidades em algoritmos e estruturas de dados.

```
