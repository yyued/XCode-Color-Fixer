# XCode-Color-Fixer
StoryBoard / XIB 颜色偏差很严重，怎么破？XCode-Color-Fixer帮你忙！

当使用 StoryBoard 和 XIB 中的拾色器进行RGB设值的时候，XCode会选择sRGB色域，但是，美术给予我们的色值都是标准RGB（generic RGB）。
于是，我们有了这个小工具。
你可以在Build App之前，在工程目录下执行一个命令，即可完成sRGB到generic RGB的色域转换。

我们来看看，Storyboard和XIB与真实颜色到底相差多少，以下ViewController背景色是IB设置的，小View的背景色是代码设置的。
![compare](https://raw.githubusercontent.com/duowan/XCode-Color-Fixer/master/sample/compare.png)

只要我们运行这个小工具，就能得到真实的色值。
![command](https://raw.githubusercontent.com/duowan/XCode-Color-Fixer/master/sample/command.png)

## 安装方法 

1. 将bin/rgb复制到/usr/local/bin/目录下 (cp ./bin/rgb /usr/local/bin/rgb)
2. 设置权限 (sudo chmod 777 /usr/local/bin/rgb)
3. 使用时，cd 到工程目录，再执行 rgb 即可
