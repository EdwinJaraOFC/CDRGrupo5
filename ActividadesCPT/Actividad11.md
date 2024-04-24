<p align="left">
  <img src="https://semanadelcannabis.cayetano.edu.pe/assets/img/logo-upch.png" width="150">
  <h1 align="center">Actividad 11: Conceptos de introducción a las redes</h1>
</p>

## Problema 2: Optimización de protocolos y caché
**Escenario:** Una empresa de streaming de video experimenta interrupciones frecuentes en la entrega de contenido a los clientes. La infraestructura actual utiliza multicast para distribuir contenido, pero aún enfrenta problemas de latencia y pérdida de paquetes. 

### 1. Explica cómo mejorarías el rendimiento utilizando técnicas de caché de red. ¿Dónde colocarías estos cachés y por qué?**

<p align="justify">
Se busca en el caché local en lugar de volver a preguntar al servidor,el caché permite  almacenar los datos para un acceso más rápido, pues cuando no se encuentra el caché local este envía una consulta al solucionador DNS para comprobar su caché y en caso que este no encuentre una ip que coincida con el host este envía una consulta a su servidor de DNS preferido y en caso de no recibir respuesta por un tiempo determinado este consultara a un servidor dns alternativo.<br>
Una manera de mejorar el rendimiento sería usar la delegación de esta manera se podría regular el tráfico entrante a los servidores DNS. Estos servidores caché se colocarán en diferentes áreas por ejemplo distritos que luego pasan la información a un servidor de ciudad para luego a la del país de esta manera disminuye el tráfico en los servidores.
</p>

### 2. ¿Cómo afecta el protocolo de transporte al rendimiento del streaming de video? Considera TCP vs UDP y justifica tu elección.** 

<p align="justify">
Afecta en las velocidades de carga y tiempo de respuesta, porque un servicio de streaming con protocolos lentos, pero seguros, puede presentar interrupciones en la reproducción del video. Se usa UDP principalmente, porque presenta una mayor velocidad de envío, puesto que, comparado al TCP, no se almacenan tantas variables como con el segundo tipo de conexión mencionado (el número de FLAG, números de secuencia, etc.) y no establece tantas conexiones. 
</p>

### 3. Propone una solución usando Anycast para optimizar la entrega de contenido. ¿Cómo funcionaría en este contexto?

<p align="justify">
El anycast es algo así como un compromiso entre un unicast y un multicast. Con anycast, hay varios destinos que comparten la misma dirección IP. Se envía un mensaje que posiblemente podría ir a cualquiera de estos destinos, pero siempre se enruta al destino más cercano. De esta forma, un anycast llegará a su destino en el menor tiempo posible. Si no mencionamos explícitamente la forma de comunicación, suponemos que es unicast. 
</p>

### 4. Desarrolla un modelo simplificado para calcular el efecto de la caché en la reducción de latencia. 

<p align="justify">
Mientras más caché se almacene en el dispositivo, más información para el acceso rápido tendrá el usuario, para así evitar requests constantes al servidor. Sin embargo, también tomará espacio significativo en el almacenamiento del usuario o en la capacidad del proxy intermediario para retener esta información en pro de una conexión más rápida con los datos almacenados de las páginas web usadas con frecuencia.<br>
Un posible modelo útil para el cálculo del efecto que tiene el caché en la reducción de latencia, sería, una vez implementado, sería la comparación directa entre el tiempo en envío y recepción de paquetes con y sin la aplicación de las técnicas de memoria caché.
</p>
