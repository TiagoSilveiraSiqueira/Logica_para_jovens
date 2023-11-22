# Exercícios: Estruturas de Controle - Se/Outro e Rotações

## Exercício 1: Rotação Condicional

Você está criando um jogo onde um personagem precisa se movimentar em direções específicas com base nas teclas pressionadas. Implemente um código que utilize estruturas de controle para ajustar a rotação do personagem com base nas teclas pressionadas.

### Tarefas

1. Crie uma função `tecla_pressionada(tecla)` que simula a verificação se uma tecla específica foi pressionada.
2. Implemente um código que utilize estruturas de controle `if-else` para ajustar a rotação do personagem com base nas teclas pressionadas ("esquerda" ou "direita").
3. Imprima a direção resultante da rotação.

#### Exemplo de Código:

```python
# Função para simular tecla pressionada
def tecla_pressionada(tecla):
    return tecla in ["esquerda", "direita"]

# Solicita a tecla ao usuário
tecla = input("Digite a tecla pressionada (esquerda/direita): ")

# Verifica a rotação com base na tecla
if tecla_pressionada(tecla):
    if tecla == "esquerda":
        print("Personagem rotacionando para a esquerda.")
    elif tecla == "direita":
        print("Personagem rotacionando para a direita.")
else:
    print("Tecla inválida. Nenhuma rotação realizada.")
```
# Exercício 2: Controle de Rotações Condicionais
Você está desenvolvendo um simulador de movimento de um objeto em uma interface gráfica. Implemente um código que utilize estruturas de controle para determinar a quantidade de rotações com base na direção inserida pelo usuário.

Tarefas
Solicite a direção desejada para a rotação ("esquerda" ou "direita").
Utilize estruturas de controle if-else para ajustar a quantidade de rotações com base na direção.
Imprima a quantidade total de rotações no console.
Exemplo de Código:
```python

# Solicita a direção da rotação ao usuário
direcao_rotacao = input("Digite a direção desejada para a rotação (esquerda/direita): ")

# Inicializa a quantidade padrão de rotações
quantidade_rotacoes = 0

# Verifica a direção e ajusta a quantidade de rotações
if direcao_rotacao.lower() == "esquerda":
    quantidade_rotacoes = -1
    print("Objeto rotacionando para a esquerda.")
elif direcao_rotacao.lower() == "direita":
    quantidade_rotacoes = 1
    print("Objeto rotacionando para a direita.")
else:
    print("Direção inválida. Nenhuma rotação realizada.")

# Imprime a quantidade total de rotações
print("Quantidade de Rotações:", quantidade_rotacoes)
```

# Exercício 3: Tomada de Decisão em Jogo
Você está desenvolvendo um jogo de aventura onde o protagonista deve fazer escolhas que afetam o desenvolvimento da história. Implemente um código que utilize estruturas de controle if-else para determinar as consequências de uma escolha feita pelo jogador.

Tarefas
Solicite ao jogador que faça uma escolha ("abrir porta" ou "ignorar porta").
Utilize estruturas de controle para determinar as consequências da escolha do jogador.
Imprima as consequências da escolha no console.
Exemplo de Código:
```python

# Solicita a escolha ao jogador
escolha_jogador = input("Você deseja 'abrir porta' ou 'ignorar porta'? ")

# Verifica as consequências da escolha
if escolha_jogador.lower() == "abrir porta":
    print("Você abriu a porta e encontrou um tesouro!")
else:
    print("Você ignorou a porta e perdeu a oportunidade de encontrar algo valioso.")
```
