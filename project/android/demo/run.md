
## 跑通
1 需要linux环境，WINDOWS下cmake生成出来是sln，不是makefile
2 linux环境下安装android studio，用xlunch投影到WINDOWS。 studio打开路径/project/android/demo
3 gradle / android-gradle-plugin / android-build-tools 版本升级下，各种库gradle配置方式用新的DSL，老版本在android studio已经跑不通了
4 ndk版本不要动，这个和cmakelist语法有关，改了27编译不了。版本 21.4.7075529

