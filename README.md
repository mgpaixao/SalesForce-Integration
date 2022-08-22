# SalesForce-Integration

O propósito desse projeto é diminuir as tarefas repetitivas e que estavam espalhadas por diversas plataformas. Centralizar as informações dos candidatos e dos alunos em um só lugar, no Salesforce.

Na primeira parte do projeto, integrei o site e o sistema de testes técnicos (CodeSignal) com o Salesforce. 

Veja abaixo o fluxo das informações.


![SalesForce Integrations@2x](https://user-images.githubusercontent.com/63682265/185831033-af4d6042-011b-4807-8302-f2d75c60b646.png)


# CodeSignal

CodeSignal é uma plataforma de gerenciamento de testes técnicos usados no processo seletivo dos novos candidatos da empresa. O sistema da Codesignal disponibiliza um Webhook onde ela entrega informações sobre o usuário e os resultados dos testes com todas as informações que são cruciais pra gente. 

# Webflow - Site da Empresa

No Webflow estava hospedado o site qu coma landing page que desenvolvi para que os candidatos fizessem o cadastro. Então integrei o site da empresa que mandava todas as informações coletadas no formulário de cadastro para o RDStation e para o LogicApps que manda pro Salesforce. Eu tomei a decisão de não excluir o fluxo de persistencia de dados das plataformas originais, pois caso algo desse errado, sempre teriamos o backup dos dados nas plataformas originais.

# RdStation

O RDStation é o sistema que gerenciava os emails e campanhas que realizavamos, alí estava todos os cadastros e templates de email marketing. Dentro do RDStation eu desenvolvi um webhook para que enviasse os dados cadastrais de cada novo cadastro para o LogicApps que manda para o Salesforce.

# LogicApps

O LogicApps é um IPaas (Integration Plataform as a Service) que escolhi para fazer a mediação entre todas as integrações. pois ali tem centenas de conectores nativos que facilitava o desenvolvimento quase que NO Code dessas integrações, e me dá visibilidade do que está acontecendo, possibilidade de monitorar cada trigger, extrair métricas, ver onde está o problema, gargalos e etc. Além disso, eu escolhi tratar os dados no LogicApps, antes de inseri-los no Salesforce. Veja abaixo um dos fluxos do logic apps. 

![Animação](https://user-images.githubusercontent.com/63682265/185838658-5cc2411d-7f6d-4c83-9ba5-b5bd679b137b.gif)

