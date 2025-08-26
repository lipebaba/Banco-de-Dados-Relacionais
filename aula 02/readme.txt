*Anotações Banco de Dados Relacionais*


Tema central: Banco de Dados Relacionais.

Foco na modelagem através de MER e DER.

O MER representa a realidade de um sistema.

Entidades → objetos ou conceitos do mundo real.

Atributos → características das entidades.

Relacionamentos → ligações entre entidades.

Relacionamentos podem ser binários, ternários ou maiores.

O mais comum é o relacionamento binário.

Exemplo: aluno–trabalho (muitos para muitos).

Exemplo: diretor–departamento (um para um).

Exemplo: autor–livro (muitos para muitos).

Exemplo: equipe–jogador (um para muitos).

Exemplo: cliente–encomenda (um para muitos).

Cada caso reforça diferentes cardinalidades.

O MER abstrai a realidade e organiza dados.

O DER traduz o MER para o modelo relacional.

O DER aproxima o projeto do banco real.

A aula também explica generalização.

Generalização → agrupa entidades semelhantes.

Vai do específico para o genérico.

Exemplo: “Conta-corrente” e “Conta-poupança” → “Contas”.

Isso reduz a complexidade.

Outro ponto é a especialização.

Especialização → divide entidade genérica em específicas.

Vai do genérico para o específico.

Exemplo: “Contas” → “Conta-corrente” e “Conta-poupança”.

Aumenta a flexibilidade do modelo.

Há o conceito de superclasse.

Superclasse → atributos comuns às subclasses.

Subclasse → atributos específicos de cada categoria.

O MER serve como base para projetar bancos de dados.

Ele auxilia a compreender o sistema de forma conceitual.

Mostra como entidades se conectam no mundo real.

Facilita o diálogo entre analistas e desenvolvedores.

O DER, por sua vez, é mais técnico.

Ele traduz conceitos para tabelas relacionais.

Representa chaves primárias e estrangeiras.

Define como os dados serão armazenados no SGBD.

A boa modelagem previne redundâncias.

Também ajuda a evitar inconsistências.

O modelo correto facilita consultas futuras.

Garante que os relacionamentos sejam claros.

Mantém integridade entre as entidades.

Apoia a escalabilidade do sistema.

Favorece a manutenção e evolução do banco.

MER e DER são complementares.

O MER foca no conceitual.

O DER foca no lógico.

Ambos são essenciais em qualquer projeto de banco de dados.

Conclusão: a modelagem é a base para bancos organizados e confiáveis.
