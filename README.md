# Idolon
A PHP Image Server

## Requirements
- PHP 7
- imagemagick's convert Method
    - therefore, get imagemagick installed on your Operating System
    - e.g. Linux:  `$ sudo apt-get install imagemagick`
    - @see https://www.imagemagick.org/script/index.php, https://github.com/ImageMagick/ImageMagick

## Usage

Frontend HTML
~~~
<!DOCTYPE html>
<html lang="de">
    <head>
        <title></title>
    </head>
    <body>
    
        <!-- request an image with width 250px -->        
        <img src="example.php?i=example.jpg&x=250">
        
    </body>
</html>
~~~

Backend example.php
~~~php
<?php

// Idolon Class
require_once 'Idolon.php';

$oIdolon = new \Idolon();
$oIdolon
    ->setImagePath(/path/to/my/image/folder/)
    ->serve();
~~~

**see examples folder**