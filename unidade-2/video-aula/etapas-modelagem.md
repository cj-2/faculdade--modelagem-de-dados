# Modelagem de Dados

## Objetivos da Modelagem

- Identificar os diferentes componentes de dados, considerando os dados brutos e processados, bem como entidades.
- Identificar as relações entre os diferentes componentes de dados.
- Identificar os usos antecipados dos dados (chamados requisitos), com o reconhecimento dos dados mais valiosos para empresa.
- Identificar os pontos fortes e restrições da tecnologia (hardware e software) que será utilizado durante o projeto.
- Construir um modelo preliminar das entidades e suas relações.

## Levantamento de Requisitos

É o processo que levantamos os requisitos básicos do sistema.

- Quem são os atores do processo?
- O que o analista deve buscar?
- Como encontramos a informação?
- A dinâmica do levantamento e análise de requisitos.

## Regras de Negócio

Não devem depender de um sistema, são regras que existem, independe do sistema existir.

**Exemplos:**

- Todo cliente deve ser cadastrado.
- O CPF e e-mail são obrigatórios quando um cliente é cadastrado.
- Toda venda deve gerar um cupom fiscal.
- É obrigatório ser fornecido um CPF para a geração de um cupom fiscal.
- Uma venda dever ser realizada somente por um funcionário do departamento de vendas.

## Tipos de Modelos de Dados

### Modelo Conceitual

- Entidades importantes e as relações entre elas.
- Nenhum atributo é especificado
- Nenhuma chave primária é especificada.

### Modelo Lógico

- Independente de banco de dados.
- Possui todas as entidades e relações entre elas.
- Todos os atributos para cada entidade são especificados.
- A chave primária de cada entidade é especificada.
- São especificadas chaves estrangeiras (chaves que indentificam a relação entre diferentes entidades)
- A normalização ocorre neste nível.

### Modelo Físico

- Especifica todas as tabelas e colunas.
- Chaves estrangeiras são usadas para identificar relações entre tabelas.
- Considerações físicas podem fazer com que o modelo de dados físico sejam bastantes diferentes do modelo de dados logicos.
- Especificação de que tipo de banco de dados será utilizado.