# PHP Content Repository Browser

## Installation
* clone repo
* bash install_vendors.sh
* adust www/index.php to your configuration options (if you start jackrabbit with the default settings, those don't have to be changed)
* add a virtual host to your apache like

```
<VirtualHost *:80>
  DocumentRoot /opt/git/phpcrbrowser/www
  ServerName phpcr.lo
</VirtualHost>
```

* add an /etc/hosts entry for phpcr.lo
* start jackrabbit
* call http://phpcr.lo/

## Configuration
To change the default configuration either adjust the file `conf/config.d/00-default.yml` or create a new config for your workspace based on `conf/config.d/10-example.yml-dist`. When using a custom configuration the environment variable `OKAPI_ENV` needs match the name given in the configuration. With Apache this is done using `SetEnv OKAPI_ENV example` in the virtual host context. 
