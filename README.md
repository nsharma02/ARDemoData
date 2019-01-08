# ARDemoData


Using ARKit 2.0

1) Wall Decoration :  To decorate wall by putting picture with frames of any size using Augmented Reality

Start ARSession with configuration
An ARAnchor will get added , once vertical plane detected.
Tap on added object and select image/frame of your choice.
This app adds multiple objects and  odify them.

ImageChaneType protocol - manages and return selected picture/frame to controller
func addOrUpdateFrame - when user selects a frame
func addOrUpdatePicture - when user selects a picture

2) Gallery Info : It displays infomation/details corresponding to picture on wall.
Start ARSession with ARImageConfiguration
Add image to configuartion.trackingImages  = <set of UIImages to track>
ImageInfoData Model class contains image with its description.
func renderer(_ renderer: SCNSceneRenderer, didAdd node: SCNNode, for anchor: ARAnchor) function that create text node once track image detected.


3) Save My Work : This allow user to save their work(put pictures on wall) on firebase and can reload again whenever required.
Kindly  select both frame and image , before saving.
find vertical plane, add image and frame.
save data with unique id.

4) Exibition : Aim to create a virtual exibition of picures

Solution 1 :  Create ARPortal(a virtual room) and add pictures to room wall. 
Refer this for creating room wall images.
https://docs.unity3d.com/Manual/class-Cubemap.html
check function - addExibitionRoom(hitResult : ARHitTestResult)

Solution 2 :  place picture at any coordinate after world origin load.
check function - addPictures(hitResult : ARHitTestResult)

It detect horizontal surface, tap to place pictures



 
