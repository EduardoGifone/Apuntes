# PHP NOTES

***

## Indice <a id="id-indice"></a>
* [Comentarios](#id-comments)
* [Variables](#id-var)
* [Operaciones](#id-operations)
* [Operadores unarios](#id-unary-operators)

***

## Comentarios <a id="id-comments"></a>
```php
<?php
// Primera forma de comentario

/* Segunda froma de comentario, 
esta soporta multiples lineas*/

# Tercera forma de comentario
?>
```

[Indice](#id-indice)

## Variables <a id="id-var"></a>
```php
<?php
$variable_entera = (integer) -23;
$variable_float = (float) -23.76;
$variable_string = (string) "Eduardo";
$variable_boolean_true = (boolean) true;
$variable_boolean_false = (boolean) false;
?>
```

[Indice](#id-indice)

## Operaciones <a id="id-operations"></a>
```php
<?php 
$a = (integer) 2; 
$b = (integer) 3; 
$c = (float) 3.14; 
echo 'La suma de $a + $b es: <b>'.($a + $b).'</b><br>'; 
echo 'La resta de $a - $c es: <b>'.($a - $c).'</b><br>'; 
echo 'La multiplicación de $a * $b es: <b>'.($a / $c).'</b><br>'; 
echo 'La división de $a / $b es: <b>'.($a / $b).'</b><br>'; 
echo 'La módulo de $a % $b es: <b>'.($a % $b).'</b><br>';
?>
```

[Indice](#id-indice)

## Operadores unarios <a id="id-unary-operators"></a>
```php
<?php
$a = (integer) 10; 
echo 'El valor de a inicial es: '.$a.'<br>'; 
echo 'Operador pre incremento es: '.(++$a).'<br>'; 
echo 'Operador post incremento es: '.($a++).'<br>'; 
echo 'Operador pre decremento es: '.(--$a).'<br>'; 
echo 'Operador post decremento es: '.($a--).'<br>';
?>
```

[Indice](#id-indice)