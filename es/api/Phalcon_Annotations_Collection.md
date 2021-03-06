# Clase **Phalcon\\Annotations\\Collection**

*implementa* [Iterator](http://php.net/manual/en/class.iterator.php), [Traversable](http://php.net/manual/en/class.traversable.php), [Countable](http://php.net/manual/en/class.countable.php)

<a href="https://github.com/phalcon/cphalcon/blob/master/phalcon/annotations/collection.zep" class="btn btn-default btn-sm">Código fuente en GitHub</a>

Representa una colección de anotaciones. Esta clase permite recorrer fácilmente un grupo de anotaciones

```php
<?php

// Recorrer anotaciones
foreach ($classAnnotations as $annotation) {
    echo "Nombre = ", $annotation->getName(), PHP_EOL;
}

// Verificar si las anotaciones tienen algo específico
var_dump($classAnnotations->has("Cacheable"));

// Obtener una anotación específica de la colección
$annotation = $classAnnotations->get("Cacheable");

```

## Métodos

public **__construct** ([*array* $reflectionData])

Constructor de Phalcon\\Annotations\\Collection

public **count** ()

Devuelve el número de anotaciones en la colección

public **rewind** ()

Rebobina el iterador interno

public [Phalcon\Annotations\Annotation](/[[language]]/[[version]]/api/Phalcon_Annotations_Annotation) **current** ()

Devuelve la anotación actual en el iterador

public **key** ()

Devuelve la llave/posición actual del iterador

public **next** ()

Mueve el puntero interno de iteración a la siguiente posición

public **valid** ()

Verifica si la anotación actual del iterador es válida

public **getAnnotations** ()

Devuelve las anotaciones internas como un arreglo

public **get** (*string* $name)

Devuelve la primera anotación que coincide con un nombre

public **getAll** (*string* $name)

Devuelve todas las anotaciones que coinciden con un nombre

public **has** (*string* $name)

Comprobar si existe una anotación en una colección