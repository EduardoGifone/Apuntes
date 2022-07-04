# HTML NOTES

***

## Indice <a id="id-indice"></a>
* [Estructura basica](#id-basic-struct)
* [Contenido basico](#id-basic-content)
* [h](#id-h)
* [p](#id-p)
* [Comentarios](#id-comment)
* [figure - figcaption](#id-fig)
* [Imagen](#id-img)
* [Video](#id-video)
* [Audio](#id-audio)
* [a](#id-a)
* [Lista Desordenada](#id-ul)
* [Lista Ordenada](#id-ol)
* [Inputs](#id-input)
* [Boton](#id-button)
* [Radio](#id-radio)
* [Checkbox](#id-checkbox)
* [Formulario](#id-form)
* [Time](#id-time)
* [Estilo de letras](#id-style-font)
* [hr](#id-hr)
* [div](#id-div)
* [table](#id-table)

***

## Estructura basica <a id="id-basic-struct"></a>
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

[Indice](#id-indice)

## Contenido basico del head <a id="id-basic-content"></a>
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

[Indice](#id-indice)

## Etiqueta h <a id="id-h"></a>
```html
<h1>Hola Mundo</h1>
<h2>Hola Mundo</h2>
<h3>Hola Mundo</h3>
<h4>Hola Mundo</h4>
<h5>Hola Mundo</h5>
<h6>Hola Mundo</h6>
```

[Indice](#id-indice)

## Etiqueta Parrafo <a id="id-p"></a>
```html
<p>
    Este contenido esta dentro de un parrafo
</p>
```

[Indice](#id-indice)

## Etiqueta comentario <a id="id-comment"></a>
```html
<!--Esto es un Comentario-->
```

[Indice](#id-indice)

## Etiquetas figure y figcaption <a id="id-fig"></a>
```html
<figure>
    <img src="direccion-imagen" alt="Photo of Camper Cat executing a roundhouse kick">
    <br>
    <figcaption>
        Master Camper Cat demonstrates proper form of a roundhouse kick.
    </figcaption>
</figure>
```

[Indice](#id-indice)

## Etiqueta Imagen <a id="id-img"></a>
```html
<img src="direccion-imagen" alt="texto-equivalente" title="titulo-imagen">
```

[Indice](#id-indice)

## Etiqueta video <a id="id-video"></a>
```html
<video src="direccion-video" title="titulo-video" controls=""></video>
```

[Indice](#id-indice)
		
## Etiqueta audio <a id="id-audio"></a>
```html
<audio src="video_prueba.mp4" controls=""></audio>

<audio id="meowClip" controls>
    <source src="audio/meow.mp3" type="audio/mpeg">
    <source src="audio/meow.ogg" type="audio/ogg">
</audio>
```

[Indice](#id-indice)

## Etiqueta anchor (enlaces) <a id="id-a"></a>
```html
<a href="#final">Ir al Final</a>
<a href="https://youtube.com">Click aqui </a>Para ir a youtube
<a href="https://youtube.com" target="_blank">Click aqui </a>Para ir a youtube en una pestania aparte
```

[Indice](#id-indice)

## Etiqueta Lista Desordenada - Unordered List <a id="id-ul"></a>
```html
<ul>
    <li>Leche</li>
    <li>Huevo</li>
    <li>Pan</li>
</ul>
```

[Indice](#id-indice)

## Etiqueta Lista ordenada - Ordered List <a id="id-ol"></a>
```html
<ol>
    <li>Leche</li>
    <li>Huevo</li>
    <li>Pan</li>
</ol>
```

[Indice](#id-indice)

## Etiqueta input <a id="id-input"></a>
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

[Indice](#id-indice)

## Etiqueta boton <a id="id-button"></a>
```html
<button type="submit"></button>
```

[Indice](#id-indice)

## Etiqueta Botones radio <a id="id-radio"></a>
```html
<label for="indoor"><input id="indoor" type="radio" name="indoor-outdoor" value="indoor" checked> Indoor</label>
<label for="outdoor"><input id="outdoor" type="radio" name="indoor-outdoor" value="outdoor"> Outdoor</label><br>
```

[Indice](#id-indice)

## Botones checkbox <a id="id-checkbox"></a>
```html
<label for="loving"><input id="loving" type="checkbox" name="personality" value="loving" checked> Loving</label>
<label for="lazy"><input id="lazy" type="checkbox" name="personality" value="lazy"> Lazy</label>
<label for="energetic"><input id="energetic" type="checkbox" name="personality" value="energetic"> Energetic</label><br>
```

[Indice](#id-indice)

## Etiqueta Formulario <a id="id-form"></a>
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

[Indice](#id-indice)

## Etiqueta time <a id="id-time"></a>
```html
<time datetime="2013-02-13">last Wednesday</time>
```

[Indice](#id-indice)

## Estilos para las letras <a id="id-style-font"></a>
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

[Indice](#id-indice)

## Etiqueta Linea Horizontal <a id="id-hr"></a>
```html		
<hr>
```

[Indice](#id-indice)

## Etiqueta div <a id="id-div"></a>
```html 
<div>
    <h4>Estoy dentro de un div</h4>
    <p>Esto tambien esta dentro de un div</p>
</div>
```	

[Indice](#id-indice)

## Etiqueta tabla <a id="id-table"></a>
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

[Indice](#id-indice)