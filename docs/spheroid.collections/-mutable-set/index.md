//[Spheroid Script](../../index.md)/[spheroid.collections](../index.md)/[MutableSet](index.md)



# MutableSet  
 A generic unordered collection of elements that does not support duplicate elements, and supports adding and removing elements.  
  
interface [MutableSet](index.md)<[E](index.md) : Any?>  : [Set](../-set/index.md), [MutableCollection](../-mutable-collection/index.md)   


## Functions  
  
|  Name|  Summary| 
|---|---|
| [add](../-mutable-collection/add.md)| Adds the specified element to the collection.  <br>abstract override fun [add](../-mutable-collection/add.md)(element: [E](index.md)): [Boolean](../../spheroid/-boolean/index.md)  <br><br><br>
| [clear](../-mutable-collection/clear.md)| Removes all elements from this collection.  <br>abstract override fun [clear](../-mutable-collection/clear.md)()  <br><br><br>
| [contains](../-collection/contains.md)| abstract operator override fun [contains](../-collection/contains.md)(element: [E](index.md)): Boolean  <br><br><br>
| [isEmpty](../-collection/is-empty.md)| abstract override fun [isEmpty](../-collection/is-empty.md)(): [Boolean](../../spheroid/-boolean/index.md)  <br><br><br>
| [remove](../-mutable-collection/remove.md)| Removes a single instance of the specified element from this collection, if it is present.  <br>abstract override fun [remove](../-mutable-collection/remove.md)(element: [E](index.md)): [Boolean](../../spheroid/-boolean/index.md)  <br><br><br>
| toString| open override fun toString(): String  <br><br><br>


## Properties  
  
|  Name|  Summary| 
|---|---|
| [size](index.md#spheroid.collections/MutableSet/size/#/PointingToDeclaration/)|  abstract override val [size](index.md#spheroid.collections/MutableSet/size/#/PointingToDeclaration/): [Long](../../spheroid/-long/index.md)   <br>

