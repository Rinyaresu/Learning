# Rails
### [1. O que é o Rails?](https://guiarails.com.br/getting_started.html#o-que-e-o-rails-questionmark)

**Ruby on Rails** é um [[framework livre]] que promete aumentar velocidade e facilidade no desenvolvimento de sites orientados a banco de dados (_database-driven web sites_), uma vez que é possível criar aplicações com base em estruturas pré-definidas. Frequentemente referenciado como **Rails** ou **RoR**, o Ruby on Rails é um projeto de código aberto escrito na linguagem de programação [[Ruby]] As aplicações criadas utilizando o framework Rails são desenvolvidas com base no padrão de arquitetura [[MVC]] (_Model_-_View_-_Controller_)

---

Ruby on Rails foi uma extração de [[David Heinemeier Hansson]] de um projeto seu, o gerenciador de projetos **Basecamp**. Foi lançado a público pela primeira vez em 2003.

--- 

O **Rails** é um "meta-_framework_" (ou seja, um _framework de frameworks_), composto pelos seguintes _frameworks_:

### [[Active Record]]

O [[Active Record]] é uma camada de mapeamento objeto-relacional (_object-relational mapping layer_), responsável pela interoperabilidade entre a aplicação e o banco de dados e pela abstração dos dados.

### [[Action Pack]]

Compreende o [[Action View]] (geração de visualização de usuário, como [[HTML]], [[XML]], [[JavaScript]], entre outros) e o [[Action Controller]] (controle de fluxo de negócio).

### [[Action Mailer]]

O [[Action Mailer]] é um framework responsável pelo serviço de entrega e até mesmo de recebimento de e-mails. É relativamente pequeno e simples, porém poderoso e capaz de realizar diversas operações apenas com chamadas de entrega de correspondência.

### [[Active Support]]

[[Active Support]] é uma coleção de várias classes úteis e extensões de bibliotecas padrões, que foram considerados úteis para aplicações em Ruby on Rails.

### [[Action WebServices]]

Provê uma maneira de publicar [[API]] interoperaveis com o Rails, sem a necessidade de perder tempo dentro de especificações de protocolo. Implementa [[WSDL]] e [[SOAP]]

O Action Web Service não estará mais presente na versão 2.0 no Rails, visto que o mesmo está voltando-se para a utilização do modelo [[REST]]. Mesmo assim, aos ainda interessados em utilizá-lo, será possível fazê-lo através da instalação de um [[plugin]].

---
[[Concepts]]
Rails é um software opinativo. Assumindo que há uma "melhor" maneira para fazer as coisas, e foi projetado para encorajar essa maneira - e, em alguns casos para desencorajar alternativas. Se você aprender o "Rails Way", provavelmente terá um grande aumento de produtividade. Se você insistir nos velhos hábitos de outras linguagens, tentando usar os padrões que você aprendeu em outro lugar, você pode ter uma experiência menos feliz.

A filosofia do Rails possui dois princípios fundamentais:

-   **Não repita a si mesmo:** [[DRY]] (don't repeat yourself) é um conceito de desenvolvimento de software que estabelece que "Todo conhecimento deve possuir uma representação única, de autoridade e livre de ambiguidades em todo o sistema". Ao não escrever as mesmas informações repetidamente, o código fica mais fácil de manter, de expandir e com menos _bugs_.
-   [[CoC]] O Rails possui convenções sobre as melhores maneiras de fazer muitas coisas em uma aplicação web, devido a essas convenções você não precisa especificar detalhes através de arquivos de configuração infinitos.