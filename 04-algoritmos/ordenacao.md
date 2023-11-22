# Algoritmos de Ordenação

Os algoritmos de ordenação são fundamentais em ciência da computação e são utilizados para organizar elementos em uma determinada ordem, seja crescente ou decrescente. Existem vários algoritmos de ordenação, cada um com suas características e eficiência. Vamos explorar alguns deles.

## Bubble Sort

O Bubble Sort é um dos algoritmos de ordenação mais simples. Ele percorre a lista diversas vezes, compara elementos adjacentes e os troca se estiverem na ordem errada.

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

## Merge Sort

O Merge Sort é um algoritmo de ordenação eficiente que utiliza a estratégia de divisão e conquista. Ele divide a lista em partes menores, ordena essas partes e, em seguida, combina-as para obter a lista final ordenada.

```python
def merge_sort(lista):
    if len(lista) > 1:
        meio = len(lista) // 2
        esquerda = lista[:meio]
        direita = lista[meio:]

        merge_sort(esquerda)
        merge_sort(direita)

        i = j = k = 0

        while i < len(esquerda) and j < len(direita):
            if esquerda[i] < direita[j]:
                lista[k] = esquerda[i]
                i += 1
            else:
                lista[k] = direita[j]
                j += 1
            k += 1

        while i < len(esquerda):
            lista[k] = esquerda[i]
            i += 1
            k += 1

        while j < len(direita):
            lista[k] = direita[j]
            j += 1
            k += 1

# Exemplo de Uso
numeros = [64, 34, 25, 12, 22, 11, 90]
merge_sort(numeros)
print("Lista Ordenada:", numeros)
```

## Exercício de Implementação

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

---

Estes são apenas alguns exemplos de algoritmos de ordenação. Cada algoritmo possui suas vantagens e desvantagens em termos de desempenho, e a escolha do algoritmo apropriado depende do contexto em que será aplicado.

Continue explorando diferentes algoritmos de ordenação para aprimorar suas habilidades em algoritmos e estruturas de dados.

```
