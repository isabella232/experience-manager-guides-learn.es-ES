---
title: La API de REST funciona con atributos condicionales
description: Obtenga información acerca de la API de REST para trabajar con atributos condicionales
source-git-commit: fad5049962f258bbe59c7d172436d82b3d6cd68f
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 2%

---


# La API de REST funciona con atributos condicionales {#id175UB30E05Z}

La siguiente API de REST permite agregar atributos condicionales en un perfil de carpeta.

## Añadir un atributo condicional en un perfil de nivel de carpeta

Método de POST que agrega atributos condicionales a un perfil determinado de nivel de carpeta.

**URL de solicitud**:\
http://*&lt;aem-guides-server>*: *&lt;port-number>*/bin/fmdita/folderprofiles

**Parámetros**:\
|Nombre|Tipo|Descripción|Requerida| ----|----|--------|----------- |`:operation`|Cadena|Sí|Nombre de la operación a la que se llama. El valor de este parámetro es ``ADDATTRIBUTEPROFILES``. <br> **Nota:** El valor distingue entre mayúsculas y minúsculas.| |`profilename`|Cadena|Sí|Nombre para mostrar del perfil de nivel de carpeta en el que se deben agregar los atributos condicionales.| |`conditionalprofiles`|Matriz JSON|Sí|Matriz JSON que consta del nombre y los valores del atributo condicional. El siguiente fragmento de código de ejemplo muestra la matriz JSON con dos atributos: `platform` y `product` con varios valores asignados a ellos.|

```JSON
[  {    name: "platform",    
        values: [       
                {value: "win", label: "Windows"},       
                {value: "mac", label: "Mac OS"}    
                ]},
                {    
                    name: "product",    
                    values: [      
                        {value: "aem_1", label: "AEM 6.1"},     
                        {value: "aem_4,  label: "AEM 6.4"}  
                        ]  
                }]
```

**Valores de respuesta**:\
Devuelve una respuesta HTTP 200 \(Correcto\).

