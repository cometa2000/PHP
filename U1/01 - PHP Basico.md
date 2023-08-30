# Primeros pasos 
Para empezar a escribir código de PHP lo que necesitaremos empezar hacer es lo siguiente:
### ==1. Prender Apache en Laragon==
1. Abre Laragon en tu computadora.
2. En la interfaz de Laragon, busca y haz clic en el botón "Iniciar Todo". Esto iniciará el servidor web Apache en tu entorno local.
![[Pasted image 20230824185418.png]]

### ==2. Crear una nueva carpeta de proyecto==
1. Abre la carpeta de instalación de Laragon en tu sistema.
2. Busca la carpeta llamada "www". Esta carpeta es el directorio raíz donde se alojan tus proyectos web.
3. Dentro de la carpeta "www", crea una nueva carpeta con el nombre de tu proyecto. Por ejemplo, podrías llamarla "mi-proyecto-php".
![[Pasted image 20230824185716.png]]

### ==3. Abrir Visual Studio Code y cargar el proyecto==
1. Abre Visual Studio Code en tu computadora (asegúrate de tenerlo instalado).
2. En Visual Studio Code, selecciona "File" (Archivo) en la barra de menú y luego "Open Folder" (Abrir carpeta).
![[Pasted image 20230824190336.png]]
3. Navega y selecciona la carpeta del proyecto que creaste en el "Paso 2" ("mi-proyecto-php").![[Pasted image 20230824190257.png]]
4. Una vez que la carpeta del proyecto esté abierta en Visual Studio Code, podrás comenzar a escribir y editar tu código PHP.
### ==4. Visualizar el código PHP en el navegador==
1. Abre tu navegador web preferido (por ejemplo, Chrome, Firefox).
2. En la barra de direcciones del navegador, ingresa la siguiente URL: `http://localhost/nombre-de-tu-proyecto`. Reemplaza "nombre-de-tu-proyecto" con el nombre real de la carpeta de tu proyecto.
3. Presiona Enter. El navegador cargará la página web generada por tu código PHP.

# Variables y su uso 
Una variable en PHP es un contenedor que almacena información o datos y les asigna un nombre único. Estos nombres de variables se utilizan para acceder y manipular los datos almacenados en ellas. Las variables son fundamentales en la programación, ya que permiten almacenar y manejar diferentes tipos de datos, como números, cadenas de texto, objetos y más.

En PHP, puedes crear una variable utilizando el símbolo de dólar ($) seguido del nombre de la variable. Aquí hay un ejemplo básico:
```php
$nombre = "Juan"; 
$edad = 25; 
$altura = 1.75;
```

Algunas reglas para nombrar variables en PHP son las siguientes:
1. Usar únicamente características latinos (0-9,o-z,A-Z) y guion bajo
2. No utilizar características especiales.
3. Si se puede utilizar guion bajo al comienzo del nombre de una variable.
4. Nombrar las variables con significado semántico.
5. Tener en cuenta que se distinguen entre nombres con mayúsculas y minúsculas. Ej. apellido Materno no es igual a apellido materno.
6. Evitar palabras.

La definición de constantes de hace con la función define() Como primer para los parámetros el nombre de la parámetro después para el segundo parámetro el valor de dicha constante

# Operaciones Aritméticas #
Las operaciones aritméticas son operaciones matemáticas que se realizan en valores numéricos para realizar cálculos. PHP admite una variedad de operadores aritméticos estándar que te permiten realizar sumas, restas, multiplicaciones, divisiones y más. Aquí tienes una definición y ejemplos de las operaciones aritméticas en PHP:
```php
<?php
    print(5 + 4)    //Suma
    print(5 - 4)    //Resta
    print(5 * 4)    //Multiplicacion
    print(5 / 4)    //Divicion
    print(5 % 4)    //Resto
    print(5 ** 4)   //Potenciacion
?>
```

# Operaciones Lógicas 
Las operaciones lógicas son operaciones que se realizan sobre valores booleanos (verdadero o falso) con el objetivo de evaluar o comparar condiciones. Estas operaciones son fundamentales en la lógica de programación ya que permiten tomar decisiones basadas en el estado de verdad de diferentes expresiones.

En PHP las ponderaciones lógicas son las siguientes:

| Nombre | Símbolo |
| ------ | ------- |
| AND    |      &&     |
| OR     |     ||    |
| NOT    |     !    |

| Ejemplo   | Nombre            | Descripción                                   |
| --------- | ----------------- | --------------------------------------------- |
| $a == $a  | Igual             | true si $a es igual a $b y son del mismo tipo |
| $a === $h | Idéntico          | true si $a es igual a $b, y del mismo tipo                                              |
| $a != $b  | Diferente         | true si $a no es igual a $b después de la manipulación de tipos                                             |
| $a !== $h | No idéntico       | true si $a no es igual a $b, o si no son del mismo tipo                                              |
| $a <> $b  | Diferente         | true si $a no es igual a $b después de la manipulación de tipos                                              |
| $a < $b   | Menor que         | true si $a es estrictamente menor que $b                                              |
| $a > $b   | Mayor que         | true si $a es estrictamente mayor que $b                                               |
| $a <= $b  | Mayor o igual que | true si $a es menor o igual que $b                                              |
| $a >= $b  | Menor o igual que | true si $a es mayor o igual que $b                                              |
| $a <=> $b | Nave espacial     | Un integer menor que, igual                                               |
|           |                   |                                               |

