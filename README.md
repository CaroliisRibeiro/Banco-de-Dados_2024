# Banco_de_Dados_1_2024

## 1º Projeto da disciplina de Banco de Dados 1 

# Sistema de Gerenciamento de Biblioteca 

![06aaaf5758865ee026e82eba6780ca7b](https://github.com/CaroliisRibeiro/Banco-de-Dados_2024/assets/127742540/b723605b-e1de-42a0-a499-3198332e72b4)

#### Objetivo: Desenvolver um sistema de gerenciamento de biblioteca utilizando o Modelo Entidade-Relacionamento (MER).

O sistema escolhido para este projeto é o de Gerenciamento de Biblioteca. Através dele, pude compreender, elaborar e aplicar os conteúdos estudados em sala de aula, abrangendo uma variedade de tópicos, tais como: Visão geral de banco de dados, Modelo Entidade-Relacionamento (MER) - incluindo entidades, atributos, chaves, relacionamentos e cardinalidades, além do Modelo Entidade-Relacionamento estendido, que aborda especialização-generalização e agregação. Também explorei o Mapeamento MER → Relacional, abordando entidades, atributos, chaves, relacionamentos, cardinalidades, relacionamentos n-ários, especialização-generalização e agregação. Além disso, discuti o uso de Ferramentas CASE e forneci exemplos práticos para ilustrar esses conceitos.

Neste projeto, você terá a oportunidade de visualizar a modelagem conceitual, que é a fase que sucede a análise de requisitos em um projeto de banco de dados. Durante esta etapa, traduzi os requisitos identificados anteriormente para diagramas e modelos, representando visualmente os conceitos e processos de negócio relacionados ao Sistema de Gerenciamento de Biblioteca.

Em última análise, este projeto não apenas me preparou para enfrentar desafios futuros na concepção e implementação de sistemas de gerenciamento de biblioteca, mas também destacou a importância da modelagem conceitual na criação de soluções eficazes e eficientes para problemas do mundo real.

#### Link Projeto

https://universidadecatolica-my.sharepoint.com/:f:/g/personal/ana_00000801596_unicap_br/EsljtOvUje5OvTBJ04lxBXoBcyRvwx4SWajtFlFlC5jK0A?e=daKN7m

#### Imagem Projeto
![Projeto banco de Dados Ana Carolina Ribeiro](https://github.com/CaroliisRibeiro/Banco-de-Dados_2024/assets/127742540/8e7d3586-6dd4-442c-ba08-07eb32370c2c)


### 1. ​Requisitos Mínimos e Extras :
## Criadas as entidades principais envolvidas no sistema :Livro, Autor, Usuário e Empréstimo.
- Outras entidades: Devolução, Promoção, Midia, Doação, Sebo_E-comerce, Parcerias.

## Os atributos essenciais para cada entidade foraam criados: 
- **Livro**
- ID_Livro(chave), titulo, autor, ano, edição, editora, area, gÊnero, quant_livros,status;
  
- **E-book**
-  ID_E-book(chave), titulo, autor, ano, edição, editora, area, gÊnero, link, quant_livros,status;
  
**Usuário** 
- ID_usuário(chave), nome, CPF, login,senha_usuário, cel, end, gênero, status_Usuário.
  
**Funcionário**
- ID_Func, nome, login,senha_usuário, cel, end, gênero,função, status_func;
- Expecializações: Professor, auxliar_Biblio e Bibliotecário;
  
**Empréstimo**
- ID_Livro(Chave), ID_emprest, ID_func, ID_usuário, Data_emprest;
  
**Devolução**
- ID_Livro(Chave), ID_devolução,ID_emprest, ID_func, ID_usuário, Data_dev;
  
**Multa**
- Data_emprest, data_dev,tempo_permanecia, ID_Livro, ID_Usuário,livro_danificado;
  
**Promoções**
- Livro_mes(ID_Livro - Chave) ,Cineteca(ID_Usuário e ID_Func- Chaves), Ranking_leiores(ID_Usuário - Chave), clube_leitura(ID_Usuário e ID_Func- Chaves), Aniversariante_mes(ID_Usuário - Chave);
  
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

## Relacionamentos estabbelecidos entre as entidades:
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
  
## Utilizar cardinalidades para especificar a quantidade de entidades em cada lado do relacionamento.
- Nesse projeto a mioria da cardonalidade é (1,n), pois em relação a entidade Funcionário, temos o exemplo de: "1" Funcionário cadasdra "n" Usuários e "n" usuários é cadaastrado por 1 Funionário;
- Outro caso que aconteceu no projeto foi o de (1,1): "1" Funcinário coordena "1" Midia e também "1" Funcionário coordena "1" Sebo_E-comerce.

## Especialização-generalização
- Funcionário Expecializações: Professor, auxliar_Biblio e Bibliotecário( mesmos atributos de Funcionáro);
- Promoções Especializações: Livro_mes(ID_Livro - Chave) ,Cineteca(ID_Usuário e ID_Func- Chaves), Ranking_leiores(ID_Usuário - Chave), clube_leitura(ID_Usuário e ID_Func- Chaves), Aniversariante_mes(ID_Usuário - Chave);
- Midia Especializações: Noticia(Local, muno,tema,area, ), redes sociais(e-mail_biblioteca-chave) , evento( nome,interno, externo);
- Sebo_E-comerce Especializações: vendedor(e-mail, cel, cpf, ID_vendor - chave), Cliente(e-mail, cel, cpf, ID_cliente-chave);
- Parceria Especializações: professor(ID_func), commercio_local(CNPJ/CPF, Nome_comercial,end) estudante(IDU_suário).



