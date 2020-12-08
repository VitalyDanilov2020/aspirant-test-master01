## Steps to work with project ##
1. git clone https://github.com/VitalyDanilov2020/aspirant-test.git
2. cd aspirant-test
3. composer install
4. docker-compose up --build -d
5. docker exec -ti aspirant-test-master01_app_1  sh -c "php bin/console orm:schema-tool:create"
6. docker exec -ti aspirant-test-master01_app_1  sh -c "php bin/console orm:schema-tool:update -f"

Запуск сервера:
 docker exec -ti aspirant-test-master01_app_1  sh -c "cd public; php -S 0.0.0.0:8080"

Для получения данных с itunes, необходимо выполнить 
 docker exec -ti aspirant-test-master01_app_1  sh -c "php bin/console fetch:trailers"
