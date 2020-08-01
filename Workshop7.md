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

## Heroku Login

En esta parte es cuando hacemos el match con Heroku empezando con el comando:

```bash
    //el -i es para que sea sin necesidad de interfaz grafica
   heroku login -i
```

Seguidamente  ingresamos nuestro email y password con los que nos registramos en Heroku para loguearnos y la realizacion del Procfile:

```bash
    echo "web: vendor/bin/heroku-php-apache2 public/" > Procfile
```

## Creando la aplicacion de Heroku desde CLI

Con este comando creamos la aplicacion con los parameteos del procfile (php apache2) como el comando no lleva mas argumentos el usa el nombre del dominio aleatorio <https://warm-sea-58098.herokuapp.com/>

```bash
    heroku create
```

## Primer deploy

Para el primer deploy, en vez de origin utilizamos heroku

```bash
   git push heroku master
```

Luego seteamos las variables de entorno que se ocupan con el comando:

1. Primero extraemos el Key con el siguiente comando

```bash
   cat .env | grep APP_KEY
```

2. Seteamos la llave con el siguiente comando

```bash
  heroku config:set APP_KEY= key
```
