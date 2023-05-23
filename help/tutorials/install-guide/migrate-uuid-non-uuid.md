---
title: Migración de contenido de no UUID a UUID
description: Descubra cómo migrar contenido de No UUID a UUID
source-git-commit: 5ac066bb8db32944abd046f64da11eeb1bdbe467
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%

---


# Migración de contenido de no UUID a UUID {#id226TI0U20XA}

>[!IMPORTANT]
>
> Puede migrar el contenido que no sea UUID al servidor UUID. AEM Para migrar al servidor UUID, debe tener instalado un servidor que no sea UUID con guías de usuario versión 4.0 de las guías de usuario.

Siga estos pasos para migrar el contenido que no es UUID:

>[!NOTE]
>
> Cada paso es crucial y la falta de cualquiera de los pasos puede conducir a datos de servidor fallidos o dañados. Asegúrese de completar todos los pasos.

1. Asegúrese de que **Activar iniciadores de flujo de trabajo de procesamiento posterior** in *com.adobe.fmdita.config.ConfigManager* y **Habilitar procesamiento posterior de la versión** in *com.adobe.fmdita.postprocess.version.PostProcessVersionObservation* están activadas.

   ```http
   http://<server name>:<port>/system/console/configMgr/com.adobe.fmdita.config.ConfigManager
   ```

1. Instale la versión UUID de la siguiente versión principal sobre la versión que no sea UUID. Por ejemplo, si utiliza la versión 4.0 sin UUID, debe instalar la versión 4.1 de UUID.

1. En la pestaña Lanzador, deshabilite los siguientes flujos de trabajo y cualquier otro flujo de trabajo que se ejecute en /content/dam mediante lanzadores en `http://localhost:4502/libs/cq/workflow/content/console.html`:

   - **Recurso de actualización DAM** workflow
   - **Reescritura de metadatos DAM** workflow

1. Deshabilitar **Activar iniciadores de flujo de trabajo de procesamiento posterior** in *com.adobe.fmdita.config.ConfigManager* y deshabilitar **Habilitar procesamiento posterior de la versión** in *com.adobe.fmdita.postprocess.version.PostProcessVersionObservation*.

   ```http
   http://<server name>:<port>/system/console/configMgr/com.adobe.fmdita.config.ConfigManager
   ```

1. Añadir un registrador independiente para `com.adobe.fmdita.uuid.upgrade.UuidUpgrade.`

   La respuesta del explorador también está disponible en /content/uuid-upgrade/logs.

1. Ejecute la consulta determinada en una carpeta con datos más pequeños con `doReviews=false` antes de ejecutarlo en / content/dam: `http://localhost:4502/bin/dxml/uuid_upgrade?root=/content/dam/test&doReviews=false`

   >[!TIP]
   >
   >  Puede comprobar si todos los archivos de la carpeta se han actualizado correctamente y si todas las características funcionan únicamente para esa carpeta.

**Parámetros para la consulta:**

    - `root`: Carpeta raíz donde la actualización debe realizarse \(Utilice /content/dam para todo el repositorio.\)
    - &quot;doReviews&quot;: true/false \(Si las revisiones deben actualizarse o no. El valor predeterminado es false.\)
    - &quot;doBaselines&quot;: true/false \(Si las líneas de base deben actualizarse o no. El valor predeterminado es True.\)
    - `processLevel`: -1\(error sin restauración\), 0\(error con restauración\), 1\(error con errores\), 2\(actualizado correctamente\) \(Al reintentar el script tras el error, solo se procesarán de nuevo los archivos con &quot;fmUpgradeStatus&quot; &lt;= processLevel; de lo contrario, se ignorará. El valor predeterminado es 1.\)
    - `ignoreImageVersions`: true/false \(Ignora el procesamiento de las versiones de la imagen. El valor predeterminado es false.\)
    >[!NOTA]
    >
    > Podemos ejecutar la migración de contenido en el nivel de carpeta o en el contenido completo/dam o en la misma carpeta \(volver a ejecutar migración\).

1. Una vez que el servidor se haya migrado correctamente, habilite los siguientes flujos de trabajo y posprocesamiento para seguir trabajando en el servidor:

   - **Recurso de actualización DAM** workflow
   - **Metadatos DAM** workflow

>[!NOTE]
>
> Si algunos archivos no se procesan o están dañados antes de la migración, permanecerán dañados incluso después de la migración.

