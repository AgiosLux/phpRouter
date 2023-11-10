# phpRouter

PHP advanced Router classes like Laravel

## Installation

```shell
composer require agioslux/phprouter
```

## Example of use

Here, a simple example of use:

```php
<?php

require_once "vendor/autoload.php";

use Agioslux\Phprouter\Router;
use Agioslux\Phprouter\Response;

$url = "http://localhost/phpRouter";
$router = new Router($url);

$router->get('/', [
	function () {
		return new Response(200, "Example of GET request");
	}
]);

$router->post('/', [
	function () {
		return new Response(200, "Example of POST request");
	}
]);

$router->put('/', [
	function () {
		return new Response(200, "Example of PUT request");
	}
]);

$router->delete('/', [
	function () {
		return new Response(200, "Example of DELETE request");
	}
]);

$router->run()->sendResponse();
```

To  set HTTP Code on Request, use:

```php
$response->setHttpCode(200);
```

> Replace 200 for to your HTTP status code

## Dependencies

* php >= 8.1
