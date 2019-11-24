# Case de Avaliação Hackathon-TI - Qualidade

## O Desafio
Criar um processo para garantia da qualidade em empresa de software
### O problema
A empresa XY Sistemas desenvolve sistemas de gestão integrada (ERPs). Nos últimos 5 anos, as equipe de desenvolvimento passo de 4 para 45 pessoas e a carteira de clientes passou de 2 para 125 empresas. Atualmente, o ERP desenvolvido roda o banco de dados MSSQL Server e servidor de aplicações Apache Tomcat 8.5, onde estão hospedados tanto os webservices quanto os componentes da lógica do sistema. A camada de apresentação foi construída com HTML e JQuery. Ocorre que o número de falhas no software vem aumentando e está causando impacto e insatisfação junto aos clientes. Inclusive, alguns contratos já foram rescindidos. Sua missão é criar um processo de garantia da qualidade, com o objetivo de reverter a situação atual, buscando maior qualidade e, consequentemente, satisfação junto aos clientes da XY Sistemas.
### Os requisitos
Crie os processos e os documente, justificando a importância de cada atividade.
Determine as tecnologias, sistemas, softwares e quaisquer elementos que considere importantes para o processo de garantia da qualidade na XY Sistemas.
Determine os papéis a serem desempenhados para o processo que você está propondo.
Todas as suas decisões e escolhas devem ser justificadas na documentação do projeto
Todos os artefatos desenvolvidos devem ser disponibilizados para análise técnica


## A Solução Proposta

### Premissas
A XY sistemas desenvolve ERPs
A XY sistemas trabalha em formato Ágil (SCRUM)
Workflow de um desenvolvimento: TO DO > IN DEV > IN TEST > DONE

### Processos
#### Monitoria de Infra
Adicionar as seguintes monitorias de disponibilidade de infra:
Disponibilidade do servidor Apache Tomcat: pings a cada 10s no endereço da aplicação
Disponibilidade do servidor MSSQL Server: query simples submetida a cada 10s.


#### Etapas de Qualidade durante os desenvolvimentos
Assumindo a premissa de que os desenvolvedores da XY Sistemas trabalham em formato Ágil, metodologia SCRUM, temos duas sugestões para melhorar a qualidade do que é produzido:

* 1. Introduzir testes unitários da camada de aplicação HTML + JQuery utilizando o QUnit. Uma tarefa só pode ser passada do status “IN DEV” para o status “IN TEST” uma vez que o desenvolvedor tenha garantido a qualidade unitária dos desenvolvimentos feitos, garantindo a qualidade das regras de negócio. Idealmente, o time faria uso de TDD, metodologia de desenvolvimento orientada a testes (vide seção Métodos).
* 2. Introduzir testes integrados para os webservices e camada de aplicação. Esses testes serão conduzidos pela figura do QA (ver a seção Papeis) com base em requisitos e condições de aceite (ver seção Métodos). As ferramentas utilizadas para isso serão o Postman (para validação de webservices) e Planos de Teste (para a validação da camada de Aplicação); esses planos de teste são embasados na metodologia BDD (vide seção Métodos).
