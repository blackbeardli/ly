# 2019年07月20日

## 关于c语言，回顾

&nbsp;&nbsp;上节理解了gcc命令，从源文件（.c文件）编译到目标文件（.o文件或.out文件）。如果需要编译的文件太多，不适用gcc逐条编译的话，编写一个Makefile文件即可，声明由哪个文件编译到哪个文件，其中的内容逐级查找，递归编译。直接执行 `make` 命令即可。  
  
## 解释 return 0 的含义

&nbsp;&nbsp;简要概括就是：操作系统是根据这个return 值去判断该程序是否正确执行，如果不是0 ，程序会报出错误码，不会继续向下执行。

## 尝试使用vscode编写了aaa.c文件

代码示例如下：

        #include <stdio.h>
        int main(int argc, char const *argv[])
        {
            printf("一共有 %d 个参数传入\n",argc);
            int i=0;
            for (i = 0;i<argc;i++)
            {
            printf("这是%d, 命令是 %s\n",i,argv[i]);
            }
            return 0;
        }

遇到了问题：第4行42字符，“，”不小心使用了中文标点，导致报错，更改后编译却发现没有更改好，用vi命令更改好了之后发现在vscode更改了但是没有保存导致了编译产生错误。严密注意标点符号的情况。

## 关于for循环

我使用vscode代码自动填充了很多内容，这里再多理解一下。

        int i=0;//声明一个变量，'=0' 可以不写
        for (i = 0;i<argc;i++)  //声明for循环，参数i，i++是自增，i要在i<argc 这个条件限制下。亲测，将“i<argc”和“i++”换位，没有问题。
        {
        printf("这是%d, 命令是 %s\n",i,argv[i]); //这里注意要加上分号“；”
        }

2019年07月20日16:35:24

    ```
    fugrfhgjfj
    ```

