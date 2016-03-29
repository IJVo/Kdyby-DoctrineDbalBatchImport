Kdyby/DoctrineDbalBatchImport
======

This package provides an implementation of a readonly collection wrapper, so you can return collections from your entities,
without having to copy the contents of the collection, or exposing the object's state outside of it's control.

[![Build Status](https://travis-ci.org/Kdyby/DoctrineDbalBatchImport.svg?branch=master)](https://travis-ci.org/Kdyby/DoctrineDbalBatchImport)
[![Downloads this Month](https://img.shields.io/packagist/dm/kdyby/doctrine-dbal-batchimport.svg)](https://packagist.org/packages/kdyby/doctrine-dbal-batchimport)
[![Latest stable](https://img.shields.io/packagist/v/kdyby/doctrine-dbal-batchimport.svg)](https://packagist.org/packages/kdyby/doctrine-dbal-batchimport)
[![Join the chat at https://gitter.im/Kdyby/Help](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/Kdyby/Help)


Installation
------------

The best way to install Kdyby/DoctrineDbalBatchImport is using  [Composer](http://getcomposer.org/):

```sh
$ composer require kdyby/doctrine-dbal-batchimport
```


Usage
-----

Simply wrap your collection and return it.

```php
public function getComments() : Collection
{
	return new ReadOnlyCollectionWrapper($this->comments);
}
```

Now you can use the `Collection` api as you're used to, you just cannot modifying it :)


-----

Homepage [http://www.kdyby.org](http://www.kdyby.org) and repository [http://github.com/Kdyby/DoctrineDbalBatchImport](http://github.com/Kdyby/DoctrineDbalBatchImport).
