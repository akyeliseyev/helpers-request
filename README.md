English | [Русский](https://github.com/cs-eliseev/helpers-request/blob/master/README.ru_RU.md)

REQUEST CSE HELPERS
=======

[![Travis (.org)](https://img.shields.io/travis/cs-eliseev/helpers-request.svg?style=flat-square)](https://travis-ci.org/cs-eliseev/helpers-request)
[![Codecov](https://img.shields.io/codecov/c/github/cs-eliseev/helpers-request.svg?style=flat-square)](https://codecov.io/gh/cs-eliseev/helpers-request)
[![Scrutinizer code quality](https://img.shields.io/scrutinizer/g/cs-eliseev/helpers-request.svg?style=flat-square)](https://scrutinizer-ci.com/g/cs-eliseev/helpers-request/?branch=master)

[![Packagist](https://img.shields.io/packagist/v/cse/helpers-request.svg?style=flat-square)](https://packagist.org/packages/cse/helpers-request)
[![Minimum PHP Version](https://img.shields.io/badge/php-%3E%3D%207.1-8892BF.svg?style=flat-square)](https://packagist.org/packages/cse/helpers-request)
[![Packagist](https://img.shields.io/packagist/l/cse/helpers-request.svg?style=flat-square)](https://github.com/cs-eliseev/helpers-request/blob/master/LICENSE.md)
[![GitHub repo size](https://img.shields.io/github/repo-size/cs-eliseev/helpers-request.svg?style=flat-square)](https://github.com/cs-eliseev/helpers-request/archive/master.zip)

The helpers allows you to Request processing. Get value for POST/GET/REQUEST method by key and set default value, check exist AJAX, POST and GET method - all this is available in this library.

Project repository: https://github.com/cs-eliseev/helpers-request

**DEMO**
```php
switch(true) {
    case Request::isAjax():
    case Request::isPost():
        Request::post('example', 5);
        break;
    case Request::isGet():
        Request::getRequestUri();
        break;
}
```

***

## Introduction

[CSE HELPERS](https://github.com/cs-eliseev/helpers/blob/master/README.md) is a collection of several libraries with simple functions written in PHP for people.

Despite using PHP as the main programming language for the Internet, its functions are not enough. REQUEST CSE HELPERS solves the problem set default value to POST, GET and REQUEST method, and check exist AJAX, POST and GET method.

[CSE HELPERS](https://github.com/cs-eliseev/helpers/blob/master/README.md) was created for the rapid development of web applications.

**CSE Helpers project:**
* [Array CSE helpers](https://github.com/cs-eliseev/helpers-arrays)
* [Cookie CSE helpers](https://github.com/cs-eliseev/helpers-cookie)
* [Date CSE helpers](https://github.com/cs-eliseev/helpers-date)
* [Email CSE helpers](https://github.com/cs-eliseev/helpers-email)
* [IP CSE helpers](https://github.com/cs-eliseev/helpers-ip)
* [Json CSE helpers](https://github.com/cs-eliseev/helpers-json)
* [Math Converter CSE helpers](https://github.com/cs-eliseev/helpers-math-converter)
* [Phone CSE helpers](https://github.com/cs-eliseev/helpers-phone)
* [Request CSE helpers](https://github.com/cs-eliseev/helpers-request)
* [Session CSE helpers](https://github.com/cs-eliseev/helpers-session)
* [Word CSE helpers](https://github.com/cs-eliseev/helpers-word)

Below you will find some information on how to init library and perform common commands.

## Install

You can find the most recent version of this project [here](https://github.com/cs-eliseev/helpers-request).

### Composer

Execute the following command to get the latest version of the package:
```bash
composer require cse/helpers-request
```

Or file composer.json should include the following contents:
```json
{
    "require": {
        "cse/helpers-request": "*"
    }
}
```

### Git

Clone this repository locally:
```bash
git clone https://github.com/cs-eliseev/helpers-request.git
```

### Download

[Download the latest release here](https://github.com/cs-eliseev/helpers-request/archive/master.zip).

## Usage

The class consists of static methods that are conveniently used in any project. See example [examples-request.php](https://github.com/cs-eliseev/helpers-request/blob/master/examples/examples-request.php).

**POST data by key name**

Example:
```php
$_POST['example'] = 12345;
Request::post('example');
// 12345
```

Set default value:
```php
Request::post('example_2', 12345);
// 12345
```

**GET data by key name**

Example:
```php
$_GET['example'] = 12345;
Request::get('example');
// 12345
```

Set default value:
```php
Request::get('example_2', 12345);
// 12345
```

**REQUEST data by key name**

Example:
```php
$_REQUEST['example'] = 12345;
Request::request('example');
// 12345
```

Set default value:
```php
Request::request('example_2', 12345);
// 12345
```

**Is AJAX**

Example:
```php
$_SERVER['HTTP_X_REQUESTED_WITH'] = 'xmlhttprequest';
Request::isAjax();
// true
```

**Is POST**

Example:
```php
$_SERVER['REQUEST_METHOD'] = Request::METHOD_POST;
Request::isPost();
// true
```

**Is GET**

Example:
```php
$_SERVER['REQUEST_METHOD'] = Request::METHOD_GET;
Request::isGet();
// true
```

**Get request Uri**

Example:
```php
$_SERVER['HTTP_REFERER'] = '/link/example';
Request::getRequestUri();
// /link/example
```

Set default value:
```php
Request::getRequestUri('/link/home');
// /link/home
```

Ajax Uri:
```php
$_SERVER['HTTP_X_REQUESTED_WITH'] = 'xmlhttprequest';
$_SERVER['REQUEST_URI'] = '/link/example_ajax';
Request::getRequestUri();
// /link/example_ajax
```

**Is redirect to HTTPS**

Example:
```php
Request::isRedirectedToHttps('http://google.com');
// true
```


## Testing & Code Coverage

PHPUnit is used for unit testing. Unit tests ensure that class and methods does exactly what it is meant to do.

General PHPUnit documentation can be found at https://phpunit.de/documentation.html.

To run the PHPUnit unit tests, execute:
```bash
phpunit PATH/TO/PROJECT/tests/
```

If you want code coverage reports, use the following:
```bash
phpunit --coverage-html ./report PATH/TO/PROJECT/tests/
```

Used PHPUnit default config:
```bash
phpunit --configuration PATH/TO/PROJECT/phpunit.xml
```


## Donating

You can support this project [here](https://www.paypal.me/cseliseev/10usd). 
You can also help out by contributing to the project, or reporting bugs. 
Even voicing your suggestions for features is great. Anything to help is much appreciated.


## License

The REQUEST CSE HELPERS is open-source PHP library licensed under the MIT license. Please see [License File](https://github.com/cs-eliseev/helpers-request/blob/master/LICENSE.md) for more information.

***

> GitHub [@cs-eliseev](https://github.com/cs-eliseev)