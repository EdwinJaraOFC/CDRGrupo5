<p align="left">
  <img src="https://semanadelcannabis.cayetano.edu.pe/assets/img/logo-upch.png" width="150">
  <h1 align="center">Actividad 11: Conceptos de introducción a las redes</h1>
</p>

## Problema 2: Optimización de protocolos y caché
**Escenario:** Una empresa de streaming de video experimenta interrupciones frecuentes en la entrega de contenido a los clientes. La infraestructura actual utiliza multicast para distribuir contenido, pero aún enfrenta problemas de latencia y pérdida de paquetes. 

### 1. Explica cómo mejorarías el rendimiento utilizando técnicas de caché de red. ¿Dónde colocarías estos cachés y por qué?
<p align="justify">
Para acceder al cache desde un ordenador primero busca en el caché local en lugar de volver a preguntar al servidor,el caché permite  almacenar los datos previamente cargados para un acceso más rápido, pues cuando no se encuentra el caché local este envía una consulta al solucionador DNS para comprobar su caché y en caso que este no encuentre una ip que coincida con el host este envía una consulta a su servidor de DNS preferido y en caso de no recibir respuesta por un tiempo determinado este consultara a un servidor dns alternativo.<br><br>
Una manera de mejorar el rendimiento sería usar la delegación de esta manera se podría regular el tráfico entrante a los servidores DNS. Estos servidores caché se colocarán en diferentes áreas por ejemplo distritos que luego pasan la información a un servidor de ciudad para luego a la del país de esta manera disminuye el tráfico en los servidores.
</p>
<p align="center">
  <img src="https://github.com/EdwinJaraOFC/CDRGrupo5/assets/150296803/b837e371-bde3-4a07-83b2-0eabe4048399">
</p>

### 2. ¿Cómo afecta el protocolo de transporte al rendimiento del streaming de video? Considera TCP vs UDP y justifica tu elección.
<p align="justify">
Afecta en las velocidades de carga y tiempo de respuesta, porque un servicio de streaming con protocolos lentos, pero seguros, puede presentar interrupciones en la reproducción del video. Se usa UDP principalmente, porque presenta una mayor velocidad de envío, puesto que, comparado al TCP, no se almacenan tantas variables como con el segundo tipo de conexión mencionado (el número de FLAG, números de secuencia, etc.) y no establece tantas conexiones. 
</p>
<p align="center">
  <img src="https://github.com/EdwinJaraOFC/CDRGrupo5/assets/150297452/8ee58a94-f39e-4337-8a82-e4b039f21670">
</p>

### 3. Propone una solución usando Anycast para optimizar la entrega de contenido. ¿Cómo funcionaría en este contexto?
<p align="justify">
Para optimizar la entrega de contenido, implementaremos Anycast. Configuraremos servidores Anycast en ubicaciones estratégicas para abordar los problemas de latencia y pérdida de datos. Cuando los usuarios soliciten contenido, sus solicitudes serán dirigidas automáticamente al servidor Anycast más cercano y eficiente en la red, garantizando una entrega optimizada del contenido.

Ventajas de Anycast sobre Multicast en este caso:

- **Reducción de la latencia:** Anycast dirige las solicitudes de los usuarios al servidor más cercano geográficamente, lo que reduce significativamente la latencia en comparación con la difusión de datos a través de multicast a través de la red.
- **Mayor control y escalabilidad:** Anycast permite una mayor flexibilidad y control al dirigir las solicitudes de los usuarios a servidores específicos, lo que facilita la escalabilidad y la gestión de la red en comparación con multicast, que puede ser más difícil de controlar en entornos grandes y complejos.
- **Menor impacto en la red:** Anycast solo envía datos al servidor más cercano, lo que reduce la carga en la red en comparación con multicast, que puede generar tráfico adicional al enviar datos a múltiples destinos simultáneamente.
</p>

![image](https://github.com/EdwinJaraOFC/CDRGrupo5/assets/150296803/dbfea90a-bf3e-48dc-8038-a0f373ce7592)

### 4. Desarrolla un modelo simplificado para calcular el efecto de la caché en la reducción de latencia. 
<p align="justify">
Mientras más caché se almacene en el dispositivo, más información para el acceso rápido tendrá el usuario, para así evitar requests constantes al servidor. Sin embargo, también tomará espacio significativo en el almacenamiento del usuario o en la capacidad del proxy intermediario para retener esta información en pro de una conexión más rápida con los datos almacenados de las páginas web usadas con frecuencia.<br><br>
Un posible modelo útil para el cálculo del efecto que tiene el caché en la reducción de latencia, sería, una vez implementado, sería la comparación directa entre el tiempo en envío y recepción de paquetes con y sin la aplicación de las técnicas de memoria caché.
</p>
<p align="center">
  <img src="https://github.com/EdwinJaraOFC/CDRGrupo5/assets/150297452/551f20ea-e0c7-4fbc-9912-55862ff5ffd6">
</p>
