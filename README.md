# Banco_de_Dados_1_2024

## 1º Projeto da disciplina de Banco de Dados 1

---
·Criadas as entidades principais envolvidas no sistema :Livro, Autor, Usuário e Empréstimo.
<p> Outras entidades: Devolução, Promoção, Midia, Doação, Sebo_E-comerce, Parcerias.</p>

· Os atributos essenciais para cada entidade foraam criados: 
- **Livro**
- ID_Livro(chave), titulo, autor, ano, edição, editora, area, gÊnero, quant_livros,status;</p>

- **E-book**
-  ID_E-book(chave), titulo, autor, ano, edição, editora, area, gÊnero, link, quant_livros,status;</p>

**Usuário** 
- ID_usuário(chave), nome, CPF, login,senha_usuário, cel, end, gênero, status_Usuário; </p>

**Funcionário**
- ID_Func, nome, login,senha_usuário, cel, end, gênero,função, status_func;</p>
- Expecializações: Professor, auxliar_Biblio e Bibliotecário;</p>

**Empréstimo**
· --- ID_Livro(Chave), ID_emprest, ID_func, ID_usuário, Data_emprest;</p>

**Devolução**
- ID_Livro(Chave), ID_devolução,ID_emprest, ID_func, ID_usuário, Data_dev;</p>

**Multa**
--- Data_emprest, data_dev,tempo_permanecia, ID_Livro, ID_Usuário,livro_danificado;</p>

**Promoções**
- Especialikzações:</p>
- Livro_mes,Cineteca, Ranking_leiores, clube_leitura, Aniversariante_mes;</p>

**Midia**u
- ID_func
- Especializações: Noticia(Local, muno,tema,area, ), redes sociais(e-mail_biblioteca-chave) , evento( nome,interno, externo);
**Doação**
  - ID_usu,ID_livro,gênero,Titulo, autor, editora,area
**Multa**
-Id_ Likvro, data_e3mpres, gÊnero, tempo_de_Permanencia, titulo, autor, editora, area;
**Sebo_E-comerce**
Editora, autor, editora, titulo, area, genero
- especializações vendedor(e-mail, cel, cpf, ID_vendor;
**Parcerias**
- Especializações: professor(ID_func), commercio_local(CNPJ/CPF, Nome_comercial,end) estudante(IDU_suário)
.


Relacionamentos estabbelecidos entre as entidades:
**Reserva**
usuário-livro/E-book; funcionário-livro/E-book;
**Efetua**
- Emprestimo-usuário-livro/E-book; emprestimo-Funcionário-livro/E-book,
- Devolução-usuário-livro/E-book; emprestimo-Funcionário-livro/E-book,
**Cadastra**
  Funcionário-LIvro/E-book/Usuário;
  **
· Utilizar cardinalidades para especificar a quantidade de entidades em cada lado do relacionamento.
- 


· Modelar a especialização-generalização, por exemplo, se há diferentes tipos de usuários (aluno, professor) com atributos específicos.
