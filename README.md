# Alomundo Java WEB com Docker e jib-maven-plugin

Aplicação **Alomundo WEB** desenvolvida em **Java** e executada em um container Docker através do jib-maven-plugin.

## Sobre o projeto

 - O projeto foi desenvolvido utilizando o **NetBeans**.
 - O nome do projeto deve ser **alomundow_java_jib_docker**.
 - Utiliza o **Java 8**.
 - Utiliza o **Apache Tomcat 9** como servidor de aplicações Web.
 - Utiliza o **Apache Maven** para automatizar o processo de construção da aplicação.
 - Utiliza o **jib-maven-plugin** para criar as imagens do Docker. O que **dispensa o Dockerfile ou compose.yml**.
 - A aplicação é empacotada no formato **WAR (Web Application Archive)**.
 - Utiliza o **Docker** para criar uma imagem e executar a aplicação em um container.

## Comandos Docker
 - Utilizar o terminal do Windows Powershel em modo administrador.

### Login no docker
 - ```docker login```

### Construir a aplicação usando o plugin
 - ```mvn compile jib:dockerBuild```

### Executar a aplicação
 - ```docker run -d -p 8080:8080 osmarbraz/alomundow_java_jib_docker:0.0.1```

### Abra o navegador em:
 - http://localhost:8080/
 ou
- http://localhost:8080/?nome=Java
 ou
 - http://localhost:8080/servlet/AloMundo
 ou
- http://localhost:8080/servlet/AloMundo?nome=Java

### Remover imagem
 - ```docker rmi alomundow_java_jib_docker```

## Docker Hub
 - https://hub.docker.com/r/osmarbraz/alomundow_java_jib_docker