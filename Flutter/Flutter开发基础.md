## 如何在mac上安装flutter

1. 去flutter官网下载其最新可用的安装包
2. 解压安装包到你想安装的目录
3. vim ~/.bash_profile,在该文件内配置如下参数

| export PUB_HOSTED_URL=https://pub.flutter-io.cn //国内用户需要设置 |
| ------------------------------------------------------------ |
| export FLUTTER_STORAGE_BASE_URL=https://storage.flutter-io.cn //国内用户需要设置 |
| export PATH=**PATH_TO_FLUTTER_GIT_DIRECTORY**/flutter/bin:$PATH |

PATH_TO_FLUTTER_GIT_DIRECTORY 这个换成你安装flutter的路径

4. 执行source ~/.bash_profile(==这时候终端不能关闭，如果关闭当前终端执行flutter doctor会出现找不到flutter的提示，这时候需要重新执行source ~/.bash_profile==)

5. 如果想flutter命令永久有效，这需要这么做：

   ```js
   1、open ~/.zshrc 
   如果提示文件不存在，则执行
   2、vim ~/.zshrc 
   3、将~/.bash_profile里的文件内容复制到~/.zshrc 
   4、执行source ~/.zshrc
   ```

   

6. 执行flutter doctor

7. 创建应用，可以用终端创建 如：==flutter create myapp==

8. 如果需要在xcode运行flutter项目，需要做以下几步操作
   * 首先进入该项目，如cd myapp
   * sudo chmod -R 777 *（777表示可读可写可执行， *表示所有文件）
   * 如果执行上述两部操作有问题，可以再进入flutter的sdk目录下，执行sudo chmod -R 777 *



## flutter调试模式切换

* r键:点击后热加载，也就算重新加载
* p键：显示网格，这个可以很好的掌握布局情况
* o键：切换android和iOS的预览模式
* q键：退出调试预览模式



