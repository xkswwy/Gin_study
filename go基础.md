# 基础

## 1..创建一个hello

1.使用vscode创建一个hello文件  在hello文件下创建一个go.mod文件

main 是用来写主函数  编译运行后产生hello.exe 运行程序

2.导入包输入import  







![image-20221026195926809](C:\Users\sb\AppData\Roaming\Typora\typora-user-images\image-20221026195926809.png)

3.终端输入命令

使用go build  加上项目名运行

![image-20221026200233024](C:\Users\sb\AppData\Roaming\Typora\typora-user-images\image-20221026200233024.png)





![image-20221026200211450](C:\Users\sb\AppData\Roaming\Typora\typora-user-images\image-20221026200211450.png)



其他命令

![image-20221026200455777](C:\Users\sb\AppData\Roaming\Typora\typora-user-images\image-20221026200455777.png)



总结：go.mob里写导入依赖  main.go 主函数 导入其他包使用import  exe是生成程序

## 2.导入快捷命令

类似配置输入输出

![image-20221026202551052](C:\Users\sb\AppData\Roaming\Typora\typora-user-images\image-20221026202551052.png)



## 3.依赖管理

要导入别人的依赖  项目中必须有一个 go mod   导入依赖  没有的话自己创建

![image-20221026205513205](C:\Users\sb\AppData\Roaming\Typora\typora-user-images\image-20221026205513205.png)



使用别人依赖

![image-20221026205532820](C:\Users\sb\AppData\Roaming\Typora\typora-user-images\image-20221026205532820.png)



## 4.变量和常量



go中声明  var + 名字 +类型  一般

中括号批量声明

变量声明后必须使用

![image-20221026211038482](C:\Users\sb\AppData\Roaming\Typora\typora-user-images\image-20221026211038482.png)



2.可不声明 根据类型

函数内存可使用短声明  n:=10



![image-20221026211301616](C:\Users\sb\AppData\Roaming\Typora\typora-user-images\image-20221026211301616.png)



3.常量 const

![image-20221026211333389](C:\Users\sb\AppData\Roaming\Typora\typora-user-images\image-20221026211333389.png)



4.iota记录常量中的索引

![image-20221026211352637](C:\Users\sb\AppData\Roaming\Typora\typora-user-images\image-20221026211352637.png)





## 5.数据类型

整形 两大类 有符号和无符号类型



![image-20221026214919694](images/image-20221026214919694.png)



![image-20221026214955085](images/image-20221026214955085.png)



不同表示进制

下面的案例是输入不同机制  使用10进制显示

![image-20221026215033033](images/image-20221026215033033.png)



浮点数

![image-20221026215344266](images/image-20221026215344266.png)



![image-20221026215410813](images/image-20221026215410813.png)





字符串常用函数 调用strings类的函数

![image-20221026215528697](images/image-20221026215528697.png)

替换前后缀





如果字符串是多行  使用反引号

![image-20221026215508190](images/image-20221026215508190.png)



byte和runne

使用中午或者日文时使用



![image-20221026215815561](images/image-20221026215815561.png)

打印例子

使用rune可以正常显示中文

![image-20221026215857935](images/image-20221026215857935.png)



重点：修改字符串需要将其先进性转化。再转回string

![image-20221026220020321](images/image-20221026220020321.png)





## 6.结构



if语句

![image-20221031113319113](images/image-20221031113319113.png)



for

![image-20221027121223603](images/image-20221027121223603.png)





switch

![image-20221027121258561](images/image-20221027121258561.png)



![image-20221027121320632](images/image-20221027121320632.png)



goto跳出所有循环

![image-20221027121348717](images/image-20221027121348717.png)





## 7.数组

1.定义数组

注意数组的长度也属于数组的一部分，长度不相等，两个数组不想恒

![image-20221027122352869](images/image-20221027122352869.png)



2.初始化

直接var 变量名=数组类型

![image-20221027122442594](images/image-20221027122442594.png)



3.数组的遍历

![image-20221027122540338](images/image-20221027122540338.png)



4.二维数组



![image-20221027122614507](images/image-20221027122614507.png)



5.多维数组只有一层使用...来让显示器推到长度

![image-20221027122702227](images/image-20221027122702227.png)



