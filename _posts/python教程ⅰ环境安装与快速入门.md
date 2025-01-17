---
title: Python教程Ⅰ环境安装与快速入门
tags: []
id: '2801'
categories:
  - - 技术贴
date: 2021-08-23 22:05:10
---

## 01 Python简介

```
    Python是一种解释型语言，对比C/C++，Python程序不需要编译即可运行，因此具有很强的跨平台性。另外，所有的命令都是逐行发送到Python解释器执行，不需要经过链接过程，因此代码顺序十分重要。      
                                
                                                                             C/C++(左)与Python(右)的程序执行对比
                                    
    
```

**Python应用领域广阔**，在Web应用后端开发、云基础设施建设、网络数据采集（爬虫）、自动化测试、数据分析、机器学习等领域都有着广泛的应用。

**Python也存在一些缺点**，例如执行效率稍低、代码无法加密以及框架太多，良莠不齐等。

## 02 如何学习Python

```
    
```

  
本次教程将主要从已学的C/C++出发，讲解Python基本语法，大家也可以基于此学习流程控制、面向对象的编程方法（OOP）。

**阅读Python教程**  
网络上Python教程良莠不齐，此处推荐  
[https://www.liaoxuefeng.com/wiki/1016959663602400](https://www.liaoxuefeng.com/wiki/1016959663602400)  
官方文档本身就是不错的教程， 见  
[https://docs.python.org/zh-cn/3/](https://docs.python.org/zh-cn/3/)。

**观看视频学习，不建议，为什么**  
观看视频更多是一种观察 + 模仿，而阅读文档是读书 + 思考，前者更适用于入门，但对于深入学习，往往后者效率更高。并且文档的时效性更强，有许多修正，需要培养阅读文档的能力。

**多练习！！！**

## 03 环境安装

```
    首先，让我们来安装环境！
```

对Windows系统，推荐使用Anaconda环境，对Linux或Mac OS系统，推荐使用Miniconda环境。

为什么不使用纯Python环境呢？尽管Anaconda也有体积较大等缺点，但首先，**纯Python环境包版本管理不便**，例如进行机器学习时，学习他人代码往往需要不同版本的TF与Pytorch，创建虚拟环境就可以很好解决这一问题；其次，**纯Python环境需要自己安装需要数据科学必要的包**。

![Anaconda](../../wp-content_uploads/2021/08/Anaconda.jpg)

Anaconda

```
    Anaconda安装步骤：       
        [01] 下载Anaconda安装包     
    
```

  
[https://mirrors.tuna.tsinghua.edu.cn/help/anaconda/](https://mirrors.tuna.tsinghua.edu.cn/help/anaconda/)

![在开源镜像站下载安装包](../../wp-content_uploads/2021/08/%E5%9C%A8%E5%BC%80%E6%BA%90%E9%95%9C%E5%83%8F%E7%AB%99%E4%B8%8B%E8%BD%BD%E5%AE%89%E8%A3%85%E5%8C%85-1024x325.jpg)

在开源镜像站下载安装包

```
        [02] 添加环境变量        
                                
                                                                              将Anaconda添加到环境变量中
                                    
    环境变量可以认为是Windows搜索程序的路径，执行程序时，Windows系统会在环境变量中逐个搜索，如果找不到，则会返回找不到可执行文件。       
                                
                                                                              未搜索到环境变量
                                    
        [03] 修改源       
    
```

  
[https://mirrors.tuna.tsinghua.edu.cn/help/anaconda/](https://mirrors.tuna.tsinghua.edu.cn/help/anaconda/) ；  
修改pip源，具体参见  
[https://mirrors.tuna.tsinghua.edu.cn/help/pypi/](https://mirrors.tuna.tsinghua.edu.cn/help/pypi/)

**让我们来测试环境！**

### \[01\] 打开命令提示符

```
    Win+S 搜索命令提示符 或 Win+R 输入cmd然后回车      
        [02] 输入如下命令        
    
```

  

> python
> 
> ### \[03\] 打开交互式命令行
> 
> 试试输入1124 \*\* 122 然后回车，这是在计算1124的122次方（于是你就获得了一个强大的计算器）
> 
> ![测试环境代码](../../wp-content_uploads/2021/08/%E6%B5%8B%E8%AF%95%E7%8E%AF%E5%A2%83%E4%BB%A3%E7%A0%81.jpg)
> 
> 测试环境代码
> 
> **我不想在黑框框里编程！**  
> 可安装文本编辑器（或集成开发环境， IDE）  
> Python脚本文件是纯文本文件，理论上只需要记事本即可编辑，编辑后即可使用Python解释器运行。但是记事本没有代码补全、代码高亮、代码警告等。
> 
> ![通过记事本编辑Python脚本文件](../../wp-content_uploads/2021/08/%E9%80%9A%E8%BF%87%E8%AE%B0%E4%BA%8B%E6%9C%AC%E7%BC%96%E8%BE%91Python%E8%84%9A%E6%9C%AC%E6%96%87%E4%BB%B6.jpg)
> 
> 通过记事本编辑Python脚本文件
> 
> **1\. 使用PyCharm**  
> JetBrain公司出品，堪称神器，参考  
> https://blog.csdn.net/zfcjhdq/article/details/104919067

**2\. 使用Vscode**  
Microsoft出品，支持多种编程语言，本身是个文本编辑器，可通过扩展支持各类IDE功能，参考  
[https://code.visualstudio.com/docs/languages/python](https://code.visualstudio.com/docs/languages/python) ，通过清华邮箱可申请专业版。

## 04 快速入门

```
        [01] 第一个Python程序       
    
```

  
用文本编辑器打开这个文件，添加内容

                `
                    print('Hello, world!')`
            

```
    在此处打开cmd，输入python hello.py       
                                
                                                                               第一个Python程序
                                    
    对比C，这就十分简洁       
                    
                #include <stdio.h></code></pre>
<p>int main() {
printf(&quot;Hello, world!&quot;);
return 0;
}


与C语言对比
        [02] Python数据类型及变量     
    Python是一种强类型语言同时也属于动态类型语言， Python的变量具有明确的类型，虽然这种类型可以改变。        
                    
                #include <stdio.h></code></pre>
<p>a = 100
b = 12.345
c = 1 + 5j
d = 'hello, world'
e = True
print(type(a))    # &lt;class 'int'&gt;
print(type(b))    # &lt;class 'float'&gt;
print(type(c))    # &lt;class 'complex'&gt;
print(type(d))    # &lt;class 'str'&gt;
print(type(e))    # &lt;class 'bool'&gt;


Python的各种数据类型
                    
                int a = 100;</code></pre>
<p>double b = 12.345;</p>
<h1>include <complex.h></h1>
<p>double _Complex c = 1.0+5.0<em>I;
const char</em> d = &quot;hello, world&quot;;  


C的数据类型
        [03] Python运算符     
    Python运算符与C差异不大，需要注意的是除法与C定义不同。Python // 被称为 floor divide（除之后向下取整）       
                    
                a = 29</code></pre>
<p>b = 3
print('%d + %d = %d' % (a, b, a + b))   #29 + 3 = 32
print('%d - %d = %d' % (a, b, a - b))   #29 - 3 = 26
print('%d <em> %d = %d' % (a, b, a </em> b))   #29 * 3 = 87
print('%d / %d = %f' % (a, b, a / b))   #29 / 3 = 9.666667
print('%d // %d = %d' % (a, b, a // b)) #29 // 3 = 9
print('%d %% %d = %d' % (a, b, a % b))  #29 % 3 = 2
print('%d <strong> %d = %d' % (a, b, a </strong> b)) #29 ** 3 = 24389


Python中运算符

那么，Python中 -1//2 与C中 -1/2 相同吗？

Python中//是除后向下取整，结果为-1，C的除法/采取截断，结果为0。
                    
                a = 10</code></pre>
<p>b = 3
a += b       # 相当于: a = a + b
a <em>= a + 2   # 相当于: a = a </em> (a + 2)
print(a)     # 算一下这里会输出什么


Python其他运算符
                    
                flag0 = 1 == 1</code></pre>
<p>flag1 = 3 &gt; 2
flag2 = 2 &lt; 1
flag3 = flag1 and flag2
flag4 = flag1 or flag2
flag5 = not (1 != 2)
print('flag0 =', flag0)  # flag0 = True
print('flag1 =', flag1)  # flag1 = True
print('flag2 =', flag2)  # flag2 = False
print('flag3 =', flag3)  # flag3 = False
print('flag4 =', flag4)  # flag4 = True
print('flag5 =', flag5)  # flag5 = False


Python逻辑运算符

Python有一个神奇的运算符，但并不推荐使用
                    
                x = 10</code></pre>
<p>print(7 &lt;= x &lt;= 11)  # True, which equals to (7 &lt;= x) and (x &lt;= 11)
print(7 &lt;= x &lt;= 9)   # False


为什么不推荐使用呢？C/C++的残留编程习惯可能会造成一些错误！比如说：
                    
                print(False == False == False) # Is True or False?
            
        
    True     
        [04] Python类型转换        
    Python是一种强类型语言， Python的变量具有明确的类型，虽然这种类型可以改变      
                    
                a = 100</code></pre>
<p>b = 12.345
a = b  # a = 12.345
a = int(b)  # a = 12
a = float(a)  # a = 12.0
c = &quot;12.045&quot;
a = float(c)  # a = 12.045


Python变量类型转换
                    
                #include <stdio.h></code></pre>
<p>int main(){
int a = 100;
double b = 12.345;
a = b;            //Not allowed!
a = (int)b;
a = (double)a;    //Not allowed!<br />
}


C变量类型转换
        [05] Python输入输出        
    输入输出比C更加便捷       
                    
                print('The quick brown fox', 'jumps over', 'the lazy dog')</code></pre>
<p>print('100 + 200 =', 100 + 200)
a = 10
b = 20
print(str(a) + ' + ' + str(b) + ' = ' + str(a + b))
print(a, '+', b, '=', a + b)
print('%d + %d = %d' % (a, b, a + b))
name = input(&quot;请输入名字：&quot;)
age = int(input(&quot;请输入年龄：&quot;))
print(name,&quot;的年龄为&quot;, age)


Python输入输出
        [06] Python字符串及常用数据结构      
    Python中，字符串格式化与C相同       
                    
                print('Hi, %s, you have $%d.' % ('Michael', 1000000))</code></pre>
<p>A = &quot;hello&quot;
if A == &quot;&quot;:
print(&quot;A is a empty string&quot;)


Python字符串格式化
        [07] Python流程控制        
    Python使用缩进来表示代码块，一般我们使用4个空格作为缩进，请不要使用Tab！严禁混用。流程控制语句如以下例子， if for while后有冒号: 请不要遗漏！     
                    
                age = 28</code></pre>
<p>if age &gt;= 18:
print('your age is', age)
print('adult')
Other code...


                
                    age = 3
if age &gt;= 18:
    print('your age is', age)
    print('adult')
else:
    print('your age is', age)
    print('teenager')
            
                    
                age = 3</code></pre>
<p>if age &gt;= 18:
print('adult')
elif age &gt;= 6:
print('teenager')
else:
print('kid')


                
                    sum = 0
for x in [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]:
    sum = sum + x
print(sum)
sum = 0
for x in range(11):
    sum += x
print(sum)
            
    for循环（对象必须可以遍历）      
                    
                sum = 0</code></pre>
<p>n = 99
while n &gt; 0:
sum = sum + n
n = n - 2
print(sum)


while循环
        [08] Python函数      
    Python使用def关键字来定义函数      
                    
                def add(a, b):
return a + b
            
        
    定义函数     
                    
                def acc(a, b, c):
return a, a + b, a + b + c
            
        
    函数可返回多个返回值
读者可做一个小练习：编写一个函数 fib(n)，返回第 n 个斐波那契数        
[09] Python其他常用语法
    交换两个对象的值     
                    
                a, b = b, a
            
        
    列表推导式        
                    
                print([x ** 2 for x in range(11)])
            
        
    还有很多语法糖……        
        [10] Python面向对象编程、字典、集合、dunder（魔术方法）、Python包管理工具     
    此部分已经在下一次教程推出，点击标题即可查看！     
        05 参考阅读        
    [1] https://github.com/jackfrued/Python-100-Days

[2] https://www.liaoxuefeng.com/wiki/1016959663602400

[3] https://docs.python.org/zh-cn/3/        
技术贴征稿事宜
    暑假期间我们将继续开放技术贴征稿！
技术贴推送是向全系同学传播与分享软件技术知识的良好渠道，我们致力于为同学们提供最实用的技术知识，为同学们的学习科研带来更多便利。
如果你有自己独特的技术小技巧，如果你乐于分享自己常用的实用工具软件，如果你希望与大家交流技术知识，欢迎联系我们投稿！成功过稿将会获得稿费噢！
```