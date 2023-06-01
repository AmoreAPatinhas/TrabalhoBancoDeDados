# TRABALHO 01: Amor&Patinhas
Trabalho desenvolvido durante a disciplina de BD1

# Sumário

### 1. COMPONENTES<br>
Integrantes do grupo<br>
Isabella Bissoli: <isabellabg244@gmail.com><br>
Isabella Sampaio: <isabellasmsantos47@gmail.com><br>
Ludmila Dias: ludmiladias.inf@gmail.com <br>
Marcela Starling: marcela.sfl@hotmail.com <br>
Renzo Avance: <renzogavance@gmail.com><br>

### 2.INTRODUÇÃO E MOTIVAÇAO<br>

É de extrema importância ter um sistema eficiente de controle para auxiliar os administradores e voluntários no gerenciamento das atividades internas e na vida dos animais. O abrigo Amor&Patinhas atua não apenas como um lar temporário para esses animais, mas também como uma porta de entrada para que eles encontrem famílias amorosas e tenham uma segunda chance na vida. Todo animal ao chegar no abrigo, necessita de uma identificação e tratamento digno enquanto estiver em vida.
 

### 3.MINI-MUNDO<br>

Todo animal ao chegar no abrigo, necessita que um administrador o cadastre com algumas informações básicas para ser identificado, como a raça, nome, idade, data que chegou ao abrigo, cor e espécie (as espécies dos animais devem ser diferenciadas através de códigos). A espécie do animal se distingue por Gato ou Cachorro. Já a raça, informa a família do animal (exemplo: vira-lata, siamês, golden retriever...)
 
Do sistema espera-se que seja possível que o administrador cadastre também os voluntários que tenham interesse para ajudar nas atividades do abrigo e no cuidado dos animais. Ao demonstrar interesse, esse voluntário se torna um funcionário do abrigo e pode contribuir de várias formas, caso tenha alguma formação na área animal (como um veterinário), poderá auxiliar em consultas, aplicação e dosagem de remédios. Caso não tenha, é alocado para manutenções gerais, limpeza, alimentação e banho. Deve ser possível inserir os dados dos funcionários do abrigo, colocando nome, cpf, telefone, email, endereço e ocupação (onde irá atuar no abrigo, qual tarefa…) para que assim seja possível controlar a entrada e saída de pessoas no abrigo e sua atuação.
Todos os funcionários devem estar vinculados a pelo menos um animal ou vários. O animal pode estar relacionado a um ou vários funcionários, pois pode existir a necessidade de ter um veterinário supervisionando e outro funcionário dando banho e comida. 
O sistema deve possibilitar que o administrador ou o voluntário gere uma ficha, ou histórico, do animal (caso requisitado pelo usuário), contendo todas as informações que foram cadastradas do mesmo, para facilidade de visualização e controle

O sistema de adoção funciona da seguinte forma: Um interessado demonstra o interesse a um animal ou vários e é exibido na listagem de interesses para que ele passe por toda uma avaliação (se está adapto a receber seu novo amigo em sua residência). E caso seja o escolhido, o administrador poderá vincular o interessado ao animal, confirmando o processo de adoção. Para controle, antes do vinculo ocorrer, um cadastro do adotante deve ser feito no sistema com as informações: Nome, telefone, CPF, email e endereço.


### 4.RASCUNHOS BÁSICOS DA INTERFACE (MOCKUPS)<br>
 > Menu e login

![Captura de tela 2023-05-31 102636](https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/assets/95357142/3c345d7a-b359-4c93-9806-3d53029db0bf)

> Menu principal e Edição de dados

![Captura de tela 2023-05-31 102707](https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/assets/95357142/3b2eb39c-4632-43a9-94d4-135a52772688)

> Informações do animal e dados médicos de cada

![Captura de tela 2023-05-31 102743](https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/assets/95357142/22398020-9125-4c7a-b781-c95fb1e93d0d)
 
> Cronograma de tratamentos e agendamentos

![Captura de tela 2023-05-31 102810](https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/assets/95357142/cc5b94c9-dee6-42ec-bb6d-1378a3dfd9ad)

> Cadastrar animal e voluntário

![Captura de tela 2023-05-31 102926](https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/assets/95357142/016d7c83-162f-4257-b317-8391200cf82c)


