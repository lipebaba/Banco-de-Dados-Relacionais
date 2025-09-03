Anotações Banco de dados - Aula 03

Relacionamento N:M (muitos para muitos)

Um relacionamento N:N (muitos para muitos) geralmente se transforma em uma
terceira tabela (também chamada de entidade associativa ou tabela de ligação)

Exemplo:

Entidade: Cliente N<>N Produto
Cria a terceira entidade associativa Pedidos
Cliente 1<>N Pedidos N<>1 Produto


Relacionamento 1:M (um para muitos)

Regra de Transformação: O atributo-chave da entidade no lado "um" (1) do
relacionamento se torna um atributo-chave estrangeira na entidade no lado
"muitos" (N).

Exemplo:

Entidade: Categoria (lado 1, chave primária: id_categoria)
Entidade: Livro (lado N, chave primária: id_livro)
Na tabela Livro, você adicionará uma coluna id_categoria que será uma chave
estrangeira, referenciando a tabela Categoria.

Entidades Fracas (Weak Entities)

Regra: Uma entidade fraca é aquela que não pode ser identificada de forma
única por seus próprios atributos. Ela precisa da chave primária de outra
entidade (a entidade proprietária) para formar sua chave. No DER, ela é
representada por um retângulo com linha dupla e o relacionamento com a
entidade proprietária por um losango com linha dupla.

Regras de Integridade (Integrity Rules)

Embora não sejam visuais no DER, são princípios cruciais que o modelo deve seguir:

Integridade de Entidade: A chave primária de uma entidade não pode ter valores nulos.
Isso garante que cada linha na tabela seja única e identificável.

Integridade Referencial: Uma chave estrangeira deve ter um valor que corresponda a
uma chave primária na tabela referenciada, ou deve ser completamente nula. Isso evita
"links quebrados" entre as tabelas.

