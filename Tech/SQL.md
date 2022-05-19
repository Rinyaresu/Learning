#  SQL
SQL é um acrônimo de _Structured Query Language_ que, em português, refere-se à linguagem de consulta estruturada, mas que, na comunidade de [[Banco de dados]], tratamos simplesmente como SQL. Essa linguagem apresenta um conjunto de comandos com suas respectivas sintaxes para que operações sejam disparadas para o servidor de banco de dados. O SGBD, enquanto um servidor para processar as consultas do seu requisitante, interpreta a consulta e dispara internamente as ações no banco de dados.

## A Utilização de um Banco de dados e a Linguagem SQL

Todos os envolvidos citados anteriormente precisarão lidar direta ou indiretamente, em algum grau, com uma linguagem específica para o trato com Banco de Dados, a comumente denominada SQL. 

## Exemplos de comandos 

Para exemplificar, imagine que um administrador do banco de dados precisa criar um banco de dados e, neste banco de dados, criar uma tabela de CLIENTES. Neste caso, ele precisa usar o comando `CREATE DATABASE` para o banco de dados e precisa também do comando de `CREATE TABLE` para criação da tabela. No exemplo abaixo, estes comandos são demonstrados. Para a tabela VENDAS, apenas os campos de código, de nome e de contato foram considerados e outros detalhes do comando foram abstraídos para simplificar a explicação neste momento.

```sql
--- Comando para criação de uma tabela ---
CREATE TABLE CLIENTES
CODIGO     INTEGER PRIMARY KEY
NOME       VARCHAR(50)
CONTATO    VARCHAR(2)
```

Com a tabela criada e ainda nesse sentido de compreender a natureza dos comandos em SQL, caso um usuário queira inserir um dado nessa tabela ou queira consultar os dados da tabela, ele pode usar os comandos de _INSERT_ e _SELECT_ , respectivamente. Eles estão expostos na sequência:

```sql
--- Comando para inserção de um novo registro ---
INSERT INTO CLIENTES(CODIGO,NOME,CONTATO)
  VALUES (10, 'Kaique Linhares', '71 998765432') 
  
--- Comando para consulta em uma tabela ---
SELECT NOME, CONTATO FROM CLIENTS
```

Esses são apenas alguns exemplos de comandos para compreendermos esta unidade de introdução que trata da natureza na linguagem SQL quando lidamos com nosso banco de dados. Vale também destacar a simplicidade dos comandos. Ainda sem aprofundar, creio que você, enquanto aluno, deve ter conseguido obter uma noção do que os comandos devem provocar nas respectivas tabelas.


## Subconjuntos do SQL
Os comandos da linguagem SQL podem ser classificados quanto ao seu propósito diante do banco de dados. Perceba que o primeiro comando de “CREATE TABLE” criou e, portanto, definiu uma parte da estrutura no banco de dados. Os outros dois comandos permitem que os dados da tabela possam ser manipulados com inserção e alteração. Essa distinção entre definir a estrutura do banco de dados e manipular os dados de suas tabelas é uma classificação comum dos comandos de SQL em subconjuntos. O primeiro refere-se a um subconjunto de comandos - chamado de DDL, acrônimo de _Data Definition Language_ que, em português, significa linguagem de definição dos dados. Nesse grupo estão comandos justamente para criar tabelas, alterar seus atributos, excluir elementos, definir as restrições sobre os dados, como chaves primárias e outras.
