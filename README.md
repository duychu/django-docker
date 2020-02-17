# django-docker
Dockerize the django with custom django project


docker-compose -f .\docker-compose.prod.yml down -v
docker-compose -f .\docker-compose.prod.yml build
docker-compose -f .\docker-compose.prod.yml up -d

docker-compose -f .\docker-compose.prod.yml exec web python manage.py migrate --noinput
docker-compose -f .\docker-compose.prod.yml exec web python manage.py createsuperuser
docker-compose -f .\docker-compose.prod.yml exec web python manage.py collectstatic --no-input --clear
