---
title: Función de publicación de PDF nativo | Trabajar con estilos de barras de cambios personalizados
description: Aprenda a aplicar estilos en las barras de cambios.
source-git-commit: 79de97e667bffae8d120deee68a0a82011047cf5
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Trabajar con estilos de barras de cambios personalizados

Una barra de cambios es una línea vertical que identifica visualmente el contenido nuevo o revisado. AEM guías le permite mostrar una barra de cambios a la izquierda del contenido modificado dentro de los temas y también los temas modificados en la tabla de contenido de la salida del PDF.

Para obtener más información sobre cómo mostrar la barra de cambios, consulte *Crear PDF con barra de cambios entre versiones publicadas* configurar en
[Salida del PDF de publicación](../web-editor/native-pdf-web-editor.md).

## Se ha cambiado el contenido de los temas

La barra de cambios aparece a la izquierda del contenido en los temas que se han insertado, cambiado o eliminado.

Puede modificar los siguientes estilos para mostrar el contenido modificado y entre con las barras de cambios.


>[!NOTE]
>
>Estos estilos forman parte de `layout.css` y puede editarlos según sea necesario.

Por ejemplo, puede utilizar el atributo de color en la variable `.inserted-block` para definir la forma en que aparece el contenido insertado en la salida del PDF publicado.


```css
...
.inserted-block { 
  color: #2ECC40; 
  display: inline; 
  -ro-comment-content: " "; 
  -ro-comment-style: underline; 
  -ro-comment-title: "Inserted"; 
  -ro-comment-date: attr(data-time); 
  -ro-comment-dateformat: "yyyy/dd/MM HH:mm:ss"; 
} 
...
```

Del mismo modo, puede usar la variable `.deleted-block` para definir la forma en que aparece el contenido eliminado en la salida del PDF publicado.

```css
...
.deleted-block { 
  display: inline; 
  color: #FF6961; 
  text-decoration: line-through; 
  -ro-comment-content: " "; 
  -ro-comment-style: strikeout; 
  -ro-comment-title: "Deleted"; 
  -ro-comment-date: attr(data-time); 
  -ro-comment-dateformat: "yyyy/dd/MM HH:mm:ss"; 
} 
...
```

Puede usar `.inserted-change-bar` y `.deleted-change-bar` para modificar el aspecto de las barras de cambios que aparecen a la izquierda del contenido actualizado.

Por ejemplo, puede utilizar `-ro-change-bar-color` atributo en `.inserted-change-bar` estilo para mostrar la barra de cambios insertada en color verde. También puede utilizar `-ro-change-bar-color` atributo en `.deleted-change-bar` estilo para mostrar la barra de cambios eliminada en color rojo.

```css
...
.inserted-change-bar { 
  -ro-change-bar-color: #2ECC40; 
} 

.deleted-change-bar { 
  -ro-change-bar-color: #FF6961; 
  } 
...
```

<img src="./assets/changed-bar-content.png" alt="Se ha cambiado el contenido del tema de la barra" width="500">

## Tema cambiado en la Tabla de contenido (TOC)

También puede añadir una barra de cambios a la izquierda de los temas modificados en la tabla de contenido de la salida del PDF. Puede usar `-ro-change-bar-color` en la variable `.changed-topic` estilo para agregar una barra de cambios en el color que elija para los temas actualizados en la lista de TDC.

Por ejemplo, puede agregar una barra de cambio de color verde.

```css
...
.changed-topic { 
 -ro-change-bar-color: #2ECC40; 
}  
...
```


Muestra una barra de cambios verde en todos los temas de la tabla de contenido en los que se han actualizado algunos. Puede hacer clic en el tema modificado en la tabla de contenido y ver los cambios detallados.

<img src="./assets/changed-bar-TOC.png" alt="TDC de barra modificada" width="500">
