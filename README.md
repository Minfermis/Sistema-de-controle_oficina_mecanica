#  Sistema de controle e gerenciamento de execução de ordens de serviço em uma oficina mecânica 


<img aling="center" alt="MySQL" src="https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white" />
<img aling="center" alt="Dio" width="60px" src="https://hermes.digitalinnovation.one/assets/diome/logo.png" />
<img aling="center" alt="Github" width="90px" src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" />

### <br>Descrição do Desafio
Agora você irá criar um esquema conceitual do zero. A partir da narrativa fornecida você será capaz de criar todas as entidades, relacionamentos e atributos. Caso encontre algo que não foi definido na narrativa, utilize a sua compreensão do contexto e deixe uma descrição no README do seu github. para verificação.


### Objetivo:
Cria o esquema conceitual para o contexto de oficina com base na narrativa fornecida

### Narrativa:

* Clientes levam veículos à oficina mecânica para serem consertados ou para passarem por revisões  periódicas

* Cada veículo é designado a uma equipe de mecânicos que identifica os serviços a serem executados e preenche uma OS com data de entrega.

* A partir da OS, calcula-se o valor de cada serviço, consultando-se uma tabela de referência de mão-de-obra

* O valor de cada peça também irá compor a OSO cliente autoriza a execução dos serviços
A mesma equipe avalia e executa os serviços

* Os mecânicos possuem código, nome, endereço e especialidade

* Cada OS possui: n°, data de emissão, um valor, status e uma data para conclusão dos trabalhos. 

### Meu Projeto

Para criar o meu Sistema de controle e gerenciamento de execução de ordens de serviço em uma oficina mecânica usei o **MySQL**. 

A primeira Entidade criada foi **Cliente**, no meu caso decidi criar mais outra Entidade chamado **Veículo**, onde tenho certeza que facilitaria a coleta de dados em ambas entidades. Após o **Veículo**, temos duas Entidades com propósitos diferentes, onde a escolha fica para o cliente, que tipo de serviço ele quer para o seu carro. Assim temos as Entidades **Revisão** (Serve para fazer as revisões periódicas do carro) e **Concerto** (Com intuito de fazer a Manutenção de um problema ou avaria). 

Depois da escolha do cliente em qual tipo de serviço será escolhido. Temos a Entidade **Avaliação/Mecânico** Nesse setor será avaliado que tipo serviço será feito sobre a revisão ou o concerto, quais são as peças que irão necessitar. Onde em seguida o Mecânico responsável tera que cadastrar a **OS (Ordem de serviço)**. 

Passando pela **OS** os dados vão para **Almoxarifado** com o Código de peça. Onde volta com o valor para **OS**. Assim segue para Entidade **Serviços** que é responsavel para armazenar os tribustos: Mão de obra, Tipo de Serviço e o Valor de peças. 

Passando pelo o serviços nós temos agora temos a Entidade **Orçamento**, Onde pega todos os dados de serviço e mão de obra e cria o valor total a ser pago. COm isso eu jogo esses dados para Entidade **Execução/Mecânico** em M:N criando uuma nova Tabela chamada **Autorização Cliente**, como diz onome é onde fica a decisão do cliente em relizar ou não o serviço a ser feito no veículo. Com a autorização do cliente passamos para próxima Entidade, com o dever de finalizar o processo, e ainda coloquei um atributo (nulo) chamado "OBS" que serve para o Mecânico alertar qualquer problema no ocorrido durante o concerto ou algo que a avaliação não reparou. Assim terminamos o processo Sistema de controle e gerenciamento de execução de ordens de serviço em uma oficina mecânica.
