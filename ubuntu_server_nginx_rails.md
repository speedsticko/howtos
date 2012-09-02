hostname
lsb_release -a


touch /etc/nginx/sites-available/kwanacademy.org
touch /etc/nginx/sites-available/checkee.com

---------------------------------------------------------------
server {
    listen   80;
    server_name www.example.com example.com;
    access_log /srv/www/example.com/logs/access.log;
    error_log /srv/www/example.com/logs/error.log;

    location / {
        root   /srv/www/example.com/public_html;
        index  index.html index.htm;
    }
}
--------------------------------------------------------------

mkdir -p /srv/www/kwanacademy.org/public_html
mkdir -p /srv/www/kwanacademy.org/logs

ln -s /etc/nginx/sites-available/example.com /etc/nginx/sites-enabled
/etc/init.d/nginx restart

