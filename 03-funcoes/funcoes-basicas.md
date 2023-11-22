# Funções Básicas

Em programação, funções são blocos de código reutilizáveis projetados para realizar uma tarefa específica. Elas ajudam a organizar o código, tornando-o mais modular e fácil de entender. Neste tópico, exploraremos funções básicas.

## Sintaxe de Função

A sintaxe básica de uma função em muitas linguagens de programação é a seguinte:

```python
def nome_da_funcao(parametro1, parametro2, ...):
    # Código da função
    # ...
    return resultado
```

- `def`: Palavra-chave que inicia a definição de uma função.
- `nome_da_funcao`: Nome escolhido para a função.
- `(parametro1, parametro2, ...)`: Parâmetros são valores que a função aceita como entrada.
- `return resultado`: A instrução `return` define o valor a ser retornado pela função.

## Exemplo Prático

Vamos considerar uma função simples que calcula a soma de dois números:

```python
def soma(a, b):
    resultado = a + b
    return resultado
```

Agora, podemos chamar essa função com diferentes valores:

```python
# Chamada da função
resultado_soma = soma(5, 3)
print("A soma é:", resultado_soma)
```

Neste exemplo, a função `soma` aceita dois parâmetros (`a` e `b`), calcula a soma e retorna o resultado.

## Exercício de Implementação

Implemente uma função chamada `quadrado` que aceite um número como parâmetro e retorne o quadrado desse número.

#### Exemplo de Código:

```python
def quadrado(numero):
    resultado = numero ** 2
    return resultado

# Chamada da função
numero = 4
resultado_quadrado = quadrado(numero)
print(f"O quadrado de {numero} é: {resultado_quadrado}")
```

---

Continue explorando diferentes casos de uso para funções básicas. Elas são uma ferramenta poderosa para tornar seu código mais modular e fácil de entender.

```
