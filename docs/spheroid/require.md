//[Spheroid Script](../index.md)/[spheroid](index.md)/[require](require.md)



# require  
 
Throws an [IllegalArgumentException](-illegal-argument-exception/index.md) if the [value]() is false.  
  
  
fun [require](require.md)(value: [Boolean](-boolean/index.md)): [Unit](-unit/index.md)  


 
Throws an [IllegalArgumentException](-illegal-argument-exception/index.md) with the result of calling [lazyMessage]() if the [value]() is false.  
  
  
fun [require](require.md)(value: [Boolean](-boolean/index.md), lazyMessage: () -> [Any](-any/index.md)): [Unit](-unit/index.md)  



