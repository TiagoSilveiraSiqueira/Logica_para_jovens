# Projeto 2: Aplicativo de Lista de Compras

## Descrição do Projeto

Desenvolva um aplicativo de lista de compras que permita aos usuários criar, gerenciar e compartilhar listas de itens de compras. O aplicativo deve oferecer uma experiência fácil de usar, permitindo aos usuários adicionar, editar e excluir itens da lista.

## Funcionalidades Principais

1. **Adicionar Itens:** Os usuários devem ser capazes de adicionar itens à lista de compras, especificando o nome do item, a quantidade desejada e, opcionalmente, outras informações relevantes.

2. **Editar Itens:** Permita que os usuários editem informações sobre os itens da lista, como a quantidade desejada ou detalhes adicionais.

3. **Excluir Itens:** Deve haver a capacidade de remover itens da lista de compras.

4. **Marcar Itens como Comprados:** Os usuários devem poder marcar os itens como comprados, indicando que foram adquiridos.

5. **Criar Listas Diferentes:** Permita aos usuários criar várias listas de compras para diferentes finalidades (por exemplo, lista de supermercado, lista de material de limpeza).

6. **Compartilhar Listas:** Implemente a funcionalidade de compartilhamento, permitindo que os usuários compartilhem suas listas de compras com outras pessoas.

## Requisitos Técnicos

- Armazene as listas de compras de forma persistente para que os dados sejam mantidos entre diferentes sessões do aplicativo.
- Considere a usabilidade ao projetar a interface do usuário para garantir uma experiência amigável.

## Exemplo de Implementação (Web App em Flask - Python)

A seguir, um exemplo simples de implementação usando Flask para criar um aplicativo web de lista de compras. Este é apenas um ponto de partida, e você pode expandir ou modificar conforme necessário.

**Observação:** Certifique-se de ter o Flask instalado antes de executar o exemplo (`pip install flask`).

```python
from flask import Flask, render_template, request, redirect, url_for

app = Flask(__name__)

# Lista de compras (exemplo simples, considere usar um banco de dados em um projeto real)
compras = []

@app.route('/')
def index():
    return render_template('index.html', compras=compras)

@app.route('/adicionar', methods=['POST'])
def adicionar():
    nome_item = request.form['nome_item']
    quantidade = request.form['quantidade']
    compras.append({'nome_item': nome_item, 'quantidade': quantidade, 'comprado': False})
    return redirect(url_for('index'))

@app.route('/editar/<int:index>')
def editar(index):
    compra = compras[index]
    return render_template('editar.html', index=index, compra=compra)

@app.route('/atualizar/<int:index>', methods=['POST'])
def atualizar(index):
    nome_item = request.form['nome_item']
    quantidade = request.form['quantidade']
    compras[index] = {'nome_item': nome_item, 'quantidade': quantidade, 'comprado': False}
    return redirect(url_for('index'))

@app.route('/excluir/<int:index>')
def excluir(index):
    compras.pop(index)
    return redirect(url_for('index'))

@app.route('/marcar_comprado/<int:index>')
def marcar_comprado(index):
    compras[index]['comprado'] = not compras[index]['comprado']
    return redirect(url_for('index'))

if __name__ == '__main__':
    app.run(debug=True)
```

### Estrutura do Projeto

- `templates/index.html`: Página inicial que exibe a lista de compras.
- `templates/editar.html`: Página para editar um item da lista de compras.

**Observação:** Este é um esboço inicial e você pode adaptá-lo conforme necessário para atender aos requisitos específicos e às tecnologias de sua escolha.
