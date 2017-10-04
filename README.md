# DomQuery


DomQuery is a PHP library that allows you to easily traverse and modify the DOM (HTML/XML). As a libery it aims to be a 'jQuery in PHP', excluding functionality not related to the DOM (like AJAX etc.).  

## Installation


Install the latest version with

```bash
$ composer require rct567/dom-query
```

## Basic Usage

``` php
$dom = new DomQuery('<div><h1 class="title">Hello</h1></div>');

echo $dom->find('h1')->text(); // output: Hello
echo $dom->find('h1')->getHtml(); // output: <h1 class="title">Hello</h1>
echo $dom->find('div > h1')->class; // ouput: title
echo $dom->find('div > h1')->attr('class'); // ouput: title
echo $dom->find('div > h1')->prop('tagName'); // ouput: h1
echo (string) $dom->find('div > h1'); // output: <h1 class="title">Hello</h1>
echo count($dom->find('div, h1')); // output: 2
```

## About

### Requirements

- Works with PHP 7.0 or above 
- Requires libxml PHP extension (enabled by default)
- Can also be used a a standalone class (no external dependencies)
