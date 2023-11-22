# Exercício 3: Operadores Fundamentais

## Descrição

Você está desenvolvendo um programa para calcular o preço total de compras em uma loja online. Implemente um código que utilize operadores aritméticos para calcular o valor total do carrinho de compras.

### Tarefas

1. Declare variáveis para representar os preços de três itens no carrinho.
2. Declare uma variável para a quantidade de cada item escolhido pelo usuário.
3. Utilize operadores aritméticos para calcular o preço total do carrinho.
4. Imprima o preço total no console.

## Exemplo de Código

```python
# Declare variáveis de preços
preco_item1 = 25.99
preco_item2 = 15.50
preco_item3 = 10.75

# Declare variáveis de quantidade
quantidade_item1 = int(input("Quantidade do Item 1: "))
quantidade_item2 = int(input("Quantidade do Item 2: "))
quantidade_item3 = int(input("Quantidade do Item 3: "))

# Calcule o preço total do carrinho
preco_total = (preco_item1 * quantidade_item1) + (preco_item2 * quantidade_item2) + (preco_item3 * quantidade_item3)

# Imprima o preço total
print("Preço Total do Carrinho: $", preco_total)
```
# Desafio Extra
Permita que o usuário adicione mais itens ao carrinho e atualize o código para lidar com uma quantidade variável de itens.

