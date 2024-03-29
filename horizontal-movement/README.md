![](../images/line3.png)

### Horizontal Movement

<sub>[previous](../bounce-ball/README.md#user-content-get-ball-to-bounce) • [home](../README.md#user-content-gms2-animation---table-of-contents) • [next](../squash-stretch/README.md#user-content-squash-and-stretch)</sub>

![](../images/line3.png)

In the video we have the ball moving left to right and our ball is boucing straight up and down.  Lets fix that.

<br>

---


##### `Step 1.`\|`ANIM`|:small_blue_diamond:

Open up **P4v**.  Select the top folder of the **GameMaker** project. Press the <kbd>Checkout</kbd> button.  Checkout out all files in P4V so that they are all writable (otherwise they will be read only and none of the changes will be saved). Select a **New** changelist and add a message describing the unit of work you will be performing. Press the <kbd>OK</kbd> button.

Open up the project you are working on in **GameMaker**. 

![checkout files and create new changelist](images/checkoutFiles.png)

![](../images/line2.png)

##### `Step 2.`\|`ANIM`|:small_blue_diamond: :small_blue_diamond: 

Open up **obj_ball | Create Event** and add an **hspeed** of `4`.  This will give it a boost.

![add hspeed of 4 to ball](images/addHspeedToBall.png)

![](../images/line2.png)

##### `Step 3.`\|`ANIM`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Now *press* the <kbd>Play</kbd> button in the top menu bar to launch the game. Woops the ball starts in the center.  Lets move it off screen to the top left then play again.  The ball is not going far enough.  I found an **hspeed** of `10` works best. The ball keeps going off screen but we will add some horizontal ground friction next.

https://user-images.githubusercontent.com/5504953/151790171-9fa117dc-2603-4306-bb73-4d9107e52ded.mp4

![](../images/line2.png)

##### `Step 4.`\|`ANIM`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Now notice in the traditional animation the ball slows down after each bounce and doesn't go as far.  The friction on the bounce slows down the horizontal speed.

![illustration of ground friction](images/nonElasticBouncing.png)

![](../images/line2.png)

##### `Step 5.`\|`ANIM`| :small_orange_diamond:

Now what we will do is reduce the speed by a fraction on each bounce.  Lets open up **obj_ball | Create** event and add a new variable called `horizontal friction` and set it to `0.6`.

![alt_text](images/horFriction.png)

![](../images/line2.png)

##### `Step 6.`\|`ANIM`| :small_orange_diamond: :small_blue_diamond:

Now everytime the ball collides with the ground reduce the overall speed of the ball.  Go to the **obj_ball | End Step** event and remove 60% of the horizontal speed.

![remove 60% of horizontal speed on ground collision](images/hspeedEndStep.png)

![](../images/line2.png)

##### `Step 7.`\|`ANIM`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond:
Now *press* the <kbd>Play</kbd> button in the top menu bar to launch the game. Notice that the ball comes to a stop at the end of the level, which is what we want!

https://user-images.githubusercontent.com/5504953/151791662-7d8b68f2-6547-4b28-992f-389c74d05be1.mp4

![](../images/line2.png)

##### `Step 8.`\|`ANIM`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Now to make it perfect it would be nice if the speed of the animation of the ball would slow down when it begins to come to a stop. Lets cut the speed by half when the ball is moving less than a pixel per frame horizontally.

![ball animation slows down as it stops](images/ballSlowsDownAtStop.png)

##### `Step 9.`\|`ANIM`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Now *press* the <kbd>Play</kbd> button in the top menu bar to launch the game. Now that adds a nice touch.  

https://user-images.githubusercontent.com/5504953/151793115-31715c9a-af8a-4ddd-94ba-cdb958087170.mp4

![](../images/line2.png)

##### `Step 10.`\|`ANIM`| :large_blue_diamond:

Open up **P4V**.  Select the top folder and press the **Add** button.  We want to add all the new files we created during this last session.  Add these files to the last change list you used at the begining of the session. Press the <kbd>OK</kbd> button.

![add new and changed files to p4v](images/add.png)

![](../images/line2.png)

##### `Step 11.`\|`ANIM`| :large_blue_diamond: :small_blue_diamond: 

Now you can submit the changelist by pressing both <kbd>Submit</kbd> buttons.

![submit changelist to p4v](images/submit.png)



___


![](../images/line.png)

<!-- <img src="https://via.placeholder.com/1000x100/45D7CA/000000/?text=Next Up - Squash and Stretch"> -->
![alt_text](images/banner.png)

![](../images/line.png)

| [previous](../bounce-ball/README.md#user-content-get-ball-to-bounce)| [home](../README.md#user-content-gms2-animation---table-of-contents) | [next](../squash-stretch/README.md#user-content-squash-and-stretch)|
|---|---|---|
