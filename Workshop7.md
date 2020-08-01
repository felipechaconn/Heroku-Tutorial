# Laravel Heroku

En este Markdown vamos a ver como hosteamos  una web en Heroku

## Primeros pasos

1. Primero ingresamos a Heroku y creamos una cuenta,seguimos los pasos de confirmación y de creación de nueva contraseña.

2. Creamos un app y le colocamos el nombre que gustemos

## CLI

1. Antes de instar el CLI necesitamos instalar y actualizar dependencias que utilizará HEROKU,

2. Instalamos en la maquina vagrant  el CLI con el comando

```bash
    curl https://cli-assets.heroku.com/install.sh | sh
```

## Creación de proyecto Laravel

1. Creamos esl proyecto de laravel en nuestra maquina local y luego lo trasladamos (vagrant rsync) con composer con el siguienjte comando:

```bash
    composer create-project --prefer-dist laravel/laravel=6.0 HelloHeroku
```

