# 꼬리별 [KKoribyeol]
## 데브옵스 (Zinnia)
![Zinnia](https://user-images.githubusercontent.com/48639421/113505991-0575f800-957d-11eb-84db-47cc3ad5dd78.png)

푸시 서비스가 필요해서 사용해본 NHN Cloud의 TOAST 푸시 서비스,  
TOAST 푸시 서비스를 사용하면서 느꼈던 불편한 점을 개선하여  
모두가 사용할 수 있는 푸시 서비스를 만드는 것이 목표인 프로젝트!

## Feature
- Docker Swarm Mode를 통해 스택을 만들고 Docker-Compose를 이용해 kkoribyeol-compose.yml 파일을 토대로 서비스 실행
- Rolling Update를 통해 20초마다 Docker Hub를 확인하여 CI-CD 환경 구성
- Apache 대신 Nginx를 이용하여 효율적인 리소스 사용 환경 구성 (서비스가 하나라 별 효과는 없음)
- 아래 명령으로 Swarmpit 이미지 구동
```
sudo docker run -it --rm \
  --name swarmpit-installer \
  --volume /var/run/docker.sock:/var/run/docker.sock \
  swarmpit/install:1.9
```

## To do list
- 엘라스틱 아이피 설정
- 도메인과 ec2 아이피 매칭
- S3를 통한 
