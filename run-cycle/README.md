<img src="https://via.placeholder.com/1000x4/45D7CA/45D7CA" alt="drawing" height="4px"/>

### Animating a Run Cycle

<sub>[previous](../) • [home](../README.md#user-content-gms2-background-tiles--sprites---table-of-contents) • [next](../)</sub>

<img src="https://via.placeholder.com/1000x4/45D7CA/45D7CA" alt="drawing" height="4px"/>

Now lets try and animate a walk cycle we can use in the game. This is for a platformer side view.  So I found reference of a person walking who is directly at 90 degrees from the camera.

<br>

---


##### `Step 1.`\|`BTS`|:small_blue_diamond:

It is always good when making your first walk cycle to use some reference.  In this case we will be tracing a stick person animation.  Just like the ball for walking/running we need to animate the player without translation (like running on a treadmill).  There is lots of good reference on YouTube.  Lets use this one. Click on the picture below to view the video on YouTube.

[![how to animate a ball in 2d](https://img.youtube.com/vi/vq9A5FD8G5w/0.jpg)](https://www.youtube.com/watch?v=vq9A5FD8G5w)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 2.`\|`BTS`|:small_blue_diamond: :small_blue_diamond: 

For reference I took screenshot of every 10<sup>th</sup> frames of the animation.  This resulted in a 9 frame walk cycle.  I took it with 1 frame less than a full walk cycle (right foot swinghing forward below hip all the way to right foot 1 frame before right hip).  If you loop it creates a seamless walk cycle. I scaled down the sequence but left it larger than I want in the game for more precision pencil work (I will scale it down to game size later). You can download the [AnimReference.psd file here](images/AnimReference.psd). 

![walk animation reference layers](images/walkRef.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 3.`\|`BTS`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

I used procreate on an iPad but you can use Photoshop or countless other paint packages.  It is best to use a tablet again for animation.  I added a white layer on top of the first layer.  I changed the opactity to about 70%. This allows me to see the drawing while still able to see the pose for tracing.

![white semi-opaque layer](images/whiteLayer.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 4.`\|`BTS`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Then I traced a stick-person on top of each pose on its own layer above the white one.  I tried to keep the forward limbs a bit darker than the back leg and arm.

![trace single frame of walk](images/tracedImage.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 5.`\|`BTS`| :small_orange_diamond:

Now I move the white tracing layer up and add a layer for the remaining 8 frames and get a pose drawn for each reference frame. 

https://user-images.githubusercontent.com/5504953/152154007-f5998b7a-2943-4e12-ba9c-f9536d02a9e6.mp4

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 6.`\|`BTS`| :small_orange_diamond: :small_blue_diamond:

Remove all reference, white and any background.  You should just have 8 transparent layers.  Trim the image and change the longest side to `128`. Then adjust the canvas to `128` so we get a square frame.  Make sure the feet are at the very bottom of the frame.

![rescale images](images/scaleTrim.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 7.`\|`BTS`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond:

Export each frame as a `.png` file naming them `spr_walk_1` to `spr_walk_9`.

![export 9 animation frames](images/eachFrame.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 8.`\|`BTS`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Create a new sprite called `spr_walk` and press the <kbd>Import</kbd> button.  Import the 9 animation frames.

![import 9 animations](images/sprWalk.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 9.`\|`BTS`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Adjust the **FPS** (Frames per Second) to a speed that looks right to you.  I selected `12`.

https://user-images.githubusercontent.com/5504953/152157005-97dffc82-d01c-4595-81de-682d20bd5693.mp4

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 10.`\|`BTS`| :large_blue_diamond:

*Right click* on **Objects** and select **New | Object** and name it `obj_player`. Set the **Sprite** to `spr_walk`.

![create obj_player and assign walk sprite](images/objWalk.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 11.`\|`BTS`| :large_blue_diamond: :small_blue_diamond: 
 
 *Right click* on **rm_ball_bounce** and select **Duplicate** and name it `rm_player`. Change the **Room Order** to place this room on the top of the list. Remove `obj_ball` and add `obj_player` to the center room on the floor.

![duplicate rm_ball_bounce for room player and add player to room](images/rmPlayer.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>


##### `Step 12.`\|`BTS`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond: 

Now *press* the <kbd>Play</kbd> button in the top menu bar to launch the game. Now we can see our animation in game!

https://user-images.githubusercontent.com/5504953/152159169-c55a937c-05c0-4a11-add0-d5f419530dd7.mp4

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 13.`\|`BTS`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond:  :small_blue_diamond: 

![alt_text](images/.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 14.`\|`BTS`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:  :small_blue_diamond: 

![alt_text](images/.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 15.`\|`BTS`| :large_blue_diamond: :small_orange_diamond: 

![alt_text](images/.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 16.`\|`BTS`| :large_blue_diamond: :small_orange_diamond:   :small_blue_diamond: 

![alt_text](images/.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 17.`\|`BTS`| :large_blue_diamond: :small_orange_diamond: :small_blue_diamond: :small_blue_diamond:

![alt_text](images/.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 18.`\|`BTS`| :large_blue_diamond: :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

![alt_text](images/.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 19.`\|`BTS`| :large_blue_diamond: :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

![alt_text](images/.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 20.`\|`BTS`| :large_blue_diamond: :large_blue_diamond:

![alt_text](images/.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 21.`\|`BTS`| :large_blue_diamond: :large_blue_diamond: :small_blue_diamond:

![alt_text](images/.png)

___


<img src="https://via.placeholder.com/1000x4/dba81a/dba81a" alt="drawing" height="4px" alt = ""/>

<img src="https://via.placeholder.com/1000x100/45D7CA/000000/?text=Next Up - ADD NEXT PAGE">

<img src="https://via.placeholder.com/1000x4/dba81a/dba81a" alt="drawing" height="4px" alt = ""/>

| [previous](../)| [home](../README.md#user-content-gms2-background-tiles--sprites---table-of-contents) | [next](../)|
|---|---|---|
