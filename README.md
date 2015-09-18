# lib-advkv-couchbase
Key Value Persistence implemtation for Couchbase, requires Generis 2.7

## Installing

This library will require the php module installed on the application servers:

Either run:

* ```sudo pecl install couchbase```
* Or follow the instructions on https://github.com/couchbaselabs/php-couchbase

You still need to enable the module in the PHP config file. To do so, either edit your php.ini or add a couchbase.ini file in /etc/php5/conf.d with the following contents: extension=couchbase.so.

## Configuring

Next configure it in your local tao instace in */config/generis/persistences.php*
```php
'couchbaseKeyValue' => array(
    'driver' => 'oat\couchbase\CouchbaseDriver',
    'cluster' => 'couchbase://localhost',
    'bucket' => 'your_tao_bucket',
    'password' => 'your_tao_bucket_password' //optional
)
````

For more examples look at http://forge.taotesting.com/projects/tao/wiki/Data_abstractions
