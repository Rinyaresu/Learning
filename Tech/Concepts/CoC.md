#  CoC

**Convenção sobre configuração** ou **programação por convenção** (do inglês _Convention over configuration_ - CoC) é um modelo de [desenvolvimento de software](https://pt.wikipedia.org/wiki/Desenvolvimento_de_software) que busca diminuir o número de decisões que os [desenvolvedores](https://pt.wikipedia.org/wiki/Programador) precisam tomar. Visa ganhar simplicidade sem perder flexibilidade.

O bordão "convenção sobre configuração" essencialmente significa que o desenvolvedor precisa de definir apenas aspectos não convencionais da aplicação. Por exemplo, podemos adotar uma convenção de nomes, nas quais o nome da tabela no [[Banco de dados]] será sempre o plural da classe persistente. Se existe uma classe "Venda" no modelo, a tabela correspondente no [[Banco de dados]] será chamada, por padrão, "vendas". Somente no caso de alguém se desviar deste modelo tornar-se-ia necessário escrever código específico relacionando a classe a tabela, como se se resolvesse chamar a tabela "produtos_vendidos".

Quando a convenção implementada pela ferramenta que se utiliza corresponde ao comportamento desejado, o desenvolvedor gasta menos esforço (ou não há sequer esforço) na redação de [arquivos de configuração](https://en.wikipedia.org/wiki/Configuration_file) Somente se o comportamento desejado for distinto da convenção implementada é que se torna necessário elaborar configurações.

Esta visão permite ao programador trabalhar num nível maior de abstração sem a necessidade da criação de uma camada de abstração.