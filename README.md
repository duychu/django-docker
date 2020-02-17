# django-docker
Dockerize the django with custom django project


docker-compose.exe -f .\docker-compose.prod.yml down -v
docker-compose.exe -f .\docker-compose.prod.yml build
docker-compose.exe -f .\docker-compose.prod.yml up -d

docker-compose.exe -f .\docker-compose.prod.yml exec web python manage.py migrate --noinput
