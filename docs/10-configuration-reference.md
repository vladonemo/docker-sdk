This document is a draft. See [Docker SDK](https://documentation.spryker.com/docs/docker-sdk) for the official documentation.

> Audience:
>
> - Everybody who doesn't know how to configure docker/sdk in particular cases.
>
> Outcome:
> - You have a handbook of common cases that could be helpful.

## Outline

1. List all common configuration cases we have faced in the community channel, etc.


## Structure



This document is a quick reference for the most common configuration options of docker/sdk.



### How to configure Opcache

```yaml
image:
    tag: spryker/php:7.3
    php:
        ini:
            "opcache.revalidate_freq": 0
            "opcache.enable_cli": 0
            "opcache.enable": 0
            ...
```

### How to define a memory limit

```yaml
image:
    tag: spryker/php:7.3
    php:
        ini:
            "memory_limit": 512m
```

### How to provide custom environment variables to Spryker applications

```yaml
image:
    tag: spryker/php:7.3
    environment:
        MY_CUSTOM_ENVIRONMENT_VARIABLE: 1
        ...
```

:::(Info)()
The environment variables defined in `environment` are embedded into all application images.
:::