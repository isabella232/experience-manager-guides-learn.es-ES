---
title: AEM Personalizar diccionario predeterminado
description: AEM Aprenda a personalizar el diccionario predeterminado de la aplicación
source-git-commit: 6051181e243cf71919901093c1b5590f21832545
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 1%

---


# AEM Personalizar diccionario predeterminado {#id209SD8000WU}

AEM El editor web se puede configurar para que utilice el corrector ortográfico o el corrector ortográfico del explorador, así como para que utilice el corrector ortográfico de la aplicación. AEM Si decide trabajar con el corrector ortográfico de la, tendrá la flexibilidad de definir la lista de palabras personalizadas. AEM A continuación, estas palabras personalizadas se añaden al diccionario de recursos y estas palabras no se marcan con \(como incorrectas\) en el Editor web.

AEM Realice los siguientes pasos para crear la lista de palabras personalizadas, que se agregan en el diccionario de:

1. Cree el archivo user\_dictionary.txt con una lista de palabras que desee definir en el diccionario personalizado.

   >[!NOTE]
   >
   > Cada palabra personalizada debe definirse en una nueva línea.

1. Guarde el archivo en la siguiente ubicación del repositorio Git de Cloud Manager:

   /apps/fmdita/config

1. Guarde el archivo.

   Confirme los cambios y ejecute la canalización \(CI/CD\) de Cloud Manager para implementar los cambios de configuración.


AEM Los autores necesitarían reiniciar su sesión del editor web para obtener la lista de palabras personalizadas actualizada en el diccionario de palabras de la aplicación.

**Tema principal:**[ Personalizar editor web](conf-web-editor.md)

