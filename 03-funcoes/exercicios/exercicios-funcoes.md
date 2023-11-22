# Exercícios: Funções Básicas e Avançadas

## Exercício 1: Função Básica

Implemente uma função chamada `soma` que aceite dois parâmetros e retorne a soma desses dois valores.

#### Exemplo de Código:

```python
def soma(a, b):
    resultado = a + b
    return resultado

# Chamada da função
resultado_soma = soma(5, 3)
print("A soma é:", resultado_soma)
```

## Exercício 2: Parâmetros Padrão

Implemente uma função chamada `saudacao` que aceite o nome de uma pessoa e um parâmetro opcional de saudação com um valor padrão de "Olá". A função deve imprimir a saudação seguida pelo nome.

#### Exemplo de Código:

```python
def saudacao(nome, saudacao="Olá"):
    print(f"{saudacao}, {nome}!")

# Chamada da função
saudacao("Maria")  # Saída: Olá, Maria!
saudacao("João", "Oi")  # Saída: Oi, João!
```

## Exercício 3: Retorno Múltiplo

Implemente uma função chamada `divisao_e_resto` que aceite dois parâmetros, realize a divisão e retorne tanto o resultado da divisão quanto o resto.

#### Exemplo de Código:

```python
def divisao_e_resto(dividendo, divisor):
    resultado_divisao = dividendo // divisor
    resto = dividendo % divisor
    return resultado_divisao, resto

# Chamada da função
resultado, resto = divisao_e_resto(10, 3)
print(f"Resultado: {resultado}, Resto: {resto}")
```

## Exercício 4: Função Anônima (Lambda)

Crie uma função anônima (lambda) que dobre um número.

#### Exemplo de Código:

```python
dobro = lambda x: x * 2

# Chamada da função
resultado = dobro(5)
print(f"O dobro de 5 é {resultado}")
```

## Exercício 5: Função de Média Ponderada

Implemente uma função chamada `media_ponderada` que aceite três parâmetros: `nota1`, `nota2` e `peso2`. Calcule a média ponderada das notas e retorne o resultado.

#### Exemplo de Código:

```python
def media_ponderada(nota1, nota2, peso2):
    media = (nota1 + (nota2 * peso2)) / (1 + peso2)
    return media

# Chamada da função
nota1 = 8
nota2 = 9
peso2 = 2
resultado_media = media_ponderada(nota1, nota2, peso2)
print(f"A média ponderada é: {resultado_media}")
```

---

Esses exercícios são projetados para consolidar o entendimento sobre funções, desde as básicas até as mais avançadas. Experimente resolver cada exercício para aprimorar suas habilidades de programação.

```
