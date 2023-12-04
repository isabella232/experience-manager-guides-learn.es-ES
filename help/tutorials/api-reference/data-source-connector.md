---
title: API de REST para registrar un conector de fuente de datos
description: Obtenga información acerca de la API de REST para registrar un conector de fuente de datos
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# API de REST para registrar un conector de fuente de datos {#id236LG0Y0CXA}

La siguiente API de REST le permite registrar un conector de fuente de datos.

## Registrar un conector de origen de datos

Método de GET que registra un conector de origen de datos.

**URL de solicitud**:
`http://server:port/bin/guides/v1/konnect/config/register?path=<uploaded file path>`

**Parámetro**: |Nombre|Tipo|Descripción|Requerida| ----|----|--------|----------- |`path`AEM |Cadena|Sí|Cadena que señala a una ruta de acceso en el repositorio de. Puede ser una ruta en el `/content/dam or /var/dxml`.|

**Ejemplo**:\
`http://host:4502/bin/guides/v1/konnect/config/register?path=/var/dxml/konnect/jira.json`
