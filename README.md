# apache2

how to enable HSTS apache2

a2enmod headers

# and then add this line to your site configuration

<VirtualHost *:443>

Header always set Strict-Transport-Security "max-age=15552000; includeSubDomains"

</VirtualHost>
