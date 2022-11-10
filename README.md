# TRABALHO 01:  Sistema da Confeitaria Dociê
Trabalho desenvolvido durante a disciplina de Banco de dados

# Sumário

### 1. COMPONENTES<br>
Integrantes do grupo<br>
Camila Egydio: camilafragaegydio@gmail.com<br>
Davi Nunes: davinunesribeiro@gmail.com<br>
Isabelly Andrades: isabellyandrades.ifes@gmail.com<br>
Yasmin Santana: mamin8172@gmail.com<br>

### 2.INTRODUÇÃO E MOTIVAÇÃO<br>

> A Confeitaria Dociê tem o objetivo de melhorar seu atendimento. Sendo uma empresa recente, fica localizada em um lugar de difícil acesso e entrega apenas para o estado do Espírito Santo. O sistema delivery da Dociê tem a intenção de melhorar o atendimento e entrega dos produtos, facilitando a compra de seus clientes através de um site de pedidos. Para este sistema realizar as operações será necessário o armazenamento do Cliente, Motoboy, Pedido e Produto. O sistema deverá gerar os pedidos e a entrega dos clientes de forma segura, gerando relatórios provenientes dessas ações. 
 

### 3.MINI-MUNDO<br>

>O sistema delivery da Dociê conterá as informações aqui detalhadas. Do CLIENTE armazenará o seu código, cpf, nome e o seu ou seus telefones. Do MOTOBOY serão armazenados código, nome, cnh, placa da moto utilizada na entrega e salário. Do PEDIDO serão armazenados código e data e hora. De ENDEREÇO serão armazenados código, cep, número e logradouro. De BAIRRO serão armazenados código e bairro. De CIDADE serão armazenados código e cidade. De TIPO_LOGRADOURO serão armazenados código e tipo. De COMPLEMENTO serão armazenados código e complemento.<br>
> Um cliente pode ter um ou vários telefones enquanto um telefone pode ter um cliente. Um cliente pode fazer um ou vários pedidos enquanto um pedido pode ser feito por um cliente. Um pedido pode ter um motoboy entregando enquanto um motoboy pode entregar vários pedidos. Um pedido pode ter uma forma de pagamento enquanto uma forma de pagamento pode ter vários pedidos. Um pedido pode ter um endereço enquanto um endereço pode ter nenhum ou vários pedidos. Um endereço pode ter um tipo_logradouro mas um tipo_logradouro pode ter nenhum ou vários endereços. Um endereço pode ter um bairro mas um bairro pode ter nenhum ou vários endereços. Um endereço pode ter um cidade mas um cidade pode ter nenhum ou vários endereços.




### 4.PERGUNTAS A SEREM RESPONDIDAS E TABELA DE DADOS<br>
    
> A Confeitaria Dociê precisa inicialmente dos seguintes relatórios:
* Relatório de desempenho dos funcionários. Mostrará o nome de cada motoboy e sua quantidade de entregas desde quando começou a trabalhar no local. 
* Relatório que visa controlar a frequência dos clientes. As linhas resultantes devem apresentar o nome de cada cliente e a quantidade de pedidos já feitos por este.
* Relatório dos produtos favoritos e mais almejados. Será necessário o nome do produto e quantas vezes ele foi comprado. 
* Relatório de pesquisa residencial. O bairro mais frequente em compras, sendo necessário seu endereço e quantidade de produtos vendidos para este local. 
* Relatório sobre o melhor horário de vendas. Sendo necessário a data e hora das compras. 


 ### 5.MODELO CONCEITUAL<br>
        
