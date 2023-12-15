# Entregables

Primer Entrega

Conexion a API de tipos de cambios de todas las monedas vigentes, para observar la variacion de los valores.
Cree el codigo en COLABORATORY, luego lo descargue e importe en Visual Studio.

Desde mi maquina local, instale las librerias necesarias, a traves de comandos en CMD. 
Luego, desde el VSC, las importe.

El codigo se encuentra comentado, con cada uno de los pasos que fui realizando.

Desde DBeaver, realice la conexion en Redshift, y cree la tabla para que mas adelante, los datos obtenidos puedan ser insertados en la misma.

CREATE TABLE CurrencyExchange (
    ID INT PRIMARY KEY,
    Currency VARCHAR(50) NOT NULL,
    ExchangeRate DECIMAL(10, 2) NOT NULL,
    LastUpdated TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

![image](https://github.com/DanisaAltamirano/entregables/assets/149590620/6a442463-03a3-4cb5-989c-ef8e465bde9b)

#Entrega 2
Importe la libreria pandas, y psycopg2
Cree un DF, que me permitio realizarle transformaciones a los datos, inclusive agregar una columna (ID)

Luego con la librerias de psycopg2, y sqlalchemy cree un engine, que me permitio crear conexion con la bd postgres, donde se encontraba mi esquema, y la tabla creada para la entrega1.

Dentro del codigo, llamo a las variables establecidas en el .env. Lo que me permite seguir una buena practica.

Luego, creo la conexion a traves de una cadena. 
Con "cursor" inserto los datos del df a la tabla. El codigo respondera si la conexion fue exitosa, y si los datos fueron insertados correctamente.

Luego, la conexion se cerrará.
Adjunto captura que comprueba que los datos se cargan cada vez que ejecuto el codigo. 
![image](https://github.com/DanisaAltamirano/Entregables/assets/149590620/1a8fa50e-faa4-4a2e-8e02-c6832878caf3)

![image](https://github.com/DanisaAltamirano/Entregables/assets/149590620/3b72dcaa-51f1-4451-b754-cb119895d17d)

