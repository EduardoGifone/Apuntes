# CSS NOTES

***

## FONT

### Tamanio de fuente
```css 
font-size: 30px;
```

### Tipo de letra
```css
font-family: FAMILY_NAME, GENERIC_NAME;
```

### Grosor de texto
```css
font-weight: 800px;
```

### Distancia entre lineas en un bloque
```css
line-height: 25px;
```
    
### Color (texto..)
```css
color: orange;
```

## BACKGROUND

### Color del fondo
```css
background-color: green;
```
    
### Background con imagen
```css
background: url(direccion-de-la-imagen.png/jpeg/jpg);
```

### Repeat del background
```css
background-repeat: no-repeat;
```

### Posicion del fondo
```css
background-position: center;
```

### Size del background
```css
background-size: cover;
```

### Para que el fondo no se mueve cuando bajamos
```css
background-attachment: fixed;
```

### Gradiente lineal (Degradados)
```css
/*background: linear-gradient(gradient_direction, color 1, color 2, color 3, ...);*/
background: linear-gradient(90deg, red, yellow, rg(204, 204, 255));
```

### Gradiente lineal repetida
```css
background: repeating-linear-gradient(
    45deg,
    yellow 0px,
    blue 40px,
    green 40px,
    red 80px
);
```

## ALTO Y ANCHO

### Alto
```css
height: 10vh;
```

### Ancho
```css
width: 100vw;
```
    
## BORDES

### Radio deo borde
```css
border-radius: 50%;
```

### Forma larga
```css
border-color: red;
border-width: 5px;
border-style: solid;
```

### Forma corta
```css
border: red 5px solid;
```

### Borde pero sin ocupar espacio
```css
outline: red 5px solid;
```

## PADDING    
```css
padding: 10px; /*Todos los lados*/
padding: 10px 10px; /*top, botton || right, left*/
padding: 10px 4px 2px 7px; /*top, botton, right, left*/
padding-top: 5px;
padding-right: 5px; 
padding-bottom: 5px; 
padding-left: 5px;
```

## MARGIN
```css
margin: 10px; /*Todos los lados*/
margin: 10px 10px; /*top, botton || right, left*/
margin: 10px 4px 2px 7px; /*top, botton, right, left*/
margin-top: 5px;
margin-right: 5px;
margin-bottom: 5px;
margin-left: 5px;
```

## Centrar elementos en bloque horizontalmente
```css
margin: auto;
```

## UNIDADES

### Unidades absolutas
    in: pulgadas
    mm: milimetros

### Unidades relativas
    em
    rem*/

## Variables

### Crear variable
```css
--nombre-variable: gray;
```

### Utilizar variable | variable de respaldo
```css
background: var(--nombre-variable, black);
```

## Media query
``` css
@media (max-width: 350px) {
    /* TU CODIGO */
}
```

## Alineacion de contenido en un elemento en bloque*/
```css
text-align: justify;
text-align: center;
text-align: right;
text-align: left;
```

## Sombra o sombras para elementos

### Sombra para caja
```css
/*offset-x - offset-y - blur-radius - spread-radius - color*/
box-shadow: 0 10px 20px rgba(0,0,0,0.19), 0 6px 6px rgba(0,0,0,0.23);
```

### Sombra o sombras para el texto
```css
text-shadow: 0 30px 15px #FFF;
```

## Opacidad en elementos
```css
opacity: 0.7;
```

## Convertir texto (mayuscula, minuscula, etc)
```css
text-transform: lowercase;
text-transform: uppercase;
text-transform: capitalize;
text-transform: initial;
text-transform: inherit;
text-transform: none;
```

## Posicion de un elemento
```css
/*top, bottom, right, left*/
position: static; /*Defecto*/
position: relative;
position: absolute;
position: fixed;
position: sticky;
```

### Superposicion de elementos
```css
z-index: 2;
```

## Transformar elementos

### Aumentar tamanio
```css
transform: scale(2); /*ambos ejes*/
transform: scale(2, 3); /*ejes especificos*/
```

### Inclinar elemento
```css
transform: skewX(-35deg); /*eje x*/
transform: skewY(12deg); /*eje y*/
transform: skewY(-35deg, 12deg); /*ambos ejes*/
```

### Trasladar
```css
transform: translate(120px, -10px);
```

### Rotar
```css
transform: rotate(45deg);
```

## Transiciones

### Forma Larga
```css
transition-property: width;
transition-duration: 4s;    
transition-timing-function: linear;
transition-delay: 1s;
```

