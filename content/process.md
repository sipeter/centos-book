# 第三章：CentOS的进程系统

## 如何暂停以及恢复当前进程的执行
- 使用`Ctrl+D`暂停当前进程。
- 进程被暂停后，使用`fg`把进程恢复到前台继续执行。
- 进程被暂停后，使用`bg`把进程恢复到后台继续执行。
- 如有多个进程被暂停，则可通过`jobs`命令查看其编号，再通过`fg [被暂停进程编号]`或`bg [被暂停进程编号]`，来恢复执行。

## 如何让linux命令在后台执行
- 在命令后加上符号`&`即可让linux命令在后台执行，例如`sellp 30 &`。
- 如该linux命令正在前台运行，可使用`Ctrl+D`暂停后，再使用`bg`把进程恢复到后台继续执行。

## 如何让后台正在运行的进程转到前台来
1. 对于所有运行的程序，我们可以用`jobs –l`指令查看，此时记住想要转到前台运行的进程的编号。
2. 我们可以用`fg %[number]`指令把一个程序调到前台来运行。

## 使用kill命令结束一个进程
`kill`命令的语法是`kill 进程的pid`；有时这样并不能终止进程，可以考虑使用`kill -9 进程的pid`，这会强制终止一个进程。

进程的pid可以通过`top`命令或`ps`命令进行查看。