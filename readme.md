# Overview

The htmel Mobile package is a simple and efficient way to build cross-platform mobile applications using web technologies. This package leverages a Capacitor-like architecture, allowing you to create mobile apps that run in WebViews on both iOS and Android devices. By updating the HTML files in the www folder, you can modify what is rendered in the application without needing to change any native code.

# Getting Started

Prerequisites
Before using the htmel Mobile package, ensure you have the following installed on your machine:

Node.js (version 12 or higher)
npm (Node Package Manager)
Xcode (for iOS development, on macOS)
Android Studio (for Android development)
Project Structure
Your project will have the following structure:

```

htmel-mobile/
├── android/
│ ├── app/
│ │ ├── src/
│ │ │ ├── main/
│ │ │ │ ├── java/com/htmelmobileapp/
│ │ │ │ │ ├── MainActivity.java # Main Android activity with WebView
│ │ │ │ │ ├── WebAppInterface.java # JavaScript interface for native code
│ │ │ │ ├── res/
│ │ │ │ │ ├── layout/
│ │ │ │ │ │ ├── activity_main.xml # Layout file for the WebView
│ │ │ │ ├── AndroidManifest.xml # Android manifest file
│ │ │ ├── build.gradle # Android build configuration
│ ├── gradle/
│ ├── settings.gradle
├── ios/
│ ├── htmelMobileApp/
│ │ ├── AppDelegate.swift # iOS entry point
│ │ ├── ViewController.swift # Main view controller with WebView
│ │ ├── WebAppBridge.swift # JavaScript-native bridge for iOS
│ │ ├── Main.storyboard # iOS UI definition (if using Storyboard)
│ ├── Info.plist # iOS configuration file
│ ├── Podfile # iOS dependencies configuration
├── www/
│ ├── index.html # Main web page (entry point)
│ ├── js/
│ │ ├── app.js # Main JavaScript for web app
│ │ ├── bridge.js # JS bridge to communicate with native
│ ├── css/
│ │ ├── style.css # Web app styles
├── plugins/
│ ├── battery-plugin/
│ │ ├── android/
│ │ │ ├── BatteryPlugin.java # Battery plugin for Android
│ │ ├── ios/
│ │ │ ├── BatteryPlugin.swift # Battery plugin for iOS
│ │ ├── battery-plugin.js # JavaScript interface for battery plugin
├── scripts/
│ ├── build.js # Build script to bundle web assets
├── package.json # Node project configuration (npm/yarn)
├── README.md # Project description and instructions
```

# Updating Content

Modify HTML Files:
Navigate to the www/ directory in your project.
Update the HTML files as needed. The main entry point is index.html, but you can add or modify other HTML files, CSS styles, and JavaScript as necessary.
Changes made to these files will reflect in the app's WebViews after building.
Building the Application:
After updating the HTML files, you will need to build the application to see your changes.
Run the following command to build the web assets:
bash
Copy code
npm run build
This command executes the build.js script, which bundles your web files for deployment.
Deploying the Application
Once you've made your updates and built your application, you can deploy it to your target platform.

Deploy to iOS:
bash
Copy code
npm run deploy:ios
Deploy to Android:
bash
Copy code
npm run deploy:android
Testing the Application
After deploying, you can test the application on the iOS Simulator or Android Emulator. You should see the updates you've made in the HTML files reflected in the app's user interface.

Conclusion

The htmel Mobile package allows you to create mobile applications using standard web technologies. By simply updating the files in the www/ folder, you can efficiently manage the content and appearance of your app. Building and deploying the application is straightforward with the provided scripts, enabling a smooth development experience across both iOS and Android platforms.
