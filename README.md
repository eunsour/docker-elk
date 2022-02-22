# Integrate Filebeat, Kafka, Logstash, Elasticsearch And Kibana
In this integration <b>filebeat</b> will install in all servers where your application is deployed and <b>filebeat</b> will read and ship latest logs changes from these servers to <b>Kafka</b> topic as configured for this application.

<b>Logstash</b> will subscribe log lines from <b>kafka</b> topic and perform parsing on these lines make relevant changes, formatting, exclude and include fields then send this processed data to <b>Elasticsearch</b> Indexes as centralize location from different servers.

<b>Kibana</b> is linked with <b>Elasticsearch</b> indexes which will help to do analysis by search, charts and dashboards .
<br><br>

# Pipeline
![git_imame](https://user-images.githubusercontent.com/50271311/155036578-c1f2517f-cf4b-4eb0-a9fe-4d25d7031e70.png)
<br><br>


# Getting started 
```bash
git clone https://github.com/eunsour/docker-efk.git
docker-compose up -d --build
```
<br>

# How to check the filebeat log
1. Access <b>Kibana</b> &rightarrow; <b>Stack Management</b> &rightarrow; <b>Index Patterns</b>
    <img width="800" alt="1" src="https://user-images.githubusercontent.com/50271311/153738149-9fcc4343-47fb-40cf-adcb-a097bc1850eb.png">

2. Create <b>Index Pattern</b> &rightarrow; Input <b>index pattern name</b> (ex. filebeat-es-*.log)
    <img width="800" alt="2" src="https://user-images.githubusercontent.com/50271311/153738153-a4ef479d-3e91-4e4e-9f4f-9ef5a5cfed92.png">
  
3. Select <b>@timestamp</b>  
    <img width="800" alt="3" src="https://user-images.githubusercontent.com/50271311/153738158-74646f4f-7057-4daf-9d68-91a88eda3834.png">

4. <b>Kibana</b> &rightarrow; <b>Analytics</b> &rightarrow; Check your dashboard in <b>Discover</b>
    <img width="800" alt="4" src="https://user-images.githubusercontent.com/50271311/153738162-14983e00-dd23-461b-b4eb-b3b44b101654.png">
