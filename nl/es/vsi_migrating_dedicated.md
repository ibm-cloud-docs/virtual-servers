---



copyright:
  years: 2017
lastupdated: "2017-10-24"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Migración de una instancia de host dedicada a otro host
{: #migrating-dedicated-host}

Puede migrar instancias de host dedicadas de un host a otro dentro del mismo POD. Seleccione la instancia que desea migra en la página Detalles del dispositivo del host o en la página Detalles del dispositivo de la instancia. Tenga en cuenta que solo se pueden migrar dos instancias simultáneamente y que el tiempo necesario para la migración depende del disco. Los discos SAN se migran más rápidamente porque los discos locales requieren que se copie el disco. Las instancias migradas están fuera de línea mientras se migran; el host permanece activo para las demás instancias de host dedicadas.
{:shortdesc}

Siga los pasos siguientes para migrar instancias de host dedicadas a otro host dedicado dentro del mismo POD desde la página Detalles del dispositivo del *host dedicado original*. 

1. Acceda al [{{site.data.keyword.slportal_full}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/) utilizando sus credenciales exclusivas. 
2. Pulse **Dispositivo > Lista de dispositivos** y seleccione el host o la instancia alojada en la lista.
3. Pulse la lista desplegable **Acciones** que hay junto a la instancia dedicada que se va a migrar.
4. Seleccione **Migrar** y especifique el host al que se migra la instancia; recuerde que el host de destino debe estar dentro del mismo POD que el host original.
5. Pulse el botón **Migrar**. 

La migración comenzará inmediatamente. Durante la migración, la instancia dedicada estará fuera hasta en su nuevo host. Puede ver la página de detalles del dispositivo del host de destino para asegurarse de que la instancia se migra correctamente.

Siga los pasos siguientes para migrar instancias de host dedicadas a otro host dedicado dentro del mismo POD desde la página Detalles de la *instancia de host dedicada*.

1. Acceda al [{{site.data.keyword.slportal}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/) utilizando sus credenciales exclusivas.
2. Pulse **Dispositivo > Lista de dispositivos** y seleccione la instancia alojada que desea migrar en la lista.
3. Pulse el enlace **Migrar** de la parte derecha de la página.
4. Seleccione el host de destino al que desea migrar la instancia; recuerde que el host de destino debe estar dentro del mismo POD que el host original.
5. Pulse el botón **Migrar**.

La migración comenzará inmediatamente. Durante la migración, la instancia dedicada estará fuera hasta en su nuevo host. Puede ver la página de detalles del dispositivo del host de destino para asegurarse de que la instancia se migra correctamente.

## Siguientes pasos
Después de migrar una instancia de host dedicada, confirme que la migración se ha realizado correctamente; para ello verifique que su estado aparece en verde en la página Detalles del dispositivo del nuevo host dedicado.
