//[Spheroid Script](../../index.md)/[spheroid.client.ar](../index.md)/[ModelNode](index.md)



# ModelNode  
 class [ModelNode](index.md) : [Node](../-node/index.md)   


## Functions  
  
|  Name|  Summary| 
|---|---|
| [getAnimationController](get-animation-controller.md)| fun [getAnimationController](get-animation-controller.md)(name: String): [AnimationController](../-animation-controller/index.md)  <br>override fun [getAnimationController](../-node/get-animation-controller.md)(animation: [Animation](../-animation/index.md)): [AnimationController](../-animation-controller/index.md)  <br><br><br>
| [getAudioController](../-node/get-audio-controller.md)| override fun [getAudioController](../-node/get-audio-controller.md)(audio: [SceneAudio](../-scene-audio/index.md)): [SceneAudioController](../-scene-audio-controller/index.md)  <br><br><br>
| [onTap](../-node/on-tap.md)| override fun [onTap](../-node/on-tap.md)(callback: () -> Unit)  <br><br><br>
| [playAnimation](play-animation.md)| fun [playAnimation](play-animation.md)(name: String, loop: Boolean): [AnimationController](../-animation-controller/index.md)  <br>override fun [playAnimation](../-node/play-animation.md)(animation: [Animation](../-animation/index.md), loop: Boolean): [AnimationController](../-animation-controller/index.md)  <br><br><br>
| [playAudio](../-node/play-audio.md)| override fun [playAudio](../-node/play-audio.md)(audio: [SceneAudio](../-scene-audio/index.md), loop: Boolean): [SceneAudioController](../-scene-audio-controller/index.md)  <br><br><br>
| toString| open override fun toString(): String  <br><br><br>


## Properties  
  
|  Name|  Summary| 
|---|---|
| [children](index.md#spheroid.client.ar/ModelNode/children/#/PointingToDeclaration/)|  override val [children](index.md#spheroid.client.ar/ModelNode/children/#/PointingToDeclaration/): [NodeCollection](../-node-collection/index.md)   <br>
| [eulerAngles](index.md#spheroid.client.ar/ModelNode/eulerAngles/#/PointingToDeclaration/)|  override var [eulerAngles](index.md#spheroid.client.ar/ModelNode/eulerAngles/#/PointingToDeclaration/): [Vector3](../../spheroid/-vector3/index.md)   <br>
| [location](index.md#spheroid.client.ar/ModelNode/location/#/PointingToDeclaration/)|  override var [location](index.md#spheroid.client.ar/ModelNode/location/#/PointingToDeclaration/): [LatLng](../../spheroid/-lat-lng/index.md)?   <br>
| [model](index.md#spheroid.client.ar/ModelNode/model/#/PointingToDeclaration/)|  var [model](index.md#spheroid.client.ar/ModelNode/model/#/PointingToDeclaration/): [Model](../-model/index.md)?   <br>
| [position](index.md#spheroid.client.ar/ModelNode/position/#/PointingToDeclaration/)|  override var [position](index.md#spheroid.client.ar/ModelNode/position/#/PointingToDeclaration/): [Vector3](../../spheroid/-vector3/index.md)   <br>
| [rotation](index.md#spheroid.client.ar/ModelNode/rotation/#/PointingToDeclaration/)|  override var [rotation](index.md#spheroid.client.ar/ModelNode/rotation/#/PointingToDeclaration/): [Quaternion](../../spheroid/-quaternion/index.md)   <br>
| [scale](index.md#spheroid.client.ar/ModelNode/scale/#/PointingToDeclaration/)|  override var [scale](index.md#spheroid.client.ar/ModelNode/scale/#/PointingToDeclaration/): [Vector3](../../spheroid/-vector3/index.md)   <br>
| [worldPosition](index.md#spheroid.client.ar/ModelNode/worldPosition/#/PointingToDeclaration/)|  override var [worldPosition](index.md#spheroid.client.ar/ModelNode/worldPosition/#/PointingToDeclaration/): [Vector3](../../spheroid/-vector3/index.md)   <br>