#### 4.1 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO

    
> O sistema Amor&Patinhas fornecerá aos funcionários e administradores os seguintes relatórios:
* Relatório que informe para o administrador os funcionários que ajudam ativamente no abrigo com as seguintes informações: nome, cpf, telefone, email e ocupação.
* Relatório que informe sobre os animais que chegaram ao abrigo e foram recebidos pelos funcionários. Deve retornar as seguintes informações: nome do animal, espécie, raça, data da chegada, pelagem e o funcionário que está relacionado a ele (Caso não exista, exibe vazio).
* Relatório do cronograma de tratamentos, que exibe por animal, quais tratamentos foram feitos nele e se existe algum agendamento futuro marcado. As informações exibidas serão: Nome do animal, espécie, tipo de tratamento, descrição do tratamento e a data e hora (tanto como tratamento já feitos e futuros)
* Relatório com o registros dos adotantes para supervisão (saber onde o animal está e com quem): Nome do adotante, nome do animal, endereço, telefone, cpf e email
* Relatório  de espécie para exibir se o animal é um cachorro ou gato e o seu nome: nome e espécie
 
 
#### 4.2 TABELA DE DADOS DO SISTEMA:
    a) Esta tabela deve conter todos os atributos do sistema e um mínimo de 10 linhas/registros de dados.
    b) Esta tabela tem a intenção de simular um relatório com todos os dados que serão armazenados 
    e deve ser criada antes do modelo conceitual
    c) Após criada esta tabela não deve ser modificada, pois será comparada com os resultados finais na conclusão do trabalho
    
    
>## Marco de Entrega 01 em:<br>

### 5.MODELO CONCEITUAL<br>

Principais entidades: Animal, Funcionário e Adotante

Relacionamentos Principais:

> Cuida (Funcionários/Animal):
1) Um funcionário cuida de um ou vários animais
2) Um animal é cuidado por um ou vários funcionários

> Adota (Interessado/Animal):
1) Um interessado adota um animal ou vários
2) Um animal pode ser adotado por apenas um adotante ou por ninguém


> Realiza (Necessitado/Castração):
1) Um necessitado realiza nenhuma ou apenas uma castração
2) Um código de castração está ligado (pode ser ligado) a um animal necessitado 

![MODELO CONCEITUAL CERTO](https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/assets/95357142/cfb22bd0-dae1-4c19-b728-b1ea92bad290)
    
    B) NOTACAO UML (Caso esteja fazendo a disciplina de analise)
    
        
    
#### 5.1 Validação do Modelo Conceitual
    [Grupo01]: Richard, Kailany e Lucas
    Observação do Grupo01:

    
    [Grupo02]: Eduardo, Lucas e Vitor
    Observação do Grupo02:
    
#### 5.2 DECISÕES DE PROJETO

A) FUNCIONÁRIO: Identificação das informações do funcionário voluntário do abrigo para segurança e organização

B) ANIMAL: Identificação das informações de cada animal que chega no abrigo para controle da quantidade e de cad aum individualmente

C) ESPÉCIE: Identifica se o animal que chegou é Cachorro ou Gato

D) ENDEREÇO: Serve para identificarmos o endereço do funcionário e do adotante para segurança do abrigo

E) ADOTANTE: código do adotante, nome do adotante, cpf, email, endereço

F) ANIMAL ADOTANTE: código a adoção, código do adotante, código do animal, data da adoção

G) PROCEDIMENTO: código do procedimento, código do animal, descrição e data

H) TIPO DE TRATAMENTO: código de tratamento e descrição

>## Marco de Entrega 02 em: (30/04/2019)<br>
#### 5.3 DESCRIÇÃO DOS DADOS 
    [objeto]: [descrição do objeto]
    
    EXEMPLO:
    CLIENTE: Tabela que armazena as informações relativas ao cliente<br>
    CPF: campo que armazena o número de Cadastro de Pessoa Física para cada cliente da empresa.<br>


### 6	MODELO LÓGICO<br>
        a) inclusão do modelo lógico do banco de dados
        b) verificação de correspondencia com o modelo conceitual 
        (não serão aceitos modelos que não estejam em conformidade)
![modelo logico](https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/assets/130158423/be605034-fd7c-4711-becd-6e3a3f547e57)

### 7	MODELO FÍSICO<br>
        a) inclusão das instruções de criacão das estruturas DDL 
        (criação de tabelas, alterações, etc..) 
![captura 1](https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/assets/78965606/7136e165-03cb-4dff-b33c-987642916aa0)
![captura 2](https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/assets/78965606/c350941f-e01a-42e3-aca9-cc621ec2ab98)
 #### SELECT:
![select table](https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/assets/78965606/54d29592-6073-4cd9-904e-9f0cb4a8982f)
        
>## Marco de Entrega 03 em: (06/05/2019)<br>
        
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
#### 8.1 DETALHAMENTO DAS INFORMAÇÕES
        a) inclusão das instruções de inserção dos dados nas tabelas criadas pelo script de modelo físico 
        b) formato .SQL

>## Marco de Entrega 04 em: (07/05/2019)<br>

#### 8.2 INCLUSÃO DO SCRIPT PARA CRIAÇÃO DE TABELAS E INSERÇÃO DOS DADOS
        a) Junção dos scripts anteriores em um único script 
        (create para tabelas e estruturas de dados + dados a serem inseridos)
        b) Criar um novo banco de dados para testar a restauracao 
        (em caso de falha na restauração o grupo não pontuará neste quesito)
        c) formato .SQL

