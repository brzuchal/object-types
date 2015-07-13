# ObjectTypes
PHP Objective implementation of primitive data types

## Installation
### Composer

Add to composer.json:-

```` json
{
    "require": {
        "mbrzuchalski/object-types": "dev-master"
    }
}
````

## Example usage

```` php
<?php
require_once 'vendor/autoload.php';

use ObjectTypes\IntegerType;
use ObjectTypes\StringType;

$stringValue = new StringType("Testing");

(string)$stringValue; // "Testing"
$stringValue->length(); // IntegerType(7)
$stringValue->replace(new StringType("Test"), new StringType("Post")); // StringType("Posting")
$stringValue->repeat(new IntegerType(2)); // StringType("TestingTesting")


$integerValue = new IntegerType(3);
$integerValue->add(new IntegerType(2)); // IntegerType(5)
$integerValue->substract(new IntegerType(2)); // IntegerType(1)
$integerValue->divide(new IntegerType(3)); // IntegerType(1)
$integerValue->multiply(new IntegerType(2)); // IntegerType(6)

````
