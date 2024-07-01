# HelloWorldB4A
Very simple B4A repository that is an example of a B4A app that can be used as reference or extended.  It includes a .gitignore file that shows which files and directories can be ignored by git and left out of the repository.

## B4X / B4A
B4A (BASIC for Android) is the android target for the B4X project (See http://www.b4x.com).  B4A includes an IDE in which to write basic code and design associated user interfaces.  It also includes facilities to debug on android emulators as well as real android hardware.

## Software Development Tools Used
For this project the following dependencies were used.  Future version of these software packages will likely work but actual versions used provided.
- B4A from: https://www.b4x.com/b4a.html
  - (I used version 12.80 64 bit edition)
  - B4A installation instructions will have you get download and install:
    - JDK from oracle.com or from OpenJDK
      - (I used oracle version jdk-8u411-windows-x64 from [oracle.com](https://www.oracle.com/java/technologies/downloads/?er=221886#java8-windows) ) 
    - Android SDK Commandline tools
      - (I used https://dl.google.com/android/repository/commandlinetools-win-9123335_latest.zip)
    - Android Required resources from B4A
      - (I used: https://www.b4x.com/android/files/resources_11_22.zip)

- BlueStacks App Player from: https://www.bluestacks.com/download.html
  - (I used version  5.21.215.1042 P64)

## Software Development Tool Setup and First Run on Emulation Device
Follow the following instructions to setup a build environment using an emulator.
1. Install B4A via the instructions here: https://www.b4x.com/b4a.html including JDK and other required software
2. Install BlueStacks Android Emulator
3. Clone this repository to your local machien with the git clone command
4. In Windows Explorer navigate to HelloWorldB4A\B4A in the cloned repository and double click on HelloWorldB4A.b4a to open the project
5. In B4A select from the B4A menu Tools->Configure Paths
6. In Configure paths window set java.exe path, for me it was C:\Program Files\Java\jdk-1.8\bin\javac.exe
7. In Configure paths window set the Android.jar path, for me it was: C:\android\platforms\android-33\android.jar
8. Save the paths just set and close the window.

9. 10. Start the BlueStacks App Player Emulator
10. In the emulator click the Gear icon along the right hand side of the emulator window to open the settings screen
11. In the settings screen in the emulator click on Advanced for the Advanced settings
12. In the Advanced Settings click the toggle to enable Android Debug Bridge (ADB) and take note of the IP address and port number shown ![image](https://github.com/nealvis/HelloWorldB4A/assets/21041294/9fd97a33-d911-4989-8241-47da686cedf6)

13. Open a command shell window in administrator mode
14. In the command shell change directory to the platform-tools directory that you previously unzipped. For me it was here: C:\android\platform-tools>
15. In the command shell connect adb to the emulator with the adb command `adb connect 127.0.0.1:5555`  If the IP address/Port number shown in the emulator was different, then use what was shown.
16. Back in the B4A IDE click the connect button in the Logs window.  (If you don't see the Logs window then open it from the Windows->Logs menu item.)

Now you should be ready to build and run the application in the emulator by selecting Project->Compile and Run from the menu in the B4A IDE.  The app should build and automatically get installed in the emulator and then automatically run in the emulator looking like this:
![image](https://github.com/nealvis/HelloWorldB4A/assets/21041294/c6149a75-81a9-4147-b5c5-cafe1e0dce12)

## Running the App After First Setup
After closing down B4A and the Emulator, to run the app in future session follow these steps:
- Open the project by navigating to HelloWorldB4A\B4A in the cloned repository and double click on HelloWorldB4A.b4a.
- Start BlueStacks App Player android emulator from the windows menu.
- From Administrator Command shell run `adb connect 127.0.0.1:5555` (use appropriate IP addr and port nubmer)
- In B4A click the Connect button in the Logger Window

At this point you should be able to compile and run as many times as needed until disconnected from the emulator.  Do this via: 
- In B4A select Project->Compile and Run from the menu.  It should install and run on emulator.

 








