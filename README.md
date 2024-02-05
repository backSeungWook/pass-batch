# Spring Batch
```https://github.com/kjs92980/pass-batch```

## Job

## Step

## Tasklet



## 어노테이션
### EnableBatchProcessing





# Docker

## docker-compose.yml
```yaml
version: "3.8"
services:
  mysql:
    container_name: mysql_local
    image: mysql:8.0.30
    volumes:
      - ./db/conf.d:/etc/mysql/conf.d
      - ./db/initdb.d:/docker-entrypoint-initdb.d
    ports:
      - "3306:3306"
    environment:
      - MYSQL_DATABASE=pass_local
      - MYSQL_USER=pass_local_user
      - MYSQL_PASSWORD=passlocal123
      - MYSQL_ROOT_PASSWORD=passlocal123
      - TZ=Asia/Seoul
```

## Makefile
```makefile
db-up:
	docker-compose up -d --force-recreate

db-down:
	docker-compose down -v
```
