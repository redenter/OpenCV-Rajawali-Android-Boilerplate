#OpenCV Android Rajawali Boilerplate

This is a boilerplate for android apps which need OpenCV and Rajawali. [OpenCV](https://en.wikipedia.org/wiki/OpenCV) is a well known library for computer vision and [Rajawali](https://github.com/Rajawali/Rajawali) is a 3D engine for android based on OpenGL. Since this project contains all the required libraries, no downloads are required.

To use this boilerplate:
1. Clone this repository
2. Import project into Android studio.
3. Run project to verify. That's it.

The following steps were followed to setup OpenCV and Rajawali.  

###Steps followed to setup OpenCV:
Source: http://stackoverflow.com/questions/27406303/opencv-in-android-studio/27421494#27421494

1. Download latest OpenCV sdk for Android from OpenCV.org and decompress the zip file.
2. Import OpenCV to Android Studio, From File -> New -> Import Module, choose sdk/java folder in the unzipped opencv archive.
3.Update build.gradle under imported OpenCV module to update 4 fields to match your project build.gradle a) compileSdkVersion b) buildToolsVersion c) minSdkVersion and 4) targetSdkVersion.
4.Add module dependency by Application -> Module Settings, and select the Dependencies tab. Click + icon at bottom, choose Module Dependency and select the imported OpenCV module.
For Android Studio v1.2.2, to access to Module Settings : in the project view, right-click the dependent module -> Open Module Settings
5. Copy libs folder under sdk/native to Android Studio under app/src/main.
6. In Android Studio, rename the copied libs directory to jniLibs.

###Steps followed to setup Rajawali:
Source: http://stackoverflow.com/questions/27406303/opencv-in-android-studio/27421494#27421494

1.Add maven { url "https://oss.sonatype.org/content/repositories/snapshots/" } to repositories in build.grade of the project.
2. Add the line to app's build.grade.
	compile 'org.rajawali3d:rajawali:1.0.186-SNAPSHOT@aar' 

