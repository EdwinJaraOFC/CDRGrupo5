<p align="left">
  <img src="https://semanadelcannabis.cayetano.edu.pe/assets/img/logo-upch.png" width="150">
  <h1 align="center">Actividad 8: Comunicaciones de TCP y UDP</h1>
</p>

## Genera tráfico de red en modo de simulación y vea multiplexación

### Genera tráfico para completar las tablas del protocolo de resolución de direcciones (ARP)
Realiza la siguiente tarea para reducir la cantidad de tráfico de red que se ve en la simulación.
1. Haz clic en MultiServer y luego haz click en Desktop tab > Command Prompt.
2. Ingresa el comando ping -n 1 192.168.1.255. Está haciendo ping a la dirección broadcast de la LAN del cliente. La opción de comando enviará sólo una solicitud de ping en lugar de las cuatro habituales. Esto tomará unos segundos ya que cada dispositivo en la red responde a la solicitud de ping de MultiServer.
3. Cierra la ventana MultiServer.

### Genera tráfico web (HTTP)
1. Cambia a modo de simulación.
2. Haz clic en Cliente HTTP y abre el Explorador Web desde el escritorio.
3. En el campo URL, introduce 192.168.1.254 y haz clic en Go (Ir). Los sobres (PDU) aparecerán en la ventana de topología.
4. Minimiza, pero no cierres, la ventana de configuración de HTTP Client. 
![image](https://github.com/EdwinJaraOFC/CDRGrupo5/assets/150297438/085933e2-4924-4a16-9a3d-4adf6e0f4806)
![image](https://github.com/EdwinJaraOFC/CDRGrupo5/assets/150297438/e5d90be3-354b-4281-8a5d-99b50ec50df6)

### Genera tráfico FTP.
1. Haz clic en FTP Client y abra el Command Prompt desde el escritorio
2. Introduce el comando ftp 192.168.1.254. Las PDU aparecerán en la ventana de simulación.
3. Minimiza, pero no cierres, la ventana de configuración de FTP Client.
![image](https://github.com/EdwinJaraOFC/CDRGrupo5/assets/150297438/a93e3728-78f3-4f60-a480-da095956bfb5)
![image](https://github.com/EdwinJaraOFC/CDRGrupo5/assets/150297438/74ca1217-39d3-470e-bd57-e72b1697fe61)

### Genera tráfico DNS.
1. Haz clic en DNS Client y abra el Command Prompt
2. Introduce el comando nslookup multiserver.pt.ptu. Aparecerá una PDU en la ventana de simulación.
3. Minimiza, pero no cierre, la ventana de configuración de DNS Client. 
![image](https://github.com/EdwinJaraOFC/CDRGrupo5/assets/150297438/2bdeaa46-0ecf-4ad1-8581-ec3b80e60eb2)
![image](https://github.com/EdwinJaraOFC/CDRGrupo5/assets/150297438/7555c3bd-a1e1-4043-b178-83747d397545)

### Genera tráfico de correo electrónico.
1. Haz clic en E-Mail Client y abre la herramienta E Mail desde el escritorio.
2. Haz clic en Compose (Redactar) y escribe la siguiente información:
- To: user@multiserver.pt.ptu
- Subject: Personalizar la línea de asunto
- E-Mail Body: personalizar el correo electrónico
3. Haz clic en Send (Enviar).
4. Minimiza, pero no cierres, la ventana de configuración de E-Mail Client. 
![image](https://github.com/EdwinJaraOFC/CDRGrupo5/assets/150297438/11c97a53-454f-438e-9e97-bd748d78ec39)
![image](https://github.com/EdwinJaraOFC/CDRGrupo5/assets/150297438/c1d524ae-be0a-4531-9df8-28ed20588e84)

### Verifica que se haya generado tráfico y que esté preparado para la simulación.
Ahora debería haber entradas de PDU en el panel de simulación para cada uno de los equipos cliente.
![image](https://github.com/EdwinJaraOFC/CDRGrupo5/assets/150297438/7565f8cd-111c-4cb4-ba33-7e440348e226)

### Examina la multiplexación a medida que el tráfico cruza la red.
Ahora utilizarás el botón Capturar/Reenviar del Panel de Simulación para observar los diferentes protocolos que viajan por la red.

**Nota:** El botón Capture/Forward ' >| ' es una flecha pequeña que apunta a la derecha con una barra vertical al lado.

1. Haz clic una vez en Capture/Forward. Todas las PDU se transfieren al switch. 
2. Haz clic en Capturar/Reenviar seis veces y observe las PDU de los diferentes hosts mientras viajan por la red. Observe que solo una PDU puede cruzar un cable en cada dirección en un momento determinado.

**¿Cómo se llama esto?**

Aparece una variedad de PDU en la lista de eventos en el Panel de simulación. **¿Cuál es el significado de los diferentes colores?**

![image](https://github.com/EdwinJaraOFC/CDRGrupo5/assets/150297438/cc41aa5d-9cf0-47e3-afdc-26d69b396d3a)
![image](https://github.com/EdwinJaraOFC/CDRGrupo5/assets/150297438/318a4273-52b3-4c68-9a34-609a1911b937)

## Examinar la funcionalidad de los protocolos TCP y UDP
 
### 3 Examinar el tráfico FTP cuando los clientes se comunican con el servidor.
- Abre el símbolo del sistema en el escritorio del cliente FTP. Inicie una conexión FTP
ingresando ftp 192.168.1.254.
- En el Panel de simulación, cambia Edit Filters para mostrar solo FTP y TCP.
- Haz clic en Capture/Forward. Haz clic en el segundo sobre PDU para abrirlo.Haz clic en la
pestaña Outbound PDU Details y desplácese hacia abajo hasta la sección TCP.
Pregunta:
- ¿Se consideran confiables estas comunicaciones?
- Registra los valores de SRC PORT (PUERTO DE ORIGEN), DEST PORT (PUERTO DE
DESTINO), SEQUENCE NUM (NÚMERO DE SECUENCIA) y ACK NUM (NÚMERO DE
RECONOCIMIENTO).
Pregunta:
-¿Cuál es el valor en el campo de bandera?
- Cierra la PDU y haz clic en Capture/Forward hasta que una PDU vuelva a FTP Client con
una marca de verificación.
- Cierra el sobre de PDU y seleccione Inbound PDU Details.
-Pregunta:
   -¿En qué cambiaron los números de puerto y de secuencia?

- Haz clic en la ficha de detalles de la PDU saliente.
-Pregunta:
-¿En qué se diferencian los números de puerto y secuencia de los resultados anteriores?

- Cierra la PDU y haz clic en Capture/Forward hasta que una segunda PDU vuelva a FTP
Client. La PDU es de un color diferente.
- Abre la PDU y selecciona Inbound PDU Details. Desplázate hasta después de la sección
TCP.
-Pregunta:
- ¿Cuál es el mensaje del servidor?
- Haz clic en Reset Simulation (Restablecer simulación).
### 4 Examina el tráfico DNS cuando los clientes se comunican con el servidor.
- Repita los pasos de la Parte 1 para crear tráfico DNS.
- En el panel de simulación, modifique las opciones de Edit Filters para que solo se muestren
DNS y UDP.
- Haz clic en el sobre de PDU para abrirlo.
- Mire los detalles del modelo OSI para la PDU saliente.
- Pregunta:
- ¿Qué es el protocolo de capa 4?

- ¿Se consideran confiables estas comunicaciones?

- Abra la ficha Detalles de PDU saliente y busque la sección UDP de los formatos de PDU.
- Registre los valores de SRC PORT y DEST PORT .
- Pregunta:
- ¿Por qué no hay números de secuencia y reconocimiento?

- Cierre la PDU y haz clic en Capture/Forward hasta que una PDU con una marca de
verificación regrese al DNS Client.
- Cierra el sobre de PDU y seleccione Inbound PDU Details.
- Pregunta:
- ¿En qué cambiaron los números de puerto y de secuencia?
- Haz clic en Reset Simulation (Restablecer simulación).

### 4 Examina el tráfico de correo electrónico cuando los clientes se comunican con el servidor
- Repite los pasos de la Parte 1 para enviar un correo electrónico a user@multiserver.pt.ptu.
- En el panel de simulación, modifique las opciones de Edit Filters para que solo se muestren
POP3, SMTP y TCP.
- Haz clic en el primer sobre de la PDU para abrirlo.
- Haz clic en la pestaña Outbound PDU Details y desplácese hacia abajo hasta la última
sección.
-Preguntas:
-¿Qué protocolo de la capa de transporte utiliza el tráfico de correo electrónico? ¿Se
consideran confiables estas comunicaciones?
- Registra los valores de SRC PORT (PUERTO DE ORIGEN), DEST PORT (PUERTO DE
DESTINO), SEQUENCE NUM (NÚMERO DE SECUENCIA) y ACK NUM (NÚMERO DE
RECONOCIMIENTO). ¿Cuál es el valor del campo de bandera?
- Cierra la PDU y haz clic en Capture/Forward hasta que una PDU regrese al E-Mail Client
con una marca de verificación.
- Haz clic en el sobre TCP PDU y seleccione Inbound PDU Details.
-Pregunta:
-¿En qué cambiaron los números de puerto y de secuencia?
- Haz clic en la ficha de detalles de la PDU saliente. ¿En qué se diferencian los números de
puerto y de secuencia con respecto a los dos resultados anteriores?
- Hay una segunda PDU de un color diferente que E-Mail Client hha preparado para enviar a
MultiServer. Este es el comienzo de la comunicación de correo electrónico. Haz clic en este
segundo sobre de PDU y seleccione Outbound PDU Details.
- Preguntas:
- ¿En qué se diferencian los números de puerto y de secuencia con respecto a las dos PDU
anteriores?
- ¿Qué protocolo de correo electrónico se relaciona con el puerto TCP 25? ¿Qué protocolo se
relaciona con el puerto TCP 110?
