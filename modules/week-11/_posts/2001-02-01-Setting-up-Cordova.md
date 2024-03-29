---
title: Setting up Cordova
module: 11
jotted: false
---

# Cordova

Cordova gives us a way to create, add platforms, compile, and emulate projects.

Deploying from Cordova is a little elusive at this point; hence why having Android Studio and XCode makes the most sense if you want to deploy from there.

To install Cordova, you must run the following command in the Command Prompt or the Terminal.

**npm install -g cordova**

Then, you can double-check to ensure it works, by typing the following.

**cordova -v**

Let's see if it works—type in the following commands.

* cordova create cordova-hello-world
* cd cordova-hello-world
* cordova platform add android
* cordova build

What are we doing in each command?

The first one creates a cordova project.  It establishes the basic structure of HTML, CSS, and JavaScript.  
The second command takes the user into the folder, and the third adds the Android platform to the project.  Finally, the fourth command builds the project.  It should indicate SUCCESS if everything okay.

If there are errors, it might be a little crazy to find them, but usually, it's a version missing or a component missing.

For iOS, it's the same, except it looks like this.

* cordova create cordova-hello-world
* cd cordova-hello-world
* cordova platform add ios
* cordova build

To see if to works in the emulator, then you need one more command.

* cordova emulate android OR
* cordova emulate ios

If you add both platforms to the same project, then it builds all added platforms.

<a href="https://umontana.zoom.us/rec/play/tZZ4c-iorGg3HoKS5QSDBPd9W421LKKs0SAf__IKyE2zWyECNFGmMrQSZbcX28Ryy3ZltmAG4Y0jersj?continueMode=true" target="_new">Video</a>