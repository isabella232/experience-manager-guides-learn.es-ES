---
title: Configuración de DITA-OT personalizada en [!DNL AEM Guides]
description: Obtenga información sobre cómo configurar DITA-OT personalizado en [!DNL Adobe Experience Manager Guides]
role: Admin
exl-id: f479c2cf-5b8b-4517-be97-81303468007a
source-git-commit: b5e64512956f0a7f33c2021bc431d69239f2a088
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---

# Configuración de DITA-OT personalizada en [!DNL AEM Guides] para AEM

Los pasos para agregar un DITA-OT personalizado se documentan en la sección _Uso de complementos DITA-OT personalizados_ del _Guía de instalación y configuración_.

En un nivel superior, los pasos son:

+ Obtenga el DITA-OT básico
   + Si desea obtener una copia de DITA-OT predeterminada de [!DNL AEM Guides], descárguelo desde la ruta `/etc/fmdita/dita_resources/DITA-OT.zip`
   + Si desea obtener una versión diferente, puede descargar desde [cesión temporal](https://www.dita-ot.org/download)
+ Realice cambios en DITA-OT como [adición de nuevo complemento](https://www.dita-ot.org/dev/topics/plugins-installing.html), o personalizar complementos existentes (consulte el ejemplo en la sección de vínculos relacionados a continuación)
+ Cargar `DITA-OT.zip` recibido a `/apps/<project-folder>/dita_resources` (crear una carpeta de proyecto personalizada es un método recomendado)
+ Añadir perfil DITA a **[!UICONTROL Herramientas]** > **[!UICONTROL Guías]** > **[!UICONTROL Perfiles DITA]** (utilice la ruta DITA-OT donde se carga el DITA-OT personalizado, consulte la captura de pantalla siguiente).
   ![Perfiles DITA](assets/dita-profile.png)

>[!MORELIKETHIS]
>
>+ [Personalización de muestras de complemento DITA-OT](https://www.dita-ot.org/dev/topics/pdf-customization.html)

