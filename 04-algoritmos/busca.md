# Algoritmos de Busca

Os algoritmos de busca são utilizados para encontrar a presença ou posição de um elemento em uma coleção de dados. Existem várias abordagens de busca, cada uma com suas características e eficiência. Vamos explorar alguns dos algoritmos de busca comuns.

## Busca Linear

A busca linear é um método simples em que cada elemento da lista é verificado sequencialmente até encontrar o elemento desejado.

```python
def busca_linear(lista, alvo):
    for i in range(len(lista)):
        if lista[i] == alvo:
            return i
    return -1

# Exemplo de Uso
numeros = [64, 34, 25, 12, 22, 11, 90]
alvo = 25
posicao = busca_linear(numeros, alvo)

if posicao != -1:
    print(f"O elemento {alvo} foi encontrado na posição {posicao}.")
else:
    print(f"O elemento {alvo} não foi encontrado na lista.")
```

## Busca Binária

A busca binária é um método eficiente aplicável apenas a listas ordenadas. Ela divide repetidamente a lista ao meio, reduzindo o espaço de busca pela metade.

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

## Exercício de Implementação

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

Estes são apenas alguns exemplos de algoritmos de busca. A escolha do algoritmo depende do contexto em que será aplicado, considerando fatores como a ordenação da lista e a eficiência desejada.

Continue explorando diferentes algoritmos de busca para aprimorar suas habilidades em algoritmos e estruturas de dados.

```
