---
title: Unity Characters
module: 12
jotted: true
---

# Characters

<iframe width="560" height="315" src="https://umontana.zoom.us/rec/play/vMYpI-j7rj03S9CcswSDBadxW9XsKa6s0iAb_fIFnR7hVncKZgXzNeQUMbGMZFYJcSkz8DiAUVB1tY5w?continueMode=true" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

In Unity, we add characters by going into the project folder, finding an image or object and dragging into the scene.

I got spiky mace by going into Enemies -> png -> 128x128 and dragging the Mace into the Scene.

I placed the Mace on the ground.  If I run it right now, it doesn't do anything.

So, in order to make it move, I need to add a couple of things.

First, it needs physics.  So, click on Add Component -> Physics 2D -> RigidBody2D.  At this point, if you run it, the Mace should fall through the ground.  Do you know why?

In order to fix this problem, we need to add collision to the Mace too.

So, go back and click Add Component -> Physics 2D -> Polygon Collider 2D.

Finally, to make the Mace move, we need to add some code.  Go to the next section to find out how to do that.
