# mxnet_windows
>在某个群答应一位朋友写一下windows下mxnet编译过程，拖了挺久。趁现在有时间写一下，比较简略，限于水平有限，如果有疏漏的地方，敬请指出，共同学习进步。

准备工作：
>1. 完整的mxnet源码，请自行去[github](https://github.com/dmlc/mxnet)下载
2. VS2013以及对应的python插件ptvs ，python，opencv（3.0+），cuda， cmake工具（3.5）等
3. 部分依赖，你可以去[happynear的github](https://github.com/happynear/caffe-windows)下载3rdparty (感谢happynear,caffe_windows目前还在用:))

#使用cmake构建vs工程
打开cmake-gui,界面大致如下：

![cmake-gui界面](http://upload-images.jianshu.io/upload_images/433010-80e3fceb4e258bd5.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

界面中的source code选择你的mxnet根目录，然后选择生成的文件目录（可以在根目录下建立windows文件夹）,下图为示例：

![cmake示例](http://upload-images.jianshu.io/upload_images/433010-410e401daeb55062.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

点击configure,选择

![cmake](http://upload-images.jianshu.io/upload_images/433010-5561cc982d91a2fd.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

可能会有一些error，如某些库找不到等，把3rdparty放在windows目录下，然后根据报错信息，修改对应路径：

![配置](http://upload-images.jianshu.io/upload_images/433010-7f16ee3971828d8a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![配置](http://upload-images.jianshu.io/upload_images/433010-cc0e2271be0d1a38.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![cmake成功](http://upload-images.jianshu.io/upload_images/433010-3b53ba43a2d96f54.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
点击generate，可以去windows目录下查看，mxnet的vs工程已经生成了。
![windows目录](http://upload-images.jianshu.io/upload_images/433010-6ceac3ebbe243b87.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
使用vs打开.sln工程文件，编译即可。

![mxnet build](http://upload-images.jianshu.io/upload_images/433010-e375047f076fcc94.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
