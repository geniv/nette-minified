Nette minified
==============
Minified version of Nette Framework, revision: 2.4-20170829

Installation
------------

```sh
$ composer require geniv/nette-authorizator
```
or
```json
"geniv/nette-authorizator": ">=1.0.0"
```

require:
```json
"php": ">=5.6.0"
```

usage:
```php
// vnuceni hlavicky
header('Content-Type: text/html; charset=UTF-8');

if (!file_exists(__DIR__ . '/vendor/autoload.php')) {
    die('Neexistuje obsah slozky vendor! Zpracujte prosim composer!');
}
// nacteni nette
require __DIR__ . '/vendor/autoload.php';

// zapnuti ladenky
Tracy\Debugger::enable(null, __DIR__ . '/log');

try {

    // pokusny text
    echo Nette\Utils\Html::el('strong')->setText('It works!');

} catch (Exception $e) {
    Tracy\Debugger::log($e);  // log exception
}
```
