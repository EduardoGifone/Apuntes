# HTML NOTES

***

## Estructura basica
```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
    </head>
    <body>
        <header>
            <nav></nav>
        </header>

        <main>
            <section></section>
        </main>

        <article>
            <section></section>
        </article>

        <footer></footer>
    </body>
</html>
```

## Contenido basico del head
```html
<head>
    <title>Mi primera pagina web</title>
    <meta charset="utf-8">
    <meta name="keywords" content="HTML">
    <meta name="description" content="Esta es una pagina la cual esta dedicada al aprendizaje de desarrollo web. No sean pendejos y denle amor">
    <meta name="author" content="Eduardo Gifone">
    <meta name="copyright" content="Eduardo Inc.">
    <meta name="robots" content="noindex">
    <link rel="icon" href="fondo.ico">
</head>
```

## Etiqueta h
```html
<h1>Hola Mundo</h1>
<h2>Hola Mundo</h2>
<h3>Hola Mundo</h3>
<h4>Hola Mundo</h4>
<h5>Hola Mundo</h5>
<h6>Hola Mundo</h6>
```

## Etiqueta Parrafo
```html
<p>
    Este contenido esta dentro de un parrafo
</p>
```
## Etiqueta comentario
```html
<!--Esto es un Comentario-->
```

## Etiquetas figure y figcaption
```html
<figure>
    <img src="direccion-imagen" alt="Photo of Camper Cat executing a roundhouse kick">
    <br>
    <figcaption>
        Master Camper Cat demonstrates proper form of a roundhouse kick.
    </figcaption>
</figure>
```

## Etiqueta Imagen
```html
<img src="direccion-imagen" alt="texto-equivalente" title="titulo-imagen">
```

## Etiqueta video
```html
<video src="direccion-video" title="titulo-video" controls=""></video>
```
		
## Etiqueta audio
```html
<audio src="video_prueba.mp4" controls=""></audio>

<audio id="meowClip" controls>
    <source src="audio/meow.mp3" type="audio/mpeg">
    <source src="audio/meow.ogg" type="audio/ogg">
</audio>
```

## Etiqueta anchor (enlaces)
```html
<a href="#final">Ir al Final</a>
<a href="https://youtube.com">Click aqui </a>Para ir a youtube
<a href="https://youtube.com" target="_blank">Click aqui </a>Para ir a youtube en una pestania aparte
```
## Etiqueta Lista Desordenada - Unordered List
```html
<ul>
    <li>Leche</li>
    <li>Huevo</li>
    <li>Pan</li>
</ul>
```

## Etiqueta Lista ordenada - Ordered List
```html
<ol>
    <li>Leche</li>
    <li>Huevo</li>
    <li>Pan</li>
</ol>
```

## Etiqueta input
```html
<input type="text" placeholder="Tex probicional" required><br>
<input type="password" required><br>
<input type="number"><br>
<input type="email"><br>
<input type="color"><br>
<input type="range" min="1" max="5"><br>
<input type="date"><br>
<input type="time"><br>
<input type="button" value="Boton"><br>
<input type="submit"><br>
<textarea readonly="">Como estas manito?</textarea>
```

## Etiqueta boton
```html
<button type="submit"></button>
```

## Etiqueta Botones radio
```html
<label for="indoor"><input id="indoor" type="radio" name="indoor-outdoor" value="indoor" checked> Indoor</label>
<label for="outdoor"><input id="outdoor" type="radio" name="indoor-outdoor" value="outdoor"> Outdoor</label><br>
```

## Botones checkbox
```html
<label for="loving"><input id="loving" type="checkbox" name="personality" value="loving" checked> Loving</label>
<label for="lazy"><input id="lazy" type="checkbox" name="personality" value="lazy"> Lazy</label>
<label for="energetic"><input id="energetic" type="checkbox" name="personality" value="energetic"> Energetic</label><br>
```

## Etiqueta Formulario
```html
<form action="url-del-servidor" method="post"></form>
```
## Otro ejemlo de formulario envolviendo los radios en un mismo grupo ademas de aniadir una leyenda
```html
<form>
    <fieldset>
        <legend>Choose one of these three items:</legend>

        <input id="one" type="radio" name="items" value="one">
        <label for="one">Choice One</label><br>

        <input id="two" type="radio" name="items" value="two">
        <label for="two">Choice Two</label><br>

        <input id="three" type="radio" name="items" value="three">
        <label for="three">Choice Three</label>
    </fieldset>
</form>
```
## Etiqueta time
```html
<time datetime="2013-02-13">last Wednesday</time>
```

## Estilos para las letras
```html
<b>Negrita</b>
<i>Italica</i>
<strike>Tachada</strike> 
<small>Chikita</small>
<strong>Strong</strong>
<u>Subrayar</u>
<em>Cursiva</em>
<s>Tachar</s>
```

## Etiqueta Linea Horizontal
```html		
<hr>
```

## Etiqueta div
```html
<div>
    <h4>Estoy dentro de un div</h4>
    <p>Esto tambien esta dentro de un div</p>
</div>
```	

## Etiqueta tabla
```html
<table border="1px">
    <tr>
        <td><b>Nombre</b></td>
        <td><b>Apellido</b></td>
        <td><b>Edad</b></td>
    </tr>
    <tr>
        <td>Eduardo</td>
        <td>Gifone Villasante</td>
        <td>19</td>
    </tr>
    <tr>
        <td>Licelith</td>
        <td>Villasante Rodriguez</td>
        <td>46</td>
    </tr>
</table>
```