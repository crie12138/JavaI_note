# Java程序概述

## 1.1 Java程序设计平台



## 1.2 Java"白皮书"关键词

- 简单性

- 面向对象

  重点放在教椐 （ 即对象）和对象的接口上。用木匠打一个比方， 一个“ 面向对象的” 木匠始终关注的是所制 作的椅子， 第二位才是所使用的工具；一个“ 非面向对象的” 木匠首先考虑的是所 用的工具。在本质上，Java 的面向对象能力与 C++是一样的。

- 分布式

  Java 有一个丰富的例程库，用于处理像 HTTP 和 FIT 之类的 TCP/IP 协议。Java 应用 程序能够通过 URL 打开和访问网络上的对象，其便捷程度就好像访问本地文件一样。

- 健壮性

  Java 和 C++ 最大的不同在于 Java 采用的指针模型可以消除重写内存 和损坏数据的可能性。

- 安全性

- 体系结构中立

- 可移植性

  与 C 和 C++ 不同，Java 规范中没有“ 依赖具体实现” 的地方基本教据类型的 大小以及有关运算都做了明确的说明 。

  **Java 中的 int 永远为 32 位的整数，而在 C/C++ 中， int 可能是 16 位整数、 32 位整 数， 也可能是编译器提供商指定的其他大小。**

- 解释性

- 高性能

- 多线程

  多线程可以带来更好的交互响应和实时行为。

- 动态性

  库中可以自由地添加新方法和实例变量， 而对客户端却没有任何影响。在 Java 中找出运行时类型信息十分简单。



## 1.3 Java applet 与 Internet



## 1.4 Java发展史



## 1.5 关于Java常见的错误

1. Java 是 HTML 的扩展

   - **Java 是一种程序设计语言；HTML 是一种描述网页结构的方式。**
2. 使用 XML, 所以不需要 Java

   - **Java 是一种程序设计语言；XML 是一种描述数据的方式。**
3. Java 是一种非常容易学习的程序设计语言

   - Java不容易学习
4. Java 将成为适用于所有平台的通用性编程语言
   - 理论上可行，但是其他语言可能会在某些领域更有优势。
   - Java在**服务器端编程和跨平台客户端应用领域**很有优势。
5. Java 只不过是另外一种程序设计语言
6. Java 是专用的，应该避免使用
7. Java 是解释型的， 因此对于关键的应用程序速度太慢了
8. 所有的 Java 程序都是在网页中运行的
9. Java 程序是主要的安全风险
10. JavaScript 是 Java 的简易版
    - JS是一种在网页中使用的脚本语言
11. 使用 Java 可以用廉价的 Internet 设备取代桌面计算机

***



# 第二章 Java程序设计环境

***



# 第三章 Java的基本程序设计结构

## 3.1 一个简单的Java应用程序

> ` public class FirstSample { ` 
> 
> ​		`		public static void main(String[] args) {`		
> 
> ​				` 		System.out.println("We will not use 'Hello, World!"');` 		
> 
> ​		` 		}` 
> 
> ` 	}`

Java应用都具有这种结构。

**Java区分大小写**，(只能是main，不能是Main)。

关键字**public**称为**访问修饰符**，用于控制程序的其他部分对这段代码的访问级別。

关键字 **class** 表明 Java 程序中的全部内容都包含在类中。

在**class**后紧跟类名。Java 中定义类名的规则很宽松。名字必须以***字母***开头，后 面可以跟字母和数字的任意组合。长度基本上没有限制。但是不能使用 Java 保留字（例如， public 或 class) 作为类名。

