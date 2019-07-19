---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-13"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Preguntas frecuentes: escalado automático
{: #faqs-auto-scale}

## ¿Da soporte el escalado automático a las instancias de escalado automático nativas?
{: faq}

Actualmente el escalado automático no da soporte a las instancias de escalado automático nativas.

## ¿Funciona el escalado automático con equilibradores de carga?
{: faq}

Sí, el escalado automático funciona actualmente para equilibradores de carga locales y utiliza una parte de la API del equilibrador de carga. Para obtener más información, consulte [Equilibradores de carga de escalado](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## ¿Cuáles son las distintas políticas de terminación de escalado automático?
{: faq}

Hay tres políticas de terminación de escalado automático: más reciente, más antiguo y más cercano al próximo cargo. Estas describen cómo elige el grupo qué miembro se va a eliminar cuando se escala hacia abajo. Para obtener más información, consulte [Política de terminación](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## ¿Qué son las políticas de escalado automático?
{: faq}

Una política contiene un conjunto de acciones y un conjunto de desencadenantes. Las políticas normalmente se componen de estos elementos: nombre, recuperación, acción y desencadenantes. Para obtener más información, consulte [Políticas](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## ¿Qué son los desencadenantes de escalado automático?
{: faq}

Los desencadenantes son condicionales que se pueden satisfacer (solo cuando el grupo está activo). Hay tres tipos de desencadenantes: único, repetitivo y de uso de recursos. Para obtener más información, consulte [Desencadenantes](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## ¿Qué es el Recuento de miembros de VSI máximo?
{: faq}

Es el número máximo de miembros que un grupo permite que esté presente. Para obtener más información, consulte [Recuento de miembros de VSI máximo](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## ¿Qué es el Recuento de miembros de VSI mínimo?
{: faq}

Es el número mínimo de miembros que un grupo permite que estén presentes. Para obtener más información, consulte [Recuento de miembros de VSI mínimo](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## ¿Qué es un activo de escalado automático?
{: faq}

Un activo es un miembro fijo de un grupo que no contribuye al recuento de miembros y que no se controla automáticamente de ninguna manera. El activo está presente para proporcionar información adicional a los desencadenantes de políticas. Por ejemplo, un activo puede contribuir a todo el porcentaje de CPU de grupo si el porcentaje de CPU se utiliza como desencadenante. Actualmente, un grupo solo puede tener activos de invitado virtuales y no hay ningún límite en cuanto al número. Además, no se necesita ningún grupo.

## ¿Qué es un grupo de escalado automático?
{: faq}

Un grupo (grupo de escalado) es una recopilación específica de grupo de activos, miembros, equilibradores de carga de escalado, VLAN y políticas. Un grupo tiene todos los parámetros para escalar, incluidos los límites de recuento de miembros y las plantillas de miembros de instancias de servidor virtual escaladas.

## ¿Qué es un miembro de escalado automático?
{: faq}

Un miembro es una unidad escalada en un grupo. Los miembros se proporcionan o se reclaman automáticamente en función de las acciones de política. Actualmente, todos los miembros son instancias de servidor virtual. En un grupo activo, nunca hay menos miembros que el mínimo o más miembros que el máximo. Aunque los miembros normalmente se añaden mediante acciones de una política, también los puede añadir manualmente un usuario.
