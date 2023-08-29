### Hola mundo
Para hacer un hola mundo con PHP necesitamos inicializar servicios en **XAMPP, Laragon, Lamp, etc**, crear la carpeta en la carpeta del servidor, en el caso de ***Arch Linux*** el directorio de la carpeta de servidor es el siguiente: /srv/http
![[Pasted image 20230824072525.png]]
Abrir la carpeta creada con **Visual Studio Code**, Dentro de **VSC** se debe crear el archivo **Index.php**, php puede ser incrustado directamente en **HTML**
![[Pasted image 20230824072815.png]]
En el apartado del body se agrega la *etiqueta* de php que es  `<?php ?>` Php al ser interpretado necesita del navegador para poder visualizar lo que hacemos.

Otras funciones para escribir texto en PHP
![[Pasted image 20230824074432.png]]

```
Las funciones de impresion tambien nos permiten mandar etiquetas HTML
```

### Variables y su uso
``` 
var_dump nos permite visualizar el tipo de dato.
```
Las variables en PHP se declaran con el signo **$**
![[Pasted image 20230824074320.png]]
Algunas reglas para nombrar variables en ***Php*** son las siguientes:
 - Usar únicamente caracteres latinos **(0-9, a-z, A-Z) y guion bajo.**
 - No utilizar **Caracteres especiales**
 - Si se puede utilizar **guion bajo al comienzo** del nombre de una variable
 - Nombrar las variables con **Significado semántico**
 - Tener en cuenta que **se distinguen entre nombres con mayúsculas y minúsculas.** Ej. ***apellidoMaterno***  no es igual a ***apellidomaterno***
 - Evitar **palabras reservadas**
La definición de constantes se hace con la función ***define()***. Como primer parámetro el nombre de la constante y como segundo parámetro el valor de dicha constante.

Para imprimir variables y constantes usamos la concatenacion **.**
![[Pasted image 20230824075624.png]]
### Operaciones aritmeticas.
Las operaciones aritmeticas en PHP son muy similares o iguales a otros lenguajes de programacion.
![[Pasted image 20230824080010.png]]
### Operaciones logicas
En PHP las operaciones logicas son las siguientes:

| Nombre | Simbolo |
| ------ | ------- |
| AND    | & ò and |
| OR     | l ò or  |
| NOT    | !       |

| Ejemplo        | Nombre            | Resultado                                                                                                                                                           |
| -------------- | ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| $a == $b       | Igual             | **`true`** si a es igual a b después de la manipulación de tipos.                                                                                                 |
| $a === $b      | Idéntico          | **`true`** si a es igual a b, y son del mismo tipo.                                                                                                               |
| $a != $b       | Diferente         | **`true`** si a no es igual a b después de la manipulación de tipos.                                                                                              |
| $a <> $b       | Diferente         | **`true`** si a no es igual a b después de la manipulación de tipos.                                                                                              |
| $a !== $b      | No idéntico       | **`true`** si a no es igual a b, o si no son del mismo tipo.                                                                                                      |
| $a < $b        | Menor que         | **`true`** si a es estrictamente menor que b.                                                                                                                     |
| $a > $b        | Mayor que         | **`true`** si a es estrictamente mayor que b.                                                                                                                     |
| $a <= $b       | Menor o igual que | **`true`** si a es menor o igual que b.                                                                                                                           |
| $a >= $b       | Mayor o igual que | **`true`** si a es mayor o igual que b.                                                                                                                           |
| $a <=> $b      | Nave espacial     | Un integer menor que, igual a, o mayor que cero cuando a es respectivamente menor que, igual a, o mayor que b. Disponible a partir de PHP 7.                      |
| $a ?? $b ?? $c | Fusión de null    | El primer operando de izquierda a derecha que exista y no sea **`null`**. **`null`** si no hay valores definidos y no son **`null`**. Disponible a partir de PHP 7. |

### Sentencia IF Else
La sentencia if nos permite ejecutar un bloque de código si una condición se cumple.

Para usar if else lo hacemos de la siguiente manera

``` php
<?php

$edad = 11;

if ($edad >= 18 and $edad < 30) {

print('Eres mayor de edad');

} elseif ($edad >= 30) {

print('Eres un adulto joven');

} elseif ($edad >= 60) {

print('Eres un adulto mayor');

} else {

print('Eres menor de edad');

}

?>
```

### Switch
La sentencia switch nos ayuda a ***evaluar*** una opcion, si hace ***match*** con algún case se ejecuta ese case hasta encontrar una sentencia ***break*** como el siguiente ejemplo:
```php
<?php

$opcion = 'HTML';

  

switch ($opcion) {

case 'HTML':

print('Lenguaje de maquetado');

break;

case 'CSS':

print('Hojas de estilo');

break;

case 'JS':

print('Lenguaje de programacion cliente');

break;

default:

print('No conozco ese lenguaje');

break;

}

  

?>
```

