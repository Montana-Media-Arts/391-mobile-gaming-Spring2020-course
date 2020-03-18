---
title: Compiling
module: 12
jotted: true
---

# Compiling

<!--<iframe width="560" height="315" src="https://www.youtube.com/embed/1fgs9Qj5_vY" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>-->

The importan of this process is getting something to compile at the end.  Unity makes it fairly simple to do having you select which platform you want to compile and then having you install the proper tools required.

## Android

If you want to compile for Android, you go to File -> Build.

From there, you will see a number of options. Make sure if you have more than one scene, you add all scenes.  Then, change your platform to Android.

If you do not have the Android tools installed, it will ask you to download them.  Download and install them and then you will be all set.

Then, there are a number of options in which you can choose.  The important ones are if you are going to create a development build, a production build, the icons, the minimum and the target platform.  Finally, if you do decide to build a production file, you will need a key which Unity helps you create.  You can self-generate a key to sign your application.

Then, you build the application and it comes through as a .apk (if it's a development build) or a .aab if you have a production build.

## iOS

Building for iOS is just as straightforward.  You can change your settings in the Player Setting, add icons, and set all your parameters before deploying to the App Store. You will want XCode installed though to make it more seamless.

