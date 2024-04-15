<h1>EAD-NOTIFICATION</h1>
<h2>Microserviço de Notificação - Ensino a Distância </h2>
<br>

<p>Microserviço responsável por enviar notificações para o Usuário assim que ele se matricular-se, finalizar, enviar tarefa ou remover um Curso. Publicando um Consumidor no RabbitMq relacionado com o EAD-COURSE.</p>

<h3>Arquitetura</h3>
<p>O Microserviço de Notificações faz parte de uma complexa arquitetura onde realiza comunicação entre Cursos e AuthUser, além de conter implenmentações de Segurança como Service Registry e API-GATEWAY.</p>
<img height="300em" src="https://github.com/adrianmuniz/ead_notification/blob/main/arquitetura_notification.png"/>

<h3>Funcionalidades</h3>
<ul>
    <li>Salvamento e Visualizações de todas as notificações com ID de Usuário e atualização se necessário</li>
    <li>Esse microserviço publica um CONSUMIDOR no RabbitMQ que é acionado ao utilizar o Curso, enviando automaticamente a notificação.</li>
    <li>Comunicação Sincrona e Assincrona Orientada a Eventos com RabbitMq</li>
    <li>Base de Dados Postgress</li>
    <li>Implementação de API-GATEWAY</li>
    <li>Configurações Externalizadas no microserviço CONFIG-SERVER</li>
    <li>Authenticação com JWT para permissões de acesso</li>
    <li>Implementa Service Registry (Spring Cloud Netflix Eureka), monitora e gerencia instancias</li>
</ul>

<h3>Como Subir?</h3>
<p>O EAD-NOTIFICATION foi implementado na Nuvem pelo HEROKU no site ead-notification. Porém é possivel rodar no ambiente DEV clonando o projeto, alterando o profile para "dev" no arquivo "application.yaml" e agora basta rodar a aplicação e enviar requisições.</p>
