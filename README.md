# mlpack_test
这是机器学习库mlpack在Windows平台下的编译使用。

## 编译环境
* 操作系统：Windows 7
* visual studio 2017 pro，Release x64下可直接编译运行

## 依赖包
* boost
* boost_unit_test_framework-vc141
* boost_program_options-vc141
* boost_random-vc141
* boost_serialization-vc141
* boost_math_c99-vc141
* OpenBLAS
* Armadillo

## 编译
参考https://keon.io/mlpack-on-windows/ （注：armadillo也可以用NuGet下载，不用另外编译）

## 使用
1. 把编译生成的C:/program files下的mlpack复制一份。该mlpack包括：
  *bin
  * include
  * lib

2. 把boost，openblas，armadillo目录下的include复制到该mlpack/include下

3. 把下面包的x64（按照你的编译模式选择32或者64）的lib包复制到该mlpack/lib下；
* boost_unit_test_framework-vc141
* boost_program_options-vc141
* boost_random-vc141
* boost_serialization-vc141
* boost_math_c99-vc141
* OpenBLAS
* Armadillo

4. vs2017新建一个项目，按https://github.com/mlpack/mlpack/wiki/WindowsBuild 方法导入头文件和包。这里，头文件为mlpack/include，包为mlpack/lib

5. 把mlpack.dll（在mlapck/bin下）和openblas包bin下.dll文件全部复制到项目Release下（与该项目可执行程序exe一个目录）

6. enjoy it
