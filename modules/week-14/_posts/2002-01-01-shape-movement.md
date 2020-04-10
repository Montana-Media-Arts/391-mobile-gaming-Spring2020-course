---
title: Make our Image Move
module: 14
jotted: true
---

# Movement

<a href="https://umontana.zoom.us/rec/play/uscqfriurD83E9CStQSDAfB_W428Kaysg3cZr_UKn0y2VSMKM1X3Z-MSZbZeipFRyMFnPsuMVfoUcOmf?continueMode=true&_x_zm_rtaid=G4Add6vVSduO6RsyHuAu_A.1586561511718.8a343e83de4846f70f0030d0dc81d501&_x_zm_rhtaid=994">Video Link</a>

If we are going to make this interesting, then we should make our image move.  How do we do that?  We will now turn to the code to make this happen.

1. Go to MainActivity.java file.
2. In the onCreate method, we must first get the drawable that we added.
3. Since we added it to an ImageView, we must get that from the layout.


```java

ImageView myView = (ImageView)findViewById(R.id.imageView2);
```

** Note: as you add new classes like ImageView, you will need to import the class into the code.  The Android Studio will help with this.

The previous gets the imageView from the layout.  Make sure you put the correct name in there.

Now, to make it move, we need another line underneath the previous one.

```java
ImageView myView = (ImageView)findViewById(R.id.imageView2);
myView.setX(myView.getX()+300);
```

This sets the x-value with the current x-value plus 300 pixels which should move it to 300 to the right.

The complete onCreate method should look like this.

```java
   protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        ImageView myView = (ImageView)findViewById(R.id.imageView2);
        myView.setX(myView.getX()+300);
    }
```

This is great, but how do we make it move?

This is where timers comes in.

So, we are going to add something else.

First, thing we need to do is move the definition of the ImageView to the class level so it can be seen everywhere.  We also need to create a new object called Timer.

So, add the following lines before the onCreate method.

```java
    Timer timer = new Timer();
    ImageView myView;
```

Now, we need to update the onCreate method so it looks like this.

```java
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        myView = (ImageView)findViewById(R.id.imageView2);
        myView.setX(myView.getX()+300);

        timer.schedule(new MoveTask(),100,1000);
    }
```

The timer will call the MoveTask class every second after a 100 millisecond delay.  What does the MoveTask class look like?

This class should be inside your MainActivity class and after your onCreate method.

```java
class MoveTask extends TimerTask {
        public void run() {
            moveShape();
        }
    }
```

This class is a special because it extends (it is a child of) the TimerTask so it is a TimerTask and can act like a clock now. Don't worry about the details!

The important part is that is calls the moveShape method.

That method looks like this.

```java
    public void moveShape() {
         myView = (ImageView)findViewById(R.id.imageView2);
         myView.setX(myView.getX()+100);
    }

```

Does this look familiar?  It should.  Those two lines in the moveShape method was in the onCreate method earlier. Now it's just being called over and over the timerTask.

The next question, is how do we get it to bounce around?