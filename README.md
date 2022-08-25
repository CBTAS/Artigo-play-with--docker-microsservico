Docker: Utilização prática no cenário de Microsserviços

O uso da virtualização em containers permite o isolamento das aplicações e a arquitetura garante uma distribuição dos recursos e agiliza a implementação de novos conteiners evitando conflitos ou paradas devido falha em algum node.
 
Iremos utilizar o play-with-docker.com para simular um ambiente que contém aplicações replicadas em um cluster swarm, contendo três instâncias (node1, node2 e node3) para subir aplicações que irão se comunicar com banco de dados mysql.
Como essa opção é gratuita e facilitada pela plataforma da DOCKER, caso tenha dúvidas de como iniciar e configurar um servidor recomendo entrar nesse artigo: 
https://www.linkedin.com/pulse/como-utilizar-play-with-dockercom-para-estudar-docker-vitor-carra/?originalSubdomain=pt

Escopo do micro-serviço:

Aplicações:
- No node1, teremos as aplicações rodando:
- Bando de dados: mysql;
- Servidor: nginx;
- Porxy-app;
- Replicas do servidor web.
- No node2 e node3, teremos apenas as replicações do servidor web.

Construção do CLUSTER DOCKER SWARM:
- Teremos o node1 e node2 configuradas como “manager”;
- O node3 será configurada como “worker.
