# JAVASCRIPT NOTES

***

## Indice <a id="id-indice"></a>
* [Repositorio base](#id-base)
* [Imprimir](#id-console-log)
* [Variables](#id-var)
* [Destructuring](#id-destructuring)
* [Operaciones](#id-operations)
* [Operaciones Logicas](#id-logical-operations)
* [Booleanos](#id-bool)

***

## Repositorio base <a id="id-base"></a>
[Javascrip Notes](https://github.com/martincrb/mastermind-js)

[Indice](#id-indice)

## Imprimir en terminal <a id="id-console-log"></a>
```js
console.log('Hola mundo');
console.log('Eduardo',a);
```

[Indice](#id-indice)

## Variables <a id="id-var"></a>
### Las variables son dinamicas
```js
console.log(typeoff variable)
```
### Tipos
```js
var numero = 2;
var string = 'Soy un texto';
var booleano = true;
var array = ["aa", "bb", 3, [1, 2]];
var objeto = {
    nombre: 'Martin', 
    apellido: 'Cristobal',
    edad: 26
}

objeto.nombre;
array[0];

var nombreFuncion = function() {}

var valorNulo = null;
var valorUndefined;
```

[Indice](#id-indice)

## Destructuring <a id="id-destructuring"></a>
```js
[x, y] = [y, x]
```

[Indice](#id-indice)

## Operaciones <a id="id-operations"></a>
### Numeros
```js
var suma = a + b;
var resta = a - b;
var mult = a * b;
var div = a / b;
var resto = a % b;
var expo = a ** b;
var a++;
a--;
a += 2;
a -= 2;
a *= 2;
a /= 2;
a %= 2;
a **= 2;
```
### Texto
```js
var nombre = 'Eduardo';
var apellido = 'Gifone Villasante';
var nombre_completo = nombre + ' ' + apellido + 23;
```

[Indice](#id-indice)

## Operadores logicos <a id="id-logical-operations"></a>
    And: &&          
    Or:||

[Indice](#id-indice)

## Booleanos <a id="id-bool"></a>
    > < >= <= == === != !==

```js
var booleanoCierto = true;
var booleanoFalso = false;
var a = '10';
var b = 10;
var aMayorQueb = a > b;
```

[Indice](#id-indice)