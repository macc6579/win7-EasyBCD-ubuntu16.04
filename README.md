# win7-EasyBCD-ubuntu16.04
小白自学教程，面向Linux初学者

PS:安装linux双系统也可以通过U盘启动，但在写盘的时候会格式化，这一点我个人来讲是不太喜欢的，所以还是用引导的方式，节约资源~

## 场景
使用EasyBCD 2.3引导，在Windows7下安装Ubuntu16.04。[未完待续，后期补图。]

## 准备工作
1. 软件：Ubuntu系统镜像；EasyBCD引导工具；EaseUS分区工具。
2. 在安装双系统之前，要为新系统分配一定的磁盘空间。

## 步骤
*注：在进行所有操作之前，如果电脑中有重要的数据请做好备份！一定！！*
1. 首先通过win+R进入Windows系统自带的分区显示窗口查看系统内存分配的情况。
建议从逻辑分区进行分割，如果系统安装失败，不会影响主分区的系统文件，从而避免原有的Windows系统也需要重装。

1.1 进入系统资源对话框如下图所示：

在win下查看了系统分配情况之后，我们使用分区工具对逻辑分区进行划分，为ubuntu系统先留出来足够的安装空间。
系统内存足够的情况下为Ubuntu留30G以上的空间，当然如果对Ubuntu需求不是很大的话可以根据自己的情况去分配，个人建议不低于10G。
*分区工具：EaseUS*
当然我也是只菜鸡……花了两天时间才完全搞定，期间在网上找了大量的安装教程作为参考，在此非常感谢百度，csdn和Linux社区提供的资料。

不扯远……鉴于是第一次安装，对ubuntu系统进行分区的情况与Windows系统还是有一定区别的。

2. 准备Linux镜像， 通过EasyBCD写入U盘（详见写入教程，可参考Google）
将下载好的ubuntu系统镜像放到c盘根目录下，然后将镜像文件解压，从…文件夹中copy这两个文件粘贴到c盘根目录下。
其中一个文件记得修改一下后缀，（不然引导系统无法识别导致报错，安装失败）

之后启动EasyBCD软件，添加一个系统引导项，具体过程如下图所示，

3. 进入win的BIOS页面，设置默认读取U盘；重启，进入Linux引导系统

4. 根据引导提示，对Linux操作系统进行资源分配
成功进入ubuntu引导界面之后，激动人心的时刻到了！对ubuntu的挂载点进行设置……
推荐选择默认的分区方案，引导系统会在空闲区域自动完成挂载点的划分。
ubuntu16.04版本中带有自动分区的选项，这为我们小白级别的新手提供了极大的便利。
当初我就是在这一步卡了蛮久，竟然还出现没有进行4k对齐的情况，后来是查资料balabala……
【哭…不合理的分区策略会对应着这种问题，或许是自己只是面不够，分配了几次，出现了各种报错，导致安装不成功。
最后，我抱着试试看的态度选择了默认分区……
想不到这是个机智的选择【开心脸…很快安装引导系统帮我分配好了挂载点，留意了一下方案，是个经典的分区策略……
当然等以后技术好了其实还可以通过命令行进行修改的，对于笔者这样的小白来说，先装好系统才是王道。

每个人电脑具体情况不同，在此不列出具体解决方案。
如果有童鞋对Linux系统分区感兴趣的话，可以查阅相关资料，根据自身需求，分区的具体方案是有很多种的，在此笔者不做赘述。

5. 关于安装之后开机引导项的解决方案在网上也有很多，笔者偷个小懒……（使用基于win的mbr方案或者基于Linux的引导方案均可，推荐mbr。）


教程阐述了笔者在安装过程中遇见的几个比较难解决的问题，希望能给各位提供一定的参考。预祝在Linux世界中玩得开心~
