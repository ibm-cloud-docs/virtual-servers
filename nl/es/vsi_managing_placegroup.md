---

copyright:
  years: 2018, 2019
lastupdated: "2019-04-24"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:note: .note}
{:new_window: target="_blank"}

# Gestión de grupos de colocación
{: #vsi_managing_placegroup}

Puede gestionar los grupos de colocación utilizando la página de grupos de colocación o la página de detalles del dispositivo de la consola de
{{site.data.keyword.cloud}}.
{:shortdesc}

## Adición de grupos de colocación

Para agregar grupos de colocación desde la página Grupos de colocación, complete los pasos siguientes:
{:shortdesc}

1. Abra la página [Grupos de colocación
![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://cloud.ibm.com/gen1/infrastructure/placement-groups){: new_window}.
2. En la página de grupos de colocación, pulse **Grupo nuevo**.
3. Especifique un nombre, una ubicación, un pod y una regla para el grupo de colocación y pulse **Crear**.

Las instancias existentes no se pueden agregar a un grupo de colocación. Solo puede agregar una instancia de servidor virtual a un grupo de colocación en el suministro. 
{:note}

## Gestión de grupos de colocación

Para gestionar grupos de colocación desde la página Grupos de colocación, complete los pasos siguientes:
{:shortdesc}

1. Abra la página [Grupos de colocación
![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://cloud.ibm.com/gen1/infrastructure/placement-groups){: new_window}.
2. En la sección Grupo de colocación, puede realizar diversas tareas de gestión.
     * Ver una lista de grupos de colocación y el número de instancias asignadas
     * Añadir un grupo
     * Cambiar el nombre de un grupo
     * Suministrar una instancia
     * Suprimir un grupo
     
Debe eliminar los servidores asignados desde el grupo de colocación antes de poder eliminar el grupo. Para eliminar una instancia de un grupo de colocación, debe eliminar o reclamar la instancia.
{:note}
