# DDL

## O que é DDL?

DDL é o acrônimo de *Data Definiition Language* que, em português, significa linguagem de definição de dados. Nesse grupo estão comandos justamente para criar tabelas, alterar seus atributos, excluir elementos, definir as restrições sobre os dados, como chaves primárias e outras.

## Comandos Básicos

Os comandos básicos de DDL são:
- `CREATE`: Cria uma tabela dentro do [[Banco de dados]]
- `DROP`: Apaga um objeto do [[Banco de dados]]

## Exemplos de Comandos

```sql
--- Exemplo de comando DLL ---
CREATE TABLE CLIENTES
CODIGO     INTEGER PRIMARY KEY
NOME       VARCHAR(50)
CONTATO    VARCHAR(2)
```
