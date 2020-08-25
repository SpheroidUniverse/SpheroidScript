//[Spheroid Script](../index.md)/[spheroid](index.md)



# Package spheroid  


## Types  
  
|  Name|  Summary| 
|---|---|
| [Any](-any/index.md)| class [Any](-any/index.md)  <br>
| [App](-app/index.md)| object [App](-app/index.md)  <br>
| [Boolean](-boolean/index.md)| class [Boolean](-boolean/index.md)  <br>
| [ByteArray](-byte-array/index.md)| class [ByteArray](-byte-array/index.md)  <br>
| [Date](-date/index.md)| class [Date](-date/index.md)  <br>
| [Decimal](-decimal/index.md)| class [Decimal](-decimal/index.md) : [Number](-number/index.md)  <br>
| [Device](-device/index.md)| object [Device](-device/index.md)  <br>
| [Distance](-distance/index.md)| class [Distance](-distance/index.md)(**meters**: [Number](-number/index.md))  <br>
| [Double](-double/index.md)| class [Double](-double/index.md) : [Number](-number/index.md)  <br>
| [Exception](-exception/index.md)| class [Exception](-exception/index.md)(**message**: [String](-string/index.md))  <br>
| [IllegalArgumentException](-illegal-argument-exception/index.md)| class [IllegalArgumentException](-illegal-argument-exception/index.md)(**message**: [String](-string/index.md)) : [Exception](-exception/index.md)  <br>
| [IllegalStateException](-illegal-state-exception/index.md)| class [IllegalStateException](-illegal-state-exception/index.md)(**message**: [String](-string/index.md)) : [Exception](-exception/index.md)  <br>
| [LatLng](-lat-lng/index.md)| class [LatLng](-lat-lng/index.md)(**lat**: [Number](-number/index.md), **lng**: [Number](-number/index.md))  <br>
| [Loadable](-loadable/index.md)| interface [Loadable](-loadable/index.md)  <br>
| [Long](-long/index.md)| class [Long](-long/index.md) : [Number](-number/index.md)  <br>
| [Number](-number/index.md)| abstract class [Number](-number/index.md)  <br>
| [Pair](-pair/index.md)| Represents a generic pair of two values.There is no meaning attached to values in this class, it can be used for any purpose. Pair exhibits value semantics, i.e. two pairs are equal if both components are equal.  <br>class [Pair](-pair/index.md)<[A](-pair/index.md) : Any?, [B](-pair/index.md) : Any?> (**first**: [A](-pair/index.md), **second**: [B](-pair/index.md))  <br>
| [Platform](-platform/index.md)| object [Platform](-platform/index.md)  <br>
| [PlatformVersion](-platform-version/index.md)| interface [PlatformVersion](-platform-version/index.md)  <br>
| [Quaternion](-quaternion/index.md)| class [Quaternion](-quaternion/index.md)(**x**: [Number](-number/index.md), **y**: [Number](-number/index.md), **z**: [Number](-number/index.md), **w**: [Number](-number/index.md))  <br>
| [Source](-source/index.md)| class [Source](-source/index.md)(**path**: [String](-string/index.md))  <br>
| [String](-string/index.md)| class [String](-string/index.md)  <br>
| [TimeInterval](-time-interval/index.md)| class [TimeInterval](-time-interval/index.md)(**days**: [Number](-number/index.md)?, **hours**: [Number](-number/index.md)?, **minutes**: [Number](-number/index.md)?, **seconds**: [Number](-number/index.md)?, **milliseconds**: [Number](-number/index.md)?)  <br>
| [Unit](-unit/index.md)| object [Unit](-unit/index.md)  <br>
| [UUID](-u-u-i-d/index.md)| class [UUID](-u-u-i-d/index.md)(**value**: [String](-string/index.md))  <br>
| [Vector3](-vector3/index.md)| class [Vector3](-vector3/index.md)(**x**: [Number](-number/index.md), **y**: [Number](-number/index.md), **z**: [Number](-number/index.md))  <br>


## Functions  
  
|  Name|  Summary| 
|---|---|
| [check](check.md)| Throws an [IllegalStateException](-illegal-state-exception/index.md) if the [value]() is false.  <br>fun [check](check.md)(value: [Boolean](-boolean/index.md)): [Unit](-unit/index.md)  <br>Throws an [IllegalStateException](-illegal-state-exception/index.md) with the result of calling [lazyMessage]() if the [value]() is false.  <br>fun [check](check.md)(value: [Boolean](-boolean/index.md), lazyMessage: () -> [Any](-any/index.md))  <br>
| [error](error.md)| Throws an [IllegalStateException](-illegal-state-exception/index.md).  <br>fun [error](error.md)()  <br>Throws an [IllegalStateException](-illegal-state-exception/index.md) with the given [message]().  <br>fun [error](error.md)(message: [Any](-any/index.md))  <br>
| [repeat](repeat.md)| Executes the given function [action]() specified number of [times]().A zero-based index of current iteration is passed as a parameter to [action]().  <br>fun [repeat](repeat.md)(times: [Long](../spheroid/-long/index.md), action: ([Long](../spheroid/-long/index.md)) -> [Unit](-unit/index.md))  <br>
| [require](require.md)| Throws an [IllegalArgumentException](-illegal-argument-exception/index.md) if the [value]() is false.  <br>fun [require](require.md)(value: [Boolean](-boolean/index.md)): [Unit](-unit/index.md)  <br>Throws an [IllegalArgumentException](-illegal-argument-exception/index.md) with the result of calling [lazyMessage]() if the [value]() is false.  <br>fun [require](require.md)(value: [Boolean](-boolean/index.md), lazyMessage: () -> [Any](-any/index.md)): [Unit](-unit/index.md)  <br>

