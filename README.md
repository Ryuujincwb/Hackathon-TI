# Case de Avalia��o Hackathon-TI - Qualidade

## O Desafio
Criar um processo para garantia da qualidade em empresa de software
### O problema
A empresa XY Sistemas desenvolve sistemas de gest�o integrada (ERPs). Nos �ltimos 5 anos, as equipe de desenvolvimento passo de 4 para 45 pessoas e a carteira de clientes passou de 2 para 125 empresas. Atualmente, o ERP desenvolvido roda o banco de dados MSSQL Server e servidor de aplica��es Apache Tomcat 8.5, onde est�o hospedados tanto os webservices quanto os componentes da l�gica do sistema. A camada de apresenta��o foi constru�da com HTML e JQuery. Ocorre que o n�mero de falhas no software vem aumentando e est� causando impacto e insatisfa��o junto aos clientes. Inclusive, alguns contratos j� foram rescindidos. Sua miss�o � criar um processo de garantia da qualidade, com o objetivo de reverter a situa��o atual, buscando maior qualidade e, consequentemente, satisfa��o junto aos clientes da XY Sistemas.
### Os requisitos
1. Crie os processos e os documente, justificando a import�ncia de cada atividade.
2. Determine as tecnologias, sistemas, softwares e quaisquer elementos que considere importantes para o processo de garantia da qualidade na XY Sistemas.
3. Determine os pap�is a serem desempenhados para o processo que voc� est� propondo.
4. Todas as suas decis�es e escolhas devem ser justificadas na documenta��o do projeto
5. Todos os artefatos desenvolvidos devem ser disponibilizados para an�lise t�cnica
## A Solu��o Proposta

### Premissas
1. A XY sistemas desenvolve ERPs em formato �gil, utilizando o Scrum.
2. O quadro de desenvolvedores ser� dividido em times (_squads_) de, no m�ximo 9 pessoas.
3. A XY Sistemas contratar� Scrums Masters e Product Owners para compor esses _squads_.
4. A XY Sistemas contratar� ao menos um profissional de Quality Assurance para cada uma das _squads_.

### Pap�is:
* Agile Master: pessoa respons�vel por atuar como facilitador do Scrum, removendo quaisquer obst�culos que sejam levantados pela equipe durante as dailies.
* Product Owner: pessoa respons�vel por definir os itens que ser�o tratados pelo time e os prioriza nas reuni�es de planejamento (Planning)
* Desenvolvedores: pessoas respons�veis por executar o desenvolvimento, resolver problemas e garantir a entrega;
* Testers (QAs): pessoa respons�vel por garantir que os requisitos foram atendidos e que o padr�o de qualidade do que foi desenvolvido est� dentro do esperado.

### Pontos de Melhoria
#### Monitoria de Infra
Adicionar as seguintes monitorias de disponibilidade de infraestrutura:
*Disponibilidade do servidor Apache Tomcat: pings a cada 10s no endere�o da aplica��o
*Disponibilidade do servidor MSSQL Server: query simples submetida a cada 10s.
*Estabelecer par�metros de qualidade para essas monitorias, como percentual de tempo dispon�vel por tempo absoluto, por exemplo, que indicar� a consist�ncia dos servi�os prestados.

#### Etapas de Qualidade durante os desenvolvimentos
Assumindo a premissa de que os desenvolvedores da XY Sistemas trabalham em formato �gil, metodologia SCRUM, temos duas sugest�es para melhorar a qualidade do que � produzido:

1. Introduzir testes unit�rios da camada de aplica��o HTML + JQuery utilizando o QUnit. 
Uma tarefa s� pode ser passada do status �In Dev� para o status �In Test� uma vez que o desenvolvedor tenha garantido a qualidade unit�ria dos desenvolvimentos feitos, garantindo a qualidade das regras de neg�cio. Idealmente, o time faria uso de TDD, metodologia de desenvolvimento orientada a testes (vide se��o M�todos).
2. Introduzir testes integrados para os webservices e camada de aplica��o. Esses testes ser�o conduzidos pela figura do QA (ver a se��o Papeis) com base em requisitos e condi��es de aceite (ver se��o M�todos). As ferramentas utilizadas para isso ser�o o Postman (para valida��o de webservices) e Planos de Teste (para a valida��o da camada de Aplica��o); esses planos de teste s�o embasados na metodologia BDD (vide se��o M�todos).

### Ferramentas
1. *Google Docs*: por sua efic�cia em fazer altera��es simult�neas em uma �nica plataforma, dessa forma melhorando a comunica��o com todos os times. Ser� utilizado para documentar os desenvolvimentos (requisitos, regras de neg�cio, crit�rios de aceite e solicita��es de altera��es) em documentos padronizados.
  1. Documento de Solicita��o de Mudan�a: ser� gerada pela �rea demandante (ou cliente) especificando a altera��o que julga necess�ria para o sistema ou m�dulo em quest�o, bem como os crit�rios de aceite.
  2. Documentos de Aceite: ser�o assinados pelas �reas demandantes (ou clientes), reconhecendo que a _feature_ solicitada est� entregue como esperado, atendendo aos requisitos e respeitando os crit�rios de aceite.

2. *Postman*: ferramenta que permite testes automatizados de APIs e Webservices. A automatiza��o de testes b�sicos de webservices garante uma maior uniformidade nos testes (e nos desenvolvimentos) e maior qualidade sem aumento significativo do tempo de teste.

3. *QUnit*: automa��o de testes unit�rios de c�digo desenvolvido em JQuery. Permite testes de regras de neg�cio.

4. *JIRA*: sistema de controle de tickets (bugs ou features) que servir� como estrutura de controle de trabalho em andamento

###  M�todo
Utilizaremos dois m�todos de trabalho complementares: o PDCA, como embasamento te�rico de melhoria cont�nua do ERP da XY Sistemas, bem como do melhoramento cont�nuo do trabalho das equipes de desenvolvimento. Para praticarmos essa melhoria cont�nua, utilizaremos o m�todo Scrum de desenvolvimento, separando as demandas em _sprints_ (de 2 a 4 semanas), que cont�m reuni�es que atendem o nosso embasamento te�rico: a reuni�o de _planning_ nos permite entender o que deve ser feito, as reuni�es di�rias (_dailies_) para acompanhamento das atividades dentro da _sprint_ e, ao final, as reuni�es de checagem: _review_ e _retrospective_. Essas �ltimas servem para a avaliar a qualidade final do produto entregue e tamb�m a qualidade dos processos internos do time de desenvolvimento.

Para pautar os desenvolvimentos e os testes, utilizaremos dois tipos de _framework_: TDD e BDD.

O TDD (_Test Driven Development_) ser� utilizado para garantir qualidade no n�vel unit�rio e ser� responsabilidade do desenvolvedor. 

O BDD (_Business Driven Development_) ser� utilizado para garantir qualidade em n�vel integrado e sua execu��o ser� de responsabilidade do QA.

## Processos
Todos os desenvolvimentos devem ser atendido em Sprints (de 2 a 4 semanas).
Durante uma sprint um desenvolvimento passa pelos seguintes status:

![transicoes](./transicoes.jpeg)

O que cada status representa:
TO DO: tarefa est� aguardando ser iniciada
In Dev: tarefa est� em desenvolvimento
In Test: tarefa foi desenvolvida e est� em teste
Waiting Homolog: a tarefa foi aprovada nos testes do time e est� aguardando a aprova��o do cliente
Done: tarefa conclu�da.

Caso a tarefa seja reprovada nas etapas de teste ou de homologa��o, esta ser� devolvida para o desenvolvedor e o status volta a ser �In Dev�.

