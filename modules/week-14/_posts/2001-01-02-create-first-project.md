<a href="https://umontana.zoom.us/rec/play/tcYpI-ypqjw3HYfE5QSDV6N6W464KaisgXUdqPoLn06wWyJWZwKhb-QUN0dyGam5XxKp65YR9kBwAjw?continueMode=true&_x_zm_rtaid=G4Add6vVSduO6RsyHuAu_A.1586561511718.8a343e83de4846f70f0030d0dc81d501&_x_zm_rhtaid=994">Video Link</a>

When you open Android Studio, it opens the last project, or you can create a new project.  We are going to create a new project and make sure we can get it run in our emulator.

1. Open **Android Studio**.
2. Either create a new project or click **File -> New -> New Project**.
3. Create a **Blank Project**.
4. Give your project a name and choose the **minimum SDK** to support it.
    - Android Studio will indicate approximately how many devices are supported based on your choice.
5. Choose **Java** as your language.
6. Click **Next**.
7. You should now see the MainActivity.  The MainActivity is where the application starts.
8. Click run and see if your application appears.  It should say **Hello World**.

Now, let's change some information and see if it updates in the emulator.

### Where do we go?

In Android, they use XML files to create the layout.  So, we need to go to the `activity_main` and make changes there.

### Where do we find this?

In the Project window, expand the app, and then go to **res -> layout -> activity_main.xml**.

Now, let's take a look at the folders.