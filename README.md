# dokku-name [![Build Status](https://img.shields.io/travis/alex-sherwin/dokku-name.svg?branch=master "Build Status")](https://travis-ci.org/alex-sherwin/dokku-name)

Custom Docker container name setup for dokku (https://github.com/progrium/dokku).

## requirements

- dokku 0.4.0+
- docker 1.8.x

## installation

```shell
# on 0.3.x
cd /var/lib/dokku/plugins
git clone https://github.com/alex-sherwin/dokku-name.git dokku-name
dokku plugins-install

# on 0.4.x
dokku plugin:install https://github.com/alex-sherwin/dokku-name.git dokku-name
```

## hooks

This plugin provides hooks:

* `docker-args-deploy`: customizes the name on deploy

# usage

In your applications folder - `$DOKKU_ROOT/$APP` - create a file called `NAME`.

Inside this file list exactly one name

```shell
myname
```

The above example will result in the following arguments being passed to docker during deploy and docker run:

```shell
--name="myname"
```

# thanks

Originally based on https://github.com/Frusty/dokku-name.git (no longer available at the time of this writing)
