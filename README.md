# development-library
开发过程中遇到的一些工具

# protobuf安装
tar zxvf protobuf-all-3.6.1.tar.gz
cd protobuf-3.6.1
./autogen.sh
./configure
make
make install

# 错误处理
./autogen.sh执行报错./autogen.sh: line 38: autoreconf: command not found
安装autoconf和automake
yum -y install gcc automake autoconf libtool make
安装g++:
yum install gcc gcc-c++

# scons安装,需要先安装python
tar zxvf scons-2.5.0.tar.gz
cd scons-2.5.0
python setup.py install

# 关于vim配置及使用的文章
https://www.cnblogs.com/ma6174/archive/2011/12/10/2283393.html
