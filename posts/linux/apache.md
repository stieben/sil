# Apache

_#debian_ _#web-server_

This is for Apache 2.4.
Don't use previous versions.

## Document root

The standard path for the files that are to be served:

```
/var/www/html/
```

### Permissions

The `html` directory and its subdirectories should be owned by `www-data:www-data` which is the user Apache is operating with:

```
sudo chown www-data:www-data -R /var/www/html/
```

Add yourself to the `www-data` group to be able to interact with the document root:

```
sudo adduser $USER www-data
```

And finally set the permissions:

```
sudo chmod 760 -R /var/www/html/ # exclude everyone outside the group
sudo chmod g+X -R /var/www/html/ # give the group the right for directory traversal
```

## Configuration

Most of the configuration is to be done inside this folder:

```
/etc/apache2/
```

## Management

```
sudo /etc/init.d/apache2 start
sudo /etc/init.d/apache2 stop
sudo /etc/init.d/apache2 restart   # all connections are reset
sudo /etc/init.d/apache2 reload    # just reload configuration

sudo update-rc.d apache2 defaults  # add to auto boot
sudo update-rc.d -f apache2 remove # remove from auto boot
```

## Modules

```
sudo a2enmod userdir               # enable userdir module
sudo /etc/init.d/apache2 reload    # reload configuration
```

## Credits

Information taken from [ubuntuusers Wiki](https://wiki.ubuntuusers.de/Apache/) and [`solancer/apache-nginx-ftp` gist](https://gist.github.com/solancer/879105abb05eb7f13ce23e822ed70dd6).
