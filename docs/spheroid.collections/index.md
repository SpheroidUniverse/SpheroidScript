//[Spheroid Script](../index.md)/[spheroid.collections](index.md)



# Package spheroid.collections  


## Types  
  
|  Name|  Summary| 
|---|---|
| [Collection](-collection/index.md)| A generic collection of elements. Methods in this interface support only read-only access to the collection; read/write access is supported through the [MutableCollection](-mutable-collection/index.md) interface.  <br>interface [Collection](-collection/index.md)<[E](-collection/index.md) : Any?>  : [Iterable](-iterable/index.md)  <br><br><br>
| [Iterable](-iterable/index.md)| Classes that inherit from this interface can be represented as a sequence of elements that can be iterated over and that supports removing elements during iteration.  <br>interface [Iterable](-iterable/index.md)<[T](-iterable/index.md) : Any?>   <br><br><br>
| [List](-list/index.md)| A generic ordered collection of elements. Methods in this interface support only read-only access to the list; read/write access is supported through the MutableList interface.  <br>interface [List](-list/index.md)<[E](-list/index.md) : Any?>  : [Collection](-collection/index.md)  <br><br><br>
| [MutableCollection](-mutable-collection/index.md)| A generic collection of elements that supports adding and removing elements.  <br>interface [MutableCollection](-mutable-collection/index.md)<[E](-mutable-collection/index.md) : Any?>  : [Collection](-collection/index.md)  <br><br><br>
| [MutableList](-mutable-list/index.md)| A generic ordered collection of elements that supports adding and removing elements.  <br>interface [MutableList](-mutable-list/index.md)<[E](-mutable-list/index.md) : Any?>  : [List](-list/index.md), [MutableCollection](-mutable-collection/index.md)  <br><br><br>
| [MutableSet](-mutable-set/index.md)| A generic unordered collection of elements that does not support duplicate elements, and supports adding and removing elements.  <br>interface [MutableSet](-mutable-set/index.md)<[E](-mutable-set/index.md) : Any?>  : [Set](-set/index.md), [MutableCollection](-mutable-collection/index.md)  <br><br><br>
| [Set](-set/index.md)| A generic unordered collection of elements that does not support duplicate elements. Methods in this interface support only read-only access to the set; read/write access is supported through the [MutableSet](-mutable-set/index.md) interface.  <br>interface [Set](-set/index.md)<[E](-set/index.md) : Any?>  : [Collection](-collection/index.md)  <br><br><br>


## Functions  
  
|  Name|  Summary| 
|---|---|
| [listOf](list-of.md)| Returns a new read-only list of given elements.  <br>fun <[T](list-of.md) : Any?> [listOf](list-of.md)(vararg elements: Array<Out [T](list-of.md)>): [List](-list/index.md)<[T](list-of.md)>  <br><br><br>
| [mutableListOf](mutable-list-of.md)| Returns a new MutableList with the given elements.  <br>fun <[T](mutable-list-of.md) : Any?> [mutableListOf](mutable-list-of.md)(vararg elements: Array<Out [T](mutable-list-of.md)>): [MutableList](-mutable-list/index.md)<[T](mutable-list-of.md)>  <br><br><br>
| [mutableSetOf](mutable-set-of.md)| Returns a new MutableSet with the given elements. Elements of the set are iterated in the order they were specified.  <br>fun <[T](mutable-set-of.md) : Any?> [mutableSetOf](mutable-set-of.md)(vararg elements: Array<Out [T](mutable-set-of.md)>): MutableSet<[T](mutable-set-of.md)>  <br><br><br>
| [setOf](set-of.md)| Returns a new read-only set with the given elements. Elements of the set are iterated in the order they were specified.  <br>fun <[T](set-of.md) : Any?> [setOf](set-of.md)(vararg elements: Array<Out [T](set-of.md)>): Set<[T](set-of.md)>  <br><br><br>

