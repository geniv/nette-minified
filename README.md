Nette minified
==============
Minified version of Nette Framework, revision: 2.4-20180918

via: https://nette.org/cs/download

Installation
------------

```sh
$ composer require geniv/nette-minified
```
or
```json
"geniv/nette-minified": "^1.0"
```

require:
```json
"php": ">=5.6"
```

usage:
```php
use Nette\Utils\Html;
use Tracy\Debugger;


// vnuceni hlavicky
header('Content-Type: text/html; charset=UTF-8');

if (!file_exists(__DIR__ . '/vendor/autoload.php')) {
    die('Neexistuje obsah slozky vendor! Zpracujte prosim composer!');
}
// nacteni nette
require __DIR__ . '/vendor/autoload.php';

// zapnuti ladenky
Debugger::enable(null, __DIR__ . '/log');

try {

    // pokusny text
    echo Html::el('strong')->setText('It works!');

} catch (Exception $e) {
    Debugger::log($e);  // log exception
}
```
