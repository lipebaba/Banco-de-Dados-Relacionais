Anotações - Aula 04 - Banco de Dados Relacionais

NORMALIZAÇÃO DE DADOS

É o processo de organizar os dados em um banco para reduzir redundâncias (repetições
desnecessárias) e evitar anomalias (problemas em inserções, atualizações e exclusões).
Exemplo prático: Se em uma tabela Pedidos eu armazeno também o endereço completo do
cliente, toda vez que o cliente mudar de endereço, eu teria que atualizar várias linhas.

Anomalias que a Normalização resolve

1.Anomalia de Inserção – Não consigo cadastrar um cliente sem que ele faça um pedido.
2.Anomalia de Atualização – Alterar um dado em um lugar, mas não em outro (ex.: telefone de
cliente).
3.Anomalia de Exclusão – Ao excluir um pedido, perco também o cadastro do cliente.

Primeira Forma Normal (1FN)

Elimina atributos multivalorados (listas em uma coluna).
Exemplo errado: Telefones: (21)99999-9999, (22)98888-8888.
Correção: Criar uma tabela Telefone com relacionamento para Cliente.

Segunda Forma Normal (2FN)

Elimina dependências parciais em chaves compostas.
Exemplo: Em uma tabela PedidosProdutos(PedidoID, ProdutoID, NomeProduto, Preço), o
atributo NomeProduto depende só de ProdutoID, não da chave composta.
Correção: Criar tabela Produto.

Terceira Forma Normal (3FN)

Elimina dependências transitivas.
Exemplo: Se Aluno(Matrícula, Curso, CoordenadorCurso), o CoordenadorCurso depende de
Curso, não diretamente de Matrícula.
Correção: Criar tabela Curso.

Modelo Lógico

O Modelo Lógico é uma representação intermediária entre o Modelo Conceitual (DER) e o Modelo Físico (SQL,
tabelas). É uma representação estruturada e formal do banco de dados, mais próxima da implementação em um
SGBD relacional, mas ainda independente de qualquer SGBD específico (como Oracle, SQL Server, MySQL).

Objetivos do Modelo Lógico

• Representar a estrutura dos dados de forma mais próxima à implementação.
• Definir os elementos necessários à criação do banco: tabelas, campos, tipos de dados,
chaves primárias e estrangeiras.
• Garantir integridade dos dados.
• Preparar a transição para o modelo físico (SQL).

Regras de Conversão

Regra 1: Toda entidade vira uma tabela e seus respectivos campos.

Regra 2: Relacionamento, para todo relacionamento NxN é preciso criar nova tabela daquele
relacionamento, não esquecendo do referencial das tabelas, levar as PK das tabelas envolvidas no
relacionamento e se tornam FK na tabela criada.

Regra 3: Relacionamento, para todo relacionamento 1xN é preciso pegar a chave primária da tabela
de lado 1 e referenciar na tabela de lado N.

Regra 4: Relacionamento, para todo relacionamento com cardinalidade 1x1, ambos os lados tem
cardinalidade mínima obrigatoriedade (1,1) é preciso unir tanto as tabelas quanto o relacionamento
em uma única tabela.

Regra 5: Relacionamento, para todo relacionamento com cardinalidade 1x1, com apenas um lado
obrigatório cria as duas tabelas e o lado 0 recebe a chave primária da outra tabela e o atributo do
relacionamento.

Regra 6: Relacionamento, para todo relacionamento com cardinalidade 1x1, com AMBOS lados
sem obrigatoriedade cardinalidade mínima (0,0) cria as duas tabelas e o relacionamento vira
terceira tabela sendo o lado 0, e recebe a chave primária da outras 2 tabelas.

