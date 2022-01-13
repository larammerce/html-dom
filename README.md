HtmlDom
=======

A HtmlDom package for Laravel 8 based on Simple HTML Dom Parser

## Installation

Add the following line to the `require` section of `composer.json`:

```json
{
    "require": {
        "larammerce/html-dom": "1.0.*"
    }
}
```

## Laravel 8 Setup

1. Add the service provider to `config/app.php`.

```php
'providers' => array(
    ...
	'Larammerce\HtmlDom\HtmlDomServiceProvider',
    ...
```
2. Add alias to `config/app.php`.

```php
'aliases' => array(	
    ...
	'HtmlDom' => 'Larammerce\HtmlDom\HtmlDom',
    ...
```

## Usage

1. Use following:

```php
$html = new \HtmlDom('http://www.example.com');

// Find all images 
foreach($html->find('img') as $element) 
       echo $element->src . '<br>';

// Find all links 
foreach($html->find('a') as $element) 
       echo $element->href . '<br>';
```

See the detailed documentation http://simplehtmldom.sourceforge.net/manual.htm

