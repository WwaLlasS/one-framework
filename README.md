Framework CSS
=============

 ### Elements

- container 960px
  - Grid 12 columns
  - row container
  - column container
- show only mobile or show only desktop class
- Navigation bar
- Base styles
  - Table styles
  - Form elements
  - headers
  - Buttons
  - Lists
  - code
  - anchor
- align-text class
- Float class
- z-index class
- Footer

#### Contenedor principal de 960px y Grid System de 12 columnas

**Main container**

El Framework cuenta con un contenedor principal ajustado para tener 960px de ancho y posicionarce en el centro de la pantalla, para obtener este contenedor basta con utilizar la clase `container` en una etiqueta `<div>` o  `<main>`.

~~~
<main class="container">
  <!-- Contenido principal de el sitio -->
</main>
~~~

**Grid System**

El Grid system esta hecho a 12 columnas y para poder usarlo tenemos que declarar un contenedor `<div>` con la clase `row` el cual sera nuestra fila, y dentro del contenedor podemos declarar nuestras columnas, ejemplo:

~~~
<main class="container"> <!-- Contenedor principal de 960px -->
  <div class="row"> <!-- Contenedor fila -->
    <div class="col sm-12 md-1 lg-1">1</div> <!-- Columnas -->
    <div class="col sm-12 md-1 lg-1">2</div>
    <div class="col sm-12 md-1 lg-1">3</div>
    <div class="col sm-12 md-1 lg-1">4</div>
    <div class="col sm-12 md-1 lg-1">5</div>
    <div class="col sm-12 md-1 lg-1">6</div>
    <div class="col sm-12 md-1 lg-1">7</div>
    <div class="col sm-12 md-1 lg-1">8</div>
    <div class="col sm-12 md-1 lg-1">9</div>
    <div class="col sm-12 md-1 lg-1">10</div>
    <div class="col sm-12 md-1 lg-1">11</div>
    <div class="col sm-12 md-1 lg-1">12</div>
  </div>
</main>
~~~

Como vieron en el ejemplo anterior, se hace uso de la clase `col` y la clase `lg`, la clase `col` declara que es una columna y la clase `lg` declara el tamaño de las columnas.

Para los tamaños de las columnas existen tres clases, las cuales nos permiten controlar los tamaños en base al tamaño de la pantalla del dispotivos desde donde de visualiza el sitio, la clase para dispositivos con resolucion de hasta 414px de ancho(*Smartphones*) es `sm`, para dispositivos con resolucion de hasta 768px de ancho(*Tablets*)  es `md` y para dispositivos de escritorio o laptops es `lg`.

>Nota: Recuerda que debes escribir la clase para el tamaño deseado(`sm`, `md`, `lg`) seguido de un guion y el numero de columnas que quieras que ocupe tu contenedor.

~~~
<main class="container"> <!-- Contenedor principal de 960px -->
  <div class="row">
    <div class="col sm-12 md-4 lg-1 text-center">sm-12 md-4 lg-1</div>
    <div class="col sm-12 md-4 lg-1 text-center">sm-12 md-4 lg-1</div>
    <div class="col sm-12 md-4 lg-1 text-center">sm-12 md-4 lg-1</div>
    <div class="col sm-12 md-4 lg-1 text-center">sm-12 md-4 lg-1</div>
    <div class="col sm-12 md-4 lg-1 text-center">sm-12 md-4 lg-1</div>
    <div class="col sm-12 md-4 lg-1 text-center">sm-12 md-4 lg-1</div>
    <div class="col sm-12 md-4 lg-1 text-center">sm-12 md-4 lg-1</div>
    <div class="col sm-12 md-4 lg-1 text-center">sm-12 md-4 lg-1</div>
    <div class="col sm-12 md-4 lg-1 text-center">sm-12 md-4 lg-1</div>
    <div class="col sm-12 md-4 lg-1 text-center">sm-12 md-4 lg-1</div>
    <div class="col sm-12 md-4 lg-1 text-center">sm-12 md-4 lg-1</div>
    <div class="col sm-12 md-4 lg-1 text-center">sm-12 md-4 lg-1</div>
  </div>
  <div class="row">
    <div class="col sm-12 md-4 lg-4 text-center">sm-12 md-4 lg-4</div>
    <div class="col sm-12 md-4 lg-4 text-center">sm-12 md-4 lg-4</div>
    <div class="col sm-12 md-4 lg-4 text-center">sm-12 md-4 lg-4</div>
  </div>
  <div class="row">
    <div class="col sm-12 md-6 lg-3 text-center">sm-12 md-6 lg-3</div>
    <div class="col sm-12 md-6 lg-9 text-center">sm-12 md-6 lg-9</div>
  </div>
  <div class="row">
    <div class="col sm-12 md-2 lg-3 text-center">sm-12 md-2 lg-3</div>
    <div class="col sm-12 md-4 lg-3 text-center">sm-12 md-4 lg-3</div>
    <div class="col sm-12 md-3 lg-3 text-center">sm-12 md-3 lg-3</div>
    <div class="col sm-12 md-3 lg-3 text-center">sm-12 md-3 lg-3</div>
  </div>
</main>
~~~

Tambien cuenta con un contenedor de columna el cual muestra su contenido de arriba hacia abajo, lo contrario al contenedor de fila, el cual muestra su contenido de izquierda a derecha, para usarlo basta con utilizar la clase `column` en lugar de `row` en un contenedor `<div>`.

