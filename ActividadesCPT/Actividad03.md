<p align="left">
  <img src="https://semanadelcannabis.cayetano.edu.pe/assets/img/logo-upch.png" width="150">
  <h1 align="center">Actividad 3: Identificación de direcciones MAC y direcciones IP</h1>
</p>

## Recopila información del PDU para la comunicación de red local

### Recopila información de la PDU a medida que un paquete viaja de 172.16.31.5 a 172.16.31.2.

a. Haz clic en 172.16.31.5 y abra el Command Prompt.
b. Introduce el comando ping 172.16.31.2.
c. Cambia al modo de simulación y repita el comando ping 172.16.31.2. Aparece una PDU junto a 172.16.31.5.
d. Haz clic en la PDU y observa la siguiente información de las pestañas Modelo OSI l y Capa de PDU saliente:

●	Destination MAC Address: 000C:85CC:1DA7
●	Source MAC Address: 00D0:D311:C788
●	Source IP Address:172.16.31.5
●	Destination IP Address: 172.16.31.2
●	At Device: 172.16.31.5

e. Haz clic en Capture / Forward (la flecha derecha seguida de una barra vertical) para mover la PDU al siguiente dispositivo. Reúna la misma información del paso 1d. Repite este proceso hasta que la PDU llegue al destino.

Formato de hoja de cálculo de ejemplo
<p align= "center">
  <img src="https://github.com/EdwinJaraOFC/CDRGrupo5/assets/150296803/23c23cb3-7020-4f17-9505-127808b42830" alt="Grupo trabajando"  />
</p>

172.16.31.5
<p align= "center">
  <img src="https://github.com/EdwinJaraOFC/CDRGrupo5/assets/150296803/ab6ec817-847c-41cd-8662-b5233495fb69" alt="Grupo trabajando" />
</p>


Switch1

