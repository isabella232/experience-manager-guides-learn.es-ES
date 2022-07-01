---
title: Cómo añadir [!DNL AEM Guides] a su [!DNL AEM as a Cloud Service] entorno
description: Obtenga información sobre cómo añadir [!DNL AEM Guides] a su [!DNL AEM as a Cloud Service] entorno
exl-id: a1e020c2-360c-4d71-b5fd-8179d9ceacda
source-git-commit: b5e64512956f0a7f33c2021bc431d69239f2a088
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---

# [!DNL AEM Guides] implementación as a Cloud Service

Obtenga información sobre cómo añadir [!DNL Guides] a su [!DNL AEM as a Cloud Service] entorno.

## Implementación manual a través de la canalización de Git de Cloud Manager

Si ha comprado [!DNL AEM Guides] as a Cloud Service antes del 29 de marzo de 2022, siga estas instrucciones de implementación:

* Si está iniciando una actualización, puede reemplazar el código generado automáticamente por [!UICONTROL Cloud Manager] con el código de la repo siguiente que ya tiene el complemento XML integrado: https://github.com/Adobe-TCS/XML-documentation-for-AEMaaCS

* Si ya tiene personalizaciones integradas en [!UICONTROL Cloud Manager] git repo, puede consultar el siguiente repositorio para obtener instrucciones sobre cómo añadir el complemento XML en su código existente: https://github.com/Adobe-TCS/DoX-Installer-for-AEMaaCS

## Implementación mediante Cloud Manager

Si es un cliente que ha comprado [!DNL AEM Guides] as a Cloud Service a partir del 29/03/2022, siga estas instrucciones para añadir [!DNL Guides] a su [!DNL AEM as a Cloud Service] entorno:

1. Inicie sesión en [!UICONTROL Cloud Manager].

1. Edite el programa para el que desea configurar [!DNL AEM Guides].

1. Cambie a **[!UICONTROL Soluciones y complementos]** pestaña .

1. En el **[!UICONTROL Soluciones y complementos]** tabla, haga clic en **[!UICONTROL Recursos]**.

1. Select **[!UICONTROL Guías]** y seleccione **[!UICONTROL Guardar]**.

Ha configurado correctamente su programa para el aprovisionamiento automático de AEM solución Guías.

![Configuración de AEM solución de guías](assets/addon-configuration.png)

>[!NOTE]
>
>Para instalar [!DNL AEM Guides] en cualquier entorno del programa integrado, debe ejecutar la canalización asociada al entorno. No se requiere ninguna configuración adicional en el código de base de Git de CM para la instalación [!DNL AEM Guides].
