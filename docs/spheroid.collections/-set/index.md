//[Spheroid Script](../../index.md)/[spheroid.collections](../index.md)/[Set](index.md)



# Set  
 A generic unordered collection of elements that does not support duplicate elements. Methods in this interface support only read-only access to the set; read/write access is supported through the [MutableSet](../-mutable-set/index.md) interface.  
  
interface [Set](index.md)<[E](index.md) : Any?>  : [Collection](../-collection/index.md)   


## Functions  
  
|  Name|  Summary| 
|---|---|
| [contains](../-collection/contains.md)| Checks if the specified element is contained in this collection.  <br>abstract operator override fun [contains](../-collection/contains.md)(element: [E](index.md)): [Boolean](../../spheroid/-boolean/index.md)  <br><br><br>
| [isEmpty](../-collection/is-empty.md)| Returns true if the collection is empty (contains no elements), false otherwise.  <br>abstract override fun [isEmpty](../-collection/is-empty.md)(): [Boolean](../../spheroid/-boolean/index.md)  <br><br><br>
| toString| open override fun toString(): [String](../../spheroid/-string/index.md)  <br><br><br>


## Properties  
  
|  Name|  Summary| 
|---|---|
| [size](index.md#spheroid.collections/Set/size/#/PointingToDeclaration/)|  Returns the size of the collection.abstract override val [size](index.md#spheroid.collections/Set/size/#/PointingToDeclaration/): [Long](../../spheroid/-long/index.md)   <br>


## Inheritors  
  
|  Name| 
|---|
| [MutableSet](../-mutable-set/index.md)

