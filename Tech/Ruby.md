# Sobre o Ruby

Já pensou porque é que o **Ruby** é tão popular? Os fãs dizem que é uma linguagem elegante, repleta de arte. E no entanto, dizem que é prática e conveniente. Afinal qual é o resultado?

## Os Ideais do Criador do Ruby

O Ruby é uma linguagem com um cuidadoso equilíbrio. O seu criador, [[Yukihiro “Matz” Matsumoto]], uniu partes das suas linguagens favoritas (Perl, Smalltalk, Eiffel, Ada e Lisp) para formar uma nova linguagem que equilibra a programação funcional com a programação imperativa.

Ele disse com frequência que está “tentando tornar o Ruby natural, não simples”, de uma forma que reflita a vida.

Elaborando sobre isto, acrescenta:

> O Ruby é simples na aparência, mas muito complexo no interior, tal como o corpo humano[1](https://www.ruby-lang.org/pt/about/#fn1).

## Sobre o Crescimento do Ruby

Desde que foi tornado público em 1995, o Ruby arrastou consigo programadores devotos em todo o mundo. Em 2006, o Ruby atingiu aceitação massiva, com a formação de grupos de usuários em todas as principais cidades do mundo e com as conferências sobre Ruby com lotação esgotada.

A Ruby-Talk, a principal [lista de e-mails](https://www.ruby-lang.org/pt/community/mailing-lists/) para a discussão sobre a linguagem Ruby atingiu uma média de 200 mensagens diárias em 2006. Recentemente a média caiu, já que o tamanho da comunidade distribuiu as discussões de uma lista central em muitos grupos menores.

Ruby está posicionado entre no top 10 da maioria dos índices que medem o crescimento da popularidade de linguagens de programação pelo mundo todo (tais como o [índice TIOBE](http://www.tiobe.com/index.php/content/paperinfo/tpci/index.html)). Muito deste crescimento é atribuído à popularidade de softwares escritos em Ruby, em particular o framework de desenvolvimento web [[Ruby on Rails]]
(<http://rubyonrails.org/>).

O Ruby também é [totalmente livre](https://www.ruby-lang.org/en/about/license.txt). Não somente livre de custos, mas também livre para utilizar, copiar, modificar e distribuir.

## Ver Tudo como um [[Objetos]]

Inicialmente, Matz estudou outras linguagens em busca de encontrar uma sintaxe ideal. Recordando a sua busca, disse, “Eu queria uma linguagem interpretada que fosse mais poderosa do que Perl e mais orientada as objetos do que Python[2](https://www.ruby-lang.org/pt/about/#fn2).”

Em Ruby, tudo é um objeto. Cada parcela de informação e código podem receber as suas próprias propriedades e ações. A Programação orientada a objetos denomina as propriedades como _variáveis de instância_ e as ações como _métodos_. A aproximação pura, da orientação aos objetos do Ruby, é geralmente demonstrada pelo seguinte trecho de código que aplica uma ação a um número.

```ruby
5.times { print "Nós *amamos* o Ruby -- ele é fantástico!" }
```

Em muitas linguagens, números e outros tipos primitivos não são objetos. O Ruby segue a influência da linguagem Smalltalk em atribuir métodos e variáveis de instância a todos os seus tipos. Esta abordagem facilita a utilização do Ruby, uma vez que as regras que se aplicam aos objetos aplicam-se a tudo em Ruby.

## A Flexibilidade do Ruby

O Ruby é visto como uma linguagem flexível, uma vez que permite aos seus utilizadores alterar partes da linguagem. Partes essenciais do Ruby podem ser removidas ou redefinidas à vontade. Partes existentes podem ser acrescentadas. O Ruby tenta não restringir o programador.

Por exemplo, a adição é realizada com o operador mais (`+`). Mas, se preferir utilizar a palavra escrita `plus`, poderia adicionar esse método à classe nativa do Ruby `Numeric`.

```ruby
class Numeric
  def plus(x)
    self.+(x)
  end
end

y = 5.plus 6
# y agora é igual a 11
```

Os operadores do Ruby são açúcar sintático para métodos. Você também pode redefini-los.

## Blocos, uma Característica Verdadeiramente Expressiva

Os blocos do Ruby são vistos como uma fonte de grande flexibilidade. Um programador pode adicionar uma _closure_ a qualquer método, descrevendo como esse método deve se comportar. A _closure_ é chamada de _bloco_ e tornou-se uma das características mais populares para os recém chegados ao Ruby vindos de outras linguagens imperativas como o PHP ou o Visual Basic.

Os blocos são inspirados nas linguagens funcionais. Matz disse, “nas _closures_ em Ruby, eu quis respeitar a cultura do Lisp[3](https://www.ruby-lang.org/pt/about/#fn3)”.

```ruby
search_engines =
  %w[Google Yahoo MSN].map do |engine|
    "http://www." + engine.downcase + ".com"
  end
```

No código acima, o bloco é descrito dentro do trecho `do ... end`. O método `map` aplica o bloco à lista de palavras fornecida. Existem muitos outros métodos em Ruby que deixam em aberto a possibilidade para o programador escrever o seu próprio bloco que complete os detalhes do que esse método deveria fazer.

## Ruby e o _Mixin_

De forma diferente a muitas linguagens de programação orientadas a objeto, o Ruby suporta somente herança simples, **propositadamente**. Mas em Ruby existe o conceito de módulos (chamados categorias em Objective-C). Os módulos são coleções de métodos.

As classes podem fazer o _mixin_ de um modulo e receber todos os métodos do módulo diretamente. Por exemplo, qualquer classe que implemente o método `each` pode fazer o _mixin_ do módulo `Enumerable`, que adiciona um conjunto de métodos que utilizam `each` para iterar.

```ruby
class MyArray
  include Enumerable
end
```

Geralmente os programadores de Ruby vêm esta abordagem como uma forma muito mais clara do que a herança múltipla, que é complexa e pode ser demasiado restritiva.

## A Aparência Visual do Ruby

Apesar de o Ruby utilizar frequentemente pontuação muito limitada e geralmente preferir palavras em inglês, alguma pontuação é utilizada para decorar o Ruby. O Ruby não necessita de declarações de variáveis. Usa simples convenções de nomes para denotar o âmbito das variáveis.

- `var` poderia ser uma variável local.
-@var` é uma variável de instância.
- `$var` é uma variável global.

Estes símbolos facilitam a leitura do código, permitindo ao programador identificar facilmente o papel de cada variável. Também deixa de ser necessário acrescentar um fastidioso sufixo `self.` a cada membro de uma instância.

## Além do Básico

O Ruby é rico em outras características, entre as quais se destacam as seguintes:

- Capacidade de tratamento de exceções, tal como em Java ou Python, de forma a facilitar o tratamento de erros.

- Um verdadeiro [[garbage collector]] _mark-and-sweep_ para todos os objectos Ruby. Não é necessário manter contadores de referência em bibliotecas de extensão (_extension libraries_). Tal como Matz diz, “Isto é melhor para a sua saúde.”

- Escrever extensões C em Ruby é mais fácil do que em Perl ou Python, com uma [[API]] refinada para chamar Ruby a partir do código C. Isto inclui chamadas para embutir Ruby em software externo, para utilizá-lo como uma linguagem interpretada dentro do software. Uma interface SWIG também se encontra disponível.

- O Ruby pode carregar bibliotecas de extensão (_extension libraries_) dinamicamente se o Sistema Operacional permitir.

- O Ruby tem um sistema de [[threading]] independente do Sistema Operacional. Portanto, para todas as plataformas nas quais o Ruby roda, temos [[multithreading]] independentemente de o Sistema Operacional suportar ou não, temos [[multithreading]] até em MS-DOS!

- O Ruby é altamente portável: é desenvolvido principalmente em ambiente GNU/Linux, mas trabalha em muitos tipos de ambientes UNIX, macOS, Windows, DOS, BeOS, OS/2, etc.

[source](https://www.ruby-lang.org/pt/about/)

## Tipos de dados

Não existem "tipos primitivos" em Ruby; todos os tipos são [classes](https://pt.wikipedia.org/wiki/Classe_(programa%C3%A7%C3%A3o) "Classe (programação)"):

- **Object** é a classe mãe de todas as outras classes em Ruby
  - **Numeric** é uma classe abstrata que representa números
    - **Integer** é uma classe que representa números inteiros
      - **Fixnum** representa números inteiros de precisão fixa
      - **Bignum** representa números inteiros de precisão infinita, dependente apenas da memória disponível
    - **Float** é uma classe que representa números de ponto flutuante (números reais)
  - **String** uma cadeia de caracteres. Pode ser delimitado por apóstrofes (') ou aspas ("). Tudo o que há entre apóstrofes é interpretado literalmente, entre aspas o programador deve se utilizar de símbolos para representar caracteres específicos, como em C. Exemplos: 'azul', "a\nb\nc"
  - **Symbol** é semelhante a uma string, mas dois símbolos iguais possuem o mesmo endereço de memória, sendo assim é ótimo para se utilizar como índice numa Hash. Porém, devido à sua natureza, o [[garbage collector]] do Ruby não os elimina. É definido com um sinal de dois pontos (:), por exemplo, :nome
  - **Array** são [[arrays]] dinâmicos, que podem ser usados para representar matrizes e vetores. É delimitado por colchetes ([]) e cada valor é separado por vírgula. Exemplo: [4, 'azul', :termometro]
    - **Hash** representa um [[vetor associativo]], e, assim como as Arrays, é dinâmica. É delimitada por chaves ({}), e o índice precede o valor com um sinal '=>'. Exemplo: {:controller => 'user', :action => 'index'}. Qualquer objeto pode ser um índice, mas os mais usados são as Strings e os Symbols
  - **Regexp** representa [[expressões regulares]], delimitadas por //. Funciona de forma semelhante a Perl. Exemplo: /a|ae/
