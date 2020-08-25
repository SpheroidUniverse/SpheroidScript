//[Spheroid Script](../../index.md)/[spheroid.collections](../index.md)/[List](index.md)



# List  
 A generic ordered collection of elements. Methods in this interface support only read-only access to the list; read/write access is supported through the MutableList interface.  
  
interface [List](index.md)<[E](index.md) : Any?>  : [Collection](../-collection/index.md)   


## Functions  
  
|  Name|  Summary| 
|---|---|
| [contains](../-collection/contains.md)| Checks if the specified element is contained in this collection.  <br>operator fun [contains](../-collection/contains.md)(element: [E](index.md)): [Boolean](../../spheroid/-boolean/index.md)  <br>
| [get](get.md)| Returns the element at the specified index in the list.  <br>operator fun [get](get.md)(index: [Long](../../spheroid/-long/index.md)): [E](index.md)  <br>
| [isEmpty](../-collection/is-empty.md)| Returns true if the collection is empty (contains no elements), false otherwise.  <br>fun [isEmpty](../-collection/is-empty.md)(): [Boolean](../../spheroid/-boolean/index.md)  <br>
| toString| fun toString(): [String](../../spheroid/-string/index.md)  <br>


## Properties  
  
|  Name|  Summary| 
|---|---|
| [size](index.md#spheroid.collections/List/size/#/PointingToDeclaration/)|  *Returns the size of the collection.*<br>val [size](index.md#spheroid.collections/List/size/#/PointingToDeclaration/): [Long](../../spheroid/-long/index.md)   <br>


## Inheritors  
  
|  Name| 
|---|
| [MutableList](../-mutable-list/index.md)

