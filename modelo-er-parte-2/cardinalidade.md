# Cardinalidade

A cardinalidade de um relacionamento se refere a capacidade de se contar
o número de entidades envolvidas nesse relacionamento.

Por exemplo: Se as instâncias de entidades A e B tiverem uma relação,
então, a cardinalidade máxima representa o **número máximo de instâncias**
da entidade B **que podem ser associadas** a instância da entidade A.

No entanto não é necessário atribuir um valor de numero para cada nível relação.
Na verdade o termo se refere a apenas dois valores possíveis: um (1) ou muitos (N).

Apesar de parecer simples, o valor máximo de cardinalidade de uma relação, nos permite
definir os três tipos de relações possíveis entre A e B.

- Um-para-muitos (1:N)
- Muitos-para-muitos (N:M)
- Um-para-um (1:1)

## Cardinalidade Máxima

### Um-para-muitos (1:N)

Essa relação descreve quando uma instância de um conjunto A, se relaciona com
diversas instâncias do conjunto B. Exemplo:

**Pessoa & Carro**

- Uma pessoa pode ter vários carros registrados em seu nome.
- Um carro pode ser registrado em apenas no nome de uma pessoa.

**Cliente & Pedido**

- Um cliente pode possuir vários pedidos.
- Um pedido pode pertencer à apenas um cliente.

### Muitos-para-muitos (N:M)

Essa relação descreve uma instância do conjunto A que se relaciona com diversas 
instâncias do conjunto B, e uma instância do conjunto B se relaciona com diversas
instâncias do conjunto A. Exemplo:

**Autor e Livro**

- Um autor pode escrever vários livros.
- Um livro pode ser escrito por vários autores.

### Um-para-um (1:1)

É uma relação de uma instância do conjunto A que se relaciona apenas cum uma instância
do conjunto B, e vice versa. Exemplo:

**Empregado e Departamento**

- Um empregado gerencia um departamento.
- Um departamento é gerenciado por apenas um empregado.

**Cliente e Login**

- Um cliente possui apenas um login.
- O login pertence à apenas um cliente.

## Cardinalidade Mínima

Refere-se ao número mínimo de instancias de uma entidade que deve ser associada
a uma única instância de uma entidade relacionada.

Ou seja, a quantidade mínima de outra instância de entidade necessária para que
outra possa existir. É uma obrigatoriedade e podem ter apenas os seguintes valores: 0 e 1.

### Cardinalidade mínima um.