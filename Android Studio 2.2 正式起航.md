# Blog
# Android从小工到专家
## Android Studio 2.2 正式起航

对 UI 布局的改进可以看出，Google 的想法是想让布局更智能更可视化，对于一些刚接触 Android 的同学无意大大降低了门槛，只不过对于一些老一辈的程序员，比如我，还是习惯直接写代码调 UI 来的直接。

评：这个布局很强大，但是宝宝不喜欢拖来拖去，感觉设计师可以开始学 Android 了。

3
Samples Browser


不知道大家知不知道 GitHub 上 Google 有个叫 Google Samples 的组织，地址在这里：

https://github.com/googlesamples

这里罗列了 Google 的上百个关于一些代码的示例，而这其中大部分都是 Android 相关的，比如 NavigationDrawer 不会用了，google 有个 android-NavigationDrawer 的示例。而这次 Google 直接把他关联到 Android Stduio 了，你可以在 Android Studio 选中一个类直接右键点击 Find Sample Code ，神奇的事情发生了：



上图可以看到，以选中 PackageManager 为例，下面直接出现了一些 Google Sample 相关的代码，方便你快速查找该类的用法，而且还有个链接直接指向到 Android Developer 官网该类的详细介绍，简直不要太方便，我喜欢这功能！

评：这功能很实用。

4
Instant Run Improvements


Instant Run 的推出确实很不错，但是妈蛋第一次编译也太慢了吧，就是因为编译太慢我一般都是把该功能禁用的。我们先来看下 Google 官方的更新说明：

In this release, we have made many stability and reliability improvements to Instant Run. If you have previously disabled Instant Run, we encourage you to re-enable it and let us know if you come across further issues. 


卧槽，看完我笑死了，原来 Google 早知道我们会把 Instant Run 功能禁用啊，按照 Google 的说法这次更新做了改进，更稳定，更快了。鼓励我们把 Instant Run 功能打开，好吧，我尝试了一把，确实速度上比之前快不少，大家可以重新打开体验了。打开方法见下图：



评：这次我终于把 Instant Run 功能打开了。

5
Build cache (Experimental)




其实刚升级 AS 就强烈提示我升级 Gradle 到 2.14 版本，只需要把 Android Gradle plugin 的版本升级到 2.2.0 就好了。

    classpath 'com.android.tools.build:gradle:2.2.0'

为了加快 Gradle 的编译速度，Google 新增了一个编译缓存的功能，不过目前还是实验性的，具体用法就是在你的 gradle.properties 文件里加上这么一行代码：

    android.enableBuildCache=true

总体来说升级了 Gradle，加上这么一句代码，确实感觉编译快了些，大家可以自行感受下。

对了，每次编译生成的缓存在 ~/users/.android/build-cache 目录下，如果缓存过多可以手动删除该目录进行清除。

评：编译确实快了，不知道是不是错觉。

6
APK Analyzer


Google 推出了一个 APK
分析器，现在可以很方便的使用 Android Studio 进行 APK 分析。具体用法点击 Build ->  Analyze APK 然后选择你要分析的 APK 文件就可以了。

可以方便的查看全部文件和大小



可以直接查看 AndroidManifest.xml 文件



可以直接查看资源文件

查看图片



查看 xml 资源文件



可以直接查看 dex 文件



还可以对两个 apk 进行比较



评：这个功能堪称神器啊，以后人人都会逆向 APK 了。

7
Virtual Sensors in the Android Emulator


Google 这次同样改进了模拟器，这次让模拟器支持虚拟传感器：



评：对于我这种从不用模拟器的人没啥用。

8
Espresso Test Recorder (Beta)


Google 为测试新增了一个功能，就是我们可以对操作进行录像，然后根据我们的操作生成一些测试脚本，而且配合 Firebase 将更方便。



评：理论上来说此功能很不错，可以解放了测试人员的双手，只不过该功能还是测试，应该很不稳定，而且国内行情结合 Firebase 很困难，对开发意义不大，可以持续关注下。

9
总结


除以上之外，此次更新还包括对 Java 8 的支持，Jack 编译器的改进，可以调试 GPU，改进了对 C++ 的支持等，总体来说此次更新推出了不少提升 Android 开发效率的工具，性能上也做了优化，值得大家更新！

官方更新说明：
http://android-developers.blogspot.tw/2016/09/android-studio-2-2.html

PS：原创不易，觉得我的分享不错，赞赏、点击留言区上方的广告、转发、点赞都是对我的支持与鼓励！
