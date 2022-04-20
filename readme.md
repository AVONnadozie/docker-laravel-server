# Web Server

Laravel web server with Nginx.

## Laravel Application Quick Run

You can get up and running with a Laravel application inside Docker in minutes.
```
$ docker run -d -p 5000:80 --rm --name=my-laravel-app -v $PWD:/var/www avonnadozie/nginx-laravel-server
```

- Visit the Docker container URL [http://0.0.0.0:5000](http://0.0.0.0:5000)

### Arguments

Here are some arguments

- `NGINX_HTTP_PORT` - HTTP port. Default: `80`.
- `NGINX_HTTPS_PORT` - HTTPS port. Default: `443`.
- `COMPOSER_HASH` - Composer hash.
- `PHP_VERSION` - The PHP version, currently 7.3.
- `ALPINE_VERSION` - The Alpine version, currently 3.9.

### Environment Variables

Here are some configurable environment values.

- `WEBROOT` – Path to the web root. Default: `/var/www`
- `WEBROOT_PUBLIC` – Path to the web root. Default: `/var/www/public`
- `COMPOSER_DIRECTORY` - Path to the `composer.json` containing directory. Default: `/var/www`.
- `COMPOSER_INSTALL_ON_BUILD` - Should `composer install` run on build. Default: `0`.
- `PRODUCTION` – Is this a production environment. Default: `0`
- `PHP_MEMORY_LIMIT` - PHP memory limit. Default: `128M`
- `PHP_POST_MAX_SIZE` - Maximum POST size. Default: `50M`
- `PHP_UPLOAD_MAX_FILESIZE` - Maximum file upload file. Default: `10M`.
- `RUN_SCHEDULER` - Should the Laravel scheduler command run. Default: `0`.
- `RUN_MIGRATIONS_ON_BUILD` - Should the migrate command run during build. Default: `0`.
- `STARTUP_SCRIPT` - Optional script to run after container starts. Path should be an absolute path eg. `/var/www/deploy/start.sh` or relative to `WEBROOT` eg. `deploy/start.sh`
- `CRON_FILE` - Optional path to a cron file, content of file will be copied to crontab. Path should be an absolute path eg. `/var/www/deploy/cron.txt` or relative to `WEBROOT` eg. `deploy/cron.txt`

Source: [https://github.com/AVONnadozie/docker-laravel-server](https://github.com/AVONnadozie/docker-laravel-server)
