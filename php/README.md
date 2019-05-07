* 1. [Affichage](#Affichage)
* 2. [Variables](#Variables)
	* 2.1. [Les types](#Lestypes)
	* 2.2. [Déclarer une variable](#Dclarerunevariable)
	* 2.3. [constante](#constante)
* 3. [Condition](#Condition)
	* 3.1. [Condition ternaire](#Conditionternaire)
	* 3.2. [switch](#switch)
* 4. [Boucles](#Boucles)
* 5. [Fonction](#Fonction)
	* 5.1. [Retour type stricte](#Retourtypestricte)
	* 5.2. [Paramètres infinie](#Paramtresinfinie)
	* 5.3. [Fonction anonyme](#Fonctionanonyme)
	* 5.4. [Passage par référence](#Passageparrfrence)
* 6. [Tableau](#Tableau)
* 7. [Gestion des erreurs](#Gestiondeserreurs)
* 8. [Lire et écrire dans un fichier](#Lireetcriredansunfichier)


# PHP Basic cheat

##  1. <a name='Affichage'></a>Affichage

```php
<?php
echo "hello " , "world<br>";
echo "hello " . "world 2<br>";
?>
<?= "hello " , "world 3" ?>
```

##  2. <a name='Variables'></a>Variables

###  2.1. <a name='Lestypes'></a>Les types

Les types de variables les plus connues :

- int
- string
- bool
- double
- array
- NULL
- object
- iterable (variable utilisée dans le foreach)

###  2.2. <a name='Dclarerunevariable'></a>Déclarer une variable

nom de la variable = de préférence Camel case

```php
<?php
$name = "Hatim";
echo "Hello ", $name;

```

###  2.3. <a name='constante'></a>constante

```php
<?php

define("PI",    3.14); // méthode 1
echo PI, "<br>";
const WIDTH = 200; // méthode 2
echo WIDTH;
```

##  3. <a name='Condition'></a>Condition

- != différent de
- !== différent de valeur et de type

**mots-clés :** `if` `elseif` `else`

###  3.1. <a name='Conditionternaire'></a>Condition ternaire

```php
$retVal = (condition) ? a : b ;
```

###  3.2. <a name='switch'></a>switch 

```php
<?php

$menu = 1;

switch ($menu) {
    case 1:
        echo "Big mac !";
        break;
    default:
        echo "Rien";
        break;
}
```

##  4. <a name='Boucles'></a>Boucles

Possibilité d'utiliser les mots clés :

- **continue** 
- **break**

```php
while (condition){
    // code...
}
```

```php
for ($i=0; $i < 10; $i++) { 
    // code...
}
```

##  5. <a name='Fonction'></a>Fonction

```php
<?php
function maFonction($test, int $age, bool $mort = true){
    // code...
    return [$test, $age, $mort];
}
```

###  5.1. <a name='Retourtypestricte'></a>Retour type stricte

```php
<?php
function maFonction($test){ : bool
    // code...
    return $test;
}
```

###  5.2. <a name='Paramtresinfinie'></a>Paramètres infinie

```php
<?php

function infinie(...$suite){
    var_dump($suite);
}

infinie(1, 2, 3);
infinie(1, 2, 3, 4);
```

###  5.3. <a name='Fonctionanonyme'></a>Fonction anonyme

```php
<?php

$test = function (){echo "test";};
$test();
```

###  5.4. <a name='Passageparrfrence'></a>Passage par référence

```php
<?php

function ref(&$var){ $var++; }
function noref($var){ $var++; }

$a = 5;

noref($a); echo $a, "<br>"; // 5
ref($a); echo $a; // 6
```

##  6. <a name='Tableau'></a>Tableau


```php
<?php

$tab = array(); // méthode 1
$tab2 = []; // méthode 2

// sans clé
$animaux = [ "chat", "chien", "ours"];
echo($animaux[0]. "<br>"); // chat

//avec clé
$notes= [ "Robert" => 12, "Alex" => 14];
echo($notes["Robert"]); // 12

$notes["Hatim"] = 20; //ajouter une valeur avec clé
array_push($animaux, "lion"); //ajouter une valeur sans clé


array_pop($animaux); // supprime le dernier élement
array_shift($animaux); // supprime le 1er element

unset($notes["Robert"]); // supprimer par clé

$pizza  = "piece1 piece2 piece3 piece4 piece5 piece6";
$pieces = explode(" ", $pizza); // string to array
```

##  7. <a name='Gestiondeserreurs'></a>Gestion des erreurs

```php
<?php 
try {
    // code ...
} catch (Exception $e) {
    echo 'Exception reçue : ',  $e->getMessage(), "<br>";
}
```

##  8. <a name='Lireetcriredansunfichier'></a>Lire et écrire dans un fichier

Non disponible pour le moment
