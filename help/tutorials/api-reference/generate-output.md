---
title: API basada en Java para trabajar con la generación de resultados
description: Obtenga información acerca de la API basada en Java para trabajar con la generación de resultados
source-git-commit: fad5049962f258bbe59c7d172436d82b3d6cd68f
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 0%

---


# API basada en Java para trabajar con la generación de resultados {#id175UB30E05Z}

La siguiente API basada en Java permite generar resultados para un mapa DITA. Esta API está disponible en forma de paquete. Debe incluir este paquete en su código para utilizar estas API.

Detalles del paquete:

- ID de grupo: **com.adobe.fmdita**

- ID del artefacto: **api**

- Versión: **3,4**

- Paquete: ****com.adobe.fmdita.api.maps****

- Detalles de la clase:

  ```JAVA
  public class **PublishUtils** extends Object
  ```

  El **`PublishUtils`** contiene un método para generar resultados para uno o varios ajustes preestablecidos de salida.


## Generar salida

El ``generateOutput`` Este método genera la salida de un fichero de mapa DITA utilizando los ajustes preestablecidos de salida especificados.

**Sintaxis**:

```JAVA
public static void generateOutput(Session session,
String sourcePath,
String outputName)
throws GuidesApiException
```

**Parámetros**: |Nombre|Tipo|Descripción| |----|----|-----------| |`session`|javax.jcr.Session|Una sesión JCR válida.| |``sourcePath``AEM |Cadena|Ruta de acceso \(en el repositorio de\) del archivo de asignación DITA para el que se debe generar la salida.| |``outputName``|Cadena|Nombre del ajuste preestablecido de salida\(s\) que se va a utilizar para generar la salida. Se pueden especificar varios ajustes preestablecidos de salida utilizando un delimitador de barra vertical \(&quot;\|&quot;\), por ejemplo `aemsite\|pdfoutput`.|

**Excepción**: lanzamientos ``javax.jcr.RepositoryException``, `java.io.IOException`, y `java.lang.Exception`.

