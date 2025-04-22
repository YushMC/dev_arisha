# Página web de Arisha

Este sitio web utiliza astro como framework principal y css, la idea es en usar el meno js posible.

> [!NOTE]
> Cuenta con carrusel de imagenes utilizado la librería **swiper js** y un complemeto con **Vue JS**

## Instalación

### Requisitos de instalación

- Node JS
- Editor de código

### Proceso de instalación

Para iniciar, es necesario clonar este repositorio e instalar las dependencias con:

`npm install`

## Colocar informacion

Dentro de la carpeta `assets/jsons`, existen 6 archivos `.json` donde se debe colocar la información acerca de la persona, imagenes, descripciones, testimonios, contacto y redes sociales, así como las etiquetas SEO.

> [!NOTE]
> **El proyecto debe funcionar coorrectamente con esta configuración**. Pero si hay inconvenientes, a continuación se menciona la estructura interna y otras funciones.

## Desarrollo

### Estructura de archivos

Los archivos principales son:

- **Assets/**: que contienen los archivos de estilos css generales en styles/main.css

- **Components/**: fragmentos de código que pueden ser reutilizados en otros archivos. **Estos archivos estan agrupados por página:** components/index, los que estan fuera son los más generales.

- **Layouts/**: Es el archivo base de cada página.

- **Pages/**: Al colocar un archivo, este se convierte de manera inmediata en una ruta. _los archivos se referencian como un link de html normal_, `href="[nombreDelArchivo]"`

## Notas adicionales

los archivos de estructura como lo es: **layouts**, **componentes** y **paginas** deben llevar el tipo de archivo `.astro`

los archivos `.astro` no es necesario agregarlos a un template para los HTML, los scripts pueden estar dentro de una etiqueta `<script></script>` o entre **3 guiones medios** `---`

Los estilos puden estar dentro de cada archivo `.astro` y es solo con colocar la etiqueta `<style></style>`

Los archivos publicos se encuentran en la carpeta `public/`

# Producción

para generar los archivos estáticos, se debe ejecutar el comando

`npm run build`
