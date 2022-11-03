# Docker Laravel Implementation Method-2

In this project, here i implement laravel with docker (Method-2) in the local environment using the LAMP stack that includes: Apache, MySQL, PHP, and phpMyAdmin.
 
## How to Install and Run the Project

Step-1. ```git clone https://github.com/mamunurrashid1010/docker-laravel-implementation-method-2.git```<br>
Step-2. Go to project root directory<br>
Step-3. Copy ```.env.example``` to ```.env``` <br>
Step-4. Open ``` .env ``` file and update
```
DB_CONNECTION=mysql
DB_HOST=db
DB_PORT=3306
DB_DATABASE=laravelApp_db
DB_USERNAME=root
DB_PASSWORD=
```
Step-5. ```docker compose up -d``` <br>
You can see the project on ```http://127.0.0.1:8080``` <br>
Open ```phpMyAdmin``` on ```127.0.0.1:3400```

## How to run Laravel Commands
1. Go to project root directory <br>
2. Run command ```docker ps``` <br>
3. Copy project container id then run command```docker exec -it {container id} bash``` <br>
4. Now you can run any laravel command here. <br>
Example
```
php artisan migrate
```
To exit container run ```exit``` <br>
Stop and remove containers, networks, images, and volumes run ```docker compose down```

## How to run node command
1. Go to project directory <br>
2. run command 
```
docker-compose run --rm npm install
docker-compose run --rm npm run dev
docker-compose run --rm npm run production
``` 