# Sentencia IF 
La sentencia `if` es una estructura de control que permite ejecutar un bloque de código si se cumple una condición especificada. Esta condición se evalúa como verdadera o falsa, y en función de su resultado, se decide si el bloque de código dentro del `if` se ejecuta o no.

Para usar if-else lo hacemos de la siguiente manera
```php
	<?php
	    $edad = 18;
	
	    if($edad >= 18 and $edad < 30){
	        print("Eres mayor de edad");
	    }else if($edad >= 30 and $edad < 60){
	        print("Eres un adulto joven");
	    }else if($edad >= 60){
	        print("Eres un adulto mayor");
	    }else {
	        print("Eres menor de edad");
	    }
	?>
```
# switch 
La estructura de control `switch` en PHP es utilizada para tomar decisiones basadas en el valor de una expresión en lugar de condiciones múltiples como en el caso de las estructuras `if` y `else`. Es especialmente útil cuando se desea comparar una única expresión con múltiples valores posibles y ejecutar diferentes bloques de código en función del valor de esa expresión.
```php
<?php
    $opcion = "HTML";

    switch($opcion){
        case 'CSS':
            print("Hoja de estilos");
            break;
        case 'HTML':
            print("Lenguaje de maquetado");
            break;
        case 'JS':
            print("Lenguaje de programacion cliente");
            break;
        default:
            print("No conozco ese lenguaje");
            break;
    }
?>
```
# while 
El bucle "while" es una estructura de control que permite ejecutar un bloque de código repetidamente mientras una condición sea verdadera. La condición se verifica antes de cada iteración del bucle. Si la condición es verdadera, el bloque de código se ejecuta; si la condición es falsa, el bucle se detiene y el flujo de ejecución continúa con el código que sigue al bucle.
```php 
<?php
	$contador = 1; 
	while ($contador <= 5) { 
		echo "Iteración número: " . $contador . "<br>"; 
		$contador++; 
	}
?>
```
# do-while 
La estructura de control `do-while` en PHP permite ejecutar un bloque de código al menos una vez y luego repetir ese bloque mientras se cumpla una condición especificada. A diferencia de la estructura `while`, que primero verifica la condición y luego puede saltar el bloque si la condición no se cumple desde el principio, el bucle `do-while` siempre ejecutará el bloque al menos una vez antes de verificar la condición.

La sintaxis general de `do-while` en PHP es la siguiente:
```php
<?php
	$contador = 1; 
	do { 
		echo "El contador es: " . $contador . "<br>"; 
		$contador++; 
	} while ($contador <= 5);
?>
```
# arreglos 
Un arreglo (también conocido como array en inglés) es una estructura de datos que puede contener múltiples valores relacionados bajo un mismo nombre. Cada valor en un arreglo se llama "elemento", y cada elemento tiene una posición única dentro del arreglo, llamada "índice". Los arreglos son muy útiles para almacenar conjuntos de datos relacionados y acceder a ellos de manera organizada.

