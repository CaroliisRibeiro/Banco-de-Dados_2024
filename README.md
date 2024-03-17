# Banco_de_Dados_1_2024

## 1º Projeto da disciplina de Banco de Dados 1

### Criadas as entidades principais envolvidas no sistema :Livro, Autor, Usuário e Empréstimo.
<p> Outras entidades: Devolução, Promoção, Midia, Doação, Sebo_E-comerce, Parcerias.</p>

### Os atributos essenciais para cada entidade foraam criados: 
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
- ID_Livro(Chave), ID_emprest, ID_func, ID_usuário, Data_emprest;</p>
**Devolução**
- ID_Livro(Chave), ID_devolução,ID_emprest, ID_func, ID_usuário, Data_dev;</p>
**Multa**
- Data_emprest, data_dev,tempo_permanecia, ID_Livro, ID_Usuário,livro_danificado;</p>
**Promoções**
- Livro_mes(ID_Livro - Chave) ,Cineteca(ID_Usuário e ID_Func- Chaves), Ranking_leiores(ID_Usuário - Chave), clube_leitura(ID_Usuário e ID_Func- Chaves), Aniversariante_mes(ID_Usuário - Chave);</p>
**Midia**
- ID_func
- Especializações: Noticia(Local, muno,tema,area, ), redes sociais(e-mail_biblioteca-chave) , evento( nome,interno, externo);
**Doação**
- ID_usu,ID_livro,gênero,Titulo, autor, editora,area.
**Multa**
- Id_ Likvro, data_e3mpres, gÊnero, tempo_de_Permanencia, titulo, autor, editora, area;
**Sebo_E-comerce**
Editora, autor, editora, titulo, area, genero
- Especializações vendedor(e-mail, cel, cpf, ID_vendor-chave);
- Especializações Cliente(e-mail, cel, cpf, ID_cliente-chave).
**Parcerias**
- Especializações: professor(ID_func), commercio_local(CNPJ/CPF, Nome_comercial,end) estudante(IDU_suário).

### Relacionamentos estabbelecidos entre as entidades:
**Reserva**
- Usuário -> livro/E-book;
- funcionário -> livro/E-book;
**Efetua**
- Emprestimo -> usuário -> livro/E-book;
- Emprestimo -> Funcionário -> livro/E-book,
- Devolução -> usuário -> livro/E-book;
- Devolução -> Funcionário -> livro/E-book.
**Cadastra**
- Funcionário -> LIvro/E-book/Usuário;
- Funcionário -> Usuário;
-  Funcionário -> Funcionário.
**Aplica**
- Devolução -> Multa.
**Implica** 
- Emprestimo -> Devolução.
**Participa**
- Usuário -> Promoções;
- Usuário -> Doação.
  **Coordena**
- Auxiliar_Biblio -> Midia;
- Auxiliar_Biblio -> Parcerias;
- Auxiliar_Biblio -> Sebo_E-comerce.
  
### Utilizar cardinalidades para especificar a quantidade de entidades em cada lado do relacionamento.
- Nesse projeto a mioria da cardonalidade é (1,n), pois em relação a entidade Funcionário, temos o exemplo de: "1" Funcionário cadasdra "n" Usuários e "n" usuários é cadaastrado por 1 Funionário;
- Outro caso que aconteceu no projeto foi o de (1,1): "1" Funcinário coordena "1" Midia e também "1" Funcionário coordena "1" Sebo_E-comerce.

### Especialização-generalização
- Funcionário Expecializações: Professor, auxliar_Biblio e Bibliotecário( mesmos atributos de Funcionáro);</p>
- Promoções Especializações: Livro_mes(ID_Livro - Chave) ,Cineteca(ID_Usuário e ID_Func- Chaves), Ranking_leiores(ID_Usuário - Chave), clube_leitura(ID_Usuário e ID_Func- Chaves), Aniversariante_mes(ID_Usuário - Chave);
- Midia Especializações: Noticia(Local, muno,tema,area, ), redes sociais(e-mail_biblioteca-chave) , evento( nome,interno, externo);
- Sebo_E-comerce Especializações: vendedor(e-mail, cel, cpf, ID_vendor - chave), Cliente(e-mail, cel, cpf, ID_cliente-chave);
- Parceria Especializações: professor(ID_func), commercio_local(CNPJ/CPF, Nome_comercial,end) estudante(IDU_suário).


