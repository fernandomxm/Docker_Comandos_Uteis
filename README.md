# Docker_Comandos_Uteis
Docker_Comandos_Uteis

docker login registry.cloud.tenable.com (username/password) <br> 
/home/user/.docker/config.json <br>
docker images <br>
docker ps <br>
docker system info | grep -E 'Username|Registry' <br>
docker image rm <br>

docker pull alpine:latest (Download image) <br>
docker tag alpine:latest registry.cloud.tenable.com/alpine:latest (Colocar TAG) <br>
docker push registry.cloud.tenable.com/alpine:latest (Upload image para Scan Tenable) <br>
<br>
**AWS ECR** <br>
aws ecr describe-repositories <br>
aws ecr describe-images --repository-name amazonlinux <br>
aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin account.dkr.ecr.us-east-1.amazonaws.com <br>
docker pull account.dkr.ecr.us-east-1.amazonaws.com/idm/licensing <br>

**DefectDojo Docker** <br>
sudo docker ps <br>
docker exec -it 05b3a3471f6f bash <br>
root@05b3a3471f6f:/# psql -U postgres <br>
sudo docker exec -it django-defectdojo-postgres-1 /bin/bash <br>
<br>
Backup Base SH <br>
/bin/docker exec django-defectdojo-postgres-1 /bin/bash -c "pg_dump -U defectdojo defectdojo" > /banco/dump_base_defectdojo.sql <br>
