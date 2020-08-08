//[Spheroid Script](../../index.md)/[spheroid.collections](../index.md)/[MutableCollection](index.md)



# MutableCollection  
 A generic collection of elements that supports adding and removing elements.  
  
interface [MutableCollection](index.md)<[E](index.md) : Any?>  : [Collection](../-collection/index.md)   


## Functions  
  
|  Name|  Summary| 
|---|---|
| [add](add.md)| Adds the specified element to the collection.  <br>abstract fun [add](add.md)(element: [E](index.md)): [Boolean](../../spheroid/-boolean/index.md)  <br><br><br>
| [clear](clear.md)| Removes all elements from this collection.  <br>abstract fun [clear](clear.md)()  <br><br><br>
| [contains](../-collection/contains.md)| Checks if the specified element is contained in this collection.  <br>abstract operator override fun [contains](../-collection/contains.md)(element: [E](index.md)): Boolean  <br><br><br>
| [isEmpty](../-collection/is-empty.md)| Returns true if the collection is empty (contains no elements), false otherwise.  <br>abstract override fun [isEmpty](../-collection/is-empty.md)(): [Boolean](../../spheroid/-boolean/index.md)  <br><br><br>
| [remove](remove.md)| Removes a single instance of the specified element from this collection, if it is present.  <br>abstract fun [remove](remove.md)(element: [E](index.md)): [Boolean](../../spheroid/-boolean/index.md)  <br><br><br>
| toString| open override fun toString(): String  <br><br><br>


## Properties  
  
|  Name|  Summary| 
|---|---|
| [size](index.md#spheroid.collections/MutableCollection/size/#/PointingToDeclaration/)|  Returns the size of the collection.abstract override val [size](index.md#spheroid.collections/MutableCollection/size/#/PointingToDeclaration/): [Long](../../spheroid/-long/index.md)   <br>


## Inheritors  
  
|  Name| 
|---|
| [MapMarkerCollection](../../spheroid.client.ar/-map-marker-collection/index.md)
| [NodeCollection](../../spheroid.client.ar/-node-collection/index.md)
| [MutableList](../-mutable-list/index.md)
| [MutableSet](../-mutable-set/index.md)

