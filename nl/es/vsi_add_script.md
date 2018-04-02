---



copyright:
  years: 2015, 2017
lastupdated: "2017-10-24"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Adición de un script de suministro personalizado 
{: #adding-post-script}

Los scripts de suministro personalizados permiten a los usuarios especificar un URL a un script que se ejecuta en un dispositivo recién suministrado. Puede publicar y gestionar scripts de suministro personalizados en {{site.data.keyword.slportal_full}}.
{:shortdesc}

Cuando solicite un dispositivo, puede seleccionar un script de suministro personalizado si se ha publicado en la pantalla Scripts de suministro del {{site.data.keyword.slportal}}. Si un script no se ha añadido, puede proporcionar un URL. Un script de suministro puede ser cualquier archivo que el sistema operativo (SO) pueda ejecutar, incluidos archivos binarios combinados o cualquier idioma admitido por el SO. Utilice los pasos siguientes para añadir un script de suministro personalizado en el {{site.data.keyword.slportal}}.

**Nota:** esta característica solo está disponible actualmente para los sistemas operativos Linux y Unix.

## Adición de un script de suministro

1. En el menú **Dispositivos** del [{{site.data.keyword.slportal}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/){: new_window}, seleccione **Gestionar** > **Scripts de suministro**.
2. Pulse **Añadir script de suministro**.
4. En el campo Nombre, especifique un nombre de script exclusivo.
5. En el campo URL, especifique el URL exacto que se debe asociar al script.
6. Pulse **Añadir**.

## Siguientes pasos
Después de que se envíe un pedido que contiene un script de suministro, el dispositivo se puede suministrar a cualquier otro dispositivo. Antes de que el dispositivo esté disponible, el script especificado se descarga en el dispositivo. El origen del script de suministro determina el comportamiento durante este último paso del proceso de suministro. Si el script se proporciona desde un URL HTTPS, el script se descarga y se ejecuta sin necesidad de interacción adicional por parte del usuario. Si el script se proporciona sobre HTTP, el script solo se descarga. Para los scripts proporcionados sobre HTTP, el administrador debe iniciar una sesión en el dispositivo y ejecutar el script manualmente.