**Arreglos Indexados:** Un arreglo indexado en PHP es un conjunto de elementos en el que cada elemento tiene un índice numérico único que comienza desde cero.
```php
<?php
    $calificaciones = [100, 89, 78, 67, 78];
    
    echo "<pre>";
    print_r($calificaciones);
    echo "</pre>";
?>
```
# objetos 
Los objetos son elementos fundamentales de la programación orientada a objetos (POO). Un objeto es una instancia de una clase, y las clases son plantillas que definen la estructura y el comportamiento de los objetos. Las clases determinan qué propiedades (variables) y métodos (funciones) tendrán los objetos que se creen a partir de ellas.
# arreglos asociativos 
Los arreglos asociativos son estructuras de datos que te permiten almacenar pares clave-valor, donde cada valor está asociado con una clave única. A diferencia de los arreglos indexados que utilizan índices numéricos, los arreglos asociativos utilizan claves (generalmente cadenas de texto) para acceder a sus elementos. Esto es útil cuando deseas almacenar y acceder a valores con una referencia más significativa que un simple índice numérico.
```php
<?php
    $persona = [
        "nombre" => "Brayan",
        "edad" => 22,
        "direccion" => [
            "ciudad" => "CDMX",
            "alcaldia" => "Milpa Alta",
            "poblado" => "Tecomitl"
        ]
    ]

    echo "<pre>";
    print_r($persona)
    echo ">/pre>";
?>
```
# for 
El bucle `for` en PHP es una estructura de control que te permite ejecutar un bloque de código repetidamente un número específico de veces. Es especialmente útil cuando sabes cuántas iteraciones deseas realizar. La sintaxis básica del bucle `for` en PHP es la siguiente:
```php
<?php
    $calificaciones = [100, 89, 78, 67, 78];
    $mensaje = ["Hola mundo", 24, true];

    for($a = 0; $a < count($calificaciones); $a++){
        print($calificaciones[$a]);
        echo "<br>";
    };

    for($a = 0; $a < count($mensaje); $a++){
        print($mensaje[$a]);
        echo "<br>";
    };
?>
```
# for-each
En PHP, un bucle `foreach` se utiliza para iterar sobre cada elemento de una matriz (array) o una colección iterable, como un objeto `stdClass` o una instancia de una clase que implementa la interfaz `Traversable`. Proporciona una forma más sencilla y legible de recorrer los elementos en comparación con un bucle `for` tradicional.
```php
<?php

    $persona = [
        "nombre" => "Brayan",
        "edad" => 22,
        "direccion" => [
            "ciudad" => "CDMX",
            "alcaldia" => "Milpa Alta",
            "poblado" => "Tecomitl"
        ]
    ];

    foreach ($persona as $clave => $valor) {
        if (is_array($valor)) {
            echo "$clave:<br>";
            foreach ($valor as $subclave => $subvalor) {
                echo "&nbsp;&nbsp;$subclave: $subvalor<br>";
            }
        } else {
            echo "$clave: $valor<br>";
        }
    }
?>
```
# funciones 
Las funciones son bloques de código que se pueden definir y reutilizar para realizar tareas específicas. Estas funciones ayudan a organizar y modularizar el código, lo que facilita el mantenimiento y la legibilidad.
```php
<?php

    function saludar($nombre,$apellido){
        return "Hola ". $nombre." ".$apellido;
    }
    print(saludar("Brayan","Solis"));
?>
```
# clases
Las clases son la base de la programación orientada a objetos (POO) y permiten definir estructuras que encapsulan datos y comportamientos relacionados.
```php
<?php

	class Persona {
	    public $nombre;
	    public $apellido;
	    public $edad;
	
	    public function __construct($nombre, $apellido, $edad) {
	        $this->nombre = $nombre;
	        $this->apellido = $apellido;
	        $this->edad = $edad;
	    }
	}
	
	class Alumno {
	    public $matricula;
	    public $nombre;
	    public $apellido;
	    public $edad;
	
	    public function __construct($matricula, $nombre, $apellido, $edad) {
	        $this->matricula = $matricula;
	        $this->nombre = $nombre;
	        $this->apellido = $apellido;
	        $this->edad = $edad;
	    }
	
	    public function reprobar($materia) {
	        return "Reprobaste: " . $materia;
	    }
	
	    public function aprobar($materia, $calificacion) {
	        return "Aprobaste: " . $materia . " con: " . $calificacion;
	    }
	}
	
	$alumnos = new Alumno(191190104, "Brayan", "Solis", 22);
	$parker = new Persona("Brayan", "Solis", 22);
	
	echo "<pre>";
	print_r($parker);
	print_r($alumnos);
	print_r($alumnos->aprobar("POO", 70));
	echo "</pre>";

?>
```
# encapsulamiento
El encapsulamiento es un concepto fundamental en la programación orientada a objetos (POO) y se refiere a la práctica de ocultar los detalles internos de una clase mientras se proporciona una interfaz controlada para interactuar con ella. En el contexto de PHP y la POO, el encapsulamiento se logra utilizando modificadores de acceso y métodos para definir cómo se accede y se modifica el estado de los objetos.
```php
<?php
    
	class Producto {
	    protected $nombre;
	    protected $precio;
	    protected $caducidad;
	
	    public function __construct($nombre, $precio, $caducidad) {
	        $this->nombre = $nombre;
	        $this->precio = $precio;
	        $this->caducidad = $caducidad;
	    }
	
	    public function obtenerProducto($nombre) {
	        if ($nombre == $this->nombre) {
	            return "Producto: " . $this->nombre . " Precio: " . $this->precio;
	        } else {
	            return "El producto no existe";
	        }
	    }
	}
	
	$galletas = new Producto("Principe", 20, "29/03/2024");
	
	echo "<pre>";
	print_r($galletas);
	print "<br>";
	print_r($galletas->obtenerProducto("Marias"));
	print "<br>";
	print_r($galletas->obtenerProducto("Principe"));
	echo "</pre>";

?>
```
En PHP, hay tres modificadores de acceso que se utilizan para controlar el encapsulamiento en una clase:

1. **public**: Los miembros (propiedades y métodos) marcados como públicos son accesibles desde cualquier lugar, tanto desde dentro de la clase como desde fuera de ella.
    
2. **protected**: Los miembros protegidos son accesibles desde dentro de la clase y también desde las clases que heredan de ella. Sin embargo, no se pueden acceder desde fuera de estas clases.
    
3. **private**: Los miembros privados solo son accesibles desde dentro de la clase en la que se definen. No se pueden acceder ni modificar desde fuera de esa clase ni desde clases que heredan de ella.