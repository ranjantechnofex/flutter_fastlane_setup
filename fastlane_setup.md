
# Firebase, FlutteFire and Fastlane Integration

This guide simplifies integrating Firebase services into your Flutter app, leveraging the FlutterFire CLI for effortless configuration and Fastlane for automated app distribution via Firebase App Distribution.


## **Prerequisites**

* **Flutter Development Environment:**  Ensure you have Flutter installed and configured on your system.
* **Firebase Project:** Create a Firebase project on the [Firebase Console](https://console.firebase.google.com/).
* **Node.js and npm (or yarn):** Required for installing the Firebase CLI and FlutterFire CLI.



## Installation FlutterFire

**[FlutterFire CLI:](https://firebase.flutter.dev/docs/cli/)**
* **NPM Install**
  ```bash
    npm install -g firebase-tools  
  ```
* **Global Activate Flutter Fire CLI**
  ```bash
    dart pub global activate flutterfire_cli
  ```
* **Log into Firebase using your Google account**
  ```bash
    firebase login  
  ```
* **List your Firebase project**
  ```bash
    firebase projects:list  
  ```
  
* **In the root of your application**
  ```bash
    flutterfire configure  
  ```
    
## Fastlane installation
**Step1. Setup Fastlane**

  **[Fastlane Android Setup:](https://docs.fastlane.tools/getting-started/android/setup/)**
  * **Fastlane Install**
    ```bash
      sudo gem install fastlane or gem install fastlane 
    ```
  * **Navigate your terminal to your project's directory i.e android folder**
    ```bash
      fastlane init
    ```
  You'll be asked to confirm that you're ready to begin, and then for a few pieces of     information. To get started quickly:
  * Provide the package name for your application when asked (e.g. io.fabric.yourapp)
  * Press enter when asked for the path to your json secret file
  * Answer 'n' when asked if you plan on uploading info to Google Play via fastlane (we can set this up later)

  That's it! fastlane will automatically generate a configuration for you based on the information provided.

  You can see the newly created ./fastlane directory, with the following files:

  * Appfile which defines configuration information that is global to your app
  * Fastfile which defines the "lanes" that drive the behavior of fastlane
      
  The most interesting file is fastlane/Fastfile, which contains all the information that is needed to distribute your app.
