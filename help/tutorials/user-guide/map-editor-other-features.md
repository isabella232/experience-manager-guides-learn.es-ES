---
title: Otras funciones de los editores de mapas
description: Aprenda a otras funciones de los editores de mapas
source-git-commit: 7cd719921e68ac1763d09d9665d912e3697e5849
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---


# Otras funciones de los editores de mapas {#id1942D0T0HUI}

Algunas funciones comunes de los editores de mapa básico y avanzado son:

## Resolución de referencias clave {#id176GD01H05Z}

Una referencia clave de contenido DITA, o `conkeyref` es un mecanismo para insertar una parte del contenido de un tema en otro. Este mecanismo utiliza la clave para localizar el contenido que se va a reutilizar en lugar del mecanismo de referencia de contenido directo. Para obtener más información sobre las referencias directas e indirectas en DITA, consulte *direccionamiento DITA* en la especificación de idioma DITA de OASIS.

Si el tema DITA tiene referencias clave asociadas, deben resolverse antes de previsualizar, editar o revisar un tema.

Las referencias clave se resuelven sobre la base del mapa raíz configurado en el siguiente orden de prioridad:

1. Preferencias de usuario
1. Panel Vista Mapa
1. Perfil de carpeta

El mapa raíz seleccionado en Preferencias de usuario tiene la prioridad más alta para resolver referencias clave seguidas del panel Vista de mapa y el mapa raíz del perfil de carpeta. Por lo tanto, si no se establece ningún mapa en las Preferencias de usuario, se utilizará el mapa abierto en el panel Vista de mapa. Si no se abre ningún mapa en el panel Vista de mapa, se utilizará el conjunto de mapas en Perfiles de carpeta para resolver las referencias clave.

Las referencias clave se pueden almacenar en un archivo de asignación DITA o en un archivo DITA independiente. En AEM guías, puede especificar referencias clave en el nivel de proyecto o en el nivel de sesión. Si ya se ha definido un mapa raíz para la sesión del usuario, se utiliza para resolver las claves. De lo contrario, se utiliza la asignación raíz predeterminada para esa carpeta. Si no se configura un mapa raíz predeterminado, las referencias clave que faltan se resaltarán para el usuario.

Existen varias formas de resolver referencias clave en un tema DITA definiendo el mapa DITA que se utilizará en las siguientes ubicaciones:

**Propiedades del proyecto** - Puede definir una asignación raíz para resolver referencias clave al crear un proyecto en la sección Propiedades del proyecto.

Este mapa raíz se aplicará a todos los recursos \(carpetas y subcarpetas\) asociados a ese proyecto. Para el contenido al que se hace referencia en varios proyectos, se mantiene una lista alfabética de proyectos y se utiliza el mapa raíz predeterminado asociado al primer proyecto. También puede elegir el mapa DITA que se utilizará en la lista para resolver referencias clave.

**Vista previa del tema** - En el modo de vista previa del tema, haga clic en el icono Resolución de clave de la barra de herramientas y seleccione el archivo DITA que se utilizará para las referencias clave.

**Vista de edición de temas** - Haga clic en el icono Resolución de clave mientras edita un tema DITA y seleccione el archivo DITA que desea utilizar para resolver las referencias clave.

**Tema principal:**[ Trabajar con el Editor de mapas](map-editor.md)

