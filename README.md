# MobileAutomation_GS_APK

## Overview

This tutorial is a web automation framework built using Selenium WebDriver and Java. It provides a foundation for automating web applications, allowing for efficient and reliable testing of web functionalities.

## Features

- **Page Object Model (POM)**: The framework follows the Page Object Model design pattern, providing a clear separation of page elements and test logic.
- **TestNG Integration**: TestNG is used as the testing framework, offering features such as parallel execution, data-driven testing, and reporting.
- **Reporting**: Extent Reports is integrated for comprehensive and interactive test reports, making it easy to analyze test results.
- **Cross-Browser Testing**: The framework supports cross-browser testing, allowing tests to be executed on different web browsers such as Chrome, Firefox, and Safari.
- **Configurability**: The framework's configuration is easily customizable, allowing users to specify test data, environment settings, and browser configurations.

### Getting Started
Follow these steps to set up your development environment and start using Selenium with Java

### Prerequisites

1. [Java JDK](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html)
2. Choose one of the following IDE:
    - [Eclipse](https://www.eclipse.org/downloads/packages/release/2024-03/r/eclipse-ide-java-developers)
    - [IntelliJ IDEA](https://www.jetbrains.com/idea/download/)
    - [Spring Tools](https://spring.io/tools)
3. [Apache Maven](https://maven.apache.org/download.cgi)
4. [Android Studio](https://developer.android.com/studio)
5. [Java-8](https://drive.google.com/file/d/14_dSxe9CegypKgSfmkLq3n6KU98l-VzQ/view) - If needed

### Installation

1. Java JDK
    - Download the installer from the [Oracle Java SE Downloads](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) page.
    - Run the installer and set up the JDK.
2. IDE
    - Download and install your preferred IDE.
3. Apache Maven
    - Download Apache Maven from the [official website](https://maven.apache.org/download.cgi).
    - Follow installation instructions.

### Setting Up Java JDK

1. Download the JDK installer from Oracle.
2. Run the installer and select your installation folder.
3. Set up JAVA_HOME and PATH environment variables:
   - Open System Properties.
   - Navigate to Environment Variables.
   - Add JAVA_HOME with the JDK installation path.
   - Update the PATH variable to include %JAVA_HOME%\bin.
4. Verify Java installation by running java --version in a terminal.

### Installing Apache Maven

1. Check if you have Java installed by running java --version.
2. Download Apache Maven from the [official website](https://maven.apache.org/download.cgi).
3. Extract the archive to your desired location.
4. Set up M2_HOME and MAVEN_HOME environment variables:
    - Create M2_HOME and point it to the Maven installation directory.
    - Update the PATH variable to include %M2_HOME%\bin.
5. Verify Maven installation by running mvn --version in a terminal.

### Mobile Automation
1. [Android Studio](https://developer.android.com/studio) - Emulator Management
2. [Appium Inspector](https://github.com/appium/appium-inspector/releases) - Mobile Inspect Element

### Appium Download & install.
- [Appium Inspector](https://github.com/appium/appium-inspector/releases)
- [ ]  Appium server CLI → Open CMD and write

   - ```npm install –g appium ```          // it will download and install the latest stable release [-g for global install so that you can use it from anywhere]
- [ ]  Install UiAutomator2
   - ```appium driver install uiautomator2```

- [ ] Appium server GUI (Deprecated)
   - [ ]  Download and install Appium server GUI (optional if already installed in CLI server)
     https://github.com/appium/appium-desktop/releases/tag/v1.22.3-4
- [ ] Test successful Appium setup → Open CMD and write any command from below
   - ``` appium -v  ``` // tells the version number you just install
   
   - ```where appium ```// tells the location where appium installed in your computer
   
   - ```appium   ```    // run appium server with default port 4723 

### Android Studio Download, install, set ANDROID_HOME and path in environment’s system variable.

- [ ]  Download and install Android Studio
   - [Android Studio](https://developer.android.com/studio)
- [ ]  Open Environment Variables and click on the new System variable → set
  Variable name: ANDROID_HOME
  Variable value: Your Android SDK Folder Location


- [ ]  Select Path system variables then click on Edit → click on the new and add this four path variables and \
   - **important make sure they remain in this order**
     ``` 
     %ANDROID_HOME%\emulator
     %ANDROID_HOME%\tools
     %ANDROID_HOME%\platform-tools
     %ANDROID_HOME%\tools\bin 
     ```

### Android Studio SDK Manager Setup

- [ ]  Open Android SDK manager from the Tool tab
- [ ]  Select SDK Platforms →
  Checked & installed “Android API 32” and at least one Android version

- [ ]  Select SDK Tools → Uncheck Hide Obsolete Packages ⇒ Checked & installed
   1. Android SDK Build-tools 32
   2. Android Emulator
   3. Android SDK Platform-Tools
   4. Android SDK Platform-Tools(Obsolete)
   5. Intel x86 Emulator Accelerator (HAXM installer)

- In case you failed to install HAXM
  - https://www.tektutorialshub.com/android-studio/haxm-installation-failed-install-intel-haxm-in-windows/
- [ ]  Select SDK Update site → make sure all listed items are Enabled

### Android Studio AVD(Android Virtual Devices) Manager Setup / Emulator

- [ ]  Open Android AVD Manager from the Tool tab
- [ ]  Click on click Create Virtual Device ⇒ <Choose a device definition / a model > ⇒ Next ⇒ <Select system Image/ android version> ⇒ Next → provide ADV/emulator name > Finish
- [ ]  Done! you just create Android Virtual Device
- [ ]  From the Actions column, you can perform Launch, Edit, Duplicate, Wipe data,  Cold boot now, Delete .etc on your selected AVD device.

### Physical Device setup

- [ ]  Go To Your phone Settings and Tap About Phone option
- [ ]  keep Tapping on Your device version option → Until the bottom popup shows
  “No Need, You are already a developer”
- [ ]  Now search within your settings by typing “Developer options” and Tap on it.
- [ ]  Now make sure the below three options are enabled
   1. USB debugging
   2. Install via USB
   3. USB debugging (Security Settings)


### Installation Steps
To start using the framework:

1. [Fork](https://github.com/imark0007/MobileAutomation_GS_APK.git) the repository.
2. Clone, i.e, download your copy of the repository to your local machine using
```
git clone https://github.com/imark0007/MobileAutomation_GS_APK.git
```
3. Import the project into your preferred IDE (Eclipse, IntelliJ IDEA, or Spring Tools).
4. Make any desired changes or additions to the project.

### RUN!

 <aside>
💡To perform the below command without any exception. Please recheck the order of your system path variables for Android. [which we did in the earlier Android Studio section]
”Open CMD from any location and run the below command →whenever you need them”

 </aside>

### **Android Debug Bridge(adb)** → udid | install |PackageName |appActivity

### T**o show connected/active adb devices with their Unique Device Identifier(udid)**

```bash
adb devices
```

### Install APK ⇒ Many ways! you can do that

 - Drag and Drop the apk file inside the emulator
 - Install using play store 
 - Download apk file using emulator browser than install 
 - transfer apk file to emulator storage location than install 
 - Install using cmd by the helping of adb(**Android Debug Bridge**)

```bash
# if only one adb device connected to your computer 
  adb install "path to .apk"
# if multiple device are connected 
  adb -s "device-udid" install "path to .apk"  #-s source/serialNumber/Identifier
# optional options are 
# adb install [options] path -!
#-r: Reinstall an existing app, keeping its data.
#-f: Install package on the internal system memory.
#-d: Allow version code downgrade.
#-g: Grant all permissions listed in the app manifest."
# https://developer.android.com/studio/command-line/adb
```

### packageName and appActivity for any installed App

- Get packageName and appActivityackage using adb shell

  Open app in your emulator or physical device and run this command in cmd

    ```bash
    # If only one adb device is connected to your computer 
    adb shell dumpsys window | find "mCurrentFocus"
    # If multiple device are connected 
    adb -s "device-udid" shell dumpsys window | find "mCurrentFocus"   
    #-s source/serialNumber/Identifier
    # If executing the command on linux terminal replace find with grep
    ```


- Get packageName and appActivity using Apk info app

  https://play.google.com/store/apps/details?id=com.wt.apkinfo&hl=en&gl=US


### Emulator → List | Launch | Shutdown | Cold boot | Wipe data

- To show List of available emulator names

    ```bash
    emulator -list-avds
    ```

- Launch/start/Open an Emulator → after start emulator it will keep alive until close this current CMD window.

    ```bash
    emulator -avd emulator_Name
    # OR
    emulator @emulator_Name
    ```

- Close/Shutdown an Emulator → Many ways are available

  → In CMD window simply click Ctrl + C and wait for few seconds →  it will close the emulator.

  → By clicking close button in emulator UI
  → Closing the CMD window

- Start Emulator in Cold Boot view

    ```bash
    emulator -avd emulator_Name -no-snapshot-load
    # OR
    emulator @emulator_Name -no-snapshot-load
    ```

- Wipe-data/RESET an Emulator

    ```bash
    emulator -avd emulator_Name -wipe-data
    # OR
    emulator @emulator_Name -wipe-data
    ```


### uiautomatorviewer - it's a simple UI inspector. work by taking screenshots

<aside>
💡  Connect a physical device or run emulator first then proceed

</aside>

- Run UI Automator

  Simply type uiautomatorviewer in CMD. it will run the UI Automator and keep running until closing the CMD window or→ in CMD window type Ctrl + C for closing the UI Automator.

    ```bash
    uiautomatorviewer
    ```

- (Optional) if exception present when trying to run UI Automator for the first time

    <aside>
    💡 if there is an exception like this 
    -Djava.ext.dirs=..\lib\x86_64;..\lib is not supported.  Use -classpath instead.
    Error: Could not create the Java Virtual Machine.
    Error: A fatal exception has occurred. Program will exit.

    </aside>

  steps 1: Download and install java 8 .. [just simple install no need to change anything]

     - [Java-8](https://drive.google.com/file/d/14_dSxe9CegypKgSfmkLq3n6KU98l-VzQ/view) - If needed

  steps 2: open uiautomatorviewer.bat with a text editor from the below location
  C:\Users\your_user_name\AppData\Local\Android\Sdk\tools\bin

  step 3: Find these lines of code inside the file

    ```bash
    rem Check we have a valid Java.exe in the path.
    set java_exe=
    call ..\lib\find_java.bat
    ```

  step 4: Replace with these lines of code and save the file

    ```bash
    rem Check we have a valid Java.exe in the path.
    set java_exe=C:\Program Files\Java\jdk1.8.0_321\jre\bin\java.exe
    rem call ..\lib\find_java.bat
    ```

  step 5: Done! now try to run uiautomatorviewer.bat hopefully it will works


### Appium Server

- Appium Server in the CLI

  simply type appium in CMD.  it will start the server and keep running until closing the CMD window or→ in CMD window type Ctrl + C for closing the server.

    ```bash
    appium   // it will run the appium server with the default port: 4723 
    ```

   - If you want to run appium server in a different port

       ```bash
       appium -p 4126  // here 4726 is your costume port
       ```



    <aside>
    💡 If you need any help related to write appium --help
    
    </aside>

- Appium Server in the GUI

  Open Appium server GUI application and click on start button ⇒ run server

  For closing the server simply click on close button


### Appium inspector - it's an advanced UI inspector for mobile OS

<aside>
💡 Run Appium server and connect a physical device or run emulator first then proceed

</aside>

- Run Appium Inspector

  Run Appium Inspector by clicking on and setting Remote Path →   /wd/hub

  ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0868e573-fa0a-4701-b392-d113241d59b7/Untitled.png)

- Desired Capabilities
   - To start a session → with an only connected or running adb device and specific automation engine
     if multiple devices are connected then it will start with priority one.

       ```bash
       {
         "platformName": "android",
           "automationName": "UiAutomator2",
           "deviceName": "local"
       }
       ```

   - To start a session with a specific physical or emulator device and specific automation engine

       ```bash
       {
         "platformName": "android",
           "automationName": "UiAutomator2",
           "deviceName": "local",
           "udid" : " adb device or emolator udid" //open CMD then type  adb devices it will show
       }
       ```

   - To start a session with a specific physical or emulator device, open specific app(already installed in your device) and specific automation engine

       ```bash
       {
         "appium:deviceName": "Xiaomi MI 8",
         "platformName": "android",
           "automationName": "UiAutomator2",
           "deviceName": "local",
         "appPackage": "Your app package name", //for General Store apk : com.androidsample.generalstore
         "appActivity": "Your app Activity name"//for General Store apk : com.androidsample.generalstore.SplashActivity
       }
       ```

   - To start a session with a specific device, install app and specific automation engine

       ```bash
       {
         "appium:deviceName": "Xiaomi MI 8",
         "platformName": "android",
           "automationName": "UiAutomator2",
           "deviceName": "local",
           "app": "Your app's APK file location" //example: File f = new File("src/test/resources");
       }
       ```

   - For more Appium Desired Capabilities

     https://appium.io/docs/en/2.0/guides/caps/

##### Maven Dependencies

```xml
  <dependencies>
    <!-- https://mvnrepository.com/artifact/io.appium/java-client -->
    <dependency>
        <groupId>io.appium</groupId>
        <artifactId>java-client</artifactId>
        <version>9.2.2</version>
    </dependency>
    <!-- https://mvnrepository.com/artifact/org.testng/testng -->
    <dependency>
        <groupId>org.testng</groupId>
        <artifactId>testng</artifactId>
        <version>7.8.0</version>
        <scope>test</scope>
    </dependency>
    <!-- https://mvnrepository.com/artifact/org.seleniumhq.selenium/selenium-java -->
    <dependency>
        <groupId>org.seleniumhq.selenium</groupId>
        <artifactId>selenium-java</artifactId>
        <version>4.19.0</version>
    </dependency>

    <!-- https://mvnrepository.com/artifact/commons-io/commons-io -->
    <dependency>
        <groupId>commons-io</groupId>
        <artifactId>commons-io</artifactId>
        <version>2.13.0</version>
    </dependency>
    <!-- https://mvnrepository.com/artifact/org.apache.commons/commons-lang3 -->
    <dependency>
        <groupId>org.apache.commons</groupId>
        <artifactId>commons-lang3</artifactId>
        <version>3.13.0</version>
    </dependency>
    <!-- https://mvnrepository.com/artifact/commons-validator/commons-validator -->
    <dependency>
        <groupId>commons-validator</groupId>
        <artifactId>commons-validator</artifactId>
        <version>1.7</version>
    </dependency>
</dependencies>
```

## I personally used IntelliJ IDEA 2023.3.6 and Physical Device i.e. Xiaomi MI 8

### Contributing

Contributions to this project are welcome! If you have suggestions for improvements, new features, or bug fixes, please feel free to open an issue or submit a pull request.

