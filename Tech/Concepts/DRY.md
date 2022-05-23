# DRY

## O que é DRY?

O princípio **DRY, 'Não se Repita'**, é um importante princípio que procura reduzir a duplicação de código e os problemas oriundos dessa prática.

A definição formal desse princípio diz :

"Cada parte do conhecimento deve ter uma representação única, não ambígua e definitiva dentro do sistema."

Extraindo o cerne do princípio : **'Não escreva código duplicado'**  **_(embora o princípio seja mais que isso)_**

O código duplicado cria os seguintes problemas:

- A impossibilidade de garantir que todas as instâncias repetidas serão modificadas quando uma alteração for requerida; _(aumenta a chance de bugs)_

- Requer o gerenciamento de memória e ciclos de runtime para processar blocos de códigos idênticos; _(impacta o desempenho da aplicação)_

Esta expressão foi cunhada por [[Andy Hunt]] e [[Dave Thomas]]  em seu livro [[The Pragmatic Programmer]] Ele se aplica amplamente, incluindo [esquema de banco de dados](https://pt.wikipedia.org/wiki/Esquema_de_banco_de_dados), [plano de teste](https://en.wikipedia.org/wiki/Test_plan), [[Compilador]] e mesmo [documentação de software](https://pt.wikipedia.org/wiki/Documenta%C3%A7%C3%A3o_de_software) .
