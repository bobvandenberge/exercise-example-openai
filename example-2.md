# Title
Even of oneven? 

# Description
Mensen kunnen gemakkelijk bepalen of een getal even of oneven is. Laten we eens onderzoeken of de computer dit cruciale verschil ook zo makkelijk ziet!


```steps
1. Schrijf een applicatie die bepaalt of een getal even of oneven is.
```

# LearningObjectives
Een nieuwe arithmetic operator leren gebruiken, namelijk modulo


# Example
```php
<?php

$input = readline("Vul een getal in" . PHP_EOL);

if ($input % 2 === 0) {
    echo "Dit is een even getal";
} else {
    echo "Dit is een oneven getal";
}
```