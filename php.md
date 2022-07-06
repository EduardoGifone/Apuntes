# PHP NOTES

***

## Indice <a id="id-indice"></a>
* [Comentarios](#id-comments)
* [Variables](#id-var)
* [Operaciones](#id-operations)
* [Operadores unarios](#id-unary-operators)
* [Arreglos](#id-array)
* [Estructura if-else](#id-if-else)
* [Estructura switch](#id-switch)
* [Estructura for](#id-for)
* [Estructura while](#id-while)
* [Estructura do while](#id-do-while)
* [Estructura foreach](#id-for-each)
* [Funcion](#id-function)
* [Procedimiento](#id-process)
* [Funcion Recursiva](#id-recursive-function)
* [Importar codigo](#id-import-code)

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

## Arreglos <a id="id-array"></a>
```php
<?php 
	//Declaración de arreglos
    $primer_arreglo = []; 
    $primer_arreglo[0] = 'Hola'; 
    $primer_arreglo[1] = 'Mundo'; 
    echo 'Mensaje de bienvenida: <b>'.$primer_arreglo[0].' '.$primer_arreglo[1].'</b><br>'; 
?>
```

[Indice](#id-indice)

## Estructura if-else <a id="id-if-else"></a>
```php
<?php 
	//Convertir el nombre del dia en ingles a español
    $dia_actual = (string) date("D"); 
    $nombre dia = (string) ''; 
    if($dia_actual == 'Mon'): 
       $nombre_dia = 'Lunes'; 
    elseif($dia_actual == 'Tue'): 
       $nombre_dia = 'Martes'; 
    elseif($dia_actual == 'Wed'): 
       $nombre_dia = 'Miércoles'; 
    elseif($dia_actual == 'Thu'): 
       $nombre_dia = 'Jueves'; 
    elseif($dia_actual == 'Fri'): 
       $nombre_dia = 'Viernes'; 
    elseif($dia_actual == 'Sat'): 
       $nombre_dia = 'Sabado'; 
    else: 
       $nombre_dia = 'Domingo'; 
    endif; 
    echo 'Hoy es: <b>'.$nombre_dia.'</b><br>'; 
?>
```

[Indice](#id-indice)

## Estructura switch <a id="id-switch"></a>

```php
<?php 
	//Convertir el nombre del dia en ingles a español
    $dia_actual = (string) date("D"); 
    $nombre_dia = (string) ''; 
    switch ($dia_actual): 
        case 'Mon': 
          $nombre_dia = 'Lunes'; 
        break; 
        case 'Tue': 
          $nombre_dia = 'Martes'; 
        break; 
        case 'Wed': 
          $nombre_dia = 'Miércoles'; 
        break; 
        case 'Thu': 
          $nombre_dia = 'Jueves'; 
        break; 
        case 'Fri': 
          $nombre_dia = 'Viernes'; 
        break; 
        case 'Sat': 
          $nombre_dia = 'Sabado'; 
        break; 
        default: 
          $nombre_dia = 'Domingo'; 
        break; 
    endswitch; 
    echo 'Hoy es: <b>'.$nombre_dia.'</b><br>'; 
?>
```

[Indice](#id-indice)

## Loop for <a id="id-for"></a>
```php
<?php 
	//Mostrar los números impares menores al número 100
	$cantidad = (integer) 100; 
	$i = (integer) 0; 
	echo 'Números impares del 1 al 100<br>'; 
	for($i = 1; $i<=$cantidad ; $i++): 
 		if($i % 2): 
 		  echo 'Número impar: '.$i.'<br>'; 
		endif; 
	endfor; 
?>
```

[Indice](#id-indice)

## Loop while <a id="id-while"></a>
```php
<?php 
	//Mostrar los números impares menores al número 100
	$cantidad = (integer) 0; 
	echo 'Números impares del 1 al 100<br>'; 
	while($cantidad<=100): 
 		if(!($cantidad % 2)): 
 			echo 'Número impar: '.$cantidad.'<br>'; 
		 endif; 
 		$cantidad++; 
	endwhile; 
?>
```

[Indice](#id-indice)

## Loop do while <a id="id-do-while"></a>
```php
<?php 
	//Mostrar los números impares menores al número 100	
	$cantidad = (integer) 0; 
	echo 'Números impares del 1 al 100<br>'; 
	do{
 		if(!($cantidad % 2)): 
 			echo 'Número impar: '.$cantidad.'<br>'; 
		 endif; 
 		$cantidad++; 
	}while($cantidad<=100);
?>
```

[Indice](#id-indice)

## Loop for each <a id="id-for-each"></a>
```php
<?php 
	//Imprimir los elementos del arreglo información
	$informacion = []; 
	$informacion = array( 
 	'Carlos', 
	'Zulma', 
 	'Mario' 
	); 
	echo '<b>Recorrido del arreglo con foreach</b>'.'<br>';

	foreach($informacion as $valor): 
		print 'El nombre es: '.$valor.'<br>'; 
	endforeach; 
    echo'<br>';

	echo '<b>Recorrido del arreglo con for</b>'.'<br>';

	for($i = 0; $i<= count($informacion) ; $i++): 
 		print 'El nombre es: '.$informacion[$i].'<br>'; 
	endfor; 
?>
```

[Indice](#id-indice)

## Funciones <a id="id-function"></a>
```php
<?php
 	//Función: determinar si un año es bisiesto
	$anio = (integer)2022;
	function esbisiesto($anio)
	{
		if($anio%4==0):
			return true;
		else:
			return false;
		endif;
	}
	echo ‘El año es bisiesto: ’.esbisiesto($anio).’<br>’;
?>
```

[Indice](#id-indice)

## Procedimiento <a id="id-process"></a>
```php
<?php 
	//Procedimiento: imprime los datos (nombre y edad) de una persona
	$nombre = (string)’Juan Carlos’;
	$AnioNacimiento = (integer)2001;
	function ImprimirDatos($nombre, $AnioNacimiento)
	{
		echo ’Nombre: ’.$nombre.’<br>’;
		echo ’Edad: ’.(2022-$AnioNacimiento).’<br>’;
		return;
	}
	ImprimiDatos($nombre, $AnioNacimiento);
?>
```

[Indice](#id-indice)

## Funcion recursiva <a id="id-recursive-function"></a>
```php
<?php 
	function recursividad($a) 
	{ 
		 if ($a < 20) { 
			echo "$a <br>"; 
			recursividad($a + 1); 
		} 
	} 
	recursividad(1); 
?>
```

[Indice](#id-indice)

## Importar codigo <a id="id-import-code"></a>
|funcion|utilidad|
|-|-|
|require()|El codigo importado es *obligatorio*, en caso de *no exister* salta *error* y se *detiene* el programa.|
|include()|El codigo importado no es *obligatorio*, en caos de *no exister* salra *warning*.|

[Indice](#id-indice)