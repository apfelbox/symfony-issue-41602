Reproducer for Symfony Issue 41602
==================================

[See issue](https://github.com/symfony/symfony/issues/41602)

The class `TestClass` is not used, but autoconfigured. It should ideally be just ignored.

That is a common case to have optional classes that integrate into optional dependencies.


To reproduce
------------

1. install
2. run `php bin/console cache:clear`


Error
-----

```
In ClassExistenceResource.php line 74:
                                                                                   
  [ReflectionException]                                                            
  Class "Some\Missing\MissingClass" not found while loading "App\Test\TestClass".  
```
