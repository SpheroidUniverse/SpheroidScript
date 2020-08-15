//[Spheroid Script](../../index.md)/[spheroid.collections](../index.md)/[MutableList](index.md)



# MutableList  
 A generic ordered collection of elements that supports adding and removing elements.  
  
interface [MutableList](index.md)<[E](index.md) : Any?>  : [List](../-list/index.md), [MutableCollection](../-mutable-collection/index.md)   


## Functions  
  
|  Name|  Summary| 
|---|---|
| [add](../-mutable-collection/add.md)| Adds the specified element to the collection.  <br>abstract override fun [add](../-mutable-collection/add.md)(element: [E](index.md)): [Boolean](../../spheroid/-boolean/index.md)  <br><br><br>
| [clear](../-mutable-collection/clear.md)| Removes all elements from this collection.  <br>abstract override fun [clear](../-mutable-collection/clear.md)()  <br><br><br>
| [contains](../-collection/contains.md)| abstract operator override fun [contains](../-collection/contains.md)(element: [E](index.md)): [Boolean](../../spheroid/-boolean/index.md)  <br><br><br>
| [get](../-list/get.md)| Returns the element at the specified index in the list.  <br>abstract operator override fun [get](../-list/get.md)(index: [Long](../../spheroid/-long/index.md)): [E](index.md)  <br><br><br>
| [isEmpty](../-collection/is-empty.md)| abstract override fun [isEmpty](../-collection/is-empty.md)(): [Boolean](../../spheroid/-boolean/index.md)  <br><br><br>
| [remove](../-mutable-collection/remove.md)| Removes a single instance of the specified element from this collection, if it is present.  <br>abstract override fun [remove](../-mutable-collection/remove.md)(element: [E](index.md)): [Boolean](../../spheroid/-boolean/index.md)  <br><br><br>
| [set](set.md)| Replaces the element at the specified position in this list with the specified element.  <br>abstract operator fun [set](set.md)(index: [Long](../../spheroid/-long/index.md), element: [E](index.md)): [E](index.md)  <br><br><br>
| toString| open override fun toString(): [String](../../spheroid/-string/index.md)  <br><br><br>


## Properties  
  
|  Name|  Summary| 
|---|---|
| [size](index.md#spheroid.collections/MutableList/size/#/PointingToDeclaration/)|  abstract override val [size](index.md#spheroid.collections/MutableList/size/#/PointingToDeclaration/): [Long](../../spheroid/-long/index.md)   <br>

