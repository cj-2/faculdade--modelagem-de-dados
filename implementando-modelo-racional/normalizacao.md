# Normalização

É um processo para avaliar e corrigir estruturas de tabelas, minimizando redundancias
e a probabilidade de anomalias. Acontece depois da criação do modelo conceitual do
banco de dados. É comum que o modelo conceitual sofra modificações depois dessa etapa.

A normalização funciona através de estágios chamados **Formas Normais.**

- Primeira Forma Normal (1FN)
- Segunda Forma Normal (2FN)
- Terceira Forma Normal (3FN)

Sendo que 3FN é melhor que 2FN é melhor que 1FN.

## Necessidade de Normalização

Normalmente utilizada em duas situações:

- Melhorar um banco de dado recem projetado.
- Melhor ou criar um novo banco de dados a partir de um existente.

## Anomalias

Os três tipos de anomalias que ocorrem em banco de dados não normalizados:

- Inserção
- Atualização
- Exclusão

## 1 Forma Normal (1FN)

Para definir que uma tabela está na primeira forma normal, todas as colunas 
devem possuir um valor único e não deve haver grupos repetitivos (colunas)
em uma linha ou atributo compostos.

**Regras**

- 1 Não devem existir colunas com dados repetidos ou similares.
- 2 Cada item de dados deve ser atômico (não possuir valores compostos).
- 3 Cada linha deve ser única, isto é, deve possuir uma chave primária.
- 4 Cada campo deve ter um nome exclusivo.

### Exemplo Ruim

**Tabela 1**

| id_Cliente | Nome_Cliente  | Telefone1 | Telefone2 | Telefone3  |
|------------|---------------|-----------|-----------|------------|
|  123       | João da Silva | 1234-5678 | 4567-9876 | 7894-56123 |

Os números de telefones são do mesmo tipo, ou seja, são repetidos. 
Esse tipo de modelagem fere a 1 regra da 1FN.

**Tabela 2**

| id_Cliente | Nome_Cliente  | Email                                      |
|------------|---------------|--------------------------------------------|
|  123       | João da Silva | joao.silva@gmail.com; joaozinho@gmail.com; |

Essa tabela possui coluna com valores compostos, ferindo a 2 regra da 1FN.
Os dados não são atômicos.

### Exemplo Certo

Levando em consideração a **Tabela 2**, essa seria a solução normalizada:

**Tabela 4** 

| id_Cliente | Nome_Cliente  |
|------------|---------------|
| 123        | João da Silva |
| 125        | José Ferreira |

**Tabela 5**

| Id_Email | Id_Cliente | Email                |
|----------|------------|----------------------|
| 1        | 123        | joao.silva@gmail.com |
| 2        | 125        | jose@gmail.com       |

## 2 Forma Normal (2FN)

Para uma tabela estar na segunda forma normal 2FN, ela deve estar na 1FN
e não possuir campos que sejam funcionalmente dependentes de parte
da chave primária.

**Regras**

- A tabela deve estar já na primeira forma normal (1FN)
- Todos os atributos não-chave devem depender da chave primária completa, ou seja, 
não contenha dependência parcial.

Resumindo, não deve haver dados que estão de fora da entidade da tabela. Assim, respeitando sua classe.

## 3 Forma Normal (3FN)

**Regras**

Além de estar na 1FN e 2FN, não possua dependências transitivas.

- A tabela deve estar na 1FN e 2FN
- Não existam atributos não-chave que dependam de outros atributos não-chave.

## Formas 4 e 5

Também existem outras formas normais mais complexas:

- A tabela está na quarta forma normal (4FN) se nenhuma instância da tabela
do banco de dados contiver dois ou mais dados independentes e multivalorados
descrevendo a entidade relevante, então ela estará na quarta forma normal.

- Uma tabela está na quinta forma normal (5FN) somente se estiver em 4NF e não
puder ser decomposta em qualquer número de tabelas menores sem perda de dados.