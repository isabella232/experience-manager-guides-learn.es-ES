---
title: Excluir párrafos dentro de un tema de la traducción
description: Exclusión de párrafos dentro de un tema de la traducción
feature: Translation
role: User
exl-id: 21e41bb4-52f3-4352-92d9-4a60f636de99
source-git-commit: b5e64512956f0a7f33c2021bc431d69239f2a088
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# Exclusión de párrafos dentro de un tema de la traducción

La forma más sencilla es utilizar translation=sin atributo.

+ Los autores pueden insertar el atributo adicional como **translation=no** en los párrafos que no desean traducir. Se debe informar al proveedor de traducción y pueden realizar la configuración al final para ignorar el texto con este atributo.
+ La traducción automática de OOTB (con conector de traducción de Microsoft de prueba) muestra el mismo comportamiento.
+ Pruebas con la traducción de Microsoft : si define **translate=no** en el nivel de párrafo, no traduce el párrafo completo. Este atributo se puede definir en cualquier elemento y el contenido dentro de ese elemento no se traducirá.


Aquí hay algunas capturas de pantalla que lo explican más a fondo:

**Contenido de origen**

![Contenido de origen](assets/source-content.jpg)

**Contenido traducido en español**

![Contenido traducido en español](assets/trans-content.jpg)
