---
title: Compiling
module: 12
jotted: true
---

# Compiling

<a href="https://umontana.zoom.us/rec/play/vpx7Ieitrj83SN3EsgSDBaR8W426equs2ihN8_RenUy8UXIKNFv0NeQbYuNYGft4RsMz9t-BXm8b9lHl?continueMode=trueY" target="_new">Video</a>

The importance of this process is getting something to compile at the end.  Unity makes it reasonably simple to do having you select which platform you want to compile, and then having you install the proper tools required.

## Android

If you want to compile for Android, you go to File -> Build.

From there, you will see many options. Make sure if you have more than one scene, you add all scenes.  Then, change your platform to Android.

If you do not have the Android tools installed, it will ask you to download them.  Download and install them, and then you will be all set.

Then, there are several options which you can choose.  The important ones are if you are going to create a development build, a production build, the icons, the minimum, and the target platform.  Finally, if you do decide to build a production file, you will need a key that Unity helps you create.  You can self-generate a key to sign your application.

Then, you build the application, and it comes through as a .apk (if it's a development build) or a .aab if you have a production build.

## iOS

Building for iOS is just as straightforward.  You can change your settings in the Player Setting, add icons, and set all your parameters before deploying to the App Store. You will want XCode installed, though, to make it more seamless.