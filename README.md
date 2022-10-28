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

> O sistema delivery da Dociê conterá as informações aqui detalhadas. Do CLIENTE armazenará o seu código, cpf, nome e telefone. De TELEFONE serão armazenados  Do MOTOBOY serão armazenados código, nome, cnh, placa da moto utilizada na entrega e salário. Do PEDIDO serão armazenados código e data e hora. De ENDEREÇO serão armazenados código, cep, número e logradouro. De BAIRRO serão armazenados código e bairro. De CIDADE serão armazenados código e cidade. De TIPO_LOGRADOURO serão armazenados código e tipo_logradouro.<br>
>Um cliente pode ter um ou vários telefones enquanto um telefone pode ter um cliente. Um cliente pode fazer um ou vários pedidos enquanto um pedido pode ser feito por um cliente. Um pedido pode ter um motoboy entregando enquanto um motoboy pode entregar vários pedidos. Um pedido pode ter uma forma de pagamento enquanto uma forma de pagamento pode ter vários pedidos. Um pedido pode ter um endereço enquanto um endereço pode ter nenhum ou vários pedidos. Um endereço pode ter um tipo_logradouro mas um tipo_logradouro pode ter nenhum ou vários endereços. Um endereço pode ter um bairro mas um bairro pode ter nenhum ou vários endereços. Um endereço pode ter um cidade mas um cidade pode ter nenhum ou vários endereços.



### 4.PERGUNTAS A SEREM RESPONDIDAS E TABELA DE DADOS<br>
    
> A Confeitaria Dociê precisa inicialmente dos seguintes relatórios:
* Relatório de capacitação dos funcionários. Mostrará o nome de cada motoboy e sua quantidade de entregas desde quando começou a trabalhar no local. 
* Relatório que visa controlar a frequência dos clientes. As linhas resultantes devem apresentar o nome de cada cliente e a quantidade de pedidos já feitos por este
* Relatório dos produtos favoritos e mais almejados. Será necessário o nome do produto e quantas vezes ele foi comprado. 
* Relatório de pesquisa residencial. O bairro mais frequente em compras, sendo necessário seu endereço e quantidade de produtos vendidos para este local. 
* Relatório sobre o melhor horário de vendas. Sendo necessário a data e hora das compras


 ### 5.MODELO CONCEITUAL<br>
        
![Alt text](https://github.com/discipbd1/trab01/blob/master/images/concept_sample.png?raw=true "Modelo Conceitual")
    
    
#### 5.1 Validação do Modelo Conceitual
    [Grupo01]: Esther, Raynan, Sofia e Carlos Eduardo
    [Grupo02]: Mariana, Bruna, Illana e Daianny

#### 5.2 Descrição dos dados 
    CLIENTE: Tabela que armazena as informações relativas ao cliente<br>
    CPF: campo que armazena o número de Cadastro de Pessoa Física para cada cliente da empresa.<br>


### 6	MODELO LÓGICO<br>
     

### 7	MODELO FÍSICO<br>
        
        
       
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
    a) inclusão das instruções de inserção dos dados nas tabelas criadas pelo script de modelo físico
    (Drop para exclusão de tabelas + create definição de para tabelas e estruturas de dados + insert para dados a serem inseridos)
    b) Criar um novo banco de dados para testar a restauracao 
    (em caso de falha na restauração o grupo não pontuará neste quesito)
    c) formato .SQL

### 9	TABELAS E PRINCIPAIS CONSULTAS<br>
   OBS: Usar o colab para apresentar os resultados que devem incluir as instruções SQL + resultados em forma de tabela.<br>
   
#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>


># Marco de Entrega 01: Do item 1 até o item 9.1<br>

#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>
#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)
    a) Criar 5 consultas que envolvam os operadores lógicos AND, OR e Not
    b) Criar no mínimo 3 consultas com operadores aritméticos 
    c) Criar no mínimo 3 consultas com operação de renomear nomes de campos ou tabelas

#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12) <br>
    a) Criar outras 5 consultas que envolvam like ou ilike
    b) Criar uma consulta para cada tipo de função data apresentada.

#### 9.5	INSTRUÇÕES APLICANDO ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)<br>
    a) Criar minimo 3 de exclusão
    b) Criar minimo 3 de atualização

#### 9.6	CONSULTAS COM INNER JOIN E ORDER BY (Mínimo 6)<br>
    a) Uma junção que envolva todas as tabelas possuindo no mínimo 2 registros no resultado
    b) Outras junções que o grupo considere como sendo as de principal importância para o trabalho

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


