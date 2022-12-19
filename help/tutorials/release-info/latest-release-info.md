---
title: Versiones de AEM Guías
description: Últimas versiones de AEM Guías y versiones de AEM previas
exl-id: 780697a9-bdc6-40c2-b258-64639fe30f88
source-git-commit: f74a9168708299d66d014dbc4bf280a1a4f07592
workflow-type: tm+mt
source-wordcount: '1114'
ht-degree: 0%

---

# [!DNL AEM Guides] Publicaciones

[!DNL Adobe Experience Manager Guides] es una aplicación implementada en AEM. Es una potente solución de administración de contenido de componentes (CCMS) de nivel empresarial que permite la compatibilidad nativa con DITA en Adobe Experience Manager, lo que permite a los AEM gestionar la creación y el envío de contenido basado en DITA.

AEM paquetes de guías están disponibles en dos variantes: compilaciones de UUID y de Non-UUID .

## Compilaciones UUID y no UUID

Las principales diferencias entre las compilaciones de UUID y no UUID son las siguientes:

|  | Compilación no UUID | UUID build |
|---|---|---|
| **Identificación de activos** | Todos los recursos se identifican mediante la ruta del recurso en el repositorio. | Todos los recursos se identifican con su UUID (ID único generado por el sistema cuando el recurso se cargó por primera vez). |
| **Creación de referencias** | Todas las referencias de contenido se crean en función de sus rutas. | Todas las referencias de contenido se crean en función de su UUID. |

### Ventajas de la compilación de UUID

* La instalación de UUID es más eficaz:
   * Las referencias son independientes de la ruta: El sistema de gestión de referencias es consciente de los vínculos, ya que las referencias se crean basándose en UUID y no en las rutas.
   * Las operaciones de mover/actualizar son eficientes: Los UUID permanecen iguales aunque los recursos se muevan a otra ruta del repositorio. Por lo tanto, no es necesario procesar las referencias entre los recursos en las operaciones de movimiento/actualización.
* La compilación de UUID es prospectiva, ya que utilizamos este marco para la configuración de nube de AEM guías también.


### Elija entre las dos compilaciones

* Si es un cliente nuevo, le recomendamos que utilice la compilación de UUID.
* Si ya es cliente de , puede elegir pasar a la compilación de UUID, ya que la migración de la compilación de no UUID a UUID ahora es posible. Para obtener más información, consulte la *Migración de contenido que no es UUID a UUID* en la sección **Instale y configure las guías de Adobe Experience Manager.**

>[!NOTE]
>
>* Los clientes deberán decidir entre el UUID y el modo que no sea UUID en el momento de la primera configuración (en caso de que necesite ayuda, conéctese con el gestor de éxito del cliente para tomar una decisión basada en su uso).
>* Al actualizar de una versión de AEM guías a una versión más reciente, los clientes deberán asegurarse de que eligen el mismo modo (UUID/no UUID) para que coincida con su modo existente. Una compilación que no es UUID no debe actualizarse directamente a una compilación UUID. Al pasar de la compilación que no es de UUID a la compilación de UUID, sería necesario migrar el contenido.


**Actualización de compilaciones**

Cuando actualiza de una versión anterior a una versión más reciente de [!DNL AEM Guides], es posible que deba ejecutar secuencias de comandos de migración. Consulte las Notas de la versión y la documentación específica de la versión para obtener instrucciones sobre la actualización.

