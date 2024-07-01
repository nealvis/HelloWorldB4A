# HelloWorldB4A
Very simple B4A repository that is an example of a B4A app that can be used as reference or extended.  It includes a .gitignore file that shows which files and directories can be ignored by git and left out of the repository.

## B4X / B4A
B4A (BASIC for Android) is the android target for the B4X project (See http://www.b4x.com).  B4A includes an IDE in which to write basic code and design associated user interfaces.  It also includes facilities to debug on android emulators as well as real android hardware.

## Software Development Tools Used
For this project the following dependencies were used.  Future version of these software packages will likely work but actual versions used provided.
- B4A from: https://www.b4x.com/b4a.html
  - (Using version 12.80 64 bit edition)
  - B4A installation instructions will have you get download and install:
    - JDK from oracle.com or from OpenJDK
      - (Using oracle version jdk-8u411-windows-x64 from [oracle.com](https://www.oracle.com/java/technologies/downloads/?er=221886#java8-windows) ) 
    - Android SDK Commandline tools
      - (Using https://dl.google.com/android/repository/commandlinetools-win-9123335_latest.zip)
    - Android Required resources from B4A
      - (Using https://www.b4x.com/android/files/resources_11_22.zip)

Emulators (optional)
- BlueStacks App Player from: https://www.bluestacks.com/download.html
  - (Using version  5.21.215.1042 P64)

- LD Player from: [http://de.ldplayer.net](https://de.ldplayer.net/)
  - (Using version 9.0.71)

## Software Development Tool Setup and First Run
Follow these instructions to setup a build environment using an emulator or a physical android device.
1. Install B4A via the instructions here: https://www.b4x.com/b4a.html including JDK and other required software
2. Clone this repository to your local machien with the git clone command
3. In Windows Explorer navigate to HelloWorldB4A\B4A in the cloned repository and double click on HelloWorldB4A.b4a to open the project
4. In B4A select from the B4A menu Tools->Configure Paths
5. In Configure paths window set java.exe path, for me it was C:\Program Files\Java\jdk-1.8\bin\javac.exe
6. In Configure paths window set the Android.jar path, for me it was: C:\android\platforms\android-33\android.jar
7. Save the paths just set and close the window.
   
8. Setup one of BlueStacks App Player, LD App Player, Phsyical Android Device)
  - **For BlueStacks App Player Emulator**
    - Download and Install BlueStacks Android Emulator from https://www.bluestacks.com/download.html
    - Start the emulator from windows start menu or otherwise.
    - In the emulator click the Gear icon along the right hand side of the emulator window to open the settings screen
    - In the settings screen in the emulator click on Advanced for the Advanced settings
    - In the Advanced Settings click the toggle to enable Android Debug Bridge (ADB) and take note of the IP address and port number shown ![image](https://github.com/nealvis/HelloWorldB4A/assets/21041294/9fd97a33-d911-4989-8241-47da686cedf6)
    - On Development machine open a command shell window in administrator mode
    - In the command shell change directory to the platform-tools directory that you previously unzipped. For me it was here: C:\android\platform-tools>
    - In the command shell connect adb to the emulator with the adb command `adb connect 127.0.0.1:5555`  If the IP address/Port number shown in the emulator was different, then use what was shown.
    - Back in the B4A IDE click the connect button in the Logs window.  (If you don't see the Logs window then open it from the Windows->Logs menu item.)
      
  - **LD Player Emulator**
    - Download and install LD Player Android Emulator from: [http://de.ldplayer.net](https://de.ldplayer.net/)
    - Start the emulator from windows start menu or otherwise.
    - Open Settings screen by clicking the Gear(right side of UI).
    - Click the "Other Settings" tab.
    - Select English from the Language dropdown and click the Save Settings button.
    - Restart the emulator if needed to see the English UI.
    - Click Gear->Other Settings again.
    - Click radio button to Enable Root Permissions.
    - Select Open Remote Connection from the ADB debugging drop down.
    - Click Save Settings button and restart the emulator.
    - From Administrator Command shell run in the platform-tools directory that was unzipped earlier run `adb devices` you should see **emulator-5554** as a device
    - In the B4A IDE click the Connect button in the Logs window.  You should see "Logger connected to emulator-5554"
      
  - **Physical Android Device**
    - Install the B4A Bridge app from the Google Play store on the device.
    - Run the B4A Bridge app on the device
    - In B4A Bridge app make sure enable FTP service is checked
    - In B4A Bridge app click the start button
    - Make note of the device IP address shown in the app
    - in B4A IDE menu select Tools->B4A Brdige->Connect->New IP  Enter the device's IP address noted above.
        
Now you should be ready to build and run the application in the emulator or the physical device by selecting Project->Compile and Run from the menu in the B4A IDE.  The app should build and automatically get installed in the emulator or device and then automatically run in the emulator or device

## Running the App in BlueStack Emulator After First Setup
After closing down the B4A IDE and the Emulator, to run the app in future session follow these steps:
- Open the project by navigating to HellowWorldB4A\B4A in the cloned repository and double click on HelloWorld.b4a file.
- Start BlueStacks App Player android emulator from the windows menu.
- From Administrator Command shell run `adb connect 127.0.0.1:5555` (use appropriate IP addr and port nubmer)
- In the B4A IDE click the Connect button in the Logger Window

At this point you should be able to compile and run as many times as needed until disconnected from the emulator.  Do this via: 
- In B4A select Project->Compile and Run from the menu.  It should install and run on emulator.


## Turning on Developer Options on a Physical Android Device
If running on a physical device without the B4A Bridge app you will need to turn on developer options by following these steps
- Open Settings
- Tap About phone or About device
- Tap Software information
- Tap Build number seven times
- Tap Settings -> Developer options
- Make sure the following settings are toggled on
  - Developer Options
  - USB Debugging  




