
Android Camera2BasicStream
===================================

This little demo is based on the Camera2Basics example. I really needed to pipe out every frame the 
camera provides to a specific endpoint e.g for streaming. The camera2 api is quite new and right now
its a little bit more complicated grab a frame and convert it to a bitmap for your processing needs.

The app will work on the nexus4 and the moto x. Why that ?

The imageformat YUV420SP is not used anymore now you have to deal with yuv_420_888. The problem is YUV_420_888 is still not implemented correctly that means you simply cant use it. It will be fixed in Android (5.1.1). The fallback is jpeg(HAL_PIXEL_FORMAT_RGBA_888) not every camera/mobile delievers that format so the implementation is kinda weak for now and not really fast but it works ! :) 


Pre-requisites
--------------

- Android SDK v23
- Android Build Tools v23.0.1
- Android Support Repository

Getting Started
---------------

This sample uses the Gradle build system. To build this project, use the
"gradlew build" command or use "Import Project" in Android Studio.
