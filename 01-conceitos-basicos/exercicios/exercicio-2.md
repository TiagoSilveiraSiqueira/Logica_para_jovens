# Exercício 2: Controle de Fluxo

## Descrição

Você está desenvolvendo um programa de autenticação de usuário. Implemente um código que verifica se um usuário tem idade suficiente para acessar um determinado conteúdo.

### Tarefas

1. Solicite a idade do usuário.
2. Utilize uma estrutura condicional (`if`, `else`) para determinar se o usuário é maior de idade (18 anos ou mais) ou menor de idade.
3. Imprima uma mensagem correspondente ao resultado no console.

## Exemplo de Código

```python
# Solicitar idade do usuário
idade = int(input("Digite sua idade: "))

# Verificar se é maior de idade
if idade >= 18:
    print("Acesso permitido! Bem-vindo ao conteúdo para maiores de idade.")
else:
    print("Desculpe, você é menor de idade. Acesso negado.")
```
Desafio Extra
Adicione uma verificação adicional para verificar se a entrada do usuário é um número válido. Se não for, exiba uma mensagem de erro.
