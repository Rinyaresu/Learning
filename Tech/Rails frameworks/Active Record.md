# Active Record

## O que é Active Record?

Em Engenharia de software, **active record** é um padrão de projeto encontrado em softwares que armazenam seus dados em [[Banco de dados relacionais]]. Assim foi nomeado por [[Martin Fowler]] em seu livro _Patterns of Enterprise Application Architecture_. A interface de um certo objeto deve incluir funções como por exemplo Inserir(Insert), Atualizar(Update), Apagar(Delete) e propriedades que correspondam de certa forma diretamente às colunas do banco de dados associado.

Active record é uma abordagem para acesso de dados num [[Banco de dados]]. Uma tabela de banco de dados ou visão(view) é embrulhada(wrapped) em uma classe. Portanto, uma instância de um objeto é amarrada a um único registo(tupla) na tabela. Após a criação e gravação de um objeto, um novo registo é adicionado à tabela. Qualquer objeto carregado obtém suas informações a partir do banco de dados. Quando um objeto é atualizado, o registro correspondente na tabela também é atualizado. A classe de embrulho implementa os métodos de acesso(setter e getter) ou propriedades para cada coluna na tabela ou visão.

Este padrão é comumente utilizado por ferramentas de persistência de objetos e em mapeamento objeto-relacional. Geralmente as relações de chave estrangeira serão expostas como uma instância do objeto do tipo apropriado por meio de uma propriedade.

## Implementação

Implementações do conceito podem ser encontradas em vários [[framework]]s para diversos ambientes de programação. Por exemplo, se um banco de dados possui a tabela `produtos` com as colunas `nome` (tipo string) e `valor` (tipo number) e o padrão de projeto Active Record é implementado na classe `Produto`, o pseudo-código:

```ruby
produto = new Produto()
produto.nome = "Produto exemplo"
produto.valor = 123.45
produto.save()
```

Irá criar um novo registro na table `produtos` com os valores fornecidos sendo grosseiramente equivalente ao comando SQL:

```sql
INSERT INTO produtos (nome, valor) VALUES ('Produto exemplo', 123.45);
```

Da mesma forma, a classe pode ser usada para consultar o banco de dados:

```ruby
b = Produto.find_first("nome", "televisor")
```

Este código criará um novo objeto do tipo `Produto` baseado no primeiro registro encontrado da tabela `produtos` onde a coluna `nome` contém o valor "televisor". O comando SQL usado pode ser similar ao seguinte (dependendo dos detalhes da implementação SQL do banco de dados):

```sql
SELECT * FROM produtos WHERE nome = 'televisor' LIMIT 1; -- MySQL ou PostgreSQL
```
