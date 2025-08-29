# Trabalhando Aplicações Serverless na Azure

## Descrição 📜

Este projeto demonstra como trabalhar com **aplicações serverless** na **Azure**, utilizando serviços como **Logic Apps**, **Azure Functions**, **Azure SQL Database** e **Azure Service Bus**. O objetivo é criar um **microserviço** que:

1. Recebe uma mensagem via **Service Bus**.
2. Processa essa mensagem com uma **Azure Function**.
3. Persiste os dados processados em um **Azure SQL Database**.

Esse fluxo de trabalho totalmente serverless permite escalar facilmente, sem se preocupar com a infraestrutura subjacente.

---

## Tecnologias Utilizadas 🛠️

Aqui estão as tecnologias principais utilizadas neste projeto:

- **Azure Logic Apps** 🌐 - Para orquestrar o fluxo de dados.
- **Azure Functions** 🔧 - Para processar mensagens e interagir com o banco de dados.
- **Azure SQL Database** 💾 - Para persistir os dados processados.
- **Azure Service Bus** 📨 - Para enviar e receber mensagens assíncronas.
- **Azure Portal** 💻 - Para configuração e monitoramento de todos os recursos.

---

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

## Reflexão 🧠
A utilização de **Azure Functions** e **Logic Apps** oferece muitos benefícios:

- **Foco no código**: Os desenvolvedores podem concentrar-se apenas na lógica de negócios.
- **Mensageria assíncrona**: O uso do **Azure Service Bus** ajuda a desacoplar os componentes do sistema, permitindo escalabilidade e flexibilidade.
- **Resiliência e escalabilidade**: A solução é resiliente a falhas e **altamente escalável**, ideal para sistemas distribuídos e baseados em eventos.

Com esses recursos, você pode construir soluções mais ágeis, rápidas e fáceis de manter, aproveitando ao máximo o potencial da **nuvem** e da **arquitetura serverless**.

---

