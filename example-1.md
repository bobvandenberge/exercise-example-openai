# Title
Auto rijden

# Description
We willen gaan controleren of iemand oud genoeg is om te beginnen met autorijlessen. Dat mag als je 16,5 jaar of ouder bent. Hiervoor gaan we een check bouwen.  

In ons programma willen we de gebruiker om zijn of haar leeftijd vragen, en daarna willen we controleren of diegene oud genoeg is. Dat betekent dat er 2 mogelijke uitkomsten zijn: **wel** of **niet** oud genoeg. In het geval dat iemand wel oud genoeg is willen we hem of haar daarmee feliciteren! Als de gebruiker niet oud genoeg is vragen we hem of haar om nog even geduld te hebben.  

Het komt vaak voor dat je in een programma wilt controleren of iets **wel** of **niet** waar is. Hiervoor gebruik je een `if` statement. Daarmee vraag je PHP om iets te controleren. Bijvoorbeeld of een variable een getal bevat wat groter is dan 100 ; `$variable > 100`. Dit noemen we een 'condition'.  

Een condition levert altijd een **wel** of **niet** uitkomst op, een **waar** of **niet waar**. In software noemen we dit een [Boolean](https://www.php.net/manual/en/language.types.boolean.php), en een boolean is altijd **True** of **False**.  

Het is netjes om de waarde die kan veranderen eerst te noemen en de constante waarde waarmee je vergelijkt als tweede te noemen in de condition. Dit komt overeen met hoe mensen normaal over dit soort vragen denken: "Is de gebruiker ouder dan 16,5?". Als je dit verkeerd om doet noemen we dat een YODA condition.  
 
We geven een `if` statement dus een condition om te controleren. Als die condition resulteert in een **True** boolean dan wordt een stuk code uitgevoerd.  

```php
if (condition) {
    code als de condition True is.
}
``` 

Soms wil je ook wat code uitvoeren als een condition niet waar is. Dit plakken we dan vast aan het `if` statement met een `else` statement. Een else statement heeft geen condition, het is namelijk precies het tegenovergestelde van de condition in het if statement. Dat ziet er zo uit:  

```php
if (condition) {
    code als de condition True is.
} else {
    code als de condition False is.
}
```

```steps
1. Gebruik het if statement om de gebruiker te vertellen of hij of zij met rijlessen kan beginnen.
```

# LearningObjectives
1. Werken met een if-statement
2. Het `float` datatype leren kennen

# Example
```php
<?php

$leeftijd = readline("Hoe oud ben je?" . PHP_EOL);

if ($leeftijd >= 16.5) {
    echo "Je mag beginnen met rijlessen!" . PHP_EOL;
} else {
    echo "Helaas, je mag nog niet beginnen met rijlessen" . PHP_EOL;
}
```