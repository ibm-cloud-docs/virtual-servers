---

copyright:
  years: 2014, 2017
lastupdated: "2017-11-17"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Certificados SSL
{: #ssl-certificates}

Secure Sockets Layer (SSL) es una tecnología que cifra el tráfico entre la aplicación de cliente y la aplicación de servidor que participan en la conversación. Este cifrado se logra mediante un sistema de claves públicas/claves privadas utilizando un certificado SSL.
{:shortdesc}

El certificado SSL contiene la clave pública del servidor, fechas en las cuales el certificado es válido, un nombre de host para el cual el certificado es válido y una firma de la autoridad de certificación que lo ha emitido. Con esta información y algunos detalles de protocolo que se intercambian durante el inicio de una sesión, el cliente puede estar razonablemente seguro de que el servidor es el servidor con el que pretende hablar.

Para obtener más información sobre certificados SSL, consulte [Iniciación a los servidores SSL](/docs/infrastructure/ssl-certificates?topic=ssl-certificates-getting-started-tutorial).
