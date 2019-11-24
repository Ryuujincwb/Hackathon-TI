# Case de Avalia��o Hackathon-TI - Qualidade

## O Desafio
Criar um processo para garantia da qualidade em empresa de software
### O problema
A empresa XY Sistemas desenvolve sistemas de gest�o integrada (ERPs). Nos �ltimos 5 anos, as equipe de desenvolvimento passo de 4 para 45 pessoas e a carteira de clientes passou de 2 para 125 empresas. Atualmente, o ERP desenvolvido roda o banco de dados MSSQL Server e servidor de aplica��es Apache Tomcat 8.5, onde est�o hospedados tanto os webservices quanto os componentes da l�gica do sistema. A camada de apresenta��o foi constru�da com HTML e JQuery. Ocorre que o n�mero de falhas no software vem aumentando e est� causando impacto e insatisfa��o junto aos clientes. Inclusive, alguns contratos j� foram rescindidos. Sua miss�o � criar um processo de garantia da qualidade, com o objetivo de reverter a situa��o atual, buscando maior qualidade e, consequentemente, satisfa��o junto aos clientes da XY Sistemas.
### Os requisitos
Crie os processos e os documente, justificando a import�ncia de cada atividade.
Determine as tecnologias, sistemas, softwares e quaisquer elementos que considere importantes para o processo de garantia da qualidade na XY Sistemas.
Determine os pap�is a serem desempenhados para o processo que voc� est� propondo.
Todas as suas decis�es e escolhas devem ser justificadas na documenta��o do projeto
Todos os artefatos desenvolvidos devem ser disponibilizados para an�lise t�cnica


## A Solu��o Proposta

### Premissas
A XY sistemas desenvolve ERPs
A XY sistemas trabalha em formato �gil (SCRUM)
Workflow de um desenvolvimento: TO DO > IN DEV > IN TEST > DONE

### Processos
#### Monitoria de Infra
Adicionar as seguintes monitorias de disponibilidade de infra:
Disponibilidade do servidor Apache Tomcat: pings a cada 10s no endere�o da aplica��o
Disponibilidade do servidor MSSQL Server: query simples submetida a cada 10s.


#### Etapas de Qualidade durante os desenvolvimentos
Assumindo a premissa de que os desenvolvedores da XY Sistemas trabalham em formato �gil, metodologia SCRUM, temos duas sugest�es para melhorar a qualidade do que � produzido:

* 1. Introduzir testes unit�rios da camada de aplica��o HTML + JQuery utilizando o QUnit. Uma tarefa s� pode ser passada do status �IN DEV� para o status �IN TEST� uma vez que o desenvolvedor tenha garantido a qualidade unit�ria dos desenvolvimentos feitos, garantindo a qualidade das regras de neg�cio. Idealmente, o time faria uso de TDD, metodologia de desenvolvimento orientada a testes (vide se��o M�todos).
* 2. Introduzir testes integrados para os webservices e camada de aplica��o. Esses testes ser�o conduzidos pela figura do QA (ver a se��o Papeis) com base em requisitos e condi��es de aceite (ver se��o M�todos). As ferramentas utilizadas para isso ser�o o Postman (para valida��o de webservices) e Planos de Teste (para a valida��o da camada de Aplica��o); esses planos de teste s�o embasados na metodologia BDD (vide se��o M�todos).
