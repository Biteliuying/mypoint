# mypoint
mypoint=&amp;i
条件编译好处：
1减少生成目标文件的长度
2可跨平台，增加程序可移植性，灵活性；就必须用条件编译
#if表达式
#else
#else if 表达式
#if_WIN32  //WaitForSingleObject()
#elif__linux__    //epoll()
#else
#endif
--------------------------------------------------------CHAPTER NINE-------------------------------------------------------
一：总述 指针非常重要
①前提知识点：//静态&动态存储区-----不同变量存在不同存储区
②有些变量内存在编译时候分配；有的在程序运行时分配；变量都占一定内存空间
int isize=sizeof(double);
printf("isize=%d\n",size);
二：地址概念
计算机中用数字描述地址，如1000（十进制）；但是计算机更习惯用16进制表示地址：如1000：0x3E8
int i = 5, j =6;     int 占4个字节，4个字节约21亿
三：直接访问和间接访问
直接访问：按变量地址存取变量值
间接访问：将变量i的地址，存放在另一个内存单元中
在C中，一般定义int，char，float，double这些变量，我们用来存放值。
mypoint=&i; //把变量i的地址保存到了mypoint
//理解成mypoint指向了i，这里所谓指向，就是通过地址体现。
指针变量：如果一个变量，比如mypoint，专门存放另外一个变量的地址，则称这个变量为“指针变量”；mypoint就是个指针变量。
//指针变量的值（也就是其中存放的值）是个地址（有人也叫指针）
//所有大家区别好：“指针变量”和“地址/指针”两个概念。“指针”就是个地址（地址也用数字表示），//指针变量是存放其他变量地址的变量，也叫该指针变量指向某某变量（比如这里的mypoint指向i）
