---

copyright:
  years: 2017
lastupdated: "2018-01-03"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# Consideraciones de capacidad
{: #capacity-considerations}

## ¿Qué está pasando?

Cuando suministre un servidor virtual, puede recibir el siguiente mensaje de error:

```
No hay suficiente capacidad para completar la solicitud.
```
{:screen}

Cuando el suministro falla, todas las instancias de servidor virtual de dicha solicitud particular fallan.
{:tip}

## ¿Por qué está pasando?

Se produce un error de capacidad cuando no hay suficientes recursos disponibles en el direccionador o centro de datos para completar la solicitud de servicio. Existen una serie de motivos por las cuales podría recibir este error. La disponibilidad de recursos cambia con frecuencia, por lo que puede esperar y volver a intentarlo más tarde.

## ¿Cómo arreglarlo?

Puede intentar volver a suministrarlo utilizando las siguientes estrategias:

1. Suministrar especificando otro direccionador.  
2. Suministrar sin especificar un direccionador.
3. Suministrar en otro centro de datos.
4. Suministrar menos instancias.
5. Distribuir las instancias suministrándolas en múltiples centros de datos.
6. Suministrar instancias de menor tamaño.
7. Modificar el almacenamiento VSI de SAN a LOCAL o LOCAL a SAN.
