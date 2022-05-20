# DML 
 Esse subconjunto essencial de comandos é denominado de [[DML]], do inglês Data Manipulation Language e, em português, linguagem de manipulação de dados. 
 DML é um subconjunto da linguagem SQL que é utilizado para realizar inclusões, consultas, alterações e exclusões de dados presentes em registros.

## Comandos Básicos
Os comandos básicos de DML são:

- `INSERT`: é usada para inserir um registro
- `UPDATE`: para mudar valores de dados
- `DELETE`: remover linhas de uma tabela
- `SELECT`: realizar consultas no banco

## Exemplo de comandos 
```sql
--- Comando para inserção de um novo registro ---
INSERT INTO CLIENTES(CODIGO,NOME,CONTATO)
  VALUES (10, 'Kaique Linhares', '71 998765432') 
  
--- Comando para consulta em uma tabela ---
SELECT NOME, CONTATO FROM CLIENTS
```
