# recipe-api
레시피 프로젝트 백엔드

## Database
MySQL: 8.0.32

### 로컬 DB 실행 방법
아래의 명령어를 쉘에 입력해 도커 컨테이너를 실행하여 사용한다.

``` shell
docker run -p 127.0.0.1:3306:3306 --name rcp_db -e MYSQL_HOST=localhost -e \
MYSQL_DATABASE=rcp_db -e MYSQL_ROOT_PASSWORD=password -d mysql:8.0.32
```

이후 `docker ps`를 입력하였을 때, 아래와 같이 실행 되었는지 확인한다.

```shell
docker ps
```
|CONTAINER ID|IMAGE|COMMAND|CREATED|STATUS|PORTS| NAMES  |
|---|---|---|---|---|---|--------|
|4ae8b4a49ec1|mysql:8.0.32|"docker-entrypoint.s…"|2 minutes ago|Up 2 minutes|127.0.0.1:3306->3306/tcp, 33060/tcp| rcp_db |
