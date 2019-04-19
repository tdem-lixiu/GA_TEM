第一章 MobaXterm的安装
=====================

1. 安装MobaXterm Personal Edition
:::::::::::::::::::::::::::::::::
笔者给出下载地址，``http://pan.baidu.com/s/1jHXiD6I``

（1）下载并解压，以管理员身份运行MobeXter-Setup-7.0.msi，进入安装界面。

（2）选择 **next** ，进入下一步。

（3）选择“接受条款”，点击 **next** 。

（4）选择安装路径，本次示范选择默认路径，点击 **next** 。

（5）安装完成，点击 **finish** 。安装完成后，将安装包内的Git.mxt3复制到 ``C:\\Program files(x86)\Mobatek\MobaXterm Personal Edition\`` 中文件夹内。
（依据你自己的安装路径）
双击快捷方式，打开软件，界面如下所示

2. 服务器的登陆与退出
:::::::::::::::::::::::::::::::::

在登录服务器时需要账户与密码，需要和管理人员（刘文韬，鲁凯亮）申请账号，在取得账号之后，在登陆界面输入

.. centered:: ssh username@192.168.199.101

比如鲁凯亮的就是

.. centered:: ssh lkl@192.168.199.101
输入完账号后，按回车键输入密码

输入密码时，不会像windows操作系统那样显示成 ``******`` ，不用理会，只管输入自己的密码，前提是保证密码正确。（密码一般默认为 ``tdemusernametdem`` ，例如鲁凯亮的密码就是 ``tdemlkltdem`` ）。输入密码之后，就可以进去操作界面了。下面一章将会介绍简单的操作命令行。退出的时候直接在界面输入 **exit** 。或者直接叉掉界面就行。 

第二章 文件处理命令
==================

1. ls
:::::::::::::::::::::::::::::::::

.. Note:: 命令英文原意：list 

命令所在路径： ``/bin/ls`` 

执行权限：所有用户

功能描述：显示目录文件

语法：

    ls 选项[-ald] [文件或目录]

    -a 显示所有文件，包括隐藏文件

    -l 详细信息显示

    -d 查看目录属性

2. cd
:::::::::::::::::::::::::::::::::

.. Note:: 命令英文原意：change directory

命令所在路径：shell内置命令

执行权限：所有用户

语法：

    cd  [目录]

功能描述：切换目录

范例：

.. centered:: cd  /   切换到根目录
.. centered:: cd  ..   回到上一级目录

说明：两个特殊的目录 . 和 .. ，分别代表当前目录和当前目录的父目录。

3. pwd
:::::::::::::::::::::::::::::::::

.. Note:: 命令英文原意：print working directory

命令所在路径： ``/bin/pwd``

执行权限：所有用户

语法：

    pwd

功能描述：显示当前所在的工作目录

范例：

.. centered:: pwd
.. centered:: 输出结果： ``/home/lkl``

4. touch
:::::::::::::::::::::::::::::::::

命令所在路径： ``/bin/touch``

执行权限：所有用户

语法：

    touch  [文件名]

功能描述：创建空文件

范例：

.. centered:: touch  newfile

5. mkdir
:::::::::::::::::::::::::::::::::

.. Note:: 命令英文原意：make directories

命令所在路径： ``/bin/mkdir``

执行权限：所有用户

语法：

    mkdir  [文件名]

功能描述：创建新目录

范例：

.. centered:: make  newdir

6. cp
:::::::::::::::::::::::::::::::::

.. Note:: 命令英文原意：copy

命令所在路径： ``/bin/cp``

执行权限：所有用户

语法：

    cp -R [源文件或目录] [目的目录]

    -R 复制目录 

功能描述：复制文件或目录

范例：

.. centered:: cp  file1  file2  dir1   将文件file1、file2复制到目录dir1
.. centered:: cp  -R  dir1  dir2    将dir1下的所有文件及子目录复制到dir2

7. mv
:::::::::::::::::::::::::::::::::

.. Note:: 命令英文原意：move

命令所在路径： ``/bin/mv``

执行权限：所有用户

语法：

    mv  [源文件或目录]  [目的目录]

功能描述：移动文件、更名

范例：

.. centered:: mv  file1  file3     将当前目录下文件file1更名为file3
.. centered:: mv  file2  dir2      将文件file2移动到目录dir2下

8. rm
:::::::::::::::::::::::::::::::::

.. Note:: 命令英文原意：remove

命令所在路径： ``/bin/rm``

执行权限：所有用户

语法：

    rm -r [文件或目录]

    -r 删除目录

功能描述：删除文件

范例：

.. centered:: mv  file3     删除文件file3
.. centered:: mv  –r  dir1     删除目录dir1

9. cat
:::::::::::::::::::::::::::::::::

.. Note:: 命令英文原意：concatenate and display files

命令所在路径： ``/bin/cat``

执行权限：所有用户

语法：

    cat  [文件名]

功能描述：显示文件内容

范例：

.. centered:: cat  /etc/issue
.. centered:: cat  /etc/services

