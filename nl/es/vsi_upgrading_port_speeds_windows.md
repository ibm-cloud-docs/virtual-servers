---



copyright:
  years: 1994, 2017
lastupdated: "2017-12-12"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Actualización de la velocidad de puerto en Windows

La velocidad de puerto predeterminada para servidores de clientes (para redes públicas y privadas) es 10 Mbps. Si le gustaría actualizar las velocidades de puerto a 100 Mbps o 1000 Mbps, abra una incidencia con la solicitud. Ventas le solicitará que apruebe el cargo mínimo y un técnico cambiará las velocidades de puerto en la red.

Una vez completada la actualización en el lado de la red, codifique las interfaces de red correspondientes en su servidor.

Siga estos pasos para forzar la velocidad de puerto en un servidor Windows. **Nota:** conéctese siempre a su servidor en la red en la que NO esté trabajando para evitar bloquearse del servidor.

1. Seleccione **Inicio > Panel de control > Conexiones de red**.
2. Pulse la conexión de red que está intentando actualizar o degradar.
  * Para actualizaciones de Puerto público seleccione **Local Area Connection 2** O **FrontEnd**.
  * Para actualizaciones de Puerto privado seleccione **Local Area Connection** O **BackEnd**.
3. En la ventana Estado de la conexión, verifique que la tarjeta de red que ha seleccionado sea el puerto que desea actualizar.
4. Seleccione el separador de soporte (anote la dirección IP):
  * Para actualizar el puerto público, la IP debería ser una dirección IP pública.
  * Para actualizar un puerto privado, la IP debería ser una dirección 10.x.x.x.
5. Si las direcciones IP no coinciden, repita los pasos 1-3 para la otra Conexión de red.

## Estado de LAN

Seleccione de nuevo el separador **General** y, a continuación, **Propiedades.** Se abre una nueva ventana.

Desde el separador **General** de la ventana **Propiedades de conexión**, seleccione **Configurar**. Se abre la ventana de propiedades del controlador.

1. Seleccione el separador **Avanzado**.
2. Seleccione **Velocidad de enlace y dúplex** en la lista de propiedades.
3. Seleccione el separador **Valor** a la derecha y establezca la velocidad de puerto que está actualizando con dúplex completo:
  1. Para 10 MBS, seleccione: 10Mbps/Full
  2. Para 100 MBS, seleccione: 100Mbps/Full
  3. Para 1000 MBS, seleccione: Auto
4. Pulse Aceptar.  

Esto provoca que el servidor se inicie inmediatamente utilizando la nueva velocidad, por lo que es posible que se desconecte brevemente mientras el enlace renegocia.
