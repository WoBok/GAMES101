## 下载
[下载地址](https://gitlab.com/libeigen/eigen/-/tree/master)  
git clone 下载到本地
## 安装
打开下载路径
```
mkdir build
cd build
cmake ..
sudo make install
```
安装后文件路径 usr/local/include/eigen3
## 测试
`vim eigentest.cpp`
```
#include <iostream>
#include <eigen3/Eigen/Dense>
using Eigen::MatrixXd;

int main()
{
	MatrixXd m(2,2);
	m(0,0) = 3;
	m(1,0) = 2.5;
	m(0,1) = -1;
	m(1,1) = m(1,0) + m(0,1);
	std::cout << m << std::endl;
}
```
运行

`g++ *.cpp -o app`  
`./app` 
 
输出：
```
3   -1
2.5 1.5
```