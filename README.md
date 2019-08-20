# alpine-php7.2-fpm-nginx-wordpress

Nginx 1.17.3 e PHP-FPM 7.2.21

Nginx:
root /var/www/html;

Supervisord:
```console
nginx -g 'daemon off;' 
php-fpm -F
```
Run the permissions below on the project folder:
```console
find . -type d -print0|xargs -0 chmod 755; find . -type f -print0|xargs -0 chmod 644; chown nginx:nginx * -R
```
