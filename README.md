# Trabalhando Aplicações Serverless na Azure

Este projeto destaca as diferenças funcionais entre o Azure Functions, Logic Apps e WebJobs.

Definir um microserviço para:

  - Receber mensagens via Service Bus;
  - Processar mensagens via Azure Function e
  - Processar dados de um Azure SQL Database.

## Tecnologias Utilizadas

Pincipais tecnologias utilizadas:

  - Azure Logic Apps - Orquestrar o fluxo de dados;
  - Azure Functions - Processar mensagens e interagir com o Banco de Dados
  - Azure SQL Database - Persistir os dados processados
  - Azure Service Bus - Enviar e receber mensagens assíncronas
  - Azure Portal - Configuração e monitoramento dos recursos.

## Arquitetura Proposta

O fluxo de dados no microserviço é o seguinte:

  - Recepção da mensagem - A Logic App inicia o processo ao receber uma mensagem enviada para o Service Bus;
  - Processamento da mensagem - A Azure Function é acionada para processar a mensagem recebida;
  - Persistência de dados - Após o processamento, a Azure Function grava as informações no Azure SQL Database.

<img width="853" height="367" alt="image" src="https://github.com/user-attachments/assets/fe020f63-39dd-4574-ab6e-b8818f2393b5" />
