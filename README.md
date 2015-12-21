# Versions

- [`1.9.9-0`, `latest` (_Dockerfile_)](https://github.com/mageinferno/docker-magento2-nginx/tree/1.9.9-0/Dockerfile)

# Description

This image is built from [`nginx`](https://hub.docker.com/_/nginx/) and contains the default webserver configuration for Magento 2.

The nginx configuration file is setup to run in tandem with `php-fpm` and `mysql` containers. It works really well with our PHP image [`mageinferno/magento2-php`](https://hub.docker.com/r/mageinferno/magento2-php), with contains the related PHP extensions and software needed to run Magento 2. The official `mysql` image works just fine with this image.

# What's in this image?

This image installs the following:

- `nginx`
- `vim`

# How to use this image?

To use this image, create Dockerfile in the root of your project with anything specific to your local development platform.

For example, if using [Dinghy](https://github.com/codekitchen/dinghy) on OS X, use:

```
FROM mageinferno/magento2-nginx:[TAG]
RUN usermod -u 501 www-data
```

Then build your custom image:

```
docker build -t myname/foobar .
```

Please see <a href="https://github.com/mageinferno/magento2-docker-compose" target="_blank">https://github.com/mageinferno/magento2-docker-compose</a> for more detailed instructions and an example development environment using Docker Compose.
