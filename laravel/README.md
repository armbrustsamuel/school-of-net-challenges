# Project Code Education - Laravel 



Generate image
```
docker build -t armbrustsamuel/laravel .
```

Run image
```
docker run -d --name laravel -p 8000:8000 armbrustsamuel/laravel
```

Install bash inside the container
```
docker exec -it laravel apk add bash
```

Enter in the container using bash 
```
docker exec -it laravel bash
```

Run docker-compose and release terminal
```
docker-compose up -d 
```

Delete all running containers 
```
docker rm $(docker ps -aq) -f
```

Generate again the build 
```
docker-compose up -d 
```

Start laravel 
```
php artisan serve --host=0.0.0.0
```

Migrate db using mysql
```
bash-4.4# php artisan migrate

# and you should see this result:
Migration table created successfully.
Migrating: 2014_10_12_000000_create_users_table
Migrated:  2014_10_12_000000_create_users_table (0.09 seconds)
Migrating: 2019_08_19_000000_create_failed_jobs_table
Migrated:  2019_08_19_000000_create_failed_jobs_table (0.05 seconds)
```