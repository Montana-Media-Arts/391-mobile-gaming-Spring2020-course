---
title: Bouncing
module: 14
jotted: true
---

# Bouncing Shapes

Somehow, we need to make sure the shape doesn't go out of bounds.  How are we going to do that?

Knowing what we know, we can look at getting the width and height of the screen and then use that in our calculations.

Luckily for us, we can get that from the the **Resources** class.

```java
    public static int getScreenWidth() {
        return Resources.getSystem().getDisplayMetrics().widthPixels;
    }
```

Now, how do we check to see if we are beyond the width?

We can create a simple if statement that check to see if we are greater or equal to the screen width and then bounce back if we are.

How do we do that?

First, we need a new variable called speed and we will put that at the top as well.

```java
int speed = 100;
```

Then, in our moveShape method, we need to change it so that it does the following.

```java
    if(myView.getX() >= getScreenWidth() || myView.getX() <= 0)
    {
        speed *= -1;
    }
```

Now, it checks for the right and left side.  However it does go off the screen.  Can you figure out how to make it not go off the screen?