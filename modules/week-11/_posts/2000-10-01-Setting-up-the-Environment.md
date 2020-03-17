---
title: Setting up the Android Environment
module: 11
jotted: true
---

# Download and install Java and Android Studio

Regardless if you are running a PC or Mac, these steps will get you up and running if you want to compile and run an Android mobile application.

1. Download and install the Java JDK [Java](https://www.oracle.com/java/technologies/javase-jdk8-downloads.html) - You will need to scroll down the page to download the proper version.  Oracle also requires that you sign in to download the JDK.
2. Once installed, then check to see what version you have.  Either open the Command Prompt in Windows (Search -> cmd), or the terminal window on a Mac (Finder -> Applications -> search for Terminal).
3. Type in java -version and make sure you see a version of the JDK appear.
4. Download the Android Studio. [Android Studio](https://developer.android.com/studio/index.html) - it is significant in size, and it takes a long time, but honestly, it's much easier than trying to install the SDK and then the emulators.  Android Studio has it all, and when you are ready to deploy, you can build your APK from Android Studio.

<iframe width="560" height="315" src="https://umontana.zoom.us/rec/play/vMZ8dLur-jo3H4aSswSDCqB-W42-Lf2s1nUXrKAOmka2VncHNVCvb-QVa-eIwX_nIF6lBISoym0Pc8Qu?continueMode=true
" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

# Download and install Gradle
1. Go to [Gradle](https://gradle.org/releases/)
2. Scroll down and find the most recent release.
3. Download it, unzip it and put in the C: drive.

# Download and install ANT

1. Navigate to [Ant Download](https://ant.apache.org/bindownload.cgi) and download the top version of ANT as a zip file.
2. Unzip the file and put it in the C: drive.

<iframe width="560" height="315" src="https://umontana.zoom.us/rec/play/tJclf7z6qmo3TtCXtASDUf5wW466fays0nBPqaBZzxvmVHNXNQauYOQVZeA0TenLsjgI0vi9h52OYd4a?continueMode=true" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

# Download and install Node.js
1. Go to node.js [nodejs.org](https://nodejs.org/en/).
2. Download the most recent version and install it using all the defaults.

# Setting up the Environment Variables

This first part is for PC's

After installing the Java JDK and Android Studio, you must set the environment variables, so Cordova knows how to create an Android project.


1. Click on Search -> Environment. (Select Edit the System Environment Variables)
2. Click the Environment Variables button on the bottom.
3. In the Environment Variables dialog, under the System Variables section, click the New button.
4. For variable name, type **JAVA_HOME**.
5. For Variable Value, click Browse and navigate to where the JDK installation.  For example, it could be here. C:\Program Files\Java\jdk1.8.0_241
6. Click OK

For the **ANDROID_HOME** environment variable, things get a little trickier.  

1. Navigate to the **App_Data** folder inside your user directory.  If you do not have hidden folders turned on, you will need to go into Windows Explorer and click the View menu item and then check Hidden Items.
2. Now, go into Environment Variables and click on New again.
3. Create a variable name called **ANDROID_HOME**.
4. For the value, click Browse and navigate to something like this (C:\Users\micha\AppData\Local\Android\Sdk)
5. Create a variable name **ANDROID_SDK_ROOT** and provide the same value as before.

For the **ANT_HOME** environment variable, create a new environment variable.

1. Click on New, and name the variable **ANT_HOME**.
2. For the value, browse to where you put the unzipped folder. The following directory path is an example. (C:\apache-ant-1.9.14-bin\apache-ant-1.9.14\bin)

Alter the **PATH** variable.

1. Click on **PATH** and click on **Edit**.
2. You want to add the following to the path.

Example paths: 
* C:\Program Files\nodejs\
* C:\Users\micha\AppData\Local\Android\Sdk\tools
* C:\Users\micha\AppData\Local\Android\Sdk\platform-tools
* C:\apache-ant-1.9.14-bin\apache-ant-1.9.14\bin
* C:\Program Files\Java\jdk1.8.0_241\jre\bin
* C:\Users\micha\AppData\Local\Android\Sdk
* C:\Gradle\gradle-6.1.1\bin

Now, close all the environment variable dialog windows and go back to the command prompt.

* adb version
* gradle -v

You should see the version of each when executing the previous commands.

We also want to check the correct installation of nodejs.  In the command prompt, type the following.

* node -v

You should see the version of nodejs installed.

For Mac's, installing is a little more straightforward.

1. Download and install the Java JDK
2. Download and install Android Studio
3. Download and install node.js
4. Download and install Gradle
5. Run the following commands in the Terminal.
    * mkdir ~/opt/gradle 
    * unzip -d ~/opt/gradle gradle-6.2.2-bin.zip
    * ls /opt/gradle/gradle-6.2.2
6. Set the path variable - export PATH=$PATH: ~/opt/gradle/gradle-6.2.2/bin 

<iframe width="560" height="315" src="https://umontana.zoom.us/rec/play/vZF4Jris-D43HNKRsQSDU6UrW469L6ysgCVI-fJcnUqzBXAFM1GlZrAWN7eJ6Xat1cT2isqPzzMgomb_?continueMode=true
" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Whew, that was a lot!

Let's move onto settings up the iOS development environment.

