# Action Pack
# O que o Action Pack faz?
[[Action Pack]] é um [[framework]] que lida e responde [[web requests]].  E provem mecanismos para [[routing]]. definindo [[controllers]] que implementam [[actions]], e geram respostas. Resumidamente o **Action Pack** controla a camada no paradigma [[MVC]].

## Módulos
- [[Action Dispatch]], analisa infamações dos [[web requests]], lida com [[routing]] definido pelo usuário, e também faz processo avançado relacionado a [[HTTP]] como negociação [[Mime-type]], parâmetros de decodificação em POST, PATCH ou PUT bodies, lidando com [[Lógica de cache HTTP]], [[cookies]], e [[sessões]].
 
- [[Action Controller]], provem a base de classes de [[controllers]] que podem ser subclasses para implementar filtros e [[actions]] para lidar com solicitações.

## Instalação 
```ruby
gem install actionpack
```
