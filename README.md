<h1>React Native Application Setup (Android)</h1>

<h2>Boilerplate and instructions for setting up a React Native Android Application</h2>

<p><a href="https://facebook.github.io/react-native/docs/getting-started.html" target="_blank">https://facebook.github.io/react-native/docs/getting-started.html</a></p>

<p>run `npm install` on cloning this repo to install necessary node modules</p>

<ul>
<strong>Requirements:</strong>
<li>Android Studio</li>
<li>Gradle</li>
<li>React Native CLI</li>
<li>NodeJS</li>
</ul>

<ol>
<strong>Instructions:</strong>
  <li>Just read and try to follow the instructions on the <a href="https://facebook.github.io/react-native/docs/getting-started.html" target="_blank">docs</a> until you execute `react-native run-android`. Also make sure to install all necessary components that Android Studio needs such as `Android SDK Platform 28` and `Intel x86 Atom_64 System Image` or `Google APIs Intel x86 Atom System Image`</li>
<li>Executing `react-native run-android` will fail. Do additional steps below</li>
<li>Go to the Android folder of the project then create/open the file `local.properties` add the line `sdk.dir = D:\\Android\\sdk` to it... where `D:\\Android\\sdk` is the path to your Android Studio Java SDK</li>
<li>Go to the Android folder of the project then open the file `gradle.properties` add the line `org.gradle.java.home=D:\\Android\\Android Studio\\jre` to it... where `D:\\Android\\Android Studio\\jre` is the path to your Android Studio Java JDK/JRE</li>
<li>Execute `react-native run-android` again. This will show a prompt on your device to allow installation. Take note that it has a timeout, once it runs out: the installation will be automatically denied. If you allow the installation, it should correctly install the app to your device</li>
</ol>

<hr>

<ul>
<strong>Additional Steps:</strong>
<li>To connect physical mobile device, setup adb... this is of course a separate tutorial. However, the gist is that you need to install the correct ADB driver for your device. The test device as of this writing was a Redmi 7A. Simply google `redmi 7a adb driver` and download & install the driver. After which, enable Developer mode and USB debugging on the Android device. This should suffice for connection using USB</li>
<li>To connect physical mobile device wirelessly, first connect the device to the computer using the USB method. Then execute `adb tcpip 5555` where 5555 is a port number. After that, execute `adb connect 192.168.137.11:5555` where 192.168.137.11:5555 is the IP of the mobile device with the corresponding port. Do `adb disconnect 192.168.137.11:5555` to disconnect once done with project</li>
<li>To enable Hot Reloading, just shake the android device and select the option from the menu</li>
</ul>

<hr>

<p>by JSON-G</p>
<p><small>at the time of this writing versions used were: android studio 3.5; gradle 5.4.1; react-native-cli 2.0.1; node v10.14.1; java sdk, jdk/jre utilized were that of the default kits installed with android studio</small></p>