>Nota: Si quieres revertir la direccion en la que se muestra el contenido tanto en contendor de columna como en el de fila, puedes usar la clase `reverse`, esto hara que por ejemplo, en el contenedor de fila, el contenido se muestre de derecha a izquierda y no de izquierda a derecha a como normalmente lo hace.

~~~
<main class="container">
  <div class="column">
    <div>Item 1</div>
    <div>Item 2</div>
    <div>Item 3</div>
  </div>
</main>

<main class="container">
  <div class="column reverse"><!-- Este mostra primero el item 3, despues el item 2 y al final el item 1 -->
    <div>Item 1</div>
    <div>Item 2</div>
    <div>Item 3</div>
  </div>
</main>
~~~
***
#### Mostrar solo en moviles o Solo en Escritorio

Tambien existen unas clases con las cuales nosotros podremos decidir que elementos mostrar segun el dispositivo desde donde se visualiza el sitio.

**Solo moviles**

Para mostrar cierto contenido solo si se visualiza desde pantallas con resoluciones igual o menores a 768px de ancho podemos usar la clase `show-only-mobile`, y basicamente el contenido solo se mostrara en tabletas y Smartphones.

**Solo escritorio**

Para decir que contenido solo se debe mostrar en pantallas con resoluciones mayores a 768px de ancho, podemos usar la clase `show-only-desktop`.
***
#### Barra de navegacion.

Tambien cuenta con una barra de navegacion ya lista, lo unico que debemos hacer es escribir la siguien estructura:

~~~
<nav class="navbar">
  <a href="#" class="logo">Brand Logo</a>
  <ul>
    <li><a href="#">Inicio</a></li>
    <li><a href="#">Nosotros</a></li>
    <li><a href="#">Contacto</a></li>
    <li><a href="#">FAQ</a></li>
  </ul>
</nav>
~~~

Existen tres clases mas que le podemos agregar a la etiqueta `<nav>`, estas clases son:

- `fixed`: Con esta clase podemos dejar la barra de navegacion fija en la parte superior de la ventana.
- `gray`: Esta clase nos sirve para  cambiar de color la barra de navegacion a gris.
- `reverse`: Esta clase invierte la manera en la que se muestra el contenido dentro del `<nav>.`

>Nota: si quieres utilizar la barra de navegacion fija en la parte superior, deberas dar padding superior al elemento que este despues del cierre de la barra `</nav>`.

***
#### Estilos base

Si bien el Framework utiliza *normalize.css* para normalizar los estilos en todos navegadores, tambien incluye algunos estilos base para ciertos elementos:

- Tablas
- Formularios
- Encabezados
- Botones
- Listas
- Anchor

>Nota: Al elemento `<table>` puedes agregarle la clase hover, para resaltar la fila en la que se pose el puntero del raton.

**Botones**

Tambien existen unas clases para dar diferentes colores a los botones ya que por defecto se muestran sin fondo, las clases son:

- `button-teal`
- `button-gray`
- `button-blue`
- `button-green`

>Nota: Si agregamos la clase `button` a un elemento `<div>`, este tomara la apariencia de un boton.

***

#### Alineado de texto

El framework incluye cuatro clases que nos permiten alinear el texto de una manera mas facil, estas clases son:

- `text-left`: Esta clase muestra el texto a la izquierda.
- `text-center`: Esta clase muestra el texto en el centro.
- `text-right`: Esta clase muestra el texto a la derecha.
- `text-justify`: Esta clase muestra el texto justificado.

~~~
<div class="col sm-12 md-4 lg-4">
  <span>Lorem ipsum</span>
  <p class="text-justify">
    Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
    Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
  </p>
</div>
~~~
***

#### Elementos flotantes

Tambien existen tres clases para los elementos flotantes, estas son:

- `left`: Flotar elementos hacia la izquierda.
- `right`: Flotar elementos hacia la derecha.
- `clear`: Le agrega la propiedad `clear:both;`
***

#### Z index

Podremos tambien implementar cinco clases que nos podran ayudar a definir el index de los elementos en el eje Z, estas clases son:

- `z-index-0`
- `z-index-1`
- `z-index-2`
- `z-index-3`
- `z-index-4`
***

#### Pie de pagina

Por ultimo el framework tambien cuenta con un pie de pagina listo para ser usado, unicamente tenemos que utilizar la siguiente estructura en el documento HTML:

~~~
<footer>
  <section class="row">
    <div class="col sm-12 md-4 lg-4">
      <span>Noticias</span>
      <input type="text"placeholder="Suscribete">
      <div class="button button-teal">Enviar</div>
    </div>
    <div class="col sm-12 md-4 lg-4">
      <span>Lorem ipsum</span>
      <p class="text-justify">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
        Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
      </p>
    </div>
    <div class="col sm-12 md-4 lg-4">
      <span>Social Media</span>
      <ul class="">
        <li><a href="#">Facebook</a></li>
        <li><a href="#">Twitter</a></li>
        <li><a href="#">Instagram</a></li>
        <li><a href="#">GitHub</a></li>
      </ul>
    </div>
  </section>
  <section class="row">
    <span>Copyright &copy; 2016 Copyright Holder All Rights Reserved.</span>
  </section>
</footer>
~~~
