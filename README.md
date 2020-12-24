### Demo运行说明

Demo地址： **[LPR](https://github.com/AleynP/LPR)**

打开项目肯定会报编译错误，要做以下修改：
1. 用AS打开项目
2. 设置项目NDK为 NDK-r14b
3. 先修改 CMakeLists.txt 文件， 把第19行修改成你本地的 OpenCV SDK 的对应路径。
4. 跟据自己的开发平台，设置 ocr 下的build.gradle  第 18 行代码 是否要注释。
完成以上步骤后再运行项目，就没有问题了。

## 更新 （2020-12-24）

之前项目使用opencv 3 和ndk r14b在我的AS编译一直出错，可能需要低版本的AS吧，索性升级成最新 **[opencv 4.5.1](https://sourceforge.net/projects/opencvlibrary/files/4.5.1/opencv-4.5.1-android-sdk.zip/download)**
升级比较简单，就是一些常量枚举改了名字，简单替换了一下，编译后目前真机测试没啥问题，ndk用的是AS自动推荐下载的版本20.0.5594570

编译环境
1. OS：Windows 10 x64
2. AS: Android Studio 3.6.3
3. OpenCV: 4.5.1
4. NDK: 20.0.5594570

## 更新（2020-6-2）：

1. 更改了取景框适配问题
2. 更改成AndroidX，使用了Google 的 CamreaX 来做相机预览
3. 分离出ocr Module ，为了方便其他项目导入识别功能
