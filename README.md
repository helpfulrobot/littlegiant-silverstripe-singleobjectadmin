# SilverStripe Single Object Administration

Single object administration via a LeftAndMain like interface. Lets your clients edit single objects similar to site config.

## Features

 * Single object administration
 * Only allows publish functionality for the object

## Installation

Installation via composer

```bash
$ composer require littlegiant/silverstripe-singleobjectadmin
```

## How to use

Simply extend the SingleObjectAdmin class instead of ModelAdmin and include the class via the `tree_class` static.

```php

class ProductSettingsAdmin extends SingleObjectAdmin
{
    private static $menu_title = "Product Settings";
    private static $tree_class = 'ProductSettings';
    private static $url_segment = "product-settings";

}
```

The single object admin assumes you have one and only have one item of the class which you are trying to administrate and
makes no attempt to try and check if this is the case, naively getting the first object which matches. It is up to you
to ensure that the class has one and only one instance created, usually via canCreate() functionality.

## License

The MIT License (MIT)

Copyright (c) 2015 Little Giant Design Ltd

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.

## Contributing


### Code guidelines

This project follows the standards defined in:

* [PSR-0](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-0.md)
* [PSR-1](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-1-basic-coding-standard.md)
* [PSR-2](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md)
