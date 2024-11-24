# React + TypeScript

## Running docker locally

```shell
docker build -t ev-test/frontend1 .
docker run --name ev-frontend1 -p 8080:80 -d  ev-test/frontend1

docker stop ev-frontend1
docker rm ev-test/frontend1
```
# AWS ECR Push
```shell
aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin ****************.dkr.ecr.us-east-1.amazonaws.com
docker build -t ev-test/frontend1 .
docker push ****************.dkr.ecr.us-east-1.amazonaws.com/ev-test/frontend1:v0.1
docker push ****************.dkr.ecr.us-east-1.amazonaws.com/ev-test/frontend1:latest

```