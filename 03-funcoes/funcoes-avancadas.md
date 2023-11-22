# Funções Avançadas

Além das funções básicas que vimos anteriormente, existem funções mais avançadas que podem melhorar a modularidade e a eficiência do código. Vamos explorar algumas dessas funcionalidades.

## Parâmetros Padrão

Funções podem ter parâmetros com valores padrão, o que significa que esses parâmetros podem ser omitidos ao chamar a função, assumindo um valor padrão predefinido.

```python
def saudacao(nome, saudacao="Olá"):
    print(f"{saudacao}, {nome}!")

# Chamada da função
saudacao("Maria")  # Saída: Olá, Maria!
saudacao("João", "Oi")  # Saída: Oi, João!
```

Neste exemplo, a função `saudacao` tem um parâmetro padrão (`saudacao="Olá"`), que pode ser substituído ao chamar a função.

## Retorno Múltiplo

Uma função em Python pode retornar múltiplos valores como uma tupla.

```python
def divisao_e_resto(dividendo, divisor):
    resultado_divisao = dividendo // divisor
    resto = dividendo % divisor
    return resultado_divisao, resto

# Chamada da função
resultado, resto = divisao_e_resto(10, 3)
print(f"Resultado: {resultado}, Resto: {resto}")
```

Neste exemplo, a função `divisao_e_resto` retorna dois valores, e esses valores são atribuídos a duas variáveis ao chamar a função.

## Funções Anônimas (Lambda)

Funções anônimas, ou lambdas, são funções pequenas e temporárias definidas usando a palavra-chave `lambda`.

```python
dobro = lambda x: x * 2

# Chamada da função
resultado = dobro(5)
print(f"O dobro de 5 é {resultado}")
```

Neste exemplo, criamos uma função lambda que dobra um número.

## Exercício de Implementação

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

Esses conceitos avançados de funções podem ser poderosos para lidar com situações mais complexas. Continue explorando essas funcionalidades para melhorar suas habilidades em programação.

```