10. more
:::::::::::::::::::::::::::::::::

命令所在路径： ``/bin/more``

执行权限：所有用户

语法：

    more  [文件名]

    （空格）或f   显示下一页

    （Enter）      显示下一行

    q或Q       退出

功能描述：分页显示文件内容

范例：

.. centered:: more  /etc/services

11. head
:::::::::::::::::::::::::::::::::

命令所在路径： ``/bin/head``

执行权限：所有用户

语法：

    head  -num  [文件名]

    -num 显示文件的前num行

功能描述：查看文件的前几行

范例：

.. centered:: head  -20  /etc/services

12. tail
:::::::::::::::::::::::::::::::::

命令所在路径： ``/bin/tail``

执行权限：所有用户

语法：

    head -num  [文件名]

    -num 显示文件的前num行

    -f 动态显示文件内容

功能描述：查看文件的后几行

范例：

.. centered:: tail  -20  /etc/services

13. ln
:::::::::::::::::::::::::::::::::

.. Note:: 命令英文原意：link

命令所在路径： ``/bin/ln``

执行权限：所有用户

语法：

    ln  -s  [源文件]  [目标文件]

    -s 创建软链接

功能描述：产生链接文件

范例：

.. centered:: ln  -s  /etc/services  /issue.soft     创建文件/etc/issue的软链接/issue.soft
.. centered:: ln  /etc/issue  /issue.hard     创建文件/etc/issue的硬链接/issue.hard

第三章 权限管理命令
===================

1. chmod
:::::::::::::::::::::::::::::::::

.. Note:: 命令英文原意：change the permissions mode of a file

命令所在路径： ``/bin/chmod``

执行权限：所有用户

语法：

    chmod  [{ugo}{+-=}{rwx}]  [文件或目录]

    [mode=421]  [文件或目录]

功能描述：改变文件或目录权限

范例：

.. centered:: chmod  g+w  file1     赋予文件file1所属组写权限

.. centered:: chmod  777  dir1     设定目录dir1为所有用户具有全部权限

.. list-table::

    * - 代表字符
      - 权限
      - 对文件的含义
      - 对目录的含义
    * - r
      - 读权限
      - 可以查看文件内容
      - 可以列出目录中的内容
    * - w
      - 写权限
      - 可以修改文件内容
      - 可以在目录中创建、删除文件
    * - x
      - 执行权限
      - 可以执行文件
      - 可以进入目录


2. chown
:::::::::::::::::::::::::::::::::

.. Note:: 命令英文原意：change file ownership

命令所在路径： ``/bin/chown``

执行权限：所有用户

语法：

    chown  [用户]  [文件或目录]

功能描述：改变文件或目录的所有者

范例：

.. centered:: chown  somebody  file1  改写文件file1的所有者为somebody

3. chgrp
:::::::::::::::::::::::::::::::::

.. Note:: 命令英文原意：change file group ownership

命令所在路径： ``/bin/chgrp`` 

执行权限：所有用户

语法：

    chown  [用户组]  [文件或目录]

功能描述：改变文件或目录的所属组

范例：

.. centered:: chown  adm  file1  改写文件file1的所属组为adm 

第四章 文件搜索命令
==================

1. which
:::::::::::::::::::::::::::::::::

命令所在路径： ``/usr/bin/which``

执行权限：所有用户

语法：

    which  [命令名称]

功能描述：显示系统命令所在目录

范例：

.. centered:: which ls

2. find
:::::::::::::::::::::::::::::::::

命令所在路径： ``/usr/bin/find``

执行权限：所有用户

语法：

    find  [搜索路径]  [搜寻关键字]

功能描述：查找文件或目录

范例：

.. centered:: find  /etc  –name  init  在目录/etc中查找文件init
.. centered:: find  /  -size  +204800  在根目录下查找大于100MB的文件
.. centered:: find  /  -user  sam  在根目录下查找所有者为sam的文件

3. locate
:::::::::::::::::::::::::::::::::

.. Note:: 命令英文原意：list files in databases

命令所在路径：``/usr/bin/locate``

执行权限：所有用户

语法：

    locate  [搜寻关键字]

功能描述：查找文件或目录

范例：

.. centered:: locate  file  列出所有和file相关的文件

4. grep
:::::::::::::::::::::::::::::::::

命令所在路径： ``/bin/locate``

执行权限：所有用户

语法：

    find  [指定字符串]  [源文件]

功能描述：在文件中搜寻字符串匹配的行并输出

范例：

.. centered:: grep  ftp  /etc/services
   
第五章 帮助命令
==============
1. man
:::::::::::::::::::::::::::::::::

.. Note:: 命令英文原意：manual

命令所在路径： ``/usr/bin/man``

执行权限：所有用户

语法：

    man  [命令或配置文件]

功能描述：获得帮助信息

范例：

.. centered:: man ls  查看ls命令的帮助信息
.. centered:: man services  查看配置文件services的帮助信息

2. info 
:::::::::::::::::::::::::::::::::

.. Note:: 命令英文原意：information

命令所在路径： ``/usr/bin/info``