6.数组是值类型与c++不一致

![image-20221027122721039](images/image-20221027122721039.png)



## 8.切片



切片

在java里面，当我们向截取数组中某一部分时，需要申请新数组，进行拷贝。

go数组缺点

![image-20221027125954266](images/image-20221027125954266.png)



切片

![image-20221027130022912](images/image-20221027130022912.png)



类似字符串截取

low high 是一个左闭又开区间

长度 容量

![image-20221027130147761](images/image-20221027130147761.png)



![image-20221027130157170](images/image-20221027130157170.png)



完整的切片表达式

![image-20221027130329848](images/image-20221027130329848.png)



make做切片，动态分配

![image-20221027130531398](images/image-20221027130531398.png)



本子

![image-20221027130553035](images/image-20221027130553035.png)

判断切片是否为空

![image-20221027133132289](images/image-20221027133132289.png)



切片拷贝，是地址

![image-20221027133150449](images/image-20221027133150449.png)



类似java插入一段字符串

![image-20221027133522974](images/image-20221027133522974.png)



扩容 两倍

![image-20221027133550375](images/image-20221027133550375.png)



使用copy函数复制

![image-20221027133811063](images/image-20221027133811063.png)



切片中删除函数  使用覆盖的思想

![image-20221027133846376](images/image-20221027133846376.png)



## 8.map

定义

![image-20221027134925149](images/image-20221027134925149.png)



基本使用

![image-20221027134940253](images/image-20221027134940253.png)



判断某个键是否存在

![image-20221027135007298](images/image-20221027135007298.png)



map遍历

![image-20221027135026839](images/image-20221027135026839.png)



delete删除键值对

![image-20221027135144018](images/image-20221027135144018.png)



![image-20221027135154693](images/image-20221027135154693.png)



两种特殊类型

![image-20221027135214384](images/image-20221027135214384.png)





## 9.函数





重点搞懂闭包概念

