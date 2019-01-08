# Docker-Symfony starter framework

To deploy this project enter in terminal:
```
git clone https://github.com/amb-it/docker-symfony.git && cd docker-symfony/docker && docker-compose up
```

after all Docker containers are up install Symfony dependecies with Composer:
```
cd ../src && composer install
```

or if you do not have local Composer, enter to php-fpm container :
```
docker exec -it php_fpm_container sh
```
and inside it enter: ``` composer install ```

After that you can check project by visiting in your browser http://localhost