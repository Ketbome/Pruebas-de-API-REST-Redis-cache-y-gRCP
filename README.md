# Análisis de Redis y gRPC

Este proyecto tiene como objetivo realizar un análisis comparativo entre Redis y gRPC. A continuación, se detallan los resultados obtenidos y las conclusiones del análisis.

## Introducción

En este proyecto se realizaron dos análisis principales: uno sobre la escalabilidad y rendimiento de Redis, y otro sobre la conveniencia de utilizar gRPC en comparación con una API REST.

## Análisis de Redis

### Descripción

En este análisis se evaluó el rendimiento y la escalabilidad de Redis. Se realizaron consultas a una API y se comparó el tiempo de respuesta al realizar la consulta directamente y al realizarla utilizando Redis como caché.

### API utilizada

Se utilizó la API de PokeApi, la cual proporciona información sobre los Pokémon y los objetos del juego "Pokemon".

### Desarrollo de la actividad

Se implementaron dos partes en este análisis:

1. Consulta a la API: Se realizó una serie de consultas a la API de PokeApi utilizando Axios. Se midió el tiempo de respuesta de cada consulta y se guardaron los resultados en un archivo de texto.

2. Consulta a la API con Redis: Se implementó una caché utilizando Redis para almacenar los resultados de las consultas a la API. Se utilizó la biblioteca `ioredis` para interactuar con Redis. Se aplicaron políticas de remoción para gestionar la memoria caché.

### Resultados

Los resultados obtenidos en el análisis de Redis demostraron que utilizar una caché con Redis puede mejorar significativamente el tiempo de respuesta de las consultas a la API. Se observó una reducción considerable en el tiempo de respuesta al realizar consultas a Pokémon que ya se encontraban en la caché.

## Análisis de gRPC vs API REST

### Descripción

En este análisis se comparó la conveniencia de utilizar gRPC en lugar de una API REST para la comunicación entre servicios. Se evaluaron aspectos como la eficiencia, la facilidad de implementación y la escalabilidad.

### Resultados

Los resultados del análisis de gRPC vs API REST indicaron que gRPC puede ser una opción más eficiente y escalable en comparación con una API REST. gRPC utiliza el protocolo de comunicación HTTP/2 y el formato de serialización de datos Protocol Buffers, lo cual permite una mayor eficiencia en la transferencia de datos.

## Conclusiones

En base a los resultados obtenidos en ambos análisis, se concluye lo siguiente:

- Redis puede mejorar el rendimiento de una aplicación al utilizarlo como caché para consultas a una API. La implementación de una política de remoción adecuada es importante para optimizar el uso de la memoria caché.

- gRPC puede ser una opción más eficiente y escalable que una API REST en determinados contextos. Sin embargo, la elección entre gRPC y API REST depende de las necesidades y características específicas del proyecto.

En general, tanto Redis como gRPC ofrecen ventajas y desventajas dependiendo del contexto de uso. Es importante evaluar cuidadosamente las necesidades del proyecto antes de tomar una decisión sobre cuál tecnología utilizar.

## Referencias

- [PokeApi](https://pokeapi.co/)