[(15条消息) Golang中闭包的理解_Erick_Lv的博客-CSDN博客_golang的闭包](https://blog.csdn.net/qq_35976351/article/details/81986496)





函数

![image-20221027154648514](images/image-20221027154648514.png)





例子

![image-20221027154718420](images/image-20221027154718420.png)



函数参数注意，先写名字 在写类型  两个以上只写后面

![image-20221027154759505](images/image-20221027154759505.png)





函数可返回多个值

![image-20221027154818650](images/image-20221027154818650.png)





全局变量和局部变量

![image-20221027154855993](images/image-20221027154855993.png)





函数类型可以提前定义，将同类型的函数可以复制给当前定义的函数

![image-20221027155001331](images/image-20221027155001331.png)

函数还可作为参数和返回值



![image-20221027155018940](images/image-20221027155018940.png)



重点闭包

1.匿名函数

好处  动态的写出来，需要什么写什么

![image-20221027155054819](images/image-20221027155054819.png)



2.闭包

好处：匿名函数不需要人为输入，可以直接使用外面的变量

![image-20221027155132595](images/image-20221027155132595.png)





defer语句

处于defer语句的比非defer会延迟进行，defer代码块中的语句倒序执行。

![image-20221027155240448](images/image-20221027155240448.png)





常见内置函数

![image-20221027155300884](images/image-20221027155300884.png)



异常处理（之后细细研究）

![image-20221027160232428](images/image-20221027160232428.png)



## 10.指针

go里面对指针的与c类似，不过其只有取值和取地址，没有偏移操作。

![image-20221027160752124](images/image-20221027160752124.png)



问题抛出

应用类型的变量声明 还必须为他分配内存空间

![image-20221027175821004](images/image-20221027175821004.png)



使用new 和mak



![image-20221027175832876](images/image-20221027175832876.png)



![image-20221027175840389](images/image-20221027175840389.png)



new 和make的区别

返回不同 new返回指针  make返回引用类型本身

![image-20221027175854762](images/image-20221027175854762.png)



什么时候用指针

对于基本类型 数组 值 改值时必须用指针 下面使用*来取值

![image-20221102133703400](images/image-20221102133703400.png)

而对于结构体 一般也用指针 只不过不需要* 来取值





## 11.结构体

自定义类型和类型别名

![image-20221027190700321](images/image-20221027190700321.png)



区别

![image-20221027190719737](images/image-20221027190719737.png)





结构体定义与c类似  不过这里同样没有什么构造函数，需要的话自己写

![image-20221027190810410](images/image-20221027190810410.png)



实例化

![image-20221027190836376](images/image-20221027190836376.png)



创建指针类型结构体。这里提一嘴，若需要传入方法里面改变其值，我们还是需要穿结构体指针

使用new运算符得到的是指针



![image-20221027191116998](images/image-20221027191116998.png)



初始化

使用键值对初始化

![image-20221027191144630](images/image-20221027191144630.png)



值列表初始化

![image-20221027191335255](images/image-20221027191335255.png)



结构体内存布局实际上类似数组 是一片连续的空间

![image-20221027191403305](images/image-20221027191403305.png)



如果实现构造函数  返回值最好是指针

因为返回是普通的结构体，必然会有一个值拷贝过程，效率慢。

![image-20221027191508091](images/image-20221027191508091.png)



接受者实际就是方便来传入结构体，然后进行操作

![image-20221027191557061](images/image-20221027191557061.png)

方法函数的特定区别

![image-20221027191743898](images/image-20221027191743898.png)



![image-20221027191806803](images/image-20221027191806803.png)



什么时候需要指针？

![image-20221027191819125](images/image-20221027191819125.png)



![image-20221027191849501](images/image-20221027191849501.png)



![image-20221027191859880](images/image-20221027191859880.png)



结构体中的继承  实际就是儿子有父亲的指针 

![image-20221027191935092](images/image-20221027191935092.png)



![image-20221027191956155](images/image-20221027191956155.png)



重点  方法的接受者

如何在go中struct加入方法

通过方法接受者模式  类似于挂载 将方法挂到对象上

![image-20221028134559355](images/image-20221028134559355.png)





也就是接受者是要被加入方法的类对象，

![image-20221028134632177](images/image-20221028134632177.png)









指针类型接受者





## 12.包

学习网站



学习地址

[Go语言基础之包 | 李文周的博客 (liwenzhou.com)](https://www.liwenzhou.com/posts/Go/11-package/)



## 13.接口

定义

![image-20221028140949759](images/image-20221028140949759.png)



实现接口

![image-20221028141000507](images/image-20221028141000507.png)











这里就实现啦一个多态的实现

步骤：

1.声明接口  接口中的函数

2.声明一个结构体

3.将结构构体上挂载添加与接口同名函数



4.写一个函数  参数类型是接口  方法里调用其方法  也就是接口类型指向其子类类型这种形式

![image-20221028140934436](images/image-20221028140934436.png)





空接口的用处  传参可以任意传

![image-20221028155325024](images/image-20221028155325024.png)



类型断言

这里类似泛型的概念

![image-20221102104430827](images/image-20221102104430827.png)



## 14.error接口

没有类似java中的trycatch来处理

这里相当于直接抛异常

![image-20221028161217443](images/image-20221028161217443.png)



![image-20221028161248304](images/image-20221028161248304.png)





自定义错误接口

![image-20221028161401345](images/image-20221028161401345.png)



输出错误

![image-20221028161415490](images/image-20221028161415490.png)





错误结构体

![image-20221028161427972](images/image-20221028161427972.png)



项目中如何处理error

默认值为nil  用两个参数接受  然后第一个是最长返回的值，第二个是异常接受，然后使用if处理是否有异常

![image-20221029170433698](images/image-20221029170433698.png)





## 15.反射

学习网址

[Go语言基础之反射 | 李文周的博客 (liwenzhou.com)](https://www.liwenzhou.com/posts/Go/13_reflect/)





与java里面类似 都是获取类对象进行操作

函数中传入参数为接口 这样子方便接受任何类型

![image-20221028203848928](images/image-20221028203848928.png)



使用reflect包下的工具

![image-20221028203912270](images/image-20221028203912270.png)



name 和kind

type是机制类型，kind多用于自定义类型



![image-20221028203934281](images/image-20221028203934281.png)





![image-20221028204000012](images/image-20221028204000012.png)





如果要修改值  必须进行转换  reflect下的类型转为原生类型

![image-20221028204029907](images/image-20221028204029907.png)



案例

![image-20221028204045123](images/image-20221028204045123.png)



通过反射改值必须使用elem

![image-20221028204120682](images/image-20221028204120682.png)



![image-20221028204130807](images/image-20221028204130807.png)



结构体反射

![image-20221028204142109](images/image-20221028204142109.png)



![image-20221028204158601](images/image-20221028204158601.png)



![image-20221028204204981](images/image-20221028204204981.png)





## 16.并发

学习笔记

[Go语言基础之并发 | 李文周的博客 (liwenzhou.com)](https://www.liwenzhou.com/posts/Go/concurrence/#autoid-0-6-3)

、

这里面管道 可边读边写

同样适用互斥和同步





需要注意

![image-20221029164855585](images/image-20221029164855585.png)



![image-20221029165637433](images/image-20221029165637433.png)

为了让main线程不那么3快执行完  我们需要等一下





![image-20221029165722236](images/image-20221029165722236.png)



启动多个go

![image-20221029165734968](images/image-20221029165734968.png)



channel类型

![image-20221029165756727](images/image-20221029165756727.png)



![image-20221029165805907](images/image-20221029165805907.png)



例子

![image-20221029165815189](images/image-20221029165815189.png)



异常情况提示

![image-20221029165824458](images/image-20221029165824458.png)



注意无缓存通道  必须要有接受者  



![image-20221029165917117](images/image-20221029165917117.png)



![image-20221029165948514](images/image-20221029165948514.png)



forrange接收值快一点

![image-20221029170019040](images/image-20221029170019040.png)



单向通道

![image-20221029170039051](images/image-20221029170039051.png)



select多路复用

![image-20221029170106001](images/image-20221029170106001.png)



案例

![image-20221029170125225](images/image-20221029170125225.png)





接下来是并发和锁  按网站学习





## 17.细节补充下划线

下划线的用处  忽略某些返回值

首先 read函数会有两个返回值  第二个一般是error



![image-20221029171628525](images/image-20221029171628525.png)





此时由于我们不想处理这个返回值

![image-20221029171701471](images/image-20221029171701471.png)



导包时的作用

![image-20221029172023226](images/image-20221029172023226.png)



细致讲解导包



[(15条消息) golang中的下划线(_)用法_raoxiaoya的博客-CSDN博客_golang 下划线](https://blog.csdn.net/raoxiaoya/article/details/108872221)



我们只要这个包的init函数，不需要导入包中其他

![image-20221029172143471](images/image-20221029172143471.png)





## 18.网络编程socket

客户端  服务端

此处学习

[Go语言基础之网络编程 | 李文周的博客 (liwenzhou.com)](https://www.liwenzhou.com/posts/Go/15_socket/#autoid-2-2-2)



#### 1.遇到问题总结3





EOF用处









## 19.定时器

单独用处  类似sleep暂停时间  有点  可以提前取消

![image-20221030123633945](images/image-20221030123633945.png)



## 20.打点器



隔一段时间做一件事



这里解析



打点器实际上就是一个通道  我们可以每隔一段时间在里面拿到值  通过select去拿 就达到啦每隔多少秒去做一个任务

![image-20221030133546107](images/image-20221030133546107.png)

![image-20221030133506423](images/image-20221030133506423.png)

解析

![image-20221030133601083](images/image-20221030133601083.png)





## 21.工作池

重点实现

![image-20221030155009671](images/image-20221030155009671.png)



![image-20221030154948082](images/image-20221030154948082.png)





## 22.workGroup实例

案例

![image-20221030161637962](images/image-20221030161637962.png)



成功案例

![image-20221030161706873](images/image-20221030161706873.png)













失败案例



![image-20221030161612933](images/image-20221030161612933.png)





原因分析

for里面的i是一个值，到最后都会是4



一定要理解for是main线程管的  go线程并发启动的

就是意思就是 我用B这种方法 然后因为我用的是for循环里面的那个i 但是有可能 i走到尾巴哦 go线程才启动 所以是4





就是原来 main线程控制i变化  go线程输入i 但是可能main线程i变化太快哦 然后go拿的时候 i以及变为4





## 23.速率限制重点





之后眼界



## 24.原子计数器

类似java的autointeger类似  i++操作是原子性的

![image-20221030185224387](images/image-20221030185224387.png)





## 25.互斥锁





![image-20221030190815640](images/image-20221030190815640.png)





![image-20221030190832868](images/image-20221030190832868.png)





## 26.通过线程通信解决互斥问题



之后细细研究 也就是通过管道 恢复的消息类型 判断此状态是否已经被其他线程占有



![image-20221030192802705](images/image-20221030192802705.png)





## 27.排序

使用格式：

sort.

![image-20221030193610498](images/image-20221030193610498.png)





自定义排序

![image-20221030194814148](images/image-20221030194814148.png)



## 28.panic

error初始是nil值  不等于nil代表遇到错误  这里使用panic类似抛出异常 而且停止程序

![image-20221030200619411](images/image-20221030200619411.png)





## 29.recover

需求   抛出pannic时  我们并不希望程序完全崩溃

![image-20221030201629304](images/image-20221030201629304.png)









## 30.字符串格式化

主要处理输出



![image-20221030202916004](images/image-20221030202916004.png)







## 31.json

json转基本数据类型



首先使用一个map【string】接口

string是为啦获取json中的key  接口是为啦获取任意值的value



![image-20221030204646136](images/image-20221030204646136.png)



基本转json

![image-20221030204732665](images/image-20221030204732665.png)





## 32.xml

![image-20221030204812924](images/image-20221030204812924.png)



## 33.时间



![image-20221030204840080](images/image-20221030204840080.png)





## 31.时间戳



![image-20221030204915747](images/image-20221030204915747.png)





## 35.时间格式化





![image-20221030204959513](images/image-20221030204959513.png)





## 36.随机数



![image-20221030205033198](images/image-20221030205033198.png)





## 37.解析url地址



![image-20221030205815633](images/image-20221030205815633.png)





## 38.文件

读文件



![image-20221030210345878](images/image-20221030210345878.png)



写文件

![image-20221030210411476](images/image-20221030210411476.png)



## 39.行过滤器



也就对输入进行处理转变为输出



![image-20221030210701652](images/image-20221030210701652.png)





## 40.文件路径

![image-20221030211134683](images/image-20221030211134683.png)

![image-20221030211208175](images/image-20221030211208175.png)





## 41.回调函数



1.首先函数也可以作为一种数据类型

声明这个类型变量后  我们就可以调用类型满足的函数

![image-20221102190252280](images/image-20221102190252280.png)



缺点 这里实际上还是调用对应函数，问题抛出 那我直接add  minus(a,b)不就行啦？不是一样效果嘛

当某个函数函数的形参列表至少有一个函数类型时。既可以通过我们传入不同的函数，实现类似java中多态的功能

这里我们caculate里面有caculate类型形参 然后传入add 或者divide 就能调用不同的功能





![image-20221102190840941](images/image-20221102190840941.png)

# Gin框架



1.helloworld

注意需要开启这个设置

![image-20221106121247563](images/image-20221106121247563.png)



r.get 方式 就是获取url  看是否能出发函数

![image-20221106121225622](images/image-20221106121225622.png)



路由有好几种方法

![image-20221106122745970](images/image-20221106122745970.png)



2.获取url参数

使用param



![image-20221106122630389](images/image-20221106122630389.png)



3.获取Query参数

url参数格式

![image-20221106124456053](images/image-20221106124456053.png)



![image-20221106124445665](images/image-20221106124445665.png)



4.获取POST参数

注意改为POST请求

浏览器上显示为JSON格式



![image-20221106130607700](images/image-20221106130607700.png)

5.post和Query混合

总结：/user/name  使用param获取参数

?user=Ton&name=wwy 使用query

post请求用ppost获取即可

显示信息  一些需要转换为json对象

![image-20221106131158134](images/image-20221106131158134.png)



6.Map参数

![image-20221106133452101](images/image-20221106133452101.png)



7.重定向



![image-20221106134703680](images/image-20221106134703680.png)



8.分组路由

也就是后面获取请求不需要每个都加上前缀

![image-20221106135151633](images/image-20221106135151633.png)



9.上传文件

![image-20221106135612356](images/image-20221106135612356.png)



10.html模板

![image-20221106135819923](images/image-20221106135819923.png)





11.中间件

![image-20221106140025773](images/image-20221106140025773.png)



