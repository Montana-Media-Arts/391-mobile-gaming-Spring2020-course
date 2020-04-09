---
title: Create First Project
module: 14
jotted: true
---

# Create First Project

When you open Android Studio, it will either open the last project you had open, or you can create a new project.  We are going to create a new project and make sure we can get it run in our emulator.

1. Open **Android Studio**.
2. Either create a new project or click **File -> New -> New Project**.
3. Create a **Blank Project**.
4. Give your project a name and choose the **minimum SDK** to support.
    - Android Studio will indicate approximately how many devices are supported based on your choice.
5. Choose **Java** as your language.
6. Click **Next**.
7. You should now see the MainActivity.  This is where the application starts.
8. Click run and see if your application appears.  It should say **Hello World**.

Now, let's change some information and see if it changes in the emulator.

### Where do we go?

In Android, they use XML files to create the layout.  So, we need to go to the `activity_main` and make changes there.

### Where do we find this?

In the Project window, expand app, and then go to **res -> layout -> activity_main.xml**.

Now, let's take a look at the folders.