### Forma corta
```css
transition: all 4s linear 1s;
```

## Sobrante del bloque
```css
overflow: visible; /*Defecto*/
overflow: auto;
overflow: hidden;
overflow: scroll;
```
    
## Encajar objeto contenidos en la etiqueta img
```css
object-fit: contain;
object-fit: cover;
object-fit: fill;
```

## Pseudo-clase hover
```css
a:hover {
  color: red;
}
```

## Pseudo-elementos ::before y ::after
```css
div::before{
  content: ""
}
```

## Animaciones

### Propiedades
```css
animation-name: colorful;
animation-duration: 3s;
animation-delay: 2s;
animation-direction: reverse;
animation-fill-mode: forwards; /*Valores: none,forwards, backwards, both*/
animation-iteration-count: infinite;
animation-timing-function: linear; /*Valores comunes:ease, ease-out, ease-in, linear*/
animation-timing-function: cubic-bezier(0.25, 0.25, 075, 0.75);
```
[Pagina para ayudar a entender el cubic-bezier](https://cubic-bezier.com/#.17,.67,.83,.67*/)

### Animar
```css
@keyframes colorful {
  0% {
    background-color: blue;
  }
  100% {
    background-color: yellow;
  }
}
```

## FLEX
```css
display: flex;
```

### Direccion del flex
```css
flex-direction: column;
flex-direction: column-reverse;
flex-direction: row;
flex-direction: row-reverse;
```

### Eje central
```css
justify-content: center;
justify-content: space-between;
justify-content: space-around;
justify-content: space-evenly;
```

### Eje transversal
```css
align-items: center;
align-items: baseline;
```

### Mover elementos extra a la siguiente fila o columna
```css
flex-wrap: nowrap;
flex-wrap: wrap;
```

### FLEX-GROW FLEX-SHRINK FLEX-BASIS

#### Contraer el elemento si el contenedor flex es mas pequenio
```css
flex-shrink: 1;
```

#### Expandir el elemento si el contenedor flex es mas grande
```css
flex-grow: 2;
```

#### Establecer tamanio inicial de un elemento
```css
flex-basis: auto;
```

#### Abreviado: flex-grow flex-shrink flex-basis
```css
flex: 2 2 300px;
```

### Orden en el que apareceran los elementos
```css
order: 2;
```

### Ajustar alineacion de cada elemento individualmente
```css
align-self: center;
align-self: baseline;
```

## GRID
```css
display: grid;
```

### Columnas
```css
grid-template-columns: 2fr 30px;
grid-template-columns: repeat(2, 1fr 50px) 20px;
```

#### Espacio entre columnas
```css
grid-column-gap: 3px;
```

#### Controlar la cantidad de columnas que un elemento tendra
```css
grid-column: 1 / 3;
```

### Filas
```css
grid-template-rows: 12px 1fr;
grid-template-rows: repeat(50, 50px);
```

#### Espacio entre filas
```css
grid-row-gap: 4px;
```

#### Controlar la cantidad de filas que un elemento tendra
```css
grid-row: 2 / 5;
```

### Espacio entre filas y columnas
```css
grid-gap: 6px;
```

### Espacio entre filas y columnas de forma separada
```css
/* filas  ||  columnas*/
grid-gap: 6px 8px;
```

### Alinear la posicion del contenido dentro de una celda horizontalmente
```css
justify-self: center;
justify-self: end;
```

### Alinear la posicion del contenido dentro de una celda verticamente
```css
align-self: center;
align-self: baseline;
```

### Alinear la posicion horizontalmente en el padre
```css
justify-items: center;
```

### Alinear la posicion verticalmente en el padre
```css
align-items: center;
```

### Crear areas
```css
grid-template-areas:
  "header header header"
  "advert content content"
  "advert footer footer";
```

#### Determinar el area de un elemento
```css
grid-area: header;
```

#### En caso de no tener un grid-template-area
```css
/*grid-area: horizontal-start / vertical-start / horizontal-end / vertical-end;*/
grid-area: 3/1/4/4;
```

### Limitar el tamanio de los elementos cuando el conteneder cambia
```css
grid-template-rows: minmax(30px, 45px);
```

### Auto fill: Rellena con espacios vacios
```css 
grid-template-rows: repeat(auto-fill, minmax(60px, 1fr));
```

### Auto fit: No rellena, estira los que hayan
```css
grid-template-rows: repeat(auto-fit, minmax(60px, 1fr));
```