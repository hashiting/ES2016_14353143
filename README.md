#DOL框架与安装
##1.DOL框架描述
DOL是一个程序的并行应用软件开发框架。

- API：DOL定义了一组计算和通信的例程，使分布式的编程，对图形平台的并行应用程序。
- DOL功能模拟：为程序员提供一个可能性来测试他们的应用程序 
- DOL映射优化：将应用程序映射到图形架构平台。

##2.DOL的安装过程
1. 实验环境在linux下进行，并使用了虚拟机安装了Ubuntu
2. 首先安装一些必须的环境（在ubuntu下）

	`$	sudo apt-get update
	
	$	sudo apt-get install ant
	
	$ 	sudo apt-get install openjdk-7-jdk
	
	$	sudo apt-get install unzip`
	
	![结果](http://p1.bqimg.com/1949/1b537caece48621f.png)
3. 接着下载一些文件

	`sudo wget http://www.accellera.org/images/downloads/standards/systemc/systemc-2.3.1.tgz
	
	sudo wget http://www.tik.ee.ethz.ch/~shapes/downloads/dol_ethz.zip`
4. 接着开始解压文件
	* 新建dol的文件夹 
	* $	mkdir dol
	* 将dolethz.zip解压到 dol文件夹中
	* $	unzip dol_ethz.zip -d dol
	* 解压systemc
	* $	tar -zxvf systemc-2.3.1.tgz
5. 编译systemc
	* $	cd systemc-2.3.1
	* $	mkdir objdir
	* $	cd objdir
	* $	../configure CXX=g++ --disable-async-updates
	* $	sudo make install
	![http://p1.bqimg.com/1949/325c016ad4ce64c0.png](http://p1.bqimg.com/1949/325c016ad4ce64c0.png)
	* $	pwd
6. 编译dol
	* $	ant -f build_zip.xml all
	* $	cd build/bin/main
	* $	ant -f runexample.xml -Dnumber=1
       ![](http://p1.bqimg.com/1949/ca4c87bbf2a8be1a.png)
 
##3.实验感想
有时的目录并不是ppt上面的路径，要回退几步就可以看到要找的文件了。
	
