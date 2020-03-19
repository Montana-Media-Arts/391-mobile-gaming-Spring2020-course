---
title: Unity Scripts
module: 12
jotted: true
---

# Unity Scripts

<iframe width="560" height="315" src="https://umontana.zoom.us/rec/play/vpIod7z9rT03HYKT4gSDBaR4W9W4Kf-s1yUY8_EJnh3mWnIFNACvZOREauU7DkzC5uKQKA43vJ-gcERt?continueMode=true" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

To make the character move, we must add some custom code.  It is C# code which is a Microsoft based language but looks familar to JavaScript, Java and C++ even.

First, select the Mace.  Then, click on Add Component, scroll to the bottom and select New Script.

From there, name the Script Movement.

It should add a script to the bottom of the list of components for the Mace.

However, we need to alter it.  So, double click on the Script in the Inspector and it should open Visual Studio 2019, 2017, etc.

From there, we must take a look at what to change.

## Custom Scripts

All custom scripts start with two main methods.  This should sound really familar!  There is a `Start` and an `Update`.  This is just like setup and draw.  They work the same, just different names.

We are going to add the following script.

```csharp
public float speed;                //Floating point variable to store the player's movement speed.

    private Rigidbody2D rb2d;        //Store a reference to the Rigidbody2D component required to use 2D Physics.

    void Start()
    {
        rb2d = GetComponent<Rigidbody2D>();
    }

    // Update is called once per frame
    void Update()
    {
        // Get the horizontal and vertical axis.
        // By default they are mapped to the arrow keys.
        // The value is in the range -1 to 1
        //Store the current horizontal input in the float moveHorizontal.
        float moveHorizontal = Input.GetAxis("Horizontal");

        //Store the current vertical input in the float moveVertical.
        float moveVertical = Input.GetAxis("Vertical");

        //Use the two store floats to create a new Vector2 variable movement.
        Vector2 movement = new Vector2(moveHorizontal, moveVertical);

        //Call the AddForce function of our Rigidbody2D rb2d supplying movement multiplied by speed to move our player.
        rb2d.AddForce(movement * speed);

```

Now, make sure you save it because if you don't it won't work.  It's quirkly like that.  Go back to Unity and run it and see if you can move with your WASD or arrow keys.

Did it work?  Great!

## Mobile Update

What if you want to make it work for mobile?  You have to change the script al ittle to handle it.  Below is an example that works on mobile. Notice the if statements and the touch events.

```csharp
  private Rigidbody2D rb2d;        //Store a reference to the Rigidbody2D component required to use 2D Physics.
    public float speed;
    void Start()
    {
        rb2d = GetComponent<Rigidbody2D>();
    }

    // Update is called once per frame
  
    void Update()
    {
        int horizontal = 0;      //Used to store the horizontal move direction.
        int vertical = 0;        //Used to store the vertical move direction.

        //Check if we are running either in the Unity editor or in a standalone build.
#if UNITY_EDITOR || UNITY_STANDALONE || UNITY_WEBPLAYER

            //Get input from the input manager, round it to an integer and store in horizontal to set x axis move direction
            horizontal = (int) (Input.GetAxisRaw ("Horizontal"));

            //Get input from the input manager, round it to an integer and store in vertical to set y axis move direction
            vertical = (int) (Input.GetAxisRaw ("Vertical"));

            //Check if moving horizontally, if so set vertical to zero.
            if(horizontal != 0)
            {
                vertical = 0;
            }


        //Check if we are running on iOS, Android, Windows Phone 8 or Unity iPhone
#elif UNITY_IOS || UNITY_ANDROID || UNITY_WP8 || UNITY_IPHONE
        float x = 0;
        float y = 0;
        // Handle screen touches.
        if (Input.touchCount > 0)
        {
            Touch touch = Input.GetTouch(0);

                Vector2 pos = touch.position;
                x = pos.x;
                y = pos.y;
         
                //Check if the difference along the x axis is greater than the difference along the y axis.
                if (Mathf.Abs(x) > Mathf.Abs(y))
                    //If x is greater than zero, set horizontal to 1, otherwise set it to -1
                    horizontal = x > 0 ? 1 : -1;
                else
                    //If y is greater than zero, set horizontal to 1, otherwise set it to -1
                    vertical = y > 0 ? 1 : -1;
            
        }


#endif //End of mobile platform dependendent compilation section started above with #elif
        Vector2 movement = new Vector2(horizontal, vertical);

        //Call the AddForce function of our Rigidbody2D rb2d supplying movement multiplied by speed to move our player.
        rb2d.AddForce(movement * speed);
    }


```

