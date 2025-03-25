# TCB Voting App

TCB Voting App es una aplicación de votación creada utilizando Docker Compose. Esta aplicación permite a los usuarios votar en diferentes opciones y ver los resultados en tiempo real.

## Descripción

La aplicación se compone de varios servicios que se ejecutan en contenedores Docker. Estos servicios incluyen:

- **Frontend**: Una aplicación web que permite a los usuarios votar.
- **Backend**: Un servidor que maneja las solicitudes de votación y almacena los resultados.
- **Base de datos**: Un servicio de base de datos para almacenar los datos de votación.

## Comandos

Para iniciar la aplicación, asegúrate de tener Docker y Docker Compose instalados en tu sistema. Luego, sigue estos pasos:

1. Clona el repositorio de la aplicación:
    ```sh
    git clone https://github.com/daniel2688/tcb-voting-app.git
    ```

2. Navega al directorio del proyecto:
    ```sh
    cd tcb-voting-app
    ```

3. Construye y levanta los contenedores utilizando Docker Compose:
    ```sh
    docker-compose up --build .
    ```

4. Accede a la aplicación en tu navegador web en `http://localhost:9100`.

## Comandos adicionales

- Para detener los contenedores:
    ```sh
    docker-compose down
    ```

- Para ver los logs de los contenedores:
    ```sh
    docker-compose logs
    ```

- Para reconstruir los contenedores sin caché:
    ```sh
    docker-compose build --no-cache
    ```

## Contribuciones

Si deseas contribuir a este proyecto, por favor, crea un fork del repositorio y envía un pull request con tus cambios.

## Licencia

Este proyecto está licenciado bajo la Licencia MIT. Consulta el archivo `LICENSE` para más detalles.

## Docker Compose File
Este archivo define dos servicios: `tcb-vote-back` y `tcb-vote-front`. El servicio `tcb-vote-back` utiliza una imagen de Redis, mientras que el servicio `tcb-vote-front` construye la imagen desde el directorio `./tcb-vote` y se conecta al servicio de Redis.