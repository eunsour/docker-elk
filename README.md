# docker-efk
도커 컨테이너 환경에서 <b>Elasticsearch, Kibana</b> 와 Logstash 보다 Resource 를 적게 소모하는 <b>Filebeat</b> 를 사용하였습니다.<br><br>

2022.02.16 Kafka, Zookeeper, Metricbeat 추가

# Getting started 
```bash
git clone https://github.com/eunsour/docker-efk.git
docker-compose up -d --build
```
<br>

# How to check the filebeat log
1. 키바나 접속 -> Stack Management -> Index Patterns
  <img width="1294" alt="1" src="https://user-images.githubusercontent.com/50271311/153738149-9fcc4343-47fb-40cf-adcb-a097bc1850eb.png">

2. Create Index Patterns -> 인덱스 명 입력 (ex. filebeat-es-*.log)
  <img width="1289" alt="2" src="https://user-images.githubusercontent.com/50271311/153738153-a4ef479d-3e91-4e4e-9f4f-9ef5a5cfed92.png">
  
3. Time field 는 @timestamp 를 선택
  <img width="1292" alt="3" src="https://user-images.githubusercontent.com/50271311/153738158-74646f4f-7057-4daf-9d68-91a88eda3834.png">

4. Kibana -> Analytics -> Discover 에서 대시보드 확인
  <img width="1289" alt="4" src="https://user-images.githubusercontent.com/50271311/153738162-14983e00-dd23-461b-b4eb-b3b44b101654.png">
