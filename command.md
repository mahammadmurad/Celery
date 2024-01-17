pip freeze > requirements.txt
docker-compose up -d --build

# Remove all docker
docker stop $(docker ps -aq) && docker rm $(docker ps -aq) && docker rmi $(docker images -aq)