![image](https://user-images.githubusercontent.com/91489199/200624508-89958683-ee9c-4cce-9c9b-22874fcf4eca.png)

    
#### 5.1 Validação do Modelo Conceitual
    [Grupo01]: Carlos Eduardo, Esther, Raynan e Sofia
    [Grupo02]: Bruna, Daianny, Illana e Mariana

### 5.2 Descrição dos dados 
    CLIENTE: Tabela que armazena as informações relativas ao cliente
    codigo: Campo que armazena o número de identificação de cada cliente          
    cpf: Campo que armazena o cpf de cada cliente
    nome: Campo que armazena o nome de cada cliente
    telefone: Campo que relaciona os telefones com cada cliente
             
    MOTOBOY: Tabela que armazena as informações relativas ao motoboy
    codigo: Campo que armazena o número de identificação de cada motoboy
    placa_moto: Campo que armazena a placa da moto de cada motoboy
    salario: Campo que armazena o salário de cada motoboy
    cnh: Campo que armazena o cnh de cada motoboy
    nome: Campo que armazena o nome de cada motoboy
              
    PRODUTO: Tabela que armazena as informações relativas ao produto
    codigo: Campo que armazena o número de identificação do produto
    nome: Campo que armazena o nome do produto
    descricao: Campo que armazena a descrição do produto
    preco: Campo que armazena o preço de cada produto
           
    FORMA_DE_PAGAMENTO: Tabela que armazena as informações relativas a forma de pagamento
    codigo: Campo que armazena o número de identificação de cada forma de pagamento
    forma: Campo que armazena o nome de cada forma de pagamento
    
    PEDIDO: Tabela que armazena as informações relativas ao pedido
    codigo: Campo que armazena o número de identificação de cada pedido
    data_hora: Campo que armazena a data e hora de cada pedido
    
    ENDERECO: Tabela que armazena as informações relativas ao endereço
    codigo: Campo que armazena o número de identificação de cada endereço
    cep: Campo que armazena o cep de cada endereço
    numero: Campo que armazena o número de cada endereço
    logradouro: Campo que armazena o logradouro de cada endereço
    
    COMPLEMENTO: Tabela que armazena as informações relativas ao complemento
    codigo: Campo que armazena o número de identificação de cada complemento
    complemento: Campo que armazena o complemento do endereço
    
    TIPO_LOGRADOURO: Tabela que armazena as informações relativas ao tipo de logradouro
    codigo: Campo que armazena o número de identificação de cada logradouro
    tipo: Campo que armazena o tipo de logradouro do endereço

    BAIRRO: Tabela que armazena as informações relativas ao bairro
    codigo: Campo que armazena o número de identificação de cada bairro
    bairro: Campo que armazena o bairro de endereço

    CIDADE: Tabela que armazena as informações relativas ao bairro
    codigo: Campo que armazena o número de identificação de cada cidade
    cidade: Campo que armazena a cidade de endereço


### 6.	MODELO LÓGICO<br>

![image](https://user-images.githubusercontent.com/91489199/200624871-8f72e604-eaea-478c-87eb-3a108c1be5a6.png)


### 7.	MODELO FÍSICO<br>
              DROP TABLE IF EXISTS CLIENTE, TELEFONE, MOTOBOY, PRODUTO, FORMA_PAGAMENTO, CIDADE, BAIRRO, TIPO_LOGRADOURO, COMPLEMENTO, ENDERECO, PEDIDO, PEDIDO_PRODUTO CASCADE;

          CREATE TABLE CLIENTE (
              codigo integer PRIMARY KEY,
              cpf varchar(14),
              nome varchar(80)
          );

          CREATE TABLE TELEFONE (
              telefone integer PRIMARY KEY,
              fk_CLIENTE_codigo integer references CLIENTE(codigo)
          );

          CREATE TABLE MOTOBOY (
              codigo integer PRIMARY KEY,
              salario float,
              placa_moto varchar(8),
              cnh varchar(11),
              nome varchar(80)
          );
          CREATE TABLE PRODUTO (
              codigo integer PRIMARY KEY,
              nome varchar(25),
              descricao varchar(200),
              preco float
          );

          CREATE TABLE FORMA_PAGAMENTO (
              codigo integer PRIMARY KEY,
              forma varchar(40)
          );

          CREATE TABLE CIDADE (
              codigo integer PRIMARY KEY,
              cidade varchar(40)
          );

          CREATE TABLE BAIRRO (
              codigo integer PRIMARY KEY,
              bairro varchar(40)
          );

          CREATE TABLE TIPO_LOGRADOURO (
              codigo integer PRIMARY KEY,
              tipo varchar(40)
          );

          CREATE TABLE COMPLEMENTO (
              codigo integer PRIMARY KEY,
              complemento varchar(80)
          );

          CREATE TABLE ENDERECO (
              codigo integer PRIMARY KEY,
              cep varchar(9),
              numero integer,
              logradouro varchar(80),
              fk_TIPO_LOGRADOURO_codigo integer references TIPO_LOGRADOURO(codigo),
              fk_BAIRRO_codigo integer references BAIRRO(codigo),
              fk_CIDADE_codigo integer references CIDADE(codigo),
              fk_COMPLEMENTO_codigo integer references COMPLEMENTO(codigo)
          );

          CREATE TABLE PEDIDO (
              codigo integer PRIMARY KEY,
              data_hora timestamp,
              FK_FORMA_PAGAMENTO_codigo integer references FORMA_PAGAMENTO(codigo),
              FK_CLIENTE_codigo integer references CLIENTE(codigo),
              FK_MOTOBOY_codigo integer references MOTOBOY(codigo),
              FK_ENDERECO_codigo integer references ENDERECO(codigo)
          );

          CREATE TABLE PEDIDO_PRODUTO (
              qtd integer,
              FK_PEDIDO_codigo integer references PEDIDO(codigo),
              FK_PRODUTO_codigo integer references PRODUTO(codigo)
          );

        
       
### 8. INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
    
       INSERT INTO PRODUTO(codigo, nome, descricao, preco) VALUES
       (1, 'Fatia Nutellaja', 'Uma deliciosa fatia de  bolo com massa de bolo branco, recheio de nutella e brigadeiro de maracujá', 12.0),
       (2, 'Fatia Moraninho', 'Uma deliciosa fatia de  bolo com massa de bolo branco, recheio de morango e brigadeiro de ninho', 12.0),
       (3, 'Fatia Choconinho', 'Uma deliciosa fatia de  bolo com massa de bolo branco, recheio de brigadeiro tradicional e  brigadeiro de ninho', 12.0),
       (4, 'Fatia Chocolate', 'Uma deliciosa fatia de  bolo com massa de bolo branco com  recheio de brigadeiro tradicional', 12.0),
       (5, 'Fatia Red velvet', 'Uma deliciosa fatia de  bolo com massa de bolo vermelho recheio de brigadeiro branco e  brigadeiro de ninho', 12.0),
       (6,  'Bolo Candy Milk', 'Um delicioso bolo de mesa servindo 30 pessoas, com massa branca, recheio de doce de leite e doce de coco.', 120.0),
       (7, 'Bolo Abachoco', 'Um delicioso bolo de mesa servindo 30 pessoas, com massa branca, recheio de doce de leite e doce de coco.', 120.0),
       (8, 'Bolo Laranja', 'Um delicioso bolo de mesa servindo 30 pessoas, com massa de laranja, recheio de limão  e brigadeiro de ninho.', 120.0),
       (9, 'Bolo Vermelho', 'Um delicioso bolo de mesa servindo 30 pessoas, com massa branca, recheio de geleia de frutas vermelhas  e brigadeiro de framboesa.', 120.0),
       (10, 'Bolo Ferrero', 'Um delicioso bolo de mesa servindo 30 pessoas, com massa de chocolate, recheio de brigadeiro de ferrero rocher e brigadeiro de amendoim.', 120.0),
       (11, 'Brownie Simples', 'Um delicioso pedaço de brownie que derrete na sua boca.', 8.0),
       (12, 'Brownie Nutella', 'Um delicioso pedaço de brownie que derrete na sua boca com cobertura de Nutella', 9.0),
       (13, 'Churros Doce de Leite', 'Um maravilhoso churros quentinho recheado de nosso delicioso doce de leite', 7.0),
       (14, 'Churros Chocolate', 'Um maravilhoso churros quentinho recheado de nosso delicioso chocolate', 7.0),
       (15, 'Churros Nutella', 'Um maravilhoso churros quentinho recheado de nutella', 7.0);

       INSERT INTO CLIENTE(codigo, cpf, nome) values
       (10, '111.111.111-11', 'Lorena Toraes'),
       (20, '222.222.222-22', 'Kauã Terra'),
       (30, '333.333.333-33', 'Esther Moraes'),
       (40, '444.444.444-44', 'Sofia Salles'),
       (50, '555.555.555-55', 'Davi Salles'),
       (60, '666.666.666-66', 'Raynan Moraes'),
       (70, '777.777.777-77', 'Carlos Eduardo'),
       (80, '888.888.888-88', 'Harian Adami'),
       (90, '999.999.999-99', 'Mayana Teixeira'),
       (100, '100.100.100-00', 'Valentina Teixeira'),
       (110, '110.110.110-10', 'Camila Egydio'),
       (120, '120.120.120-12', 'Isabelly Balestrassi'),
       (130, '130.130.130-13', 'Davi Nunes'),
       (140, '140.140.140-14', 'Yasmin Santana');

       INSERT INTO TELEFONE(telefone, fk_cliente_codigo) values
       (111111111, 10),
       (222222222, 20),
       (202020202,20),
       (333333333,30),
       (303030303,30),
       (444444444,40),
       (404040404,40),
       (555555555,50),
       (666666666,60),
       (777777777,70),
       (888888888,80),
       (999999999,90),
       (101010101,100),
       (110110110,110),
       (120120120,120),
       (130130130,130),
       (140140140, 140);

       INSERT INTO MOTOBOY(codigo, salario, placa_moto, cnh, nome) values
       (100, 5000.0, '111-abcd', 11111111111, 'Gabriel Frinhani'),
       (200, 4000.0, '222-abcd', 22222222222, 'Raíssa Dias'),
       (300, 600.0, '333-abcd', 33333333333, 'Liz Dias'),
       (400, 600.0, '444-abcd', 44444444444, 'Matheus Frinhani'),
       (500, 600.0, '555-abcd', 55555555555, 'Rafael Frinhani'),
       (600, 3000.0, '666-abcd', 66666666666, 'Eduardo Olmo'),
       (700, 3000.0, '777-abcd', 77777777777, 'Paulo Cezari'),
       (800, 4000.0, '888-abcd', 88888888888, 'Mariana Lopes'),
       (900, 2000.0, '999-abcd', 99999999999, 'Illana Cardoso'),
       (110, 5000.0, '110-abcd', 10101010101, 'Nicolle Nunes');

       INSERT INTO BAIRRO (codigo, bairro) VALUES
       (1, 'Barcelona'),
       (2, 'Praia do Canto'),
       (3, 'Jardim Camburi'),
       (4, 'Jardim da Penha'),
       (5, 'Enseada do Suá'),
       (6, 'Boa Vista'),
       (7, 'Bairro de Fátima'),
       (8, 'Jacaraípe'),
       (9, 'Manoel Plaza'),
       (10, 'Hélio Ferraz'),
       (11, 'Eurico Salles'),
       (12, 'Vista da Serra I'),
       (13, 'Morada de Laranjeiras'),
       (14, 'Jucutuquara');

       INSERT INTO CIDADE (codigo, cidade) VALUES
       (1, 'Vitória'),
       (2, 'Serra');

       INSERT INTO TIPO_LOGRADOURO (codigo, tipo) VALUES
       (1, 'Aeroporto'),
       (2, 'Alameda'),
       (3, 'Área'),
       (4, 'Avenida'),
       (5, 'Campo'),
       (6, 'Chácara'),
       (7, 'Colônia'),
       (8, 'Condomínio'),
       (9, 'Conjunto'),
       (10, 'Distrito'),
       (11, 'Esplanada'),
       (12, 'Estação'),
       (13, 'Estrada'),
       (14, 'Favela'),
       (15, 'Fazenda'),
       (16, 'Feira'),
       (17, 'Jardim'),
       (18, 'Ladeira'),
       (19, 'Lago'),
       (20, 'Lagoa'),
       (21, 'Largo'),
       (22, 'Loteamento'),
       (23, 'Morro'),
       (24, 'Núcleo'),
       (25, 'Parque'),
       (26, 'Passarela'),
       (27, 'Pátio'),
       (28, 'Praça'),
       (29, 'Quadra'),
       (30, 'Recanto'),
       (31, 'Residencial'),
       (32, 'Rodovia'),
       (33, 'Rua'),
       (34, 'Setor'),
       (35, 'Sítio'),
       (36, 'Travessa'),
       (37, 'Trecho'),
       (38, 'Trevo'),
       (39, 'Vale'),
       (40, 'Vereda'),
       (41, 'Via'),
       (42, 'Viaduto'),
       (43, 'Viela'),
       (44, 'Vila');

       insert into COMPLEMENTO(codigo, complemento) values
        (1, 'Apartamento 202'),
        (2, 'Próximo ao supermercado'),
        (3, 'Apartamento 404'),
        (4, 'Na frente do posto de gasolina'),
        (5, 'Casa roxa de esquina'),
        (6, 'Descendo a maçonaria'),
        (7, 'Portão preto com bandeira da copa'),
        (8, 'Apartamento 606'),
        (9, '');

       INSERT INTO ENDERECO (codigo, cep, numero, logradouro, fk_tipo_logradouro_codigo, fk_bairro_codigo, fk_cidade_codigo, fk_complemento_codigo) VALUES
       (1, '29160-161', 300, 'João Palácio', 4, 11, 2,1),
       (2, '29160-596', 110, 'Rachel Vitalino de Brito', 33, 10, 2,2),
       (3, '29090-160', 400, 'José Maria Vivácqua Santos', 4, 3, 1,3),
       (4, '29050-902', 200, 'Américo Buaiz', 4, 5, 1,9),
       (5, '29176-360', 30, 'Presidente Kennedy', 4, 12, 2,4),
       (6, '29166-630', 330, 'dos Sabiás', 4, 13, 2,5),
       (7, '29040-780', 1729, 'Vitória', 4, 14, 1,6),
       (8, '29160-781', 576, 'Mário Batalha', 4, 7, 2,9),
       (9, '29090-720', 425, 'Judith Leão Castello Ribeiro', 4, 3, 1,7),
       (10, '29090-370', 500, 'Italina Pereira Mota', 33, 3, 1,8),
       (11, '29090-370', 720, 'José Maria Vivácqua Santos', 4, 3, 1,9),
       (12, '29160-521', 27, 'Rio Tocantins', 33, 10, 2,4);

       INSERT INTO FORMA_PAGAMENTO(codigo, forma) VALUES
       (1, 'Pix'),
       (2, 'Dinheiro'),
       (3, 'Cartão de Crédito'),
       (4, 'Cartão de Débito'),
       (5, 'Cheque');

       INSERT INTO PEDIDO (codigo, data_hora, fk_forma_pagamento_codigo, fk_cliente_codigo, fk_motoboy_codigo, fk_endereco_codigo) VALUES
       (110, '2022-10-28 10:59', 1, 10, 100, 1),
       (111, '2022-10-27 12:00', 5, 140, 200, 12),
       (112, '2022-10-10 14:21', 3, 30, 110, 5),
       (113, '2022-09-30 15:30', 1, 100, 200, 3),
       (114, '2022-10-01 13:13', 1, 10, 100, 1),
       (115, '2022-10-01 14:09', 2, 20, 300, 4),
       (116, '2022-10-03 12:00', 4, 110, 900, 7),
       (117, '2022-09-20 16:22', 3, 80, 110, 8),
       (118, '2022-09-13 17:19', 3, 30, 700, 5),
       (119, '2022-10-25 18:02', 2, 70, 700, 6),
       (120, '2022-10-26 19:55', 4, 110, 700, 7),
       (121, '2022-10-25 12:37', 1, 100, 100, 1),
       (122, '2022-09-10 19:12', 5, 40, 110, 9),
       (123, '2022-10-10 13:11', 1, 50, 300, 10),
       (124, '2022-10-11 14:00', 1, 50, 500, 10),
       (125, '2022-10-01 12:53', 5, 140, 300, 12),
       (126, '2022-09-28 11:53', 1, 50, 600, 10),
       (127, '2022-09-13 17:11', 4, 60, 400, 11),
       (129, '2022-09-13 13:12', 5, 40, 100, 9),
       (130, '2022-10-28 14:21', 2, 20, 800, 1),
       (131, '2022-10-25 15:11', 2, 70, 400, 6),
       (132, '2022-10-23 13:22', 2, 70, 300, 6),
       (133, '2022-10-11 11:11', 1, 10, 800, 1),
       (134, '2022-09-12 12:34', 3, 80, 110, 8),
       (135, '2022-10-13 13:46', 1, 130, 200, 2),
       (136, '2022-09-09 19:20', 3, 90, 100, 1),
       (137, '2022-09-10 14:21', 2, 70, 800, 6),
       (139, '2022-10-09 13:01', 1, 100, 900, 3),
       (140, '2022-10-09 14:22', 1, 10, 500, 1),
       (141, '2022-10-08 13:59', 2, 110, 110, 7),
       (142, '2022-10-09 20:12', 2, 70, 100, 6),
       (143, '2022-10-08 16:03', 4, 120, 800, 11),
       (144, '2022-09-30 17:43', 1, 30, 400, 8),
       (145, '2022-10-01 11:20', 1, 130, 500, 2),
       (146, '2022-10-02 12:00', 1, 130, 300, 2),
       (147, '2022-10-03 13:30', 2, 140, 110, 12);


       INSERT INTO PEDIDO_PRODUTO(FK_PEDIDO_codigo, fk_produto_codigo, qtd) VALUES
       (110, 1, 3),
       (110, 10, 2),
       (111, 2, 1),
       (112, 3, 2),
       (113, 4, 1),
       (114, 5, 1),
       (115, 6, 5),
       (116, 7, 5),
       (117, 8, 4),
       (118, 9, 2),
       (119, 10, 1),
       (120, 11, 7),
       (121, 12, 2),
       (121, 6, 3),
       (122, 13, 4),
       (123, 14, 1),
       (124, 15, 1),
       (125, 1, 2),
       (126, 1, 3),
       (127, 1, 2),
       (129, 3, 4),
       (130, 3, 10),
       (131, 4, 3),
       (132, 4, 2),
       (133, 10, 2),
       (134, 10, 2),
       (135, 10,1),
       (136, 10, 1),
       (137, 12, 1),
       (139, 13, 1),
       (140, 12,1),
       (141, 13,1),
       (142, 14, 4),
       (143, 7, 2),
       (144, 7, 3),
       (145, 9, 2),
       (146, 9, 2),
       (147, 5, 4);



### 9.	TABELAS E PRINCIPAIS CONSULTAS<br>
   (https://colab.research.google.com/drive/14mcKTM0mPxcb49IRpZiF8M3iotwbsff2?pli=1&authuser=1#scrollTo=xEFt9wpSFar8)<br>
   
#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>

># Marco de Entrega 01: Do item 1 até o item 9.1<br>

#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>

      --1) Mostra todos produtos onde o preço é igual a 120.00, pois são os bolos de festa
      select * from produto where preco=120.0;

     --2) Mostra a quantidade de fatias (produto = 1 a 5) compradas 
     select * from pedido_produto where fk_produto_codigo>=1 and fk_produto_codigo<=5;

     --3)Mostra os endereços dos bairros da cidade da Serra
     select * from endereco where fk_cidade_codigo=2;

     --4) Mostra as entregas realizadas pelos motoboys com salario menor
     select * from pedido where fk_motoboy_codigo>=300 and fk_motoboy_codigo<=500;
     
