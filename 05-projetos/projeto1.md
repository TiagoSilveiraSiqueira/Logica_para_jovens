# Projeto 1: Sistema de Gerenciamento de Tarefas

## Descrição do Projeto

Desenvolva um Sistema de Gerenciamento de Tarefas que permita aos usuários criar, visualizar, editar e excluir tarefas. O sistema deve ser implementado em uma linguagem de programação de sua escolha e pode incluir uma interface de linha de comando (CLI) ou uma interface gráfica de usuário (GUI).

## Funcionalidades Principais

1. **Adicionar Tarefa:** Os usuários devem ser capazes de adicionar uma nova tarefa, especificando o título, a descrição e a data de vencimento, se aplicável.

2. **Listar Tarefas:** O sistema deve permitir que os usuários vejam uma lista de todas as tarefas existentes, exibindo informações como título, descrição e status (pendente, concluída, etc.).

3. **Editar Tarefa:** Os usuários devem poder editar uma tarefa existente, incluindo a capacidade de modificar o título, a descrição, a data de vencimento e o status.

4. **Excluir Tarefa:** Deve haver uma opção para excluir uma tarefa, removendo-a do sistema de gerenciamento.

5. **Marcar Tarefa como Concluída:** Os usuários devem ter a opção de marcar uma tarefa como concluída, alterando seu status.

## Requisitos Técnicos

- O sistema deve armazenar as tarefas de forma persistente, permitindo que os dados sejam mantidos entre diferentes execuções do programa.
- Se você optar por criar uma interface gráfica, ela deve ser intuitiva e amigável para o usuário.
- Considere a implementação de validações para garantir que as entradas do usuário sejam adequadas.

## Exemplo de Implementação (CLI em Python)

A seguir, um exemplo simples de implementação em Python usando uma interface de linha de comando (CLI). Este é apenas um ponto de partida, e você pode expandir ou modificar conforme necessário.

```python
import json
from datetime import datetime

def carregar_tarefas():
    try:
        with open('tarefas.json', 'r') as arquivo:
            return json.load(arquivo)
    except FileNotFoundError:
        return []

def salvar_tarefas(tarefas):
    with open('tarefas.json', 'w') as arquivo:
        json.dump(tarefas, arquivo, indent=2)

def adicionar_tarefa(titulo, descricao, data_vencimento):
    tarefas = carregar_tarefas()
    tarefa = {
        'titulo': titulo,
        'descricao': descricao,
        'data_vencimento': data_vencimento,
        'status': 'pendente'
    }
    tarefas.append(tarefa)
    salvar_tarefas(tarefas)

def listar_tarefas():
    tarefas = carregar_tarefas()
    for idx, tarefa in enumerate(tarefas, 1):
        print(f"{idx}. {tarefa['titulo']} ({tarefa['status']})")

# ... (implementar outras funções conforme necessário)

# Exemplo de Uso
adicionar_tarefa('Estudar Python', 'Concluir os exercícios de Python', '2023-12-31')
adicionar_tarefa('Fazer Compras', 'Comprar itens essenciais', '2023-11-30')
listar_tarefas()
```

## Considerações Finais

Este projeto proporcionará uma oportunidade prática para aplicar conceitos de programação, estruturas de dados e persistência de dados. Sinta-se à vontade para personalizar e expandir o projeto com funcionalidades adicionais.

**Observação:** Este é um esboço inicial e você pode adaptá-lo conforme necessário para atender aos requisitos específicos e às tecnologias de sua escolha.
