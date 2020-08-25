//[Spheroid Script](../../index.md)/[spheroid.collections](../index.md)/[MutableCollection](index.md)



# MutableCollection  
 A generic collection of elements that supports adding and removing elements.  
  
interface [MutableCollection](index.md)<[E](index.md) : Any?>  : [Collection](../-collection/index.md)   


## Functions  
  
|  Name|  Summary| 
|---|---|
| [add](add.md)| Adds the specified element to the collection.  <br>fun [add](add.md)(element: [E](index.md)): [Boolean](../../spheroid/-boolean/index.md)  <br>
| [clear](clear.md)| Removes all elements from this collection.  <br>fun [clear](clear.md)()  <br>
| [contains](../-collection/contains.md)| Checks if the specified element is contained in this collection.  <br>operator fun [contains](../-collection/contains.md)(element: [E](index.md)): [Boolean](../../spheroid/-boolean/index.md)  <br>
| [isEmpty](../-collection/is-empty.md)| Returns true if the collection is empty (contains no elements), false otherwise.  <br>fun [isEmpty](../-collection/is-empty.md)(): [Boolean](../../spheroid/-boolean/index.md)  <br>
| [remove](remove.md)| Removes a single instance of the specified element from this collection, if it is present.  <br>fun [remove](remove.md)(element: [E](index.md)): [Boolean](../../spheroid/-boolean/index.md)  <br>
| toString| fun toString(): [String](../../spheroid/-string/index.md)  <br>


## Properties  
  
|  Name|  Summary| 
|---|---|
| [size](index.md#spheroid.collections/MutableCollection/size/#/PointingToDeclaration/)|  *Returns the size of the collection.*<br>val [size](index.md#spheroid.collections/MutableCollection/size/#/PointingToDeclaration/): [Long](../../spheroid/-long/index.md)   <br>


## Inheritors  
  
|  Name| 
|---|
| [MapMarkerCollection](../../spheroid.client.ar/-map-marker-collection/index.md)
| [NodeCollection](../../spheroid.client.ar/-node-collection/index.md)
| [MutableList](../-mutable-list/index.md)
| [MutableSet](../-mutable-set/index.md)

