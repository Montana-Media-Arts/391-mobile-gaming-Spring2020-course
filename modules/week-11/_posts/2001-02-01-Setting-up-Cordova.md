---
title: Setting up Cordova
module: 11
jotted: false
---

# Cordova

Cordova gives us a way to create, add platforms, compile and emulate projects.

Deploying from Cordova is a little elusive at this point hence why having Android Studio and XCode makes the most sense if you want to deploy from there.

In order to install Cordova, you must run the following command in the Command Prompt or in the Terminal.

**npm install -g cordova**

Then, you can double-check to ensure it works, by typing the following.

**cordova -v**

Let's see if it works.  Type in the following commands.

* cordova create cordova-hello-world
* cd cordova-hello-world
* cordova platform add android
* cordova build

What are we doing in each command?

The first one, creates the cordova project.  It will create the basic structure of HTML, CSS, and JavaScript.  The second command takes the user into the folder so that the Android platform is added to the project.  Finally, the fourth command builds to project.  It should indicate SUCCESS if everything okay.

If there are errors, it might be a little crazy to find them, but usually it's a version missing or a component missing.

For iOS, it's the same except it looks like this.

* cordova create cordova-hello-world
* cd cordova-hello-world
* cordova platform add ios
* cordova build

To see if to works in the emulator, then you need one more command.

* cordova emulate android OR
* cordova emulate ios

If you add both platforms to the same project, then it will try to build for all platforms that are added.


<!--
<iframe width="560" height="315" src="https://www.youtube.com/embed/m57TJlG7J_g" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>-->