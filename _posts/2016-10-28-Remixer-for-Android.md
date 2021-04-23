---
layout : post
tittle: Remixer for Android
---
Yesterday, I got some info about usefull library from my friend, it is called Remixer. From their explanation, remixer is **a set of cross-platform libraries and protocols to allow the sharing of design values and live refinement of apps during the development process.**
After try some example and trial and error, I think this is a great library for handling the changes for UI operation during live development, like colors, text to view in user, and etc without **hardcode** and always repeat compile and build your code after changes some of codes. Let this library handle your task!

This library operation can handle via Cloud or your local operation, you can see it on their README explanation on their main repository [Remixer](https://github.com/material-foundation/material-remixer).

For android repo, you can see it on this [repo](https://github.com/material-foundation/material-remixer), this some important info about project structure that their made :

## Project structure

The project is defined as a gradle project with submodules.

* remixer_core: The core framework code, has no dependencies on the android framework and contains the core logic to run callbacks on changes to a Variable, etc. Most of the base classes are here
  * main: The code for the core framework
  * tests: JUnit tests for the Remixer code.
* remixer_ui: The code that shows remixes in the UI.
  * main
    * `com.google.android.libraries.remixer.ui.view` is  the code to display the UI as a BottomSheetFragmentDialog
    * `com.google.android.libraries.remixer.ui.widget` is a family of widgets that can display each individual Remixer item (variable or trigger).
    * `com.google.android.libraries.remixer.ui.widget.RemixerItemWidget` is an Interface to implement such widgets. Necessary if you want to provide different widgets.
    * `com.google.android.libraries.remixer.ui.RemixerCallbacks` is an implementation of `Application.ActivityLifecycleCallbacks` that clears up callbacks once the corresponding activity is destroyed so it doesn't leak. It needs to be registered in the `Application.onCreate()` method.
  * tests: JUnit/Robolectric tests.
* remixer_annotation: An annotation processor to make it easier to add remixes to your code.
  * main: The annotation processing code.
  * tests: JUnit tests based on actual classes to compile.
* remixer_example: This is an example app.
  * main: the code for the example app

## Building

1. Clone the repository
   ```git clone https://github.com/material-foundation/material-remixer-android.git```
2. You have two options here:
  1. Open it on Android Studio and build from there.
  2. run `./gradlew build`  on your terminal (`gradlew.bat build` on Windows).
    * This assumes that you have a copy of the android SDK and,
    * That you have exported a `ANDROID_HOME` environment variable that points to your SDK install (the directory that contains subdirectories such as `tools`, `platform-tools`, etc.)
      * If you use Android Studio on a mac that defaults to `/Users/<yourusername>/Library/Android/sdk`
      * In this case you can put `export ANDROID_HOME=/Users/<yourusername>/Library/Android/sdk` in your `~/.profile` or `~/.bash_profile` as appropriate.)

You can try build your example first. Happy coding!!


