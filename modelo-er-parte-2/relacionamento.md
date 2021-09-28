# Relacionamento

Um relacionamento descreve uma associação entre entidades. Isto é, 
a quantidade de instâncias de uma entidade em relação à outras.

Por exemplo a Relação de um vendedor e vários clientes (1,n).

- Um vendedor pode atender vários clientes.
- Um cliente pode ser ser atendido por apenas um vendedor.

Em DER, uma relação é representado por meio de um losangolo.

## Grau de Relacionamento

O número de conjuntos de entidades que participam de um relacionamento,
sendo os mais comuns o **unário**, **binário** e ternário.

### Relação Unária

É uma associação entre duas instâncias do mesmo tipo de entidade,
ou seja, R pertence E1 x E1. Exemplo:

- Todo empregado em uma determinada empresa possui um supervisor.
- Todo supervisor é um empregado.

Já que todo supervisor também é um empregado, a relação é entre instâncias
da mesma entidade.

### Relação Binária

É uma relação entre dois tipos de entidades diferentes, ou seja, 
R pertence E1 x E2. Exemplo:

- Um vendedor atende um cliente.

Vendedor e Cliente são tipos de entidades diferentes.

### Relação Ternária

É a associação entre três instâncias de tipos de entidades diferentes,
isto é, R pertence E1 x E2 x E3. Exemplo:

- Um professor pode lecionar diversas disciplinas em diversas turmas.
- Nesse caso, as entidades são: PROFESSOR, TURMA, DISCIPLINA.
- Um professor, leciona uma disciplina em uma turma.
- Uma turma precisa de um professor e um disciplina.
- Uma disciplina precisa de um professor lecionando e uma turma para assistir.