#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)
    a) Criar 5 consultas que envolvam os operadores lógicos AND, OR e Not
     --1) Salários iniciais maiores/iguais a 600 ou menores/iguais a 1000
     select motoboy.nome, motoboy.salario from motoboy where salario >= 600.00 and salario <= 1000.00;

     --2) Mostra endereços onde complemento não é vazio (código 9)
     select endereco.logradouro, endereco.fk_complemento_codigo from endereco where (fk_complemento_codigo >=1 and fk_complemento_codigo <9) or fk_complemento_codigo <> 9;

    b) Criar no mínimo 3 consultas com operadores aritméticos 
     --2) Mostra nome dos motoboys, salários do motoboy  e o salário mais 10% de bônus anual
     select motoboy.nome, motoboy.salario,
     motoboy.salario + (motoboy.salario*0.1) as bonus_sal_anual from motoboy;

     -–3) Mostra nome dos produtos, preco do produto e o produto mais o aumento de 5% anual
     select produto.nome, produto.preco,
     produto.preco + (produto.preco*0.05) as aumento_anual_produto from produto;

    c) Criar no mínimo 3 consultas com operação de renomear nomes de campos ou tabelas
       –1) Renomear telefone para celular
       select telefone as celular from telefone ;

#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12) <br>
    -- a) Criar outras 5 consultas que envolvam like ou ilike
    -- Consulta 01 - Selecionar todos os produtos que são bolos
    SELECT * FROM PRODUTO WHERE nome LIKE 'Bolo%'

    -- Consulta 02 - Selecionar todos os produtos que contém massa branca
    SELECT * FROM PRODUTO WHERE descricao LIKE '%branc%'

    -- Consulta 03 - Selecionar todos os motoboys que tem sobrenome Frinhani
    SELECT * FROM MOTOBOY WHERE nome LIKE '%Frinhani%'

    -- Consulta 04 - Selecionar todos os bairros que começam com B
    SELECT bairro FROM BAIRRO WHERE bairro LIKE 'B%'

    -- Consulta 05 - Selecionar todas as fatias que contém chocolate
    SELECT * FROM PRODUTO WHERE (nome LIKE 'Fatia%') AND (nome LIKE "______Choco%")

    -- b) Criar uma consulta para cada tipo de função data apresentada.
    -- Consulta 06 - Descobrir há quanto tempo cada pedido foi feito no sistema
    SELECT codigo, current_date as data_atual, data_hora, age(current_date, data_hora) as tempo_passado FROM PEDIDO

    -- Consulta 07 - Descobrir todos os pedidos feitos no mês 10
    SELECT * FROM PEDIDO WHERE extract('month' from data_hora) == 9

    -- Consulta 08 - Descobrir o dia da semana que os pedidos foram feitos
    SELECT codigo, date_part('dow' from data_hora) as daia_da_semana FROM PEDIDO

    -- Consulta 09 - Selecionar as placas de moto que começam com 1
    SELECT placa_moto FROM MOTOBOY WHERE placa_moto LIKE '1%'

    -- Consulta 10 - selecionar todos os cpf's que começam com 1
    SELECT nome, cpf FROM CLIENTE WHERE cpf LIKE '1%'

    -- Consulta 11 - Descobrir todos os pedidos feitos no dia 01 do mês 10
    SELECT * FROM PEDIDO WHERE extract('month' from data_hora) == 10 AND extract('day' from data_hora) == 1

    -- Consulta 12 - Descobrir todos os cep's que começam com 29160
    SELECT cep FROM ENDERECO WHERE cep LIKE '29160%'

