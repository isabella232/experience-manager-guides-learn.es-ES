---
title: Versiones de AEM Guías
description: Últimas versiones de AEM Guías y versiones de AEM previas
exl-id: 780697a9-bdc6-40c2-b258-64639fe30f88
source-git-commit: 714d335d95c54fb02b0fe02ad112fa36719dc970
workflow-type: tm+mt
source-wordcount: '784'
ht-degree: 1%

---

# [!DNL AEM Guides] Publicaciones

[!DNL Adobe Experience Manager Guides] es una aplicación implementada en AEM. Es una potente solución de administración de contenido de componentes (CCMS) de nivel empresarial que permite la compatibilidad nativa con DITA en Adobe Experience Manager, lo que permite a los AEM gestionar la creación y el envío de contenido basado en DITA.

## Explicación de UUID frente a no UUID

[!DNL AEM Guides] los paquetes están disponibles en dos modos: compilaciones de UUID y de no UUID.

Los clientes deberán decidir entre el UUID y el modo que no sea UUID en el momento de la primera configuración (conéctese con el gestor de éxito de los clientes para tomar una decisión basada en su uso).

Al actualizar desde una versión de [!DNL AEM Guides] en una versión más reciente, los clientes deberán asegurarse de que eligen el mismo modo (UUID/no UUID) para que coincida con su modo existente. Una compilación que no es UUID no debe actualizarse directamente a una compilación UUID. Pasar de la compilación que no es UUID a la compilación UUID necesitaría migración de contenido.

**Actualización de compilaciones**

Cuando actualiza de una versión anterior a una versión más reciente de [!DNL AEM Guides], es posible que necesite ejecutar algunas secuencias de comandos de migración. Consulte las Notas de la versión y la documentación específica de la versión para obtener instrucciones sobre la actualización.

No todas las rutas de actualización son compatibles directamente. Por ejemplo, la actualización directa a la versión 4.0 solo es posible desde la versión 3.8. Si está en una versión anterior a la 3.8, consulte la documentación específica de su versión para obtener instrucciones de actualización [Archivo de ayuda](https://helpx.adobe.com/xml-documentation-for-experience-manager/archive.html).
Póngase en contacto con el gestor de éxito del cliente para validar la ruta de actualización.

**[!DNL AEM Guides]Versiones**

La siguiente lista contiene la última [!DNL AEM Guides] paquetes disponibles para su instalación en AMS o On-Prem, versiones de AEM correspondientes (requisitos previos), vínculos de descarga de paquetes y otra información útil. Se recomienda utilizar solo la última versión de [!DNL AEM Guides]. Si, por algún motivo, necesita acceder a compilaciones anteriores, conéctese con el gestor de éxito de los clientes de su cuenta.

>[!NOTE]
>
>Póngase en contacto con el gestor de éxito de los clientes para obtener acceso a [!DNL AEM Guides] compilaciones para AEM as a Cloud Service.

| [!DNL AEM Guides]Versión  | Notas de la versión | AEM requisitos previos | Generar vínculos de descarga |
|---|---|---|---|
| **Guías AEM 4.1** | [Notas de la versión 4.1](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/tutorials/release-info/release-notes/on-prem-release-notes/release-notes-4.1.html) | **No UUID y UUID 4.1**<br><br> AEM 6.5 SP13, SP12, SP11 o SP10 | **No UUID**: <br> **AEM 6.5** <br>[4,1](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-1%2F4-1-non-uuid%2Fcom.adobe.fmdita-6.5-4.1.159.zip)<br><br> **UUID** <br>**AEM 6.5**  <br>[4,1](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-1%2F4-1-uuid%2Fcom.adobe.fmdita-6.5-uuid-4.1.159.zip) |
| **Guías AEM 4.0** | [Notas de la versión 4.0.x](https://helpx.adobe.com/xml-documentation-for-experience-manager/release-note/release-notes-xml-documentation-solution-4-0.html) | **No UUID y UUID 4.0.3**<br> AEM 6.5 SP12, SP11, SP10 o SP9 <br>Java: 11 o 8 <br><br> <br>**No UUID y UUID 4.0.2** <br> AEM 6.5 SP12, SP11, SP10 o SP9 <br>Java: 11 o 8 <br><br> **No UUID y UUID 4.0** <br> AEM 6.5 SP11, SP10 o SP9 | **No UUID**: <br> **AEM 6.5** <br>[4.0.3](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-0-3%2F4-0-2-non-uuid%2Fcom.adobe.fmdita-6.5-hotfix-4.0.3.1.zip)<br>[4.0.2](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-0-2%2F4-0-2-non-uuid%2Fcom.adobe.fmdita-6.5-sp-4.0.2.10.zip)  <br> [4,0](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/4-0/4-0-non-uuid/com.adobe.fmdita-6.5-4.0.70.zip)  <br><br> **UUID** <br>**AEM 6.5**  <br>[4.0.3](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-0-3%2F4-0-3-uuid%2Fcom.adobe.fmdita.uuid-6.5-hotfix-4.0.3.1.zip) <br>[4.0.2](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-0-2%2F4-0-2-uuid%2Fcom.adobe.fmdita.uuid-6.5-sp-4.0.2.10.zip)<br> [4,0](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/4-0/4-0-uuid/com.adobe.fmdita-6.5-uuid-4.0.70.zip) |
| **Guías de AEM 3.8.5** <br> 3.8.5 es una versión de SP incluida en 3.8. <br>La versión 3.8 no debe instalarse de forma independiente, ya que 3.8.5 SP contiene una corrección crítica. <br>Los clientes deben instalar primero 3.8 y luego SP 3.8.5. | [Notas de la versión 3.8.x](https://helpx.adobe.com/xml-documentation-for-experience-manager/release-note/release-notes-xml-documentation-solution-3-8.html) | **No UUID** <br> AEM 6.5 SP9 o SP8 <br> AEM 6.4 SP8 <br> AEM 6.3 SP3 <br><br> **UUID** <br> AEM 6.5 SP9 o SP8 | **No UUID**: <br> **AEM 6.5** <br> [3.8.5 SP](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8-5/com.adobe.fmdita-6.5-hotfix-3.8.5.2.zip) <br>[3,8](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8/com.adobe.fmdita-6.5-3.8.166.zip)<br> **AEM 6.4**<br> [3.8.5 SP](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8-5/com.adobe.fmdita-6.4-hotfix-3.8.5.1.zip) <br>[3,8](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8/com.adobe.fmdita-6.4-3.8.166.zip) <br> **AEM 6.3** <br> [3.8.5 SP](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8-5/com.adobe.fmdita-6.3-hotfix-3.8.5.1.zip) <br>[3,8](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8/com.adobe.fmdita-6.3-3.8.166.zip) <br><br> **UUID** <br>**AEM 6.5** <br> [3.8.5 SP](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8-5uuid/com.adobe.fmdita.uuid-6.5-hotfix-3.8.5.2.zip) <br> [3,8](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8uuid/com.adobe.fmdita.uuid-6.5-3.8.168.zip) |
