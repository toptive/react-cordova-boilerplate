# React Cordova Boilerplate

Cordova is really simple to build cross platform mobile applications, this boilerplate provides a nice starting point for your next react project.

## Getting Started

```sh
git clone https://github.com/toptive/react-cordova-boilerplate.git
cd react-cordova-boilerplate
npm install # or yarn install
```

*NOTE:* Make sure you have an up-to-date version of [Node.js](https://nodejs.org/en/) installed on your system.

### Project Structure

Here is the basic skeleton of the app repo:


```bash
├── hooks
├── platforms
├── plugins
├── public
├── res
├── scripts
├── src
	├── images
	├── **/*.css
	├── **/*.js
├── www
├── .gitignore
├── CHANGELOG.md
├── config.xml
├── package.json
├── README.md

```

The **hooks** folder is where we put out cordova hooks if it was necessary.

The **platforms** folder is where Cordova will build the application for different platforms (iOS, Android, etc). The contents of this folder will be automatically generated by the Cordova CLI, and you should never edit code in that directory.

The **Plugins** folder will contain the installed plugins.

The **scripts** folder contain helper scripts to build the application.

The **res** folder is where are stored the app icon and the splash.

The **src** folder containt the source code for the whole application.

The **www** folder is where we will code the HTML / JavaScript application. Open the index.html file in a browser to see the default application created by the Cordova CLI.

Application parameters are stored in **config.xml**.


### Web side

* How to runs the App in development mode

```sh
npm start # or yarn start
```

Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

* How to builds the App for production mode

```sh
npm run build
```
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br>
Your app is ready to be deployed!

### Mobile Site

Apache Cordova is a build system for creating native mobile apps with bundled HTML and JavaScript content. Apps built with Cordova are native apps that can be published on the app stores.

* How to install dependencies

```sh
npm install -g cordova
```

* Building for Android Platform

To be able to build for the Android platform, the Android SDK must be installed on your system. If it's not, you can skip this step and add support for another platform, or simply run the application in your browser.

Make sure the Android SDK and the ant build tool are available on your system. The Android SDK is available [here](https://developer.android.com/studio/). Both the android and ant tools must be available in your path.

```sh
cordova platform add android
npm run build:android
```

The output is a debug-signed apk-file, located in subfolder *platforms/android/app/build/outputs/apk/.*
You can deploy the apk-file to a device using the adb install command (adb = Android Debug Bridge, a command-line tool for Android).


* Building for iOS Platform

To be able to build for the iOS platform, the iOS SDK must be installed on your system. If it's not, you can skip this step and add support for another platform, or simply run the tutorial application in your browser.

```sh
cordova platform add ios
npm run build:ios
```

The output is an Xcode project, located in subfolder *platforms/ios*. Open a Finder window and navigate to the folder, there you will find the file *Homecaregps.xcodeproj*. Open this file to launch the project in Xcode. From Xcode you can run the app in the iOS simulator, or deploy the app to a devices.

# Credits

This source was generated using [create-react-app](https://github.com/facebook/create-react-app) and [Apache Cordova](https://cordova.apache.org/) projects.
