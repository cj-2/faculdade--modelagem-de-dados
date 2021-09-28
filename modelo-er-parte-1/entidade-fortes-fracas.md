# Entidades, Entidades Fortes e Fracas

Uma **Entidade** é um objeto de interesse para o usuario final e refere-se
realmente a um conjunto de entidades e não a uma única entidade.

Em outras palavas, em **MER**, uma Entidade corresponde na verdade a uma tabela.

## Exemplos de Entidade

- **Pessoa**: Estudade, Empregado, ...
- **Lugar**: Cidade, Sala, Armazém, ...
- **Evento**: Festa, Casamento, ...
- ...

Em DER, uma Entidade é nomeada utilizando subtantivos singulares. Ex:

- Aluno
- Professor
- Curso
- Turma
- Histórico

Uma **entidade** é diferente de uma **instância de entidade** e um **cojunto de entidades**. Ex

- Uma entidade define uma coleção de entidades que possumem os mesmo atributo. (Classe)
- Uma instância de entidade é um único item nessa coleção. (Objeto)
- Um conjunto de entidade é um conjunto de instâncias de entidade. (Lista de Objetos da mesma Classe ou Tabela).

Exemplo: 

- ALUNO é um tipo de entidade;
- Um aluno com o número de RGM "151623" é uma instância de entidade;
- Uma coleção de todos os alunos é um conjunto de entidades.

## Entidades Fortes e Fracas

### Entidade Forte

Se uma entidade pode existir sozinha, então essa entidade pode ser classficada como
uma **Entidade Forte**. Comumente são as primeiras a serem identificadas no processo
inicial de análise do projeto de modelagem de dados.

Ex: Um **Empregado**

### Entidade Fraca

Ao contrário de uma Entidade Forte, uma Entidade Fraca depende da existência de outras
entidades.

Ex: Um **Dependente** que deve ser vinculado a um Empregado.

Sem Empregado, não existe um dependente. Logo:
- Em Dependente deve depender da existência de um Empregado.

### Exemplo 1

#### Empregado (Forte)

- Id_Empregado
- Nome_Empregado

#### Dependente (Fraca)

- Id_Depentend
- Id_Empregado (chave estrangeira)
- Nome_Depentend

### Exemplo 2

#### Pedido (Forte)

- Id_Pedido
- ValorPedido
- Nome_Dependente

#### Itens__Pedidos (Fraca)

- Id_Pedido (chave estrangeira)
- Id_Produto (chave estrangeira)
- Id_ItemPedido

### Entidade Associativa

É uma entidade que descreve uma conexão entre duas entidades com uma relação de
muitos para muitos, por exemplo, atribuição de Empregado a Projetos.

Um Empregado pode ser atribuído a mais de um Projeto e um Projeto pode ser
atribuido a mais de um Empregado.

Se houver uma **informação sobre o relacionamento**, essas informações
serão mantidas em **uma entidade associativa,** por exemplo, o **número de
horas em que o Empregado trabalhou em um Projeto** expecífico é um atributo
da relação entre Empregado e Projeto, não de Empregado ou de Projeto.

Um **Empregado_Projeto** possui:

- Id_Empregado
- Id_Projeto
- Horas_Trabalhadas

Uma Entidade Associativa possui pelo menos duas ou mais chaves estrangerias
em sua modelagem.

### Conteúdo Complementas

- [Modelo Entidade Relacionamento (MER) e Diagrama Entidade-Relacionamento (DER)
](https://www.devmedia.com.br/modelo-entidade-relacionamento-mer-e-diagrama-entidade-relacionamento-der/14332)