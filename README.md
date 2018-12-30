# css-flexbox-gridlayout
Use cases CSS Flexbox and CSS Grid Layout

## Flexbox

- Exercises from [Diana Aceves' course in Escuela IT](https://escuela.it/cursos/taller-profesional-flexbox).

The first 3 exercises were exported as zip from my [Codepen collection](https://codepen.io/collection/DQKNRK/). Each one had this setting:

  - HTML without Preprocessor.
  
  - CSS with SCSS Preprocessor and Vendor Prefixing Autoprefixer.

  - External stylesheets:

    - [Diana CSS Normalize](https://codepen.io/diana_aceves/pen/QELXOY)

    - [Font Awesome](https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css)

### Exercise 1

  ![Exercise 1 image](images/flexbox/exercise-1.png?raw=true)

  - Exercise 1 without Flexbox

    - [Code](flexbox/1.exercise-1-without-flexbox)

    - [Demo](https://cristinafsanz.github.io/css-flexbox-gridlayout/flexbox/1.exercise-1-without-flexbox/index.html)

  - Exercise 1 with Flexbox

    - [Code](flexbox/2.exercise-1-with-flexbox)

    ```
    .total {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    ```

    - [Demo](https://cristinafsanz.github.io/css-flexbox-gridlayout/flexbox/2.exercise-1-with-flexbox/index.html)

### Exercise 2

  ![Exercise 2 image](images/flexbox/exercise-2.png?raw=true)

  - [Code](flexbox/3.exercise-2-flexbox)

    ```
    .menu-option {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    ```

    - [Demo](https://cristinafsanz.github.io/css-flexbox-gridlayout/flexbox/3.exercise-2-flexbox/index.html)

### Exercise 3

  ![Exercise 3 image](images/flexbox/exercise-3.png?raw=true)

  - Exercise 3 without Flexbox

    - [Code](flexbox/4.exercise-3-without-flexbox)

    - [Demo](https://cristinafsanz.github.io/css-flexbox-gridlayout/flexbox/4.exercise-3-without-flexbox/index.html)

  - Exercise 3 with Flexbox

    - [Code](flexbox/5.exercise-3-with-flexbox-vertical-horizontal-centering)

    ```
    body {
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .blue-box {
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
    }
    ```

    - [Demo](https://cristinafsanz.github.io/css-flexbox-gridlayout/flexbox/5.exercise-3-with-flexbox-vertical-horizontal-centering/index.html)

### Exercise 4: Header Throne

  [Inspiration](http://throne.stonedthemes.com/)

  ![Exercise 4 image](images/flexbox/exercise-4.png?raw=true)

  - [Code](flexbox/6.exercise-4-with-flexbox-header-with-menu)

  ```
  header {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  nav ul {
    display: flex;
  }
  nav li {
    padding: 0 1em;
  } 
  ```

  - [Demo](https://cristinafsanz.github.io/css-flexbox-gridlayout/flexbox/6.exercise-4-with-flexbox-header-with-menu/index.html)

### Item properties

[Class: Item properties](https://escuela.it/cursos/taller-profesional-flexbox/clase/practica-y-ejemplos-ii)

- Cross size: Eje secundario / Cross axis
  - Si se ha definido (por width o por height), ese tamaño se respetará.
  - Si no se ha definido, se utilizará todo el espacio disponible (STRETCH).
  - Si no se ha definido y se utiliza un valor diferente de stretch para align-content o align-items en el contenedor, se tomará el tamaño de su contenido.

- Main size: Eje principal / Main axis
  - Si no se ha definido el tamaño, se calculará según el contenido.
  - si se ha definido (por width o height) éste podría respetarse, podría encogerse o crecer. // hace caso o no!
    - Si no hay espacio suficiente, por defecto los items encogen para caber dentro del contenedor.
    - Si hay espacio suficiente, por defecto no crecen, porque Flexbox quiere que le digamos cómo queremos que crezcan.

- Flex-basis: Tamaño base que se considera para los cálculos, no el tamaño definitivo.
  - Siempre gana a width o height.
  - No siempre controla el ancho, en flex-direction: column, flex-basis controla el alto.
  - Sólo funciona sobre el main-axis.
  - Flex-basis gana: si utilizo la propiedad Flex que es el shorhand de flex-grow, flex-shrink, flex-basis sobreescribiré el width sin darme cuenta.
  - En responsive es fácil que pase de flex-direction: row a column, si establezco width tendré problemas.

- Flex-grow (crecimiento)
  - Controla cuánto crece un elemento para rellenar el espacio sobrante.
  - Sólo se aplica si hay espacio disponible.
  - Es un número positivo -> unidades que crecerá.
    - Unidad = Espacio disponible / suma de flex-grows en la misma línea.
      - Que se coja el doble de hueco por ej. al usar flex-grow: 2 / flex-grow: 1. No es que una sea el doble del otro.
  - Por defecto flex-grow: 0 // no crece

- Flex-shrink (estrechamiento)
  - Si el espacio disponible es negativo (el tamaño del contenedor es menor a la suma de los tamaños de los items), por defecto los items se encogen en proporciones iguales para caber en una sola línea, pero respetando el contenido o si tiene establecido min-width o min-height.
    - Unidad = Espacio disponible (será negativo) / suma de flex-shrink en la misma línea.
  - Por defecto flex-shrink: 1 // si lo necesita, encoger
    - flex-shrink: 0 // no encoge. El que más se utiliza.
    - flex-shrink: 3 // encogerá en mayor proporción si lo necesita (al tripe de velocidad)

### Exercise 5

![Exercise 5 image](images/flexbox/exercise-5.png?raw=true)

  - [Code](flexbox/7.exercise-5-search-box)

    ```
    .input-wrapper {
      display: flex;
    }
    input {
        flex-grow: 1;
    }
    ```

  - [Demo](https://cristinafsanz.github.io/css-flexbox-gridlayout/flexbox/7.exercise-5-search-box/index.html)

### Exercise 6

![Exercise 6 image](images/flexbox/exercise-6.png?raw=true)

Si hay contenido mayor al alto hará scroll y el footer se mantiene abajo y si no lo hay también.

  - [Code](flexbox/8.exercise-6-sticky-footer)

    ```
    .app {
      min-height: 100vh;
      display: flex;
      flex-direction: column;
    }
    main {
      flex-grow: 1;
    }
    ```

  - [Demo](https://cristinafsanz.github.io/css-flexbox-gridlayout/flexbox/8.exercise-6-sticky-footer/index.html)

### Exercise 7

![Exercise 7 image](images/flexbox/exercise-7.jpg?raw=true)

  - [Code](flexbox/9.exercise-7-fixed-header-footer)

    ```
    .app {
      height: 100vh;
      display: flex;
      flex-direction: column;
    }
    main {
      flex-grow: 1;
      overflow: auto;
    }
    header,
    footer {
      height: 7rem;
      flex-shrink: 0;
    }
    ```

  - [Demo](https://cristinafsanz.github.io/css-flexbox-gridlayout/flexbox/9.exercise-7-fixed-header-footer/index.html)

### Exercise 8

Main no debería contener navs, footer...por semántica. Se va usar por eso un div.

![Exercise 8 image](images/flexbox/exercise-8.jpg?raw=true)

  - [Code](flexbox/10.exercise-8-holy-grail-layout)

    ```
    .app {
      height: 100vh;
      display: flex;
      flex-direction: column;
    }
    header,
    footer {
      height: 7rem;
      flex-shrink: 0;
    }
    #main {
      flex-grow: 1;
      display: flex;
    }
    nav,
    aside {
      flex-basis: 15%;
    }
    article {
      flex-grow: 1;
      overflow: auto;
    }
    ```

  - [Demo](https://cristinafsanz.github.io/css-flexbox-gridlayout/flexbox/10.exercise-8-holy-grail-layout/index.html)

### Exercise 9

Mejor empezar con mobile (mobile first) aunque aquí se haga al revés.

![Exercise 9 image](images/flexbox/exercise-9.jpg?raw=true)

  - [Code](flexbox/11.exercise-9-holy-grail-layout-responsive)

    ```
    @media screen and (max-width: 39em){
      #main {
        flex-direction: column;
      }
      nav {
        min-height: 4rem
      }
    }
    ```

  - [Demo](https://cristinafsanz.github.io/css-flexbox-gridlayout/flexbox/11.exercise-9-holy-grail-layout-responsive/index.html)

### Exercise 10

![Exercise 10 image](images/flexbox/exercise-10.png?raw=true)

  - [Code](flexbox/12.exercise-10-list-items)

    ```
    .store {
      display: flex;
    }
    .circle {
      flex-shrink: 0;
    }
    .next {
      align-self: center;
    }
    .store-id {
      flex-basis: 20%;
      flex-shrink: 0;
    }
    .address-tpv {
      flex-grow: 1;
    }
    ```

  - [Demo](https://cristinafsanz.github.io/css-flexbox-gridlayout/flexbox/12.exercise-10-list-items/index.html)

### Exercise 11

![Exercise 11 image](images/flexbox/exercise-11.jpg?raw=true)

  - [Code](flexbox/13.exercise-11-box-columns-inside)

    ```
    .row {
        display: flex;
        justify-content: space-between;
    }
    .info-box {
        flex-basis: 44%;
        display: flex;
        flex-direction: column;
    }
    .text-container {
        flex-grow: 1;
    }
    header {
        display: flex;
    }
    .title {
        flex-grow: 1;
    }
    ```

  - [Demo](https://cristinafsanz.github.io/css-flexbox-gridlayout/flexbox/13.exercise-11-box-columns-inside/index.html)

### TODO: 
Falta por hacer la [última clase](https://escuela.it/cursos/taller-profesional-flexbox/clase/practicas-y-ejemplos-iv) a partir de minuto 47.

## CSS Grid Layout

- [Workshop Rock' n' Grid Diana Aceves](https://www.youtube.com/watch?v=p7oXrr9yjXY&feature=youtu.be)

- [Demos Codepen](https://codepen.io/collection/DLWVMR/)

- Designs: https://www.swissted.com/.

### [Demo 1](https://youtu.be/p7oXrr9yjXY?t=558)

  ![Demo 1 image](images/gridlayout/demo-1.png?raw=true)

  - [Code](gridlayout/demo-1-pet-shop-boys)

  - [Demo](https://cristinafsanz.github.io/css-flexbox-gridlayout/gridlayout/demo-1-pet-shop-boys/index.html)

  - Notes:

    - Grid 4 rows and 8 columns. 11 items in total.

      - `grid-template-rows: 4rem 4rem 4rem 4rem`: 4 rows with 4 rem 
        
        - same as `grid-template-rows: repeat(4, 4rem)`

    - At the beginning (add numbers to display them better): 
    ```
    1 2 3 4 5 6 7 8
    9 10 11
    ```

    - Item 2: `grid-column: 1`: Item 2 in line 1 (better set only the needed ones and with columns)
    ```
    1
    2 3 4 5 6 7 8 9
    10 11
    ```

    - In this case: Only is needed to change 1 coordinate for 3 items
    ```
    1
    2 
    3 
    4 5 6 7 8 9 10 11
    ```

    - After all changes remove numbers
    
### [Demo 2](https://youtu.be/p7oXrr9yjXY?t=2198)




