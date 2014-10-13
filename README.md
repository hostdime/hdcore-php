# hdcore-php

A simple wrapper around [HostDime.com](http://www.hostdime.com/)'s client API.

## Installing via Composer

The recommended method of installation is via [Composer](http://getcomposer.org)

    # Install Composer
    curl -sS https://getcomposer.org/installer | php

    # Add the library as a dependency
    php composer.phar require hostdime/hdcore:~0.1

After installing, you need to require Composer's autoloader:

    require 'vendor/autoload.php'; 

## Usage

~~~php
$public_key = 'foo';
$private_key = 'bar';
$client = new \HostDime\Api\Client($public_key, $private_key);

$servers = $client->call('server.list');

foreach ($servers as $server) {
    echo $server['name'];
}
~~~

## Reference

For a comprehensive overview of the HostDime API, please see our [API reference](https://api.hostdime.com/docs/).

## License - MIT

Copyright © 2013 HostDime.com, Inc.

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
