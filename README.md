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

### Exercise 4 (not finished)

  ![Exercise 4 image](images/flexbox/exercise-4.png?raw=true)

  - [Code](flexbox/6.exercise-4-with-flexbox-header-with-menu)

  - [Demo](https://cristinafsanz.github.io/css-flexbox-gridlayout/flexbox/6.exercise-4-with-flexbox-header-with-menu/index.html)


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




