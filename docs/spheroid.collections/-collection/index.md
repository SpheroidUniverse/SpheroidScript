//[Spheroid Script](../../index.md)/[spheroid.collections](../index.md)/[Collection](index.md)



# Collection  
 A generic collection of elements. Methods in this interface support only read-only access to the collection; read/write access is supported through the [MutableCollection](../-mutable-collection/index.md) interface.  
  
interface [Collection](index.md)<[E](index.md) : Any?>  : [Iterable](../-iterable/index.md)   


## Functions  
  
|  Name|  Summary| 
|---|---|
| [contains](contains.md)| Checks if the specified element is contained in this collection.  <br>abstract operator fun [contains](contains.md)(element: [E](index.md)): Boolean  <br><br><br>
| [isEmpty](is-empty.md)| Returns true if the collection is empty (contains no elements), false otherwise.  <br>abstract fun [isEmpty](is-empty.md)(): [Boolean](../../spheroid/-boolean/index.md)  <br><br><br>
| toString| open override fun toString(): String  <br><br><br>


## Properties  
  
|  Name|  Summary| 
|---|---|
| [size](index.md#spheroid.collections/Collection/size/#/PointingToDeclaration/)|  Returns the size of the collection.abstract val [size](index.md#spheroid.collections/Collection/size/#/PointingToDeclaration/): [Long](../../spheroid/-long/index.md)   <br>


## Inheritors  
  
|  Name| 
|---|
| [MutableCollection](../-mutable-collection/index.md)
| [List](../-list/index.md)
| [Set](../-set/index.md)

