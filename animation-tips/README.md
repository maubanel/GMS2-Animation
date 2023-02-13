![](../images/line3.png)

### Animation Tips

<sub>[previous](../run-cycle/README.md#user-content-animating-a-run-cycle) • [home](../README.md#user-content-gms2-background-tiles--sprites---table-of-contents)</sub>

![](../images/line3.png)

Lets look at some suggestions for how we can approach animating characters that are more complex than simple doodles.

<br>

---


##### `Step 1.`\|`BTS`|:small_blue_diamond:

Now lets look at character animations. Animations for games are very different than ones for movies or cartoons. Each animation is atomic (each animation represents an individual action), mostly loopable and connect to each other in a logical manner. We also want animations to be short and crisp so that the player has maximum control over the player actions.  We typically exaggerate motion and move it quickly so the player can move fast on screen.

![animating monkey](images/WalkCycle.gif)

![](../images/line2.png)

##### `Step 2.`\|`BTS`|:small_blue_diamond: :small_blue_diamond: 

What is the above animation composed of? This breaks a run cycle into 8 frames:

![frames of animating monkey](images/EightFrameWalkCycle.png)

![](../images/line2.png)

##### `Step 3.`\|`BTS`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

There are many tricks and techniques for animating characters. One of them is to start very simple and build more detail slowly:

![start low res work up](images/StartLowResWorkWayUp.png)

![](../images/line2.png)

##### `Step 4.`\|`BTS`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

You can also build it piece by piece:

![build animation piece by piece](images/PieceByPiece.png)

![](../images/line2.png)

##### `Step 5.`\|`BTS`| :small_orange_diamond:

For most animations some vertical translation helps a lot - make it bouncy.  Take a look at this amazing animation from <a href="http://probertson.tumblr.com/post/82062175084/mercenary-kings-animations" target="_blank">Mercenary Kings</a>. Keep it simple and represent the animation in as few frames as possible. Just as we want to get rid of the “grid” in the tiles; we want to lose a sense of where the animation is looping. Can you see the stitch? Can you guess how many animation frames there are? Can you see that different animations start and stop and there is a good demonstration of overlap going on here.

Look at the shading above in the feet of the robot. The back legs are dark which clearly delinates the front and back legs. In the old 8 bit games there were not enough colors in the pallette (or enough pixels in the character) to give detail and shadows. 

![scott pilgrim robot animation](http://paulrobertson.mechafetus.com/mk/exoidle.gif)


![](../images/line2.png)

##### `Step 6.`\|`BTS`| :small_orange_diamond: :small_blue_diamond:

You can continue to trace on reference then build up the form gradually.

![trace image](images/TraceOnTopOfReference.png)

![](../images/line2.png)

##### `Step 7.`\|`BTS`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond:

Now have fun and create some terrific animations for you next game!


___


<img src="https://via.placeholder.com/1000x4/dba81a/dba81a" alt="drawing" height="4px" alt = ""/>

<img src="https://via.placeholder.com/1000x100/45D7CA/000000/?text=Next Up - That's All Folks!">

<img src="https://via.placeholder.com/1000x4/dba81a/dba81a" alt="drawing" height="4px" alt = ""/>

| [previous](../run-cycle/README.md#user-content-animating-a-run-cycle)| [home](../README.md#user-content-gms2-background-tiles--sprites---table-of-contents) | 
|---|---|
