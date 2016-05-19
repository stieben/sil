# Apache

_#debian_ _#web-server_

This is for Apache 2.4.
Don't use previous versions.

## Document root

The standard path for the files that are to be served:

```
/var/www/html/
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

Information taken from [ubuntuusers Wiki](https://wiki.ubuntuusers.de/Apache/).
