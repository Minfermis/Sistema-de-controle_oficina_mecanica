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

Para criar o meu sistema de controle e gerenciamento de execução de ordens de serviço em uma oficina mecânica, utilizei o banco de dados **MySQL**. A primeira entidade criada foi **Cliente**. Além disso, decida criar uma outra entidade chamada **Veículo**, que facilite a coleta de dados relacionados a ambas as entidades.

Após a entidade **Veículo**, temos duas entidades com propósitos diferentes, onde a escolha fica a carga do cliente em relação ao tipo de serviço que deseja para o seu carro. Assim, temos como entidades **Revisão** (para realizar revisões periódicas do veículo) e **Concerto** (para realizar manutenção em caso de problemas ou avarias).

Após a escolha do cliente em relação ao tipo de serviço, temos a entidade **Avaliação/Mecânico**. Nessa etapa, são avaliados quais serviços serão realizados na revisão ou no concerto, bem como as peças necessárias. O mecânico responsável deve se cadastrar a **Ordem de Serviço (OS)** nesse momento.

Após a criação da OS, os dados são enviados para a entidade **Almoxarifado**, juntamente com o código das peças necessárias. Em seguida, o valor é atualizado no sistema operacional. Os dados prosseguem para a entidade **Serviços**, responsável por armazenar atributos como mão de obra, tipo de serviço e valor das peças.

Em seguida, passamos para a entidade **Orçamento**. Essa entidade coleta todos os dados de serviço e mão de obra para criar o valor total a ser pago. Em seguida, esses dados são enviados para a entidade **Execução/Mecânico** em uma relação muitos-para-muitos, criando uma nova tabela chamada **Autorização Cliente**. Nessa tabela, é registrada a decisão do cliente em relação à conclusão ou não do serviço no veículo.

Com a autorização do cliente, avançamos para a próxima entidade, responsável por finalizar o processo. Também adicionei um atributo (nulo) chamado "OBS" na entidade **Execução/Mecânico**, que permite ao mecânico alertar sobre qualquer problema ocorrido durante o conserto ou algo que não tenha sido identificado na avaliação. Dessa forma, o processo de controle e gerenciamento de execução de ordens de serviço em uma oficina mecânica é concluído.
