# Estruturas de Controle - Rotações

Em programação, as estruturas de controle também podem ser utilizadas para realizar rotações ou movimentos em um contexto específico, como em jogos ou animações. 

## Rotações Simples

Considere um exemplo em que queremos controlar a rotação de um objeto em uma cena 3D. Podemos usar estruturas condicionais para determinar a direção da rotação.

```python
# Solicite a direção da rotação
direcao_rotacao = input("Digite a direção desejada para a rotação (esquerda/direita): ")

# Defina a quantidade padrão de rotações
quantidade_rotacoes = 0

# Verifique a direção e ajuste a quantidade de rotações
if direcao_rotacao.lower() == "esquerda":
    quantidade_rotacoes = -1
    print("Objeto rotacionando para a esquerda.")
elif direcao_rotacao.lower() == "direita":
    quantidade_rotacoes = 1
    print("Objeto rotacionando para a direita.")
else:
    print("Direção inválida. Nenhuma rotação realizada.")

# Imprima a quantidade de rotações
print("Quantidade de Rotações:", quantidade_rotacoes)
```
Neste exemplo, o programa solicita a direção da rotação ao usuário ("esquerda" ou "direita") e ajusta a quantidade de rotações com base nessa entrada.

Rotações em Jogos
Em jogos, as estruturas de controle são frequentemente usadas para controlar o movimento e a rotação de personagens. Vamos considerar um exemplo simples:

```python
# Verifique se o jogador pressionou a tecla para a esquerda
if tecla_pressionada("esquerda"):
    jogador.rotacionar_para_esquerda()

# Verifique se o jogador pressionou a tecla para a direita
elif tecla_pressionada("direita"):
    jogador.rotacionar_para_direita()

```
Neste exemplo hipotético, a função tecla_pressionada é usada para verificar se uma tecla específica foi pressionada, e a rotação do jogador é ajustada com base nessa entrada.
