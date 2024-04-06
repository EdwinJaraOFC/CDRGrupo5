# 1 Genera tráfico de red en modo de simulación y vea multiplexación


## Preguta: 
### ¿Como se llama esto?



# 2 Examinar la funcionalidad de los protocolos TCP y UDP
 
# 3 Examinar el tráfico FTP cuando los clientes se comunican con el servidor.
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
# 4 Examina el tráfico DNS cuando los clientes se comunican con el servidor.
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