![image-20210625102306976](https://raw.githubusercontent.com/crie12138/JavaI_note/main/images/image-20210625102306976.png)

![image-20210625102410987](https://raw.githubusercontent.com/crie12138/JavaI_note/main/images/image-20210625102410987.png)

标准的命名规范为（类名 FirstSample 就遵循了这个规范）：<font color=#FF8C00>**类名是以大写字母开头的名词。如果名字由多个单词组成，每个单词的第一个字母都应该大写**</font>（这种在一个单词中间使 用大写字母的方式称为**骆驼命名法**。以其自身为例， 应该写成 CamelCase)。

**源代码的文件名必须与公共类的名字相同**，并用 .java 作为扩展名。因此，存储这段源代码的文件名必须为 FirstSample.java。

Java 中任何方法的代码都用“  **{** ” 开始，用“ **}** ”结束。每个 Java 应用程序都必须有一个 main 方法。

> `{`
>
> ​		` Systein.out.println("We will not use 'Hello, World!'");`
>
> ` }`

在上面这个 main 方法体中只包含了一条语句，其功能是：将一个文本行输出到控制台上。

在这里使用的是**System.out**对象，并调用了它的println方法。

>  Java 使用的通用语法是(等价与函数调用)：	
>
> ​											object.method(parameters)



## 3.2 注释

常见的三种注释：

1. 使用 // ，范围是从//开始到本行结束
2. 长注释使用/*    */，将一段比较长的注释括起来
3. 自动生成文档， 以/**开始， 以\*/结束, 如程序清单3-1所示

>![image-20210625105127523](https://raw.githubusercontent.com/crie12138/JavaI_note/main/images/image-20210625105127523.png)



## 3.3 数据类型

Java 是一种强类型语言。这就意味着<font color=#FF8C00>必须为每一个变量声明一种类型</font>。

Java中一共有8种基本类型，4种整型、2种浮点类型、1种用于表示Unicode编码的字符单元的字符类型char、1种用于表示真值的boolean类型。

> 注释：Java 有一个能够表示任意精度的算术包， 通常称为“ 大数值”（ big number)。 虽然被称为大数值，但它并不是一种新的 Java 类型，而是一个 Java 对象。



### 3.3.1 整型

整型用于表示没有小数部分的数值， 它允许是负数。

![image-20210625105651539](https://raw.githubusercontent.com/crie12138/JavaI_note/main/images/image-20210625105651539.png)

- 在通常情况下，int 类型最常用
- 但如果表示星球上的居住人数， 就需要使用 long 类型 了
- byte 和 short 类型主要用于特定的应用场合， 例如， 底层的文件处理或者需要控制占用存储空间量的大数组



### 3.3.2 浮点类型

![image-20210625105931096](https://raw.githubusercontent.com/crie12138/JavaI_note/main/images/image-20210625105931096.png)

- double 表示这种类型的数值精度是 float 类型的两倍（有人称之为双精度数值)。绝大部分应用程序都采用 double 类型。
- 只有很少的情况适合使用 float 类型，例如，需要单精度数据的库，或者需要存储大量数据。

下面是用于表示溢出和出错情况 的三个特殊的浮点数值：

- 正无穷大
- 负无穷大
- NaN(不是一个数字)
- 一 正整数除以 0 的结果为正无穷大。计算 0/0 或者负数的平方根结果为 NaN。



### 3.3.3 char类型

char原本用于表示单个字符。但是现在也可以用来表示一些Unicode字符。

<font color=#FF8C00>char类型的字面量值要用单引号括起来。</font>例如， 'A'表示编码值为65的对应字符常量。与 "A" 不同， "A"是包含一个字符A的字符串。

char类型也可以表示为十六进制值。

> 转义序列：
>
> ![image-20210625112531020](https://raw.githubusercontent.com/crie12138/JavaI_note/main/images/image-20210625112531020.png)



### 3.3.4 Unicode和char

码点（ code point) 是指与一个编码表中的某个字符对应的代码值。

UTF-16 编码采用不同长度的编码表示所有 Unicode 码点。

在 Java 中，char 类型描述了 UTF-16 编码中的一个代码单元。

**强烈建议不要在程序中使用char类型， 除非确实需要处理UTF-16的代码单元。最好将字符串作为抽象数据类型处理。**



### 3.3.5 boolean类型

Boolean(布尔)类型有两个值: true 和 false，用于进行逻辑条件判断。

<font color=#FF8C00>整型值和布尔值之间不能进行转换。</font>



## 3.4 变量

在 Java 中，每个变量都有一个类型。在声明变量时，变量的类型位于变量名之前。

> 例如，
>
> `double salary; `
>
> `int vacationDays; `
>
> `long earthPopulation; `
>
> `boolean done;`
>
> **每个声明以分号结尾，由于声明是一条完整的 Java语句，所以必须以分号结束。**
>
> **但 ‘ + ’ 和 ' © ’  这样的符号不能出现在变量名中，空格也不行。**
>
> 
>
> 可以在一行中声明多个变量(不提倡，逐一声明每一个变量可以提高程序的可读性)：
>
> `int i,j`



### 3.4.1 变量初始化

声明变量后，必须使用赋值语句对变量进行显式初始化，**不能使用未初始化的变量**。

> `int vacationDays; `
>
> `System.out.println(vacationDays):`

对已经声明过的变量进行赋值，变量名在等号(=)左边，取值的java表达式放在右边

> `int vacationDays;` 
>
> `vacationDays = 12;`

或者放在一行中

> `int vacationDays = 12;`

在 Java 中可以将声明放在代码中的任何地方，  对于变量的声明尽可能地靠近变量第一次使用的地方。



### 3.4.2 常量

关键字final指示常量

> `final double CM_PER_INCH = 2.54;`
>
> 关键字 final 表示**这个变量只能被赋值一次**。一旦被赋值之后，就不能够再更改了。习惯上, 常量名使用**全大写**。

某个常量可以在一个类中的多个方法中使用，通常将这些常量称为 **类常量**。 使用关键字 **static final**进行指示

> ![image-20210625112531020](https://raw.githubusercontent.com/crie12138/JavaI_note/main/images/Snipaste_2021-06-25_16-53-06.png)
>
> - **注意：类常量定位在main方法的外部**， 该类中的其他方法也可以用这个常量，
> - 如果还声明为**public**， 那么其他类也可以使用该常量。即在其他类中可以直接调用Constants2.CM_PER-INCH



## 3.5 运算符

在Java中，算术运算符 + 、- 、*、 / 表示加减乘除。

在除法中，如果两个操作数都是整数，就表示整数除法，否则表示浮点除法。

% 表示取模操作

**注意：整数被 0 除将会产生一个异常， 而浮点数被 0 除将会得到无穷大或 NaN 结果**



### 3.5.1

在Math类中，包含了各种各样的数学函数。

> 1. 计算数值的平方根，使用sqrt方法
> ![image-20210625112531020](https://raw.githubusercontent.com/crie12138/JavaI_note/main/images/Snipaste_2021-06-25_17-08-23.png)
>
>
> 2. 计算幂运算，使用pow方法
>
> `double y = Math.pow(x, a);`

与println的区别在于：

|          println           |              Math.sqrt               |
| :------------------------: | :----------------------------------: |
| 处理的是System.out**对象** | 处理的不是对象，而是一种**静态方法** |

Math类中提供的常见三角函数：

> Math.sin 
>
> Math.cos 
>
> Math.tan 
>
> Math.atan 
>
> Math.atan2

还有指数函数以及它的反函数—自然对数以及以 10 为底的对数:

> Math.exp 
>
> Math.log 
>
> Math.log10

Java 还提供了两个用于表示 π 和 e 常量的近似值：

> Math.PI
>
> Math.E

注释：不必添加前缀"Math"， 可以只在源文件的顶部import就好：

> import static java.lang.Math.*;
>
> 此处为静态导入



### 3.5.2 数值类型之间的转换

数值类型经常需要发生转变：

![image-20210625112531020](https://raw.githubusercontent.com/crie12138/JavaI_note/main/images/Snipaste_2021-06-25_17-20-57.png)

图3-1中有6个实心箭头，表示无信息丢失的转换；3个虚箭头，表示可能有精度损失的转换。

对两个不同类型的数进行二元操作时，应该先将两个值转换为同一类型。

- 如果有double，都转为double
- 否则，如果有一个float类型， 都转为float类型
- 否则，如果有一个long类型， 都转为long类型
- 否则， 两个都转为int类型



### 3.5.3 强制类型转换

有时候需要将double强制转化为int，称为强制类型转换(cast)，可能会丢失一些信息。

强制类型转换的语法格式是**在圆括号中给出想要转换的目标类型**，后面紧跟待转换的变量名。

> `double x = 9.997;`
>
> `int nx = (int)x;`
>
> 变量nx值就会变成9。强制类型转换是通过截断小数部分将浮点转为整型的。

也可以对浮点数进行舍入运算，得到最接近的整数，可是使用到Math.round方法：

> `double x z 9.997; `
>
> `int nx = (int) Math.round(x);`
>
> 变量值成为10。

**警告：如果强制类型转化超出了目标类型的表示范围，结果就会截断成一个完全不同的值**

> (byte) 300的实际值为44



### 3.5.4 结合赋值和运算符

可以在赋值中使用二元运算符，这是一种很方便的简写形式。

> x += 4 	等价于 	x = x + 4
>
> 运算符一般在“=”的左边
>
> 涉及到强制类型转化：
>
> x 为一个int型变量
>
> x += 3.5； 是合法的，x会被设置为(int)(x + 3.5)



### 3.5.5 自增与自减运算符

自增： ++

自减： --

n++ 表示变量n的当前值加1， n--表示变量n当前值减1。

“前缀”与”后缀“形式的区别：前缀会先完成加一，而后缀还是使用原来的值。

> ` int m = 7;`
>
>  `int n = 7;`
>
>  `int a = 2 * ++m; // now a is 16, m is 8` 
>
> `int b = 2 * n++; // now b is 14, n is 8 `

**建议不要在表达式中使用++， 因为这样很容易让人困惑。**



### 3.5.6 关系和boolean运算符

| 关系 | 表示 |
| :--: | :--: |
| 相等 | ==   |
| 不等 | ！= |
| 小于(等于) | <= |
| 大于(等于) | >= |
| 与 | && |
| 或 | \|\| |
| 非 | ！ |

“与”和“或”运算的性质：类似于短路，**如果第一个操作已经能够确定表达式的值，第二个操作就不必计算了**。

> 在&&中，如果第一个表达式为假，不需要再判断第二个表达式。
>
> 在||中，如果第一个表达式为真，不需要再判断第二个表达式。

Java支持三元操作符	?:	，即

> condition ? expression1 : expression2
>
> 如果条件为真，执行第一个表达式，条件为假，执行第二个表达式
>
>  
>
> x < y ? x : y 即可以返回x,y中较小的一个值。



### 3.5.7 位运算符

在处理整型类型时，可以直接对数值各个位进行操作。可以使用掩码技术得到整数中的各个位。

位运算包括：&("and")	|("or")	^("xor")	~("not")

eg:	n为一个int型变量，用二进制表示的n从右往左第四位是1，则

> int fourthBitFromRight = (n & 0b1000) / 0b1000;
>
> 会返回 1，否则返回 0。



### 3.5.8 括号与运算符级别

如果不使用括号的话，整体的运算优先级如表3-4所示的优先级次序进行计算，同一优先级按从左到右的顺序计算。

![](https://raw.githubusercontent.com/crie12138/JavaI_note/main/images/Snipaste_2021-06-26_00-11-27.png)
![](https://raw.githubusercontent.com/crie12138/JavaI_note/main/images/Snipaste_2021-06-26_00-11-53.png)

> a && b || c   等价于   (a && b) || c
>
> a += b += c	等价于	a += (b += c)



### 3.5.9 枚举类型

对于变量取值在一个有限集合内的情况，可以自定义枚举类型。

枚举类型包括有限个命名的值：

> `enum Size { SMALL, MEDIUM, LARGE, EXTRA_LARCE };`

声明一个该类型的变量：

> `Size s = Size.MEDIUM`

Size类型的变量只能存储这个类型声明中给定的枚举值，或者是null值(null表示该变量没有设置值）



## 3.6 字符串

没有内置的字符串类型，而是使用预定义类，叫**String**

### 3.6.1 子串

使用String中的substring方法

> String greeting = "Hello";
>
> String s = greeting.substring(0, 3)

此处的s 即为“Hel”的子串，子串长度为（3-0）= 3



### 3.6.2 拼接

Java允许使用 "+" 连接(拼接)字符串

> String a = "abc"
>
> String b = "123"
>
> String res = a + b

res输出结果就为abc123

多个字符串放在一起，使用定界符分割，可以是静态**join方法**：

> String all = String.join("/", "s", "m", "l",  "xl")
>
> all 输出结果为"s/m/l/xl"



### 3.6.3 不可变字符串

在java中， String定义的字符串是不能改变的，即**不可变字符串**，就像数字3永远是3，不会变成4。

但是可以改变调用该字符串的变量，去调用另一个字符串，就像把存放位置的变量3改为4一样。

> eg : 将hello改成help！
>
> `String a = "hello"`
>
> `a = a.substring(0, 3) + "p!"`
>
> 即提取出"hel"的子串，然后通过字符串拼接，修改变量a的调用



### 3.6.4 检测字符串是否相等

使用**equals方法**检测两个字符串是否相等

> 表达式： a.equals(b)
>
> 也可以直接使用字符串字面量："hello".equals(a)
>
> 如果字符串a与b相等将返回true，不相等将返回false。

**注意！**：不能使用 ”==“ 判断两个字符串相等，该运算符只能判断字符串是否在一个位置



### 3.6.5 空串与Null串

空串是一个java对象，有串长度(0), 内容(空)

String a = ""; 

判断字符串是否为空

> if( a.length() == 0 )
>
> 或者 
>
> if( a.equals("") )

null是String变量可以存放的一个特殊值，表示目前没有任何对象与该变量关联。

检测字符串是否为null（此处可以使用“==”）：

> if (a == null)

检测字符串不为空也不为null，**应该先检查str不为null**：

> if (str != null && str.length() != 0)



