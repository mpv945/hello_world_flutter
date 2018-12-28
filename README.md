# hello_world_flutter 第一个flutter项目（md文件换行只需每行前面打两个空格）

## 获取Flutter SDK[中文教程](https://flutterchina.club/get-started/install/);[官网](https://flutter.io/docs/get-started/install)   [教程课本](https://book.flutterchina.club/)
  1.获取Flutter SDK:https://storage.flutter-io.cn/flutter_infra/releases/stable/windows/flutter_windows_v1.0.0-stable.zip;每次更新最新版本  
  2.解压缩zip文件D:\soft\flutter位置，然后配置系统环境变量Path，添加一条D:\soft\flutter\bin；在用户环境变量中添加两个变量：export PUB_HOSTED_URL=https://pub.flutter-io.cn 和 export FLUTTER_STORAGE_BASE_URL=https://storage.flutter-io.cn（谷歌原域名=googleapis.com；flutter-io.cn为中国区准备的；或者用上海交大的站点FLUTTER_STORAGE_BASE_URL: https://mirrors.sjtug.sjtu.edu.cn/和PUB_HOSTED_URL: https://dart-pub.mirrors.sjtug.sjtu.edu.cn/  
  3.在cmd或者双击flutter_console.bat进入命令行flutter来初始化。该命令需要联网，上面两个url环境变量会关联上  
  4.运行完，执行flutter doctor；查看是否需要安装任何依赖项来完成安装。一般提示没安装本地的Android SDK和开发工具  
  5.安装SDK，进入https://developer.android.com/studio/?hl=zh-cn#downloads，进入下载选项，下载仅限命令行工具的包；注意要把ss的PAC，编辑本地pac，把developer.android.com加入进去。解压（我是把解压包放在新建的D:\soft\android目录下），cd到该tools目录下bin，执行.\sdkmanager.bat  --list(cmd不要.\)列出已安装和可用的包；然后安装对应的版本包.\sdkmanager.bat  "platform-tools" "platforms;android-28"；安装编译工具：.\sdkmanager.bat  "build-tools;28.0.3" ；uninstall/update为卸载/更新，[具体参考](https://developer.android.com/studio/command-line/sdkmanager?hl=zh-cn)  
  6.配置Android SDK；新增系统变量ANDROID_HOME，值为D:\soft\android；然后Path添加两条值%ANDROID_HOME%\platform-tools和%ANDROID_HOME%\tools ；执行adb，如果配置成功会输出信息  
  7.重新验证flutter doctor会提示安卓sdk已经安装ok，只是授权协议还没同意，执行flutter doctor --android-licenses，一直y，回车  
  8.安装编辑器的插件，由于使用vscode。打开ctrl+shift+x 输入flutter，在搜索结果列表中选择 ‘Flutter’, 然后点击 Install，选择 ‘OK’ 重新启动 VS Code。打开ctrl+shift+p，输入doctor, 然后选择 ‘Flutter: Run Flutter Doctor’ 查看“OUTPUT”窗口中的输出是否有问题，没问题说明成功  
  9.创建新的应用，打开ctrl+shift+p，输入flutter，然后选择 ‘Flutter: New Project’，输入 Project 名称 (如hello_world_flutter), 然后按回车键，指定放置项目的位置，选择文件夹，等待项目创建继续，并显示main.dart文件  
  10.执行adb devices，查看是否有安卓设备连接，没有就打开手机开发者模式，启动usb调试，然后连接电脑，手机会提示是否同意，点击同意，再次执行adb devices。有输出表示成功，然后在vscode右下方有Devices选择。点击F5执行调试，提示选择运行的环境，选择Dart & Flutter。最后就等待初始化，启动......,最后会在手机安装app，并启动  
  11.git关联，如果需要git管理，请在远程创建好项目，然后git clone https//github.com/youname/gittest.git(远程资源地址)把新创建的项目_back,然后把.gitgnore 复制到git克隆的目录下。把忽略文件提交，然后在复制其他的上传  

A new Flutter project.

## Getting Started
c
This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://flutter.io/docs/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://flutter.io/docs/cookbook)

For help getting started with Flutter, view our 
[online documentation](https://flutter.io/docs), which offers tutorials, 
samples, guidance on mobile development, and a full API reference.
