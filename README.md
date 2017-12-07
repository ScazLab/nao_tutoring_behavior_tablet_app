# nao_tutoring_behavior_tablet_app

Forgive me I will write more here tomorrow. Most changes from previous versions of the app are in QuestionActivity.

## App Components and Flows

# Connection to server
The connection to the server is handled in the same way as in previous versions of the app via the TCPClient and TCPClientOwner classes.
The activity which is to receive messages from the server must implement the TCPClientOwner class, and control of the TCPClient instance must be transferred to in when the activity starts up.

More information on this class can be found [here](https://github.com/ScazLab/nao_tutoring/blob/master/README.md#implementing-the-tcpclientowner-interface)

# QuestionActivity
Most of the activity in the app happens during the QuestionActivity activity. During this activity, there is a permanent question panel displaying a division question to the user. A keyboard along the bottom serves as the input to the answer input box.
On the right side, there is a Help panel, which is either blank or displays any visuals necessary to the current tutoring behavior provided.

## Messages accepted from server:

## Examples and Tutorials:

## Breaks:


## Installation Instructions: 

The following instructions are taken directly from [this previous project's README] (https://github.com/ScazLab/nao_tutoring/blob/master/README.md#installation-instructions-android-app) and were written by Arsalan Sufi. 
They explain how to get the project's Android app compiling and running.

### Installing Android Studio and the Android SDK

To get the project's tablet app compiling on your machine, first install [Android Studio](http://developer.android.com/sdk/index.html).

Once you've installed Android Studio, use it to install the Android 21 SDK:

1. If you're at the Android Studio welcome menu, navigate to *Configure > SDK Manager*.
   If you're inside a project, navigate to *Tools > Android > SDK Manager*.
2. Check **Android 5.0 (Lollipop)** (Android 21) and hit *Apply*.

Android 21 is the target SDK for the project as noted in `AndroidManifest.xml`.
You can install other Android SDKs as well.
For example, you may want to install Android 16, which is the minimum SDK that the project supports.
This is also noted in `AndroidManifest.xml`.

### Importing the Project

If you're at the welcome menu, navigate to *Check out project from Version Control > Git*.
If you're inside a project, navigate to *File > New > Project from Version Control > Git*.
After you hit *Clone*, you may or may not be given the following option:
*Would you like to create a Studio project for the sources you have checked out to...?*

**If you are given this option...**

1. Click *Yes*.
2. Hit *Next* repeatedly until you see the screen that asks you to select a project SDK.
3. If **Android 21** isn't included in the list of options,
   1. Click the plus and then *Android SDK*.
   2. Navigate to your SDK directory and hit *OK*.
      On a Mac, your SDK directory is probably `/Users/{username}/Library/Android/sdk/`.
4. You should now be able to select **Android 21**.
5. Hit *Next* and then *Finish*.

**If you aren't given this option...**

1. Navigate to *File > Project Structure...*.
2. Click the *Project* tab on the left.
3. If **Android 21** isn't included in the list of options for *Project SDK*,
   1. Click *New...* and then *Android SDK*.
   2. Navigate to your SDK directory and hit *OK*.
      On a Mac, your SDK directory is probably `/Users/{username}/Library/Android/sdk/`.
4. You should now be able to select **Android 21**.
5. For the *Project language level*, select any value greater than or equal to **6**.
6. For the *Project compiler output*, `/path/to/repo/out/` is a good option.
7. Now click the *Modules* tab on the left.
8. Even if **nao_tutoring** is already listed as a module, click on it and hit the minus to remove it.
   We're going to re-add it; this forces Android Studio to do some indexing.
9. Click the plus and then *Import Module*.
10. Navigate to the repo and hit *OK*.
11. Hit *Next* repeatedly and eventually *Finish*.
12. Click *Apply*.

### Compiling and Running the App

You should now be able to compile and run the app!
To do this, click the green run arrow.
A pop-up menu will ask you to select a deployment target.
You can run the app on an actual tablet or in an emulator. 
To run the app on a tablet, plug the tablet into your laptop and make sure that your laptop recognizes it.
The tablet should show up under the list of *Connected Devices*.
If you don't have access to a tablet, you can use the *Create New Emulator* option.
To manage your emulators, use *Tools > Android > AVD Manager*.
