![](../images/line3.png)

### Squash and Stretch II

<sub>[previous](../squash-stretch/README.md#user-content-squash-and-stretch) • [home](../README.md#user-content-gms2-animation---table-of-contents) • [next](../run-cycle/README.md#user-content-animating-a-run-cycle)</sub>

![](../images/line3.png)

Lets finish off squash and stretch by addin stretch.

<br>

---


##### `Step 1.`\|`ANIM`|:small_blue_diamond:

The final step in the video is adding stretch when the ball bounces up.  It should only be used on the high bounces (first two).

![stretch illustration](images/stretch.png)

![](../images/line2.png)

##### `Step 2.`\|`ANIM`|:small_blue_diamond: :small_blue_diamond: 

Now in your paint package we will draw 3 stretch frames.  Now it should be pointing the direction it is bouncing in.  We should do this in code.  So we should draw it with the forward direction pointing right.  It should look like so: 

![3 stretch frames](images/draw3Stretch.png)

![](../images/line2.png)

##### `Step 3.`\|`ANIM`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

So the final set of frames of the balls should include the ball, the squash and three stretch frames.

![all ball frames](images/finalBallFrames.png)

![](../images/line2.png)

##### `Step 4.`\|`ANIM`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Now remove the background and trim, scale and resize canvas to `128` by `128`.  Now the ball size has shrunk because of the long stretch piece.  I will need to re-export all the ball frames to `.png` to maintain scale. The stretch animations are exported as `spr_stretch_1.png`, `spr_stretch_2.png`, `spr_stretch_3.png`.

![trim, scale and resized frames](images/trimScale.png)

![](../images/line2.png)

##### `Step 5.`\|`ANIM`| :small_orange_diamond:

Re-import the smaller `spr_ball_1.png` through `spr_ball_6.png`, `spr_squash.png` and `spr_small_squash.png`.

![reimport squashes and ball](images/reimportFrames.png)

![](../images/line2.png)

##### `Step 6.`\|`ANIM`| :small_orange_diamond: :small_blue_diamond:

*Right click* on **Sprites** and select **New | Sprite** and name it `spr_stretch`. Press the <kbd>Import</kbd> button and select the stretch sprites.

![import three stretches](images/importStretches.png)

![](../images/line2.png)

##### `Step 7.`\|`ANIM`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond:

When the ball is below 500 pixels it needs to go from squash to stretch frames.  We will have a zone between 400 and 500 to run the stretch animation.  We will only do it if the animation has a large amount of vertical motion.  We will only switch if there is `-15` pixels per frame in `vspeed` as this means it is bouncing hard. Since we drew the angle of the streatch as `0` degrees we can set `image_angle` to `direction`. We put this as an `else if` after the squash if statement.

![add stretching logic](images/stretchLogic.png)

![](../images/line2.png)

##### `Step 8.`\|`ANIM`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Now *press* the <kbd>Play</kbd> button in the top menu bar to launch the game. It looks a bit strange.

https://user-images.githubusercontent.com/5504953/151975686-2b797825-5660-4e45-8b3c-2696005a7b3f.mp4

![](../images/line2.png)

##### `Step 9.`\|`ANIM`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

If we overlay the last frame of squash with the first frame of stretch, it is rotating on the top corner of the sprite and not the middle of the ball.  We will need to make some changes. 

![bad rotation illustration](images/badRotation.png)

![](../images/line2.png)

##### `Step 10.`\|`ANIM`| :large_blue_diamond:

So we need to rotate the ball in its center of gravity.  Open up `spr_ball`, `spr_small_squash`, `spr_squash` and `spr_stretch`. Grab the origin target and center it in the shape. You can do this by eyball as the circle is not in the center of the bounding box.  

![center origin on spr_ball](images/sprBallCenterOrigin.png)


![center origin on spr_small_squash](images/sprSmalLSquashCenterOrigin.png)

![center origin on spr_squash](images/sprSquashCenterOrigin.png)

![center origin on spr_stretch](images/sprStretchCenterOrigin.png)

![](../images/line2.png)

##### `Step 11.`\|`ANIM`| :large_blue_diamond: :small_blue_diamond: 

Now we need to readjust the y position for all the bouncing.  We moved the origin so the position of the ball will change in the room.  Open it up and drag the ball to the ground.  In my case it no longer snaps to the ground.  Open up the **grid icon** and turn off **Snap**.

![turn snap off](images/turnSnapOff.png)

![](../images/line2.png)

##### `Step 12.`\|`ANIM`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond: 

Now you can position the ball pixel by pixel and put it on the ground plane.  Record the **y** value.  Mine is `628`

![move ball to ground plane y is 628](images/newYPos.png)

![](../images/line2.png)

##### `Step 13.`\|`ANIM`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond:  :small_blue_diamond: 

Move ball back to top left corner.

![move ball back to top left corner](images/moveBallBack.png)

![](../images/line2.png)

##### `Step 14.`\|`ANIM`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:  :small_blue_diamond: 

Now our bouncing point on **y** is `628`.  Previously it was `544`.  So with 628 - 544 = 84.  So we need to add `84` units to each y position in our **obj_ball | End Step**.

![adjust y by 84 units](images/newYPositions.png)

![](../images/line2.png)

##### `Step 15.`\|`ANIM`| :large_blue_diamond: :small_orange_diamond: 

In slow motion you can see that the ball is now changing animation states properly and it looks good.

https://user-images.githubusercontent.com/5504953/152091105-f23736b4-54c5-4e0a-8f01-9962fe0eb49f.mp4

![](../images/line2.png)

##### `Step 16.`\|`ANIM`| :large_blue_diamond: :small_orange_diamond:   :small_blue_diamond: 

Now *press* the <kbd>Play</kbd> button in the top menu bar to launch the game. This is not how we would handle a ball in a game but is an example of how you approach a simple problem from an animated scene to replicating it in a "game" way.

https://user-images.githubusercontent.com/5504953/152091132-0ed66867-f410-4d12-bd50-61c79099e6b9.mp4

##### `Step 17.`\|`ANIM`| :large_blue_diamond: :small_orange_diamond: :small_blue_diamond: :small_blue_diamond:

Open up **P4V**.  Select the top folder and press the **Add** button.  We want to add all the new files we created during this last session.  Add these files to the last change list you used at the begining of the session. Press the <kbd>OK</kbd> button.

![add new and changed files to p4v](images/add.png)

![](../images/line2.png)

##### `Step 18.`\|`ANIM`| :large_blue_diamond: :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Now you can submit the changelist by pressing both <kbd>Submit</kbd> buttons.

![submit changelist to p4v](images/submit.png)

___


![](../images/line.png)

<!-- <img src="https://via.placeholder.com/1000x100/45D7CA/000000/?text=Next Up - Animating a Run Cycle"> -->
![alt_text](images/banner.png)

![](../images/line.png)

| [previous](../squash-stretch/README.md#user-content-squash-and-stretch)| [home](../README.md#user-content-gms2-animation---table-of-contents) | [next](../run-cycle/README.md#user-content-animating-a-run-cycle)|
|---|---|---|
