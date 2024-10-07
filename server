<VirtualHost *:80>
    ServerName YOUR_EC2_PUBLIC_DNS

    WSGIDaemonProcess flaskapp threads=5
    WSGIScriptAlias / /var/www/html/flaskapp.wsgi

    <Directory /var/www/html/flaskapp>
        Require all granted
    </Directory>

    Alias /static /var/www/html/flaskapp/static
    <Directory /var/www/html/flaskapp/static/>
        Require all granted
    </Directory>

    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
