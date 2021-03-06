**NativeSubprocess** is a linux native process for android bridge。

**Usage**

it creates a child process by NDK calling linux fork function. callback your android java code run in the child process inside. Such as [Watchdog](https://github.com/droidwolf/NativeSubprocess/blob/master/src/com/droidwolf/example/WatchDog.java "WatchDog") (sample [ProcessWatcher](https://github.com/droidwolf/NativeSubprocess/blob/master/src/com/droidwolf/example/ProcessWatcher.java "ProcessWatcher")) to monitor your android app service, call up the customer satisfaction survey feedback page (sample [UninstallWatcher](https://github.com/droidwolf/NativeSubprocess/blob/master/src/com/droidwolf/example/UninstallWatcher.java "UninstallWatcher")) when uninstalling your applications.

**How to use**

1. copy com.droidwolf.nativesubprocess package to your project;
2. copy libsubprocess.so library to your  libs/armeabi project directory.
3. implements Subprocess class and  override runOnSubprocess function.
4. Finally, create your child process call by Subprocess.create function.

**Authors**

droidwolf [droidwolf2010@gmail.com](mailto:droidwolf2010@gmail.com "droidwolf2010@gmail.com")


**License**

[Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0 "Apache License, Version 2.0")