#### 9.5	INSTRUÇÕES APLICANDO ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)<br>
    a) Criar minimo 3 de exclusão
    --1) Deleta o bairro Jardim da Penha
    delete from bairro where codigo=4;

    --2) Deleta o pedido 110 em pedido_produto
    delete from pedido_produto where fk_pedido_codigo =110;

    --3) Deleta o tipo logradouro 'Esplanada'
    delete from tipo_logradouro where codigo=11;
    
    b) Criar minimo 3 de atualização
    --1) Atualiza os nomes dos bolos para Bolo de Aniversário
    update produto set nome='Bolo de aniversário' where preco=120.0;

    --2) Atualiza a forma de pagamento pix para Boleto Bancário
    update forma_pagamento set forma='Boleto Bancário' where codigo=1;

    --3) Atualiza o cep do Rio Tocantins
    update endereco set cep='29280-551' where codigo=12;

#### 9.6	CONSULTAS COM INNER JOIN E ORDER BY (Mínimo 6)<br>
    a) Uma junção que envolva todas as tabelas possuindo no mínimo 2 registros no resultado
            –1) Relatório com informações a mais sobre o pedido
            select cliente.nome as "Nome do cliente", telefone.telefone as "Telefone do cliente",
            pedido.codigo as "Código do pedido", endereco.logradouro as "Logradouro",
            forma_pagamento.forma as "Forma de pagamento", motoboy.nome as "Nome do motoboy",
            pedido_produto.qtd as "Quantidade de produtos no pedido",
            produto.nome as "Nome do produto", (produto.preco *pedido_produto.qtd) as "Valor total do pedido"
            from cliente inner join telefone
            on (cliente.codigo = telefone.fk_CLIENTE_codigo)inner join pedido
            on (pedido.fk_cliente_codigo = cliente.codigo)inner join endereco
            on (pedido.fk_endereco_codigo =  endereco.codigo) inner join forma_pagamento
            on (forma_pagamento.codigo = pedido.fk_forma_pagamento_codigo) inner join motoboy
            on (pedido.fk_motoboy_codigo = motoboy.codigo) inner join pedido_produto
            on (pedido_produto.FK_pedido_codigo = pedido.codigo ) inner join produto
            on (pedido_produto.FK_produto_codigo = produto.codigo)
            order by cliente.nome;

    b) Outras junções que o grupo considere como sendo as de principal importância para o trabalho
           –2) Quantidade de telefone por cliente
           select cliente.nome, count(telefone.telefone) as qtd_tel_cliente from cliente
           inner join telefone on(cliente.codigo = telefone.fk_CLIENTE_codigo)
           group by cliente.nome
           order by cliente.nome;

           –3) Valor total de cada pedido que o cliente já fez
           select cliente.nome as "Nome do cliente",
           (pedido_produto.qtd * produto.preco) as "Valor por pedido",
           produto.nome as "Nome do produto"
           from cliente
           inner join pedido on (cliente.codigo = pedido.fk_cliente_codigo)
           inner join pedido_produto on (pedido.codigo = pedido_produto.fk_pedido_codigo)
           inner join produto on (pedido_produto.fk_produto_codigo = produto.codigo)
           order by cliente.nome

           –4) Códigos dos pedidos realizados pelos motoboys
           select motoboy.nome as "Nome do motoboy",
           pedido.fk_motoboy_codigo as "Códigos das entregas que realizadas"
           from motoboy inner join pedido on
           (motoboy.codigo = pedido.fk_motoboy_codigo)
           order by motoboy.nome

           –5) Forma de pagamento escolhida a cada pedido feito pelo cliente 
           select forma_pagamento.forma as "Formas de pagamento escolhida",
           pedido.codigo as "Código do pedido",
           cliente.nome as "Nome do cliente"
           from forma_pagamento inner join pedido on
           (forma_pagamento.codigo = pedido.fk_forma_pagamento_codigo) inner join
           cliente on (pedido.fk_cliente_codigo = cliente.codigo)
           order by cliente.nome

           –6) Logradouro do endereço, tipo de logradouro e seu respectivo complemento
           select endereco.logradouro as "Logradouro",
           TIPO_LOGRADOURO.tipo as "Tipo do logradouro", complemento.complemento as "Complemento logradouro" from endereco
           inner join complemento on (endereco.fk_complemento_codigo = complemento.codigo)
           inner join TIPO_LOGRADOURO on
           (endereco.fk_TIPO_LOGRADOURO_codigo = TIPO_LOGRADOURO.codigo)
           order by endereco.logradouro;

