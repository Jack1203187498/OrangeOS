# class02

课后问题有两个

1. 自定义添加GDT段，LDT段，GDT段对内存数据写入一个字符串，LDT段读取并打印该GDT写入的内容

2. 自定义2个GDT段AB，分属于不同特权级，实现两个代码段之间的跳转

这里面`pmtest3z.asm`实现了对于GDT、LDT段的添加和相应操作

因为比较简单所以直接无脑堆上的单个字节写入


`pmtest5z.asm`实现了两个不同特权级之间代码段的转移

高特权级到低特权级没有问题，但是低特权级到高特权级需要加入调用门


不要忘记修改Makefile哦~


There are two questions in class 2:

1. Add a GDT segment, a LDT segment. The GDT segment can write date to the memory, which the LDT segment can read.

2. Add 2 GDT segments A, B that belong to different privileges.Realize the function that A jump to B and B jump to A.

`pmtest3z.asm` is for the addition of GDT and LDT
easy to add, and fool to add one by one :)


`pmtest5z` is for the jump of 2 privileges.

High privilege to low privilege is natural, but when it comes to the opposite, we shall use the gate to enable the function.


What's more, don't forget to change the Makefile!
