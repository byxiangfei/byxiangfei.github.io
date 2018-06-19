---
layout: post
title: Routine Notes
categories: Go
description: 线程协程入门知识
keywords: co-rountine
---

### 两个寄存器

* esp 栈顶指针寄存器，指向调用栈的栈顶（始终指向，意味着栈分配到哪里了，从当前栈往高地址是已被分配了的）
* ebp 基址指针寄存器，指向当前活动栈帧的基址

一个function 调用会在栈上生成一个record ,称之为栈帧


### function 调用与栈活动(正常的情况下)

** 1.将传给被调用函数的参数从右至左压栈
** 2.将返回地址压栈，返回地址即函数调用结束后要执行的下一条指令的地址
** 3.将当前EBP 寄存器里的值压栈
** 4.将EBP寄存器的值设为ESP寄存器保存的值
** 5.在栈里为当前函数局部变量分配所需的空间，表现为修改ESP寄存器的值（一般是减4的整数倍,栈分配是从高地址向低地址分配）