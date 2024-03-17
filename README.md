# Banco_de_Dados_1_2024

## 1º Projeto da disciplina de Banco de Dados 1

---
·Criadas as entidades principais envolvidas no sistema :Livro, Autor, Usuário e Empréstimo.
<p> Outras entidades: Devolução, , Promoção, Midia, Doação, Sebo_E-comerce, Parcerias.</p>

· Os atributos essenciais para cada entidade foraam criados: 
- ** Livro
· --- ID_Livro(chave), titulo, autor, ano, edição, editora, area, gÊnero, quant_livros,status;</p>

- ** E-book
· --- ID_E-book(chave), titulo, autor, ano, edição, editora, area, gÊnero, link, quant_livros,status;</p>

<p>** Usuário
· --- ID_usuário(chave), nome, CPF, login,senha_usuário, cel, end, gênero, status_Usuário; </p>

<p>** Funcionário
· --- ID_Func, nome, login,senha_usuário, cel, end, gênero,função, status_func;</p>
· --- Expecializações: Professor, auxliar_Biblio e Bibliotecário;</p>

· <p>** Empréstimo
· --- ID_Livro(Chave), ID_emprest, ID_func, ID_usuário, Data_emprest;</p>

· <p> ** Devolução
· -- ID_Livro(Chave), ID_devolução,ID_emprest, ID_func, ID_usuário, Data_dev;</p>

<p> ** Multa
--- Data_emprest, data_dev,tempo_permanecia, ID_Livro, ID_Usuário,livro_danificado;</p>

<p> ** Promoções
--- Especialikzações:</p>




· Estabelecer relacionamentos entre as entidades, como a relação entre Livro e Autor.

· Utilizar cardinalidades para especificar a quantidade de entidades em cada lado do relacionamento.

· Modelar a especialização-generalização, por exemplo, se há diferentes tipos de usuários (aluno, professor) com atributos específicos.