No todas las rutas de actualización son compatibles directamente. Por ejemplo, la actualización directa a la versión 4.0 solo es posible desde la versión 3.8. Si está en una versión anterior a la 3.8, consulte la documentación específica de su versión para obtener instrucciones de actualización [Archivo de ayuda](https://helpx.adobe.com/xml-documentation-for-experience-manager/archive.html).
Póngase en contacto con el gestor de éxito del cliente para validar la ruta de actualización.

**[!DNL AEM Guides]Versiones**

La siguiente lista contiene la última [!DNL AEM Guides] paquetes disponibles para su instalación en AMS o On-Prem, versiones de AEM correspondientes (requisitos previos), vínculos de descarga de paquetes y otra información útil. Se recomienda utilizar solo la última versión de [!DNL AEM Guides]. Si, por algún motivo, necesita acceder a compilaciones anteriores, conéctese con el gestor de éxito de los clientes de su cuenta.

>[!NOTE]
>
>Póngase en contacto con el gestor de éxito de los clientes para obtener acceso a [!DNL AEM Guides] compilaciones para AEM as a Cloud Service.

| [!DNL AEM Guides]Versión  | Notas de la versión | AEM requisitos previos | Generar vínculos de descarga |
|---|---|---|---|
| **Guías AEM 4.1** | [Notas de la versión 4.1.x](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/tutorials/release-info/release-notes/on-prem-release-notes/release-notes-4.1.html) | **No UUID y UUID 4.1.2**<br><br> AEM 6.5 SP13, SP12, SP11 o SP10 <br>Java: 11 o 8 <br><br>**No UUID y UUID 4.1**<br><br> AEM 6.5 SP13, SP12, SP11 o SP10 | **No UUID**: <br> **AEM 6.5** <br>[4,1](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-1%2F4-1-non-uuid%2Fcom.adobe.fmdita-6.5-4.1.159.zip)<br>[4.1.2](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-1-2%2F4-1-2-non-uuid%2Fcom.adobe.fmdita-6.5-sp-4.1.2.11.zip)<br>[4.1.3](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-1-3%2F4-1-3-non-uuid%2Fcom.adobe.fmdita-6.5-sp-4.1.3.2.zip)<br><br> **UUID** <br>**AEM 6.5** <br>[4,1](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-1%2F4-1-uuid%2Fcom.adobe.fmdita-6.5-uuid-4.1.159.zip)<br>[4.1.2](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-1-2%2F4-1-2-uuid%2Fcom.adobe.fmdita.uuid-6.5-sp-4.1.2.11.zip)<br>[4.1.3](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-1-3%2F4-1-3-uuid%2Fcom.adobe.fmdita.uuid-6.5-sp-4.1.3.2.zip) |
| **Guías AEM 4.0** | [Notas de la versión 4.0.x](https://helpx.adobe.com/xml-documentation-for-experience-manager/release-note/release-notes-xml-documentation-solution-4-0.html) | **No UUID y UUID 4.0.3**<br> AEM 6.5 SP12, SP11, SP10 o SP9 <br>Java: 11 o 8 <br><br> <br>**No UUID y UUID 4.0.2** <br> AEM 6.5 SP12, SP11, SP10 o SP9 <br>Java: 11 o 8 <br><br> **No UUID y UUID 4.0** <br> AEM 6.5 SP11, SP10 o SP9 | **No UUID**: <br> **AEM 6.5** <br>[4.0.3](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-0-3%2F4-0-2-non-uuid%2Fcom.adobe.fmdita-6.5-hotfix-4.0.3.1.zip)<br>[4.0.2](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-0-2%2F4-0-2-non-uuid%2Fcom.adobe.fmdita-6.5-sp-4.0.2.10.zip)  <br> [4.0](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/4-0/4-0-non-uuid/com.adobe.fmdita-6.5-4.0.70.zip)  <br><br> **UUID** <br>**AEM 6.5**  <br>[4.0.3](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-0-3%2F4-0-3-uuid%2Fcom.adobe.fmdita.uuid-6.5-hotfix-4.0.3.1.zip) <br>[4.0.2](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-0-2%2F4-0-2-uuid%2Fcom.adobe.fmdita.uuid-6.5-sp-4.0.2.10.zip)<br> [4.0](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/4-0/4-0-uuid/com.adobe.fmdita-6.5-uuid-4.0.70.zip) |
| **Guías de AEM 3.8.5** <br> 3.8.5 es una versión de SP incluida en 3.8. <br>La versión 3.8 no debe instalarse de forma independiente, ya que 3.8.5 SP contiene una corrección crítica. <br>Los clientes deben instalar primero 3.8 y luego SP 3.8.5. | [Notas de la versión 3.8.x](https://helpx.adobe.com/xml-documentation-for-experience-manager/release-note/release-notes-xml-documentation-solution-3-8.html) | **No UUID** <br> AEM 6.5 SP9 o SP8 <br> AEM 6.4 SP8 <br> AEM 6.3 SP3 <br><br> **UUID** <br> AEM 6.5 SP9 o SP8 | **No UUID**: <br> **AEM 6.5** <br> [3.8.5 SP](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8-5/com.adobe.fmdita-6.5-hotfix-3.8.5.2.zip) <br>[3,8](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8/com.adobe.fmdita-6.5-3.8.166.zip)<br> **AEM 6.4** <br> [3.8.5 SP](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8-5/com.adobe.fmdita-6.4-hotfix-3.8.5.1.zip) <br>[3,8](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8/com.adobe.fmdita-6.4-3.8.166.zip) <br> **AEM 6.3** <br> [3.8.5 SP](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8-5/com.adobe.fmdita-6.3-hotfix-3.8.5.1.zip) <br>[3,8](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8/com.adobe.fmdita-6.3-3.8.166.zip) <br><br> **UUID** <br>**AEM 6.5** <br> [3.8.5 SP](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8-5uuid/com.adobe.fmdita.uuid-6.5-hotfix-3.8.5.2.zip) <br> [3.8](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8uuid/com.adobe.fmdita.uuid-6.5-3.8.168.zip) |
