//[Spheroid Script](../../index.md)/[spheroid.collections](../index.md)/[MutableList](index.md)



# MutableList  
 A generic ordered collection of elements that supports adding and removing elements.  
  
interface [MutableList](index.md)<[E](index.md) : Any?>  : [List](../-list/index.md), [MutableCollection](../-mutable-collection/index.md)   


## Functions  
  
|  Name|  Summary| 
|---|---|
| [add](../-mutable-collection/add.md)| Adds the specified element to the collection.  <br>fun [add](../-mutable-collection/add.md)(element: [E](index.md)): [Boolean](../../spheroid/-boolean/index.md)  <br>
| [clear](../-mutable-collection/clear.md)| Removes all elements from this collection.  <br>fun [clear](../-mutable-collection/clear.md)()  <br>
| [contains](../-collection/contains.md)| operator fun [contains](../-collection/contains.md)(element: [E](index.md)): [Boolean](../../spheroid/-boolean/index.md)  <br>
| [get](../-list/get.md)| Returns the element at the specified index in the list.  <br>operator fun [get](../-list/get.md)(index: [Long](../../spheroid/-long/index.md)): [E](index.md)  <br>
| [isEmpty](../-collection/is-empty.md)| fun [isEmpty](../-collection/is-empty.md)(): [Boolean](../../spheroid/-boolean/index.md)  <br>
| [remove](../-mutable-collection/remove.md)| Removes a single instance of the specified element from this collection, if it is present.  <br>fun [remove](../-mutable-collection/remove.md)(element: [E](index.md)): [Boolean](../../spheroid/-boolean/index.md)  <br>
| [set](set.md)| Replaces the element at the specified position in this list with the specified element.  <br>operator fun [set](set.md)(index: [Long](../../spheroid/-long/index.md), element: [E](index.md)): [E](index.md)  <br>
| toString| fun toString(): [String](../../spheroid/-string/index.md)  <br>


## Properties  
  
|  Name|  Summary| 
|---|---|
| [size](index.md#spheroid.collections/MutableList/size/#/PointingToDeclaration/)|  val [size](index.md#spheroid.collections/MutableList/size/#/PointingToDeclaration/): [Long](../../spheroid/-long/index.md)   <br>

