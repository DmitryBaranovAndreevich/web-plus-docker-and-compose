# Докеризация приложения

HOST https://mesto.baranov.nomoredomains.work
IP: 158.160.17.181 

Frontend https://mesto.baranov.nomoredomains.work
Backend https://api.mesto.baranov.nomoredomains.work
-----------------------------
для деплоя изменений:
BASH :
pm2 deploy production setup
pm2 deploy production
-----------------------------
для выпуска сертификатов на ваш домен:
sudo docker compose run --rm  certbot certonly --webroot --webroot-path /var/www/certbot/ -d {ваш домен}