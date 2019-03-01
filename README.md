# development-library
开发过程中遇到的一些工具

一、关于protobuf安装及使用的问题
# protobuf安装
tar zxvf protobuf-all-3.6.1.tar.gz
cd protobuf-3.6.1
./autogen.sh
./configure
make
make install

# 对于指定protobuf的安装位置，需要设置环境变量（如安装路径为/usr/local/protobuf）
####### add protobuf lib path ########                                           
  #(动态库搜索路径) 程序加载运行期间查找动态链接库时指定除了系统默认路径之外的其他路径
  export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/protobuf/lib/                 
  #(静态库搜索路径) 程序编译期间查找动态链接库时指定查找共享库的路径               
  export LIBRARY_PATH=$LIBRARY_PATH:/usr/local/protobuf/lib/                       
  #执行程序搜索路径                                                                
  export PATH=$PATH:/usr/local/protobuf/bin/                                       
  #c程序头文件搜索路径                                                             
  export C_INCLUDE_PATH=$C_INCLUDE_PATH:/usr/local/protobuf/include/               
  #c++程序头文件搜索路径                                                           
  export CPLUS_INCLUDE_PATH=$CPLUS_INCLUDE_PATH:/usr/local/protobuf/include/       
  #pkg-config 路径                                                                 
  export PKG_CONFIG_PATH=/usr/local/protobuf/lib/pkgconfig/

# 错误处理
./autogen.sh执行报错./autogen.sh: line 38: autoreconf: command not found
安装autoconf和automake
yum -y install gcc automake autoconf libtool make
安装g++:
yum install gcc gcc-c++

二、关于blade编译系统的使用
# scons安装,需要先安装python
tar zxvf scons-2.5.0.tar.gz
cd scons-2.5.0
python setup.py install

# 关于vim配置及使用的文章
https://www.cnblogs.com/ma6174/archive/2011/12/10/2283393.html
