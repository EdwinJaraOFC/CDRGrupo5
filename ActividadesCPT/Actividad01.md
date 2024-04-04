# Actividad 1: Creación de una red simple

## Paso 1: Construye la red simple configurando cada uno de los dispositivos dados.
a. En la interfaz de Packet Tracer selecciona los dispositivos dados: Switch 2960.<br>
b. Click en el dispositivo y en la pestaña Config, Display Name, Hostname Cambia el nombre a S1.<br>
c. Realiza el mismo procedimiento para los otros dispositivos. Llamalos PC-A, PC-B respectivamente<br>
d. Selecciona el ícono Rayo de conexiones y escoge Copper Straight-Through.<br>
e. Conecte un extremo de un cable Ethernet al puerto de NIC en PC-A. Conecte el otro extremo del cable a F0/6 en S1. Después de conectar la PC al switch, la luz de F0/6 debería tornarse ámbar y luego verde.<br>
f. Conecte un extremo de un cable Ethernet al puerto de NIC en PC-B. Conecte el otro extremo del cable a F0/1 en S1. Después de conectar la PC al switch, la luz de F0/1 debería tornarse ámbar y luego verde.<br>

![image](https://github.com/EdwinJaraOFC/CDRGrupo5/assets/150296803/bb6b0c33-0db4-4149-afbb-e82ca78e8524)

## Paso 2: Verifique la configuración y la conectividad de la PC.
a. Desde PC-A, haga clic y Desktop seleccione Command Prompt.<br>
b. En la ventana de comandos de packet tracer, verifique la configuración de la PC mediante el comando ipconfig /all.<br>
c. Escriba ping 192.168.1.11 y presione Intro. ¿Fueron correctos los resultados del ping? __________SÍ____________<br>
d. Repite los pasos anteriores para PC-B ¿Fueron correctos los resultados del ping? __________SÍ__________<br>

## PC-A: Command Prompt

![image](https://github.com/EdwinJaraOFC/CDRGrupo5/assets/150296803/a03215fa-77fb-4156-a139-a908e42998b0)

## PC-B: Command Prompt

![image](https://github.com/EdwinJaraOFC/CDRGrupo5/assets/150296803/75730581-42d7-4f7f-a8c2-3ef5f4f5ca2d)
