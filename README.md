# C31_Complete_game
for the eat animation we don’t want the animation to loop or play again and again, so to prevent that we will keep eat.looping = false.
--------------------
The computer tries to play the animation as fast as possible, but we want our animation to play a little slower so that we can see what is happening in the animation.
To slow the speed of the animation we need to set a frame delay. This is going to be a number, the higher the number the slower will be the speed.
We will set this for both the loaded animations, blink and eat.
blink.frameDelay = 20;
eat.frameDelay = 20;
We can keep any value between 15 and 20, that will look good for our animation.
------------------------------------------------------
show the effect of the value on the speed of the animation by changing it to 5 and then keeping it at 20.


-----------------------------
You will create a function that will detect the collision between the fruit body and the bunny.
To detect the collision, you are going to use a very simple algorithm. Which is to find the distance between fruit and bunny.
As the fruit moves toward the bunny, the distance decreases. We can write the condition in such a way that if the distance is less than a certain value we can say both the objects have collided.


------------------
Once the fruit falls down, we need to remove the fruit from the world. But if we remove the fruit then we can not calculate the distance between the fruit and the bunny, so we need to put the condition in such a way, it will only calculate the distance if the fruit body exists.


The second important thing is if we remove the fruit from the world then we can't draw it. Because we have deleted the body from the world, and while drawing we are referencing the x and y position of the fruit body. If a fruit body does not exist, and we are still drawing it on the canvas, then it will give us an error.
--------------------
When can we say that 2 bodies have collided?
Yes, we can say that when the distance between 2 bodies
is 0 we can say they have collided.
We will use the same logic here, we need to find the distance between the fruit and the bunny.
That we will do using the dist() function, which is an in-built function of the p5.js library.
This function needs four points:
● X position of first body or shape.
● Y position of first body or shape then,
● X position of the second body or shape.
● Y position of the second body or shape.
It will then calculate the distance between two points.
We will need a variable to store this value, so we can declare a variable here and assign the dist() function to it.



In our case, we will set it as 80.
If this condition is true then we need to remove the fruit from the world and make it null. Because when the fruit collides with the bunny it will eat the fruit, so it is supposed to disappear from the scene.
For that, we will use the World.remove() function and then set the fruit null.
