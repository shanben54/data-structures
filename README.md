# 数据结构容器库
这是用c++17实现的一些数据结构头文件，include即可使用

| 结构 | 头文件 | 复杂度 |
|---|---|---|
| 顺序表 | include/sqlist.h | 查找O(1),添加和删除O(n) |
| 链表 | include/linklist.h | 添加和删除O(1),查找O(n) |
| 顺序栈 | include/sqstack.h | 入栈和出栈O(1) |
| 顺序队列 | include/sqqueue.h | 入队和出队O(1)，最大容量有限 |
| 二叉树 | include/bitree.h | 前序/中序/后序遍历，层序遍历，非递归实现中序遍历 |

## 编译运行
**Linux / macOS**
```bash
cmake -B build
cmake --build build
./build/test_all
```
**Windows(MinGW)**
```bash
cmake -B build -G "MinGW Makefiles"
cmake --build build
./build/test_all.exe
```

## 项目目录
include:五个数据结构打包好的头文件
tests:测试文件
CMakeLists.txt:构建配置

## 环境要求
c++17 | GCC 8.1+ | CMake 3.10+ 

## 使用示例
```cpp
#include<iostream>
#include"sqstack.h"
using namespace std;

int main(){
    SqStack<int> st;
    st.Push(3);
    int e=0;
    cout<<st.Length()<<endl;
    st.GetTop(e);
    st.Pop(e);
    cout<<e<<endl;
    return 0;
}
```