执行权限：所有用户

语法：

    info [任何关键字]

功能描述：获得帮助信息

范例：

.. centered:: info ls  查看ls命令的帮助信息

3. whatis
:::::::::::::::::::::::::::::::::

命令所在路径： ``/usr/bin/whatis apropos`` 
``/usr/bin/makewhatis`` 

执行权限：所有用户

语法：

    whatis  [任何关键字]

功能描述：获得索引的简短说明信息

范例：

.. centered:: whatis ls  查看ls命令的帮助信息
 
第六章 压缩解压命令
====================

1. gzip
:::::::::::::::::::::::::::::::::

.. Note:: 命令英文原意：GNU zip

命令所在路径： ``/bin/gzip``

执行权限：所有用户

语法：

    gzip 选项 [文件]

功能描述：压缩文件

压缩后文件格式：.gz

2. gunzip
:::::::::::::::::::::::::::::::::

.. Note:: 命令英文原意：GNU unzip

命令所在路径： ``/bin/gunzip``

执行权限：所有用户

语法：

    gunzip 选项 [压缩文件]

功能描述：解压缩.gz的压缩文件

范例：

.. centered:: gunzip  file1.gz

3. tar
:::::::::::::::::::::::::::::::::

命令所在路径： ``/bin/tar``

执行权限：所有用户

语法：

.. code::

    tar 选项[cvf]  [目录]
    -c  产生.tar打包文件
    -v  显示详细信息
    -f  指定压缩后的文件名
    -z  打包同时压缩

功能描述：打包目录

压缩后文件格式：.tar.gz

范例：

.. centered:: tar  –zcvf  dir1.tar.gz  dir1  将目录dir1压缩成一个打包并压缩的文件

tar命令解压缩语法

.. code:: 

    -x  解包.tar文件
    -v  显示详细信息
    -f  指定解压文件
    -z  解压缩

范例：

.. centered:: tar  –zxvf  dir1.tar.gz

4. zip
:::::::::::::::::::::::::::::::::

命令所在路径： ``/usr/bin/tar``

执行权限：所有用户

语法：

    zip 选项[-r]  [压缩后文件名称]  [文件或目录]
    -r  压缩目录

功能描述：压缩文件或目录

压缩后文件格式：.zip

范例：

.. centered:: zip  services.zip  /etc/services  压缩文件
.. centered:: zip  –r  test.zip  /test  压缩目录

5. unzip
:::::::::::::::::::::::::::::::::

命令所在路径： ``/usr/bin/unzip``

执行权限：所有用户

语法：

    unzip  [压缩文件]

功能描述：解压.zip的压缩文件

范例：

.. centered:: unzip  test.zip  /test 

第七章 文件上传与下载以及注意事项
===============================

1. 文件上传与下载
:::::::::::::::::::::::::::::::::

启动MobeXter后，在上传文件之前一定不要先登陆，输入下面命令行上传代码

.. centered:: scp  –r  /drives/d/file  username@192.168.199.101:/home/username/work

以笔者为例

.. centered:: scp  –r  /drives/d/file  lkl@192.168.199.101:/home/lkl/work

命令行的意思是将笔者PC上D盘中的文件（夹）上传到家目录下的用户lkl下的work目录中。

在服务器上算完程序后，通常我们要将计算出来的数据下载到PC，下面给出下载文件的命令行

.. centered:: scp  –r  username@192.168.199.101:/home/username/work/shuju.dat  /drives/d

同样，以笔者为例

.. centered:: scp  –r  lkl@192.168.199.101:/home/lkl/work/shuju.dat  /drives/d

命令行的意思是将家目录下的用户lkl下的work目录中的shuju.dat数据文件下载到PC的D盘中。

2. 注意事项
:::::::::::::::::::::::::::::::::

（1）Linux严格区分大小写，命令名基本都是小写的英文字母

（2）方括号部分是可选项，可以不出现

（3）多个选项可以同时出现，例如： ``ls -ah``

（4）注意命令额参数之间的空格，多个空格也视为一个空格

（5）续行符 ``\``

（6）tab键自动补齐功能。比如 ``work`` 目录下只有 ``shuju.dat`` 一个文件，查看此文件时，输入下面命令

.. centered:: more  s

然后按一下tab键，就可直接查看 ``shuju.dat`` 中的内容，其功能相当于

.. centered:: more  shuju.dat

（7）通配符。这里说一个比较常用的通配符 ``*`` 。例如在 ``work`` 目录下有成百上千个 ``**.dat`` 文件和很多其他文件，一个个删除dat文件显然是一个很笨蛋的方法，这里通配符*就起到了很大的作用，输入下面命令

.. centered:: rm  -r  *.dat

就可以将dat文件全部删除。

（8）中断一个不需要的进程： ``Ctrl+C`` 。这里不是windows下复制的意思。

（9）杀死一个失控进程。首先在终端（即界面）输入top命令，查看自己想要杀掉的进程的PID号，（即执行程序exe前面的数字）。输入k，然后输入对应的PID号，回车即可。
