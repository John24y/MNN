
## 跑通命令行工具
首先编译(如果已编译可以跳过)`MNNConvert`，操作如下：
```
cd MNN
mkdir build && cd build
cmake -DMNN_BUILD_CONVERTER=ON -DMNN_USE_RELATIVE_SO_PATH=ON ..
make -j8
cp ./express/libMNN_Express.so libMNN_Express.so
cp ./tools/converter/libMNNConvertDeps.so libMNNConvertDeps.so
```


## 跑通安卓
https://www.yuque.com/mnn/cn/build_android

1 需要linux环境，WINDOWS下cmake生成出来是sln，不是makefile
2 linux环境下安装android studio，用xlunch投影到WINDOWS。 studio打开路径/project/android/demo
3 gradle / android-gradle-plugin / android-build-tools 版本升级下，各种库gradle配置方式用新的DSL，老版本在android studio已经跑不通了
4 ndk版本不要动，这个和cmakelist语法有关，改了27编译不了。版本 21.4.7075529

命令行编译
apt-get install -y openjdk-17-jdk
./gradlew :app:assembleDebug