# 学习方法-开卷有益

1. 高效而愉快的学习
2. 先建立一个整体框架，然后细节。
3. 在实际工作中，要培养用到什么，能够快速学习的能力。
4. 先*know how*，再*know why*
5. 软件编程是一门“**做中学**”的学科，不是会了再做，而是做了才会。
6. 适当的<u>囫囵吞枣</u>
7. 学习软件编程是在琢磨别人怎么做，而不是我认为应该怎么做的过程。

# GO语言创始人

​	1. Ken Thompson

​	2. Rob Pike

​	3. Robert Griesemer

# GO语言的特点

1. 风格统一
2. 计算能力强
3. 处理大并发能力好
4. 静态语言的安全和性能&动态语言的开发维护高效率
5. 指针
6. 必须属于一个包
7. 引入垃圾回收
8. 天然并发
9. 支持函数返回多个值
10. 管道
11. 切片slice，defer

# SDK下载

> [下载地址](https://studygolang.com/dl)
>
> 配置环境变量： 
>
> ​	GOROOT: 指定SDK安装位置
>
> ​	GOPATH:  项目目录



# GO语言快速入门

> 需求： 开发一个hello.go程序，打印 Let's GO!

```go
package main

import "fmt"

func main(){
    fmt.Println("Let's GO!")
}
```

* 进入main目录，使用go build编译   go build hello.go  即可看到有一个hello.exe  运行即可  (go build -o abc.exe hello.go)
* 也可以使用go run hello.go 运行

# GO语言的执行流程

* xx.go --> (go build xx.go) --> xx.exe --> 运行
* xx.go --> go run xx.go

**区别与联系**

> * 编译后，可以将exe拷贝到没有go运行环境的机器上运行，go run需要机器上面有go执行环境
> * 编译器会将程序运行的依赖库文件包含在可执行文件中，所以.exe变大了很多。

# GO语言开发注意事项

* GO源代码以.go结尾
* GO应用程序执行的入口是main函数
* GO语言严格区分大小写
* GO语句后不需要加分号，编译器会自动加
* **GO编译器是一行一行进行编译的，因此我们不能把多行语句写在同一行**。
* **GO语言定义的变量或者引用的包没有使用，编译不通过**

# GO语言中的转义字符（escape char）

> \t	一个制表位，实现对齐功能	
> \n	换行符	
> \\	一个\	
> \"	一个"	
> \r	一个回车	

**案例截图**

![image-20200609002026521](.\asserts\image-20200609002026521.png)

**练习题**

> 请使用一句话输出下图效果

![image-20200609002419069](.\asserts\image-20200609002419069.png)

```go
package main

import "fmt"

func main(){
	fmt.Println("姓名\t年龄\t籍贯\t住址\njohn\t12\t河北\t北京")
}
```
