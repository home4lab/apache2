# apache2

# how to enable HSTS apache2

a2enmod headers

and then add this line to your site configuration

    <VirtualHost *:443>
    Header always set Strict-Transport-Security "max-age=15552000; includeSubDomains"
    </VirtualHost>


# how to enable TLSv1.3

    vim /etc/apache2/mods-enable/ssl.conf

find SSLProtocol then add +TLSv1.3

    SSLProtocol all +TLSv1.3