#### 8.3 INCLUSÃO DO SCRIPT PARA EXCLUSÃO DE TABELAS EXISTENTES, CRIAÇÃO DE TABELA NOVAS E INSERÇÃO DOS DADOS
        a) Junção dos scripts anteriores em um único script
        (Drop para exclusão de tabelas + create para tabelas e estruturas de dados + dados a serem inseridos)
        b) Criar um novo banco de dados para testar a restauracao 
        (em caso de falha na restauração o grupo não pontuará neste quesito)
        c) formato .SQL


#### 8.4 Principais fluxos de informação e principais tabelas do sistema
        a) Quais os principais fluxos de dados de informação no sistema em densenvolvimento (mínimo 3)
        b) Quais as tabelas que conterão mais dados no sistema em densenvolvimento (mínimo 3)
        c) informe quais as 5 principais tabelas do sistema em densenvolvimento.

>## Marco de Entrega 05 em: (13/05/2019)<br>

### 9	TABELAS E PRINCIPAIS CONSULTAS<br>
    OBS: Incluir para cada tópico as instruções SQL + imagens (print da tela) mostrando os resultados.<br>
#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>
#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>

>## Marco de Entrega 06 em: (14/05/2019)<br>

#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)
    a) Criar 5 consultas que envolvam os operadores lógicos AND, OR e Not
    b) Criar no mínimo 3 consultas com operadores aritméticos 
    c) Criar no mínimo 3 consultas com operação de renomear nomes de campos ou tabelas

#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12) <br>
    a) Criar outras 5 consultas que envolvam like ou ilike
    b) Criar uma consulta para cada tipo de função data apresentada.

#### 9.5	ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)<br>

>## Marco de Entrega 07 em: (20/05/2019)<br>


#### 9.6	CONSULTAS COM JUNÇÃO E ORDENAÇÃO (Mínimo 6)<br>
        a) Uma junção que envolva todas as tabelas possuindo no mínimo 3 registros no resultado
        b) Outras junções que o grupo considere como sendo as de principal importância para o trabalho

>## Marco de Entrega 08 em: (21/05/2019)<br>

#### 9.7	CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)<br>
#### 9.8	CONSULTAS COM LEFT E RIGHT JOIN (Mínimo 4)<br>
#### 9.9	CONSULTAS COM SELF JOIN E VIEW (Mínimo 6)<br>
        a) Uma junção que envolva Self Join
        b) Outras junções com views que o grupo considere como sendo de relevante importância para o trabalho

>## Marco de Entrega 09 em: (27/05/2019)<br>

#### 9.10	SUBCONSULTAS (Mínimo 3)<br>

>## Marco de Entrega 10 em: (28/05/2019)<br>

#### 9.11 Relatórios e Gráficos 
    a)análises e resultados provenientes do banco de dados

>## Marco de Entrega 11 em: (04/06/2019)<br>

### 10	ATUALIZAÇÃO DA DOCUMENTAÇÃO DOS SLIDES PARA APRESENTAÇAO FINAL (Mínimo 6 e Máximo 10)<br>
#### a) Pontos Chave do MINI-MUNDO
#### b) 5 principais tabelas/fluxos do sistema
#### c) Perguntas que podem ser respondidads com o sistema proposto
#### d) Modelo Conceitual
#### e) Modelo Lógico
#### f) Relatórios e Gráficos mais importantes para o sistema (mínimo 5) 
#### --> Tempo de apresentação 10 minutos




### 11 Backup completo do banco de dados postgres 
    a) deve ser realizado no formato "backup" 
        (Em Dump Options #1 Habilitar opções Don't Save Owner e Privilege)
    b) antes de postar o arquivo no git o mesmo deve ser testado/restaurado por outro grupo de alunos/dupla
    c) informar aqui o grupo de alunos/dupla que realizou o teste.

### 12	TUTORIAL COMPLETO DE PASSOS PARA RESTAURACAO DO BANCO E EXECUCAO DE PROCEDIMENTOS ENVOLVIDOS NO TRABALHO PARA OBTENÇÃO DOS RESULTADOS<br>
        a) Outros grupos deverão ser capazes de restaurar o banco 
        b) executar todas as consultas presentes no trabalho
        c) executar códigos que tenham sido construídos para o trabalho 
        d) realizar qualquer procedimento executado pelo grupo que desenvolveu o trabalho
        
### 13   DIFICULDADES ENCONTRADAS PELO GRUPO<br>
>## Marco de Entrega Final em: 11/06/2019 <br>
        
### 14  FORMATACAO NO GIT: https://help.github.com/articles/basic-writing-and-formatting-syntax/
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


