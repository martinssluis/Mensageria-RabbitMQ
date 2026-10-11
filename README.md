![thumbnail-Mensageria com RabbitMQ](https://user-images.githubusercontent.com/66698429/193290606-c7424fe9-d793-436f-8bd7-164c84980359.png)


# Microsserviços na prática: mensageria com RabbitMQ


Curso da formação Java e Microsserviços com Spring e RabbitMQ da Alura


## 🔨 Objetivos do projeto

<p>  O projeto que é utilizado no curso é o Alura Food, desenvolvido no curso Microsserviços na prática: implementando com Java e Spring. 
Aqui, vamos entender as desvantagens de utilizar comunização síncrona e iremos implementar a comunicação assíncrona através do RabbitMQ. </p>

<p>  Vamos conhecer os principais conceitos envolvidos em mensageria, como padrão Pub/Sub, queues, exchanges, dead letter queues, implementando-os nos nossos microsserviços. 

<p>  Para fechar, falaremos sobre alta disponibilidade, criando um cluster localmente para replicação de filas e mensagens.</p>



## ▶️ Como rodar

Para executar a aplicação `pagamentos`, é necessário subir antes os dois containers abaixo (requer o [Docker](https://www.docker.com/)):

```bash
# MySQL (usuário root / senha root)
docker run -d --name mysql-alura -p 3306:3306 -e MYSQL_ROOT_PASSWORD=root mysql:8

# RabbitMQ (usuário guest / senha guest) - painel em http://localhost:15672
docker run -d --name rabbit-alura -p 5672:5672 -p 15672:15672 rabbitmq:3-management
```

O banco `alurafood-pagamento` é criado automaticamente na primeira execução. Aguarde alguns segundos para o MySQL terminar de iniciar antes de rodar a aplicação.

> O servidor Eureka (porta 8081) é opcional: sem ele a aplicação apenas exibe avisos de registro.

## 🔗 Links

- [RabbitMQ](https://www.rabbitmq.com/) 
- [Formação Java e Microsserviços com Spring e RabbitMQ](https://cursos.alura.com.br/formacao-java-microsservicos)   
