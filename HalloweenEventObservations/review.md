# 🎬 Observaciones del Vídeo [How to Make Halloween Landing page Using HTML CSS JS | For Beginners](https://www.youtube.com/watch?v=i5d1RO48chI&list=PLasZMtSCguZa9zC4rVX-g2_B2DrHRUFeC&index=7)

![Halloween page preview](img/HalloweenPagePreview.png)

## 🖼️ Vista previa

En la vista previa del proyecto al inicio del vídeo creo que lo más complejo para mi es la sensivilidad de la barra de navegación. También noto que tiene el código HTML bien comentado.

## 😇 El creador en verdad quiere ayudar

Sadee deja un archivo de inicio para facilitarnos el comienzo del proyeto y en el se aprecia mucho de su organización. La funcionalidad del archivo parace ser la de contener código para copiarlo y pegarlo.

## ✏️ Secciones comentadas

Veo que en el archivo CSS tiene las partes bien comentadas y eso me sorprende porque si bien sé que hay que ser ordenado no creí que se pudiera serlo tanto, supongo que cuanto más mejor.

## 🖋️ Incluso tiene distintas formas de comentar

```css
/*----------------*\
    #TÍTULOS
\*----------------*/
/*
* subtítulos
*/
```

**Ejemplo de uso:**

```css
/*---------------------------*\
    #CUSTOM PROPERTY
\*---------------------------*/
:root{

    /**
    * colors
    */

    --primary-color: lightblue;
    --secondary-color: lightcoral;
}
```

## 📄 Su planeación

Me llama la atención que se pasa más de 10mins de vídeo solo preparando los estilos.
Definitivamente voy a usar ese archivo de ayuda, son muchas cosas que configura antes de empezar. No lo haré sin antes revizar cada cosa y saber que hace.

Incluso le aplica varios estilos por defecto a elementos que todavía no tiene en su archivo HTML, no solo los clasicos margin: 0; padding: 0; y box-sizing: border-box;

## 🛵 En Marcha

### 🖊️ `<title>` 🆚 `<meta name="title">`

Ya realizando el proyecto me llama la atención que tenga la etiqueta `<title>` y también `<meta name="title">` así que le pregunté  a Copilot y me dijo que se hace por SEO ya que si bien los usuarios pueden leer `<title>` en la pestaña del navegador estos últimos lo hacen con `<meta name="title">` así como las redes sociales.

### 🌲 Favicon: icon 🆚 shortcut icon

Tenía curiosidad por saber el por qué no simplemente en el atributo **rel** usaba `icon` en vez de `shortcut icon` y pasa que este último era la forma antigua debido a que algunos navegadores no interpretaban bien **icon**, pero actualmente todos lo hacen así que ya no es necesario. También aprendí que es bueno usar el atributo **type** para especificar el tipo de archivo y que el navegador no "advine".

### 📂 ./favicon.svg 🆚 favicon.svg

También vi que para colocar la ruta del archivo svg uso una ruta explícita con `./` en vez de una relativa simplemente poniendo el nombre del archivo sabiendo que este está en el mismo directorio de indxe.html así que lo deje con la ruta relativa ya que implicitamente estoy declarando la busqueda en la misma carpeta.

### 🏹 `<script defer>` 🆚 `<script>` al final del HTML

Esto es una práctica que ya venia haciendo desde que lo descubrí. Pasa que normaalmente se declara la conexión entre es script y el archivo HTML al final de este último, pero yo siempre he pensado que se ve más ordenado `<head>` así cuando traté de usarlo allí me di cuenta de que en mi archivo JavaScript no se estabn encontrando los elemento del DOM que estaba referenciando porque el script se estaba compilando y ejecutando antes de que se hiciera el árbol del DOM preguntandole a ChatGPT supe del atributo boolano **defer** cuya mera presencia indica que el navegador cargue el script en paralelo, pero lo ejecute después de creado el árbol del DOM. Esa fue la primera vez que supe de atributos booleanos, ya después supe de `async` que aunque nunca lo he usado sé que también carga el script en paralelo, pero lo ejecuta tan pronto como termina independientemente de si existe o no DOM.

### ✍️ Custom propertys en `<html>` 🆚 `:root`

`:root` es la convención estándar para declarar variables CSS globales porque:

- Tiene mayor especificidad que `html` para estilos directos
- Funciona en cualquier tipo de documento (HTML, XML, SVG)
- Es más legible y todos lo reconocen como el lugar de variables globales

Las variables CSS se heredan y pueden sobrescribirse localmente en cualquier selector, independientemente de si se declaran en `:root` o `html`.