Si no hace match con ningún ***case*** se ejecuta el ***default***

### While

While nos permite ejecutar un bloque de código siempre y cuando una condición se cumpla. 
Una característica de while es que primero evalúa y después ejecuta. Se usa de la siguiente manera:

```php
<?php

$a = 0;

while ($a <= 10) {

print($a);

$a++;

}
?>
```

### Do while

Do while nos permite ejecutar un bloque de código siempre que se cumpla una condición. Una característica de ***Do while*** es que primero ***ejecuta*** y después ***evalúa***. Se usa de la siguiente manera:

```php
do {

print($a);

$a++;

} while ($a <= 10);
```

### Arreglos.

Los arreglos en php se hacen de la siguiente manera:
```php
<?php

  

$calificacion = [100, 99, 89, 78, 67, 76];

$arreglo = ["hola mundo", 24, true];

  

echo "<pre>";

print_r($calificacion);

echo "</pre>";

?>
```

Los arreglos pueden combinar tipos de datos sin ningún problema.

### Objetos
Los objetos en PHP únicamente existen cuando son instancias de una clase.

### Arreglos asosiativos

Los arreglos asosiativos están conformados por pares de ***clave*** - ***valor*** y se definen de la siguiente forma.
```php
$persona = [

"nombre" => 'Juan',

"edad" => 26,

"direccion" => [

"ciudad" => 'CDMX',

"alcaldia" => 'Xochimilco',

"pueblo" => 'San Gregorio'

]

];
```


Para acceder a los valores de un arreglo asosiativo lo hacemos mediante las ***claves*** o ***llaves***.
```php
echo "<pre>";

print_r($persona);

print($persona["nombre"]);

print($persona["direccion"]["alcaldia"]);

echo "</pre>";
```

### For

For es una estructura que nos permite iterar mientras una condición se cumpla, se utiliza de la siguiente manera:
 ```php
 <?php

$calificacion = [100, 99, 89, 78, 67, 76];

$arreglo = ["hola mundo", 24, true];

for ($i=0; $i < count($calificacion) ; $i++) {

print('Iteracion: ' . $i . ' Valor: ' . $calificacion[$i]);

echo "<br>";

}

for ($i=0; $i < count($arreglo) ; $i++) {

print('Iteracion: ' . $i . ' Valor: ' . $calificacion[$i]);

echo "<br>";

}

?>
```

### For each.

 Es un tipo especial de bucle que permite recorrer estructuras que contienen varios elementos.
 
 ```php
 $calificaciones = [100, 99, 89, 78, 67, 76];

$arreglo = ["hola mundo", 24, true];

  

foreach ($calificaciones as $calificacion => $value) {

print($calificacion);

echo "<br>";

}
```

### Funciones.
Las funciones de PHP, son **acciones que se realizan de manera independiente** y deben realizar únicamente una sola tarea.

```php
<?php

  

function saludar ($nombre, $apellido) {

return "Hola " . $nombre . " " . $apellido;

}

  

print(saludar('Juan', 'De la cruz'))

?>
```

### Clases. 

 Actúa como una **plantilla** para definir las características y comportamientos de los métodos y objetos

```php
<?php

  

class Persona {

public function __construct(public $nombre, public $apellido, public $edad) {

}

}

  

class Alumno {

public $matricula;

public $apellido;

public $edad;

public function __construct($matricula, $apellido, $edad) {

$this -> matricula = $matricula;

$this -> apellido = $apellido;

$this -> edad = $edad;

}

  

public function reprobar($materia) {

return "Reprobaste: " . $materia;

}

  

public function aprobar($materia, $calificacion) {

return "Aprobaste: " . $materia . " con: " . $calificacion;

}

}

$nombre = new Alumno (211190008, 'Juan', 26);

  

$juan = new Persona('Juan', 'De la cruz', 26);

echo "<pre>";

print_r($juan);

print_r($nombre);

print($nombre -> aprobar("POO", 70 ));

echo "<br>";

print($nombre -> reprobar("POO"));

echo "</pre>";
```

### Encapsulación

- **Protected**. Nos permite modificarlo dentro de la clase.
- **Public**. Nos permite modificar donde sea.
- **Private**. Solo permite modificarlo y acceder desde la propia clase.

```php
<?php

  

class Producto {

public function __construct(protected $nombre = "oreo", protected $precio = 29, protected $caducidad = "10/11/2023") {}

static public function obtenerProducto (){

return "Accedimos al metodo statico";

}

}

  

echo "<pre>";

$galletas = new Producto('Emperador', 30, "29/09/2023");

echo "<br>";

print_r($galletas -> obtenerProducto("Marias"));

echo "<br>";

print_r($galletas -> obtenerProducto("Emperador"));

echo "<br>";

print_r($galletas :: obtenerProducto());

echo "<br>";

echo "</pre>";

?>
```

