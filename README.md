Windows环境下python2.7安装mysql-python
当我们尝试用:

 pip install mysql-python #并不是MySQLdb
企图安装mysql时，我们会发现一开始进行的很顺利，但最后就会提示：

error: Microsoft Visual C++ 9.0 is required (Unable to find vcvarsall.bat).
Get it from http://aka.ms/vcpython27
1
2
因此我们根据上面提供的网址下载VCforPython27 
安装即可。

安装驱动

当我们尝试再次运行pip install mysql-python的命令时，我们发现又出错了：

No such file or directory
    error: command '"C:\Users\xxx\AppData\Local\Programs\Common\Microsoft\Visua
l C++ for Python\9.0\VC\Bin\amd64\cl.exe"' failed with exit status 2
1
2
3
我们需要下载驱动： 
64位：MySQL-python-1.2.3.win-amd64-py2.7.exe 
32位： MySQL-python-1.2.5.win32-py2.7.exe

在安装时遇到以下问题：

Python version 2.7 required, which was not found in the registry 
1
具体可参考博客：解决安装MySQL-python出现的:Python version 2.7 required, which was not found in the registry

安装成功

cmd命令行下执行：

pip install mysql
1
提示安装成功：

C:\Users\xxx>pip install mysql
Collecting mysql
  Using cached mysql-0.0.1.tar.gz
Requirement already satisfied: MySQL-python in c:\python27\lib\site-packages (from mysql)
Building wheels for collected packages: mysql
  Running setup.py bdist_wheel for mysql ... done
  Stored in directory: C:\Users\刘常榕\AppData\Local\pip\Cache\wheels\3a\83\02\e5a659e28b517bff04eee83a5fed1f36761afe8d591835cd29
Successfully built mysql
Installing collected packages: mysql
Successfully installed mysql-0.0.1
1
2
3
4
5
6
7
8
9
10
11
在python命令行下输入：

import MySQLdb
1
若无任何提示，则说明安装成功。