![image](https://github.com/EdwinJaraOFC/CDRGrupo5/assets/150296803/ecf3dc79-6835-432b-8093-5bd62fd9c039)

Concentrador (HUB)

![image](https://github.com/EdwinJaraOFC/CDRGrupo5/assets/150296803/1d280728-e507-416e-b59e-35b650a03a95)

172.16.31.2

![image](https://github.com/EdwinJaraOFC/CDRGrupo5/assets/150296803/bf0351d6-947e-439e-914b-591840cd16dd)

### Reunir información adicional de la PDU de otros ping.
Repite el proceso del paso 1 y reúna información para las siguientes pruebas:
- Ping de 172.16.31.2 a 172.16.31.3

![image](https://github.com/EdwinJaraOFC/CDRGrupo5/assets/150296803/be08a1e1-c032-44e7-b474-5fad2977f846)

- Ping de 172.16.31.4 a 172.16.31.5

![image](https://github.com/EdwinJaraOFC/CDRGrupo5/assets/150296803/aa81520e-5f11-4af1-8c03-9131da8c1a5e)

## Recopila información del PDU para la comunicación de red remota

### Recopila información de la PDU a medida que un paquete viaja de 172.16.31.5 a 10.10.10.2. 
a. Haz click en 172.16.31.5 y abra el Command Prompt.
b. Introduce el comando ping 10.10.10.2.
c. Cambia al modo de simulación y repita el comando ping 10.10.10.2. Aparece una PDU junto a 172.16.31.5.
d. Haz clic en la PDU y observe la siguiente información en la ficha Outbound PDU Layer (Capa de PDU saliente):
Destination MAC Address: 00D0:BA8E:741A
Source MAC Address: 00D0:D311:C788
Source IP Address: 172.16.31.5
Destination IP Address: 10.10.10.2
At Device: 172.16.31.5

![image](https://github.com/EdwinJaraOFC/CDRGrupo5/assets/150296803/a31f8b70-f606-4c1c-a5df-24a7d92ac239)

Pregunta:
¿Qué dispositivo tiene el MAC de destino que se muestra?
-	El Router

e. Haz clic en Capture / Forward (la flecha derecha seguida de una barra vertical) para mover la PDU al siguiente dispositivo. Reúne la misma información del paso 1d. Repite este proceso hasta que la PDU llegue al destino. Registra la información de la PDU que recopiló del ping 172.16.31.5 a 10.10.10.2 en una hoja de cálculo utilizando un formato como la tabla de muestra que se muestra a continuación: 

![image](https://github.com/EdwinJaraOFC/CDRGrupo5/assets/150296803/283a7045-38d1-4211-8086-b0d5b82ac1b7)

172.16.31.5

![image](https://github.com/EdwinJaraOFC/CDRGrupo5/assets/150296803/959e2e8a-97f7-46bc-a5a5-081f5b6c017c)

Switch1

![image](https://github.com/EdwinJaraOFC/CDRGrupo5/assets/150296803/a16c6a48-5fa0-4551-b3ca-1251255b999a)

Router

![image](https://github.com/EdwinJaraOFC/CDRGrupo5/assets/150296803/59c652c9-9452-49fa-85f7-757f85f07fe7)

Switch0

![image](https://github.com/EdwinJaraOFC/CDRGrupo5/assets/150296803/c1ae9f1d-4d35-4916-8783-b2fb8981f1f5)

Punto de acceso

![image](https://github.com/EdwinJaraOFC/CDRGrupo5/assets/150296803/1578f351-8cb1-44c2-bd5a-93fc7a6f834f)

10.10.10.2

![image](https://github.com/EdwinJaraOFC/CDRGrupo5/assets/150296803/8f492934-35b0-4ae7-88b6-ef357b4d3f94)

## Preguntas
Responde las siguientes preguntas relacionadas con los datos capturados:
1. **¿Se utilizaron diferentes tipos de cables / medios para conectar dispositivos?**
-	Sí, se utilizaron 3 tipos de cables: Inalámbrico, de cobre y de fibra óptica.
2. **¿Los cables cambiaron el manejo de la PDU de alguna manera?**
-	No, los cables solo trabajan a nivel de la capa 1.
3. **¿El hub perdió parte de la información que recibió?**
-	No.
4. **¿Qué hace el hub con las direcciones MAC y las direcciones IP?**
-	Nada, el HUB solo reenvía hacia todos sus puertos la trama que se envía.
5. **¿El punto de acceso inalámbrico hizo algo con la información que se le entregó?**
-	El punto de acceso inalámbrico vuelve a empaquetar la trama para que pueda viajar por el medio (aire).
6. **¿Se perdió alguna dirección MAC o IP durante la transferencia inalámbrica?**
-	No.
7. **¿Cuál fue la capa OSI más alta que utilizaron el hub y el punto de acceso?**
-	El hub y el punto de acceso solo trabajan a nivel de capa 1.
8. **¿El hub o el punto de acceso reprodujeron en algún momento una PDU rechazada con una “X” de color rojo?**
-	Sí, ya que al reenviar a todos los puertos, solo uno es el destino y a los demás los rechaza.
9. **Al examinar la ficha PDU Details (Detalles de PDU), ¿qué dirección MAC aparecía primero, la de origen o la de destino?**
-	Aparece primero la de destino.
10. **¿Por qué las direcciones MAC aparecen en este orden?**
-	Porque si se conoce primero la dirección MAC de destino, el dispositivo puede reenviar la trama a una dirección MAC más rápidamente.
11. **¿Había un patrón para el direccionamiento MAC en la simulación?**
-	No.
12. **¿Los switches reprodujeron en algún momento una PDU rechazada con una “X” de color rojo?**
-	Los switches no, ya que estos solo reenvían las tramas al destino requerido.
13. **Cada vez que se enviaba la PDU entre las redes 10 y 172, había un punto donde las direcciones MAC cambiaban repentinamente. ¿Dónde ocurrió eso?**
-	Sí, esto ocurrió en el router.
14. **¿Qué dispositivo usa direcciones MAC que comienzan con 00D0: BA?**
-	El router.
15. **¿A qué dispositivos pertenecían las otras direcciones MAC?**
-	Al emisor y al receptor, estos pueden ser las computadoras, HUB, switches y puntos de acceso.
16. **¿Las direcciones IPv4 de envío y recepción cambiaron los campos en alguna de las PDU?**
-	No.
17. **Cuando sigue la respuesta a un ping, a veces llamado pong, ¿ve el cambio de envío y recepción de direcciones IPv4?**
-	Sí se logra ver el cambio.
18. **¿Cuál es el patrón para el direccionamiento IPv4 utilizado en esta simulación?**
-	Cada puerto o interfaz del router debe manejar una dirección IP diferente, y cada dispositivo que está dentro de esta red que se dirigen a una interfaz no deben superponerse.
19. **¿Por qué es necesario asignar diferentes redes IP a los diferentes puertos de un router?**
-	Para poder interconectar diferentes redes.
20. **Si esta simulación se configura con IPv6 en lugar de IPv4, ¿cuál sería la diferencia?**
-	Solo se reemplazarían las direcciones IPv4 con las IPv6, en pocas palabras solo cambiaría el formato, lo demás seguiría igual.

