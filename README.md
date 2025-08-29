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

## Arquitetura do Sistema 📊

O fluxo de dados no microserviço é o seguinte:

1. **Recepção da mensagem**: A **Logic App** inicia o processo ao receber uma mensagem enviada para o **Service Bus**.
2. **Processamento da mensagem**: A **Azure Function** é acionada para processar a mensagem recebida do **Service Bus**.
3. **Persistência de dados**: Após o processamento, a **Azure Function** grava as informações no **Azure SQL Database**.

---

## Como Funciona 🔄

### 1. **Azure Logic App**

A **Logic App** é responsável por orquestrar o fluxo entre os diferentes componentes. Ela será configurada para escutar um **Azure Service Bus** para novas mensagens.

### 2. **Azure Function**

A **Azure Function** é uma função serverless que será disparada sempre que uma nova mensagem chegar ao **Service Bus**. Ela irá processar a mensagem e persistir os dados no **Azure SQL Database**.

### 3. Configurar a Logic App
Crie a **Logic App** no **Azure Portal**. Configure um acionador para a **Logic App** que irá escutar o **Azure Service Bus** e chamar a **Azure Function** quando uma nova mensagem for recebida.

---

### 4. Testar a Aplicação 🚀
Envie uma mensagem para a **fila do Service Bus** e verifique se ela foi processada corretamente e registrada no banco de dados.

1. Acesse o **Azure Portal**.
2. Envie uma mensagem para a fila configurada no **Service Bus**.
3. Monitore a execução da **Azure Function** para garantir que ela está processando a mensagem.
4. Verifique se a mensagem foi gravada corretamente no **Azure SQL Database**.

---

## Conclusão ✅
Este projeto demonstrou como criar um **microserviço serverless** utilizando os seguintes serviços da **Azure**:

- **Azure Logic Apps** 🌐
- **Azure Functions** 🔧
- **Azure SQL Database** 💾
- **Azure Service Bus** 📨

Utilizando **serviços totalmente gerenciados**, conseguimos criar uma solução **escalável** e **fácil de manter**. Com a ajuda de **Azure Functions** e **Logic Apps**, o desenvolvedor pode se concentrar no código e na lógica de negócios, sem a preocupação com a infraestrutura subjacente.

---



