# Welcome to Flutter development

This repository contains my guides/tutorials about using Flutter.

![logo](assets/flutter-logo.jpg "Flutter logo")

Once upon a time, on February 27 2018, Google annoucend the first beta of a new mobile development technology named [Flutter](https://developers.googleblog.com/2018/02/announcing-flutter-beta-1.html). It is gaining more and more attention and even some developers published apps relying on a beta version of Flutter.

This article tries to give you a glimpse of Flutter. Without further dues, let's get going :steam_locomotive:.

## Introduction

[Flutter](https://flutter.io) is a new technology that allows to make native iOS and Android apps using a single code base. In fact, we write a single programs with the [Dart programming language](https://www.dartlang.org/) and get as a result a native iOS app and as well as a native an Android. This is possible because Dart code is [compiled into native code](https://flutter.io/faq/#run-android). What's more interesting though is that UI view are not translated into their native counterpart (as opposed to [Xamarin](https://www.xamarin.com/)). Instead, it has its own 2D rendering engine that renders the views (which are called widgets as we'll see later) very efficiently.

## Setup

This README shows how to install it on macOS. I mainly followed the [guide here](https://flutter.io/setup-macos/)

- Install Xcode from the mac app store and run it at least once to launch the post setup.
- Configure Xcode command line tools by running this command `sudo xcode-select --switch /Applications/Xcode.app/Contents/Developer`
- Agree the Xcode license agreement using this command: `sudo xcodebuild -license`
- Install the Android SDK using the Android Studio installer [from here](https://developer.android.com/studio/index.html#downloads). I install Android Studio which also installs Android SDK. Here also, run Android Studio at least once in order to install additional tools.
- Add to your profile (~/.profile, ~/.bash_profile or ~/.zshrc) the `ANDROID_HOME` which point to the location of the Android SDK on you disk.
- Install one of those three IDEs (or all :) ): Visual Studio Code (VS Code), Android Studio or IntelliJ. I will be using VS Code.
- Install **Dart Code** VS Code extension.
- Install [Homebrew as described here](https://brew.sh/)
- Using homebrew, install the following packages: ios-deploy and cocoapods. Here are the commands that performs that.

```sh
brew install ios-deploy
brew install cocoapods
pod setup
```

- Download the latest [Flutter SDK here](https://flutter.io/sdk-archive/#macos). At the time of writing, I have downloaded version 0.2.8 beta.
- Unzip the archive somewhere on your disk.
- Add the flutter's bin folder to your path.
- Start an iOS simulator using `open -a Simulator`.
- Accept Android licenses using this command: `flutter doctor --android-licenses`
- Run the command `flutter doctor` in order to check if everything is ok. Depending on you environment, you should see a different output. My first output is this one because I didn't install all the required tools.

```
-> % flutter doctor
Doctor summary (to see all details, run flutter doctor -v):
[✓] Flutter (Channel beta, v0.2.8, on Mac OS X 10.13.4 17E199, locale fr-FR)
[!] Android toolchain - develop for Android devices (Android SDK 26.0.2)
    ! Some Android licenses not accepted.  To resolve this, run: flutter doctor --android-licenses
[!] iOS toolchain - develop for iOS devices (Xcode 9.3)
    ✗ ios-deploy out of date (1.9.2 is required). To upgrade:
        brew upgrade ios-deploy
    ✗ CocoaPods not installed.
        CocoaPods is used to retrieve the iOS platform side's plugin code that responds to your plugin usage on the Dart side.
        Without resolving iOS dependencies with CocoaPods, plugins will not work on iOS.
        For more info, see https://flutter.io/platform-plugins
      To install:
        brew install cocoapods
        pod setup
[✓] Android Studio (version 3.1)
[!] IntelliJ IDEA Community Edition (version 2016.2.5)
    ✗ Flutter plugin not installed; this adds Flutter specific functionality.
    ✗ Dart plugin not installed; this adds Dart specific functionality.
    ✗ This install is older than the minimum recommended version of 2017.1.0.
[!] VS Code (version 1.22.2)
[!] Connected devices
    ! No devices available

! Doctor found issues in 5 categories.
```

After following the remaining issues, except installing IntelliJ. I got the following output

```
-> % flutter doctor
Doctor summary (to see all details, run flutter doctor -v):
[✓] Flutter (Channel beta, v0.2.8, on Mac OS X 10.13.4 17E199, locale fr-FR)
[✓] Android toolchain - develop for Android devices (Android SDK 26.0.2)
[✓] iOS toolchain - develop for iOS devices (Xcode 9.3)
[✓] Android Studio (version 3.1)
[!] IntelliJ IDEA Community Edition (version 2016.2.5)
    ✗ Flutter plugin not installed; this adds Flutter specific functionality.
    ✗ Dart plugin not installed; this adds Dart specific functionality.
    ✗ This install is older than the minimum recommended version of 2017.1.0.
[✓] VS Code (version 1.22.2)
[✓] Connected devices (1 available)

! Doctor found issues in 1 category.
```

Now you are all setup and ready.

## Links

[Official guide](https://flutter.io/setup-macos/)
