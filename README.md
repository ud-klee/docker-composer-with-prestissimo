[![Build Status](https://travis-ci.org/ud-klee/docker-composer-with-prestissimo.svg?branch=master)](https://travis-ci.org/ud-klee/docker-composer-with-prestissimo)

# Supported tags and respective `Dockerfile` links

- `1.6-php7.2`, `latest`
- `1.6-php7.2-alpine`, `alpine`
- `1.6-php5.6`
- `1.6-php5.6-alpine`

# What is Composer?

Composer helps you declare, manage and install dependencies of PHP projects.

> [https://github.com/composer/composer](https://github.com/composer/composer)

# What is prestissimo

composer parallel install plugin.

> [https://github.com/hirak/prestissimo](https://github.com/hirak/prestissimo)

# How to use this image.

## Installation / Usage

1. Install the `ud-klee/composer-with-prestissimo` container:

    ``` sh
    $ docker pull ud-klee/composer-with-prestissimo
    ```

2. Create a composer.json defining your dependencies.

    ``` json
    {
        "require": {
            "monolog/monolog": ">=1.0.0"
        }
    }
    ```

3. Run Composer through the Composer container:

    ``` sh
    $ docker run --rm -v $(pwd):/app ud-klee/composer-with-prestissimo install
    ```