#### 9.7	CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)<br>
    a) Criar minimo 2 envolvendo algum tipo de junção

#### 9.8	CONSULTAS COM LEFT, RIGHT E FULL JOIN (Mínimo 4)<br>
    a) Criar minimo 1 de cada tipo

#### 9.9	CONSULTAS COM SELF JOIN E VIEW (Mínimo 6)<br>
        a) Uma junção que envolva Self Join (caso não ocorra na base justificar e substituir por uma view)
        b) Outras junções com views que o grupo considere como sendo de relevante importância para o trabalho

#### 9.10	SUBCONSULTAS (Mínimo 4)<br>
     a) Criar minimo 1 envolvendo GROUP BY
     b) Criar minimo 1 envolvendo algum tipo de junção

># Marco de Entrega 02: Do item 9.2 até o ítem 9.10<br>

### 10 RELATÓRIOS E GRÁFICOS (Usar template disponibilizado)
[Template de relatórios](https://github.com/discipbdint/public_samples/blob/main/BD_Exemplo_Relatorios_Empresa_VA.ipynb "Template relatórios")

#### a) análises e resultados provenientes do banco de dados desenvolvido (usar modelo disponível)
#### b) link com exemplo de relatórios será disponiblizado pelo professor no AVA
#### OBS: Esta é uma atividade de grande relevância no contexto do trabalho. Mantenha o foco nos 5 principais relatórios/resultados visando obter o melhor resultado possível.

    

### 11	AJUSTES DA DOCUMENTAÇÃO, CRIAÇÃO DOS SLIDES E VÍDEO PARA APRESENTAÇAO FINAL <br>

#### a) Modelo (pecha kucha)<br>
#### b) Tempo de apresentação 6:40 

># Marco de Entrega 03: Itens 10 e 11<br>
<br>
<br>
<br> 



### 12 FORMATACAO NO GIT:<br> 
https://help.github.com/articles/basic-writing-and-formatting-syntax/
<comentario no git>
    
##### About Formatting
    https://help.github.com/articles/about-writing-and-formatting-on-github/
    
##### Basic Formatting in Git
    
    https://help.github.com/articles/basic-writing-and-formatting-syntax/#referencing-issues-and-pull-requests
    
    
##### Working with advanced formatting
    https://help.github.com/articles/working-with-advanced-formatting/
#### Mastering Markdown
    https://guides.github.com/features/mastering-markdown/

    
### OBSERVAÇÕES IMPORTANTES

#### Todos os arquivos que fazem parte do projeto (Imagens, pdfs, arquivos fonte, etc..), devem estar presentes no GIT. Os arquivos do projeto vigente não devem ser armazenados em quaisquer outras plataformas.
1. <strong>Caso existam arquivos com conteúdos sigilosos<strong>, comunicar o professor que definirá em conjunto com o grupo a melhor forma de armazenamento do arquivo.

#### Todos os grupos deverão fazer Fork deste repositório e dar permissões administrativas ao usuário do git "profmoisesomena", para acompanhamento do trabalho.

#### Os usuários criados no GIT devem possuir o nome de identificação do aluno (não serão aceitos nomes como Eu123, meuprojeto, pro456, etc). Em caso de dúvida comunicar o professor.


Link para BrModelo:<br>
http://www.sis4.com/brModelo/download.html
<br>


Link para curso de GIT<br>
![https://www.youtube.com/curso_git](https://www.youtube.com/playlist?list=PLo7sFyCeiGUdIyEmHdfbuD2eR4XPDqnN2?raw=true "Title")


