# Microservices Observability with Distributed Logging, Health Monitoring, Resilient and Fault Tolerance with using Polly

### Arquitetura
<img width="724" alt="image" src="https://user-images.githubusercontent.com/39747516/178605052-8f7d0063-b69c-4022-8512-2bd824c92160.png">



- Curso:
https://medium.com/aspnetrun/microservices-observability-resilience-monitoring-on-net-a5dfbdbb0fbd

## Capítulos

## Microservice Observability com Logs Distribuídos

Nesta seção criamos um Elastic Stack que inclui Elasticsearh + Logstach + Kibana e pacote nuget SeriLog para microsserviços .net.

Usando a image do Kibana através do docker hub e alimentando o Kibana através do ELastic Stack.


## Microservice Resiliente com tolerância de falhas utilizando o Polly

Nesta seção criamos um Retry e Circuit Breaker.

## Microservices Health Monitoring usando o WatchDog

Nesta seção criamos o Health Check com métodos personalizados de verificação de integridade que incluem disponibilidades de banco de dados.
Adicionando Health Check para conectar o Redis e o RabbitMQ.

## Microservices Distribuído com OpenTelemetry usando Zipkin

Nesta seção será a implementação do OpenTelemetry com Zipkin.


### Instalação

1 - Iniciar o Docker 
1.1 - Configuração miníma do docker:
[x] **Memória: 4 GB**
[x] **Processador: 2**

2. No diretório raiz que inclui os arquivos **docker-compose.yml**, execute o comando abaixo:
``` csharp
docker-compose -f docker-compose.yml -f docker-compose.override.yml up -d
```

3. Aguarde o docker-compose finalizar a subida dos microservices.

### URL's
* **Catalog API -> http://host.docker.internal:8000/swagger/index.html**
* **Basket API -> http://host.docker.internal:8001/swagger/index.html**
* **Discount API -> http://host.docker.internal:8002/swagger/index.html**
* **Ordering API -> http://host.docker.internal:8004/swagger/index.html**
* **Shopping.Aggregator -> http://host.docker.internal:8005/swagger/index.html**
* **API Gateway -> http://host.docker.internal:8010/Catalog**
* **Rabbit Management Dashboard -> http://host.docker.internal:15672**   -- guest/guest
* **Portainer -> http://host.docker.internal:9000**   -- admin/admin1234
* **pgAdmin PostgreSQL -> http://host.docker.internal:5050**   -- admin@aspnetrun.com/admin1234
* **Elasticsearch -> http://host.docker.internal:9200** -- To Be Develop
* **Kibana -> http://host.docker.internal:5601** -- To Be Develop

* **Web Status -> http://host.docker.internal:8007** -- To Be Develop
* **Web UI -> http://host.docker.internal:8006**

1. http://host.docker.internal:8007 - Status da Web.
   
2. http://host.docker.internal:8006 Interface do Usuário.
Você pode usar o projeto da Web para **chamar microsserviços pelo API Gateway**. Ao **comprar a cesta**, você pode seguir o **registro da fila no painel do RabbitMQ**.




