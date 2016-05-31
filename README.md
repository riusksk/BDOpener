# BDOpener——开启APK调试与备份选项的Xposed模块

通常在用IDA调试android dex时，如果程序的debugable选项未开启，则无法进行smali调试，以往通常有两种做法
 
1、修改程序的AndroidManifest.xml中的debugable="true"，然后签名重打包；<br>
2、修改系统属性，将defalut.prop中ro.debugable设置为1，然后刷机进去；
 
这两种方法操作起来相对会麻烦一些，因此基于Xposed模块写了个工具，用于修改程序的debugable选项，同时也支持开启备份选项，方便数据转移。

日志输出效果：<br>
![输出日志](http://security.tencent.com/uploadimg_dir/201507/f198bf0edd38845b1ada155c67aca982.png)
 
开启前：<br>
![开启前](http://security.tencent.com/uploadimg_dir/201507/e21f0072e4b6bf03de930c2c45fc680d.png)
 
开启后：<br>
![开启后](http://security.tencent.com/uploadimg_dir/201507/af438977ad6536bff6537195aaabbe36.png)
