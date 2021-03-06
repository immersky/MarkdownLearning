# Markdown 常用语法

### 0.目录{#index}

**说明**

在段落中填写`[TOC]`，将根据全文标题级别与上下位置生成目录,不同级别的标题横向位置不一样

**代码**

```
[TOC]
```

**效果(好像显示不出):**



[toc]









### 1.斜体和粗体

**代码**

```
*斜体*
**粗体**
***加粗斜体***
~~删除线~~
```

**效果：**

_斜体_

**粗体**

***加粗斜体***

~~删除线~~

### 2.分级标题

**代码**

```
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题
```

**效果:**

# 一级标题

## 二级标题

### 三级标题

#### 四级标题

##### 五级标题

###### 六级标题

*一级标题字最大，依级递减*

### 3.超链接

*超链接语法有两种形式，行内式和参考式*

#### 3.1行内式

**语法说明：**

[]里写连接文字，（）里写链接地址，（）中的“”可以为链接指定title属性

**代码**

```
欢迎来到[gg](http://steam.imwork.net)
```

**效果:**

欢迎来到[gg](http://steam.imwork.net)

#### 3.2参考式

参考式超链接一般用在学术论文上面，或者另一种情况，如果某一个链接在文章中多处使用，那么使用引用的方式创建链接将非常好，它可以让你对链接进行统一的管理。

##### 语法说明：

```
参考式链接分为两部分，文中的写法[链接文字][连接标记],在文本的任意位置添加[连接标记]：链接地址"连接标题"，链接地址与连接标题前有一个空格
如果链接文字本身可以作为链接标记，也可以写成[链接文字][]
[链接文字]:链接地址的形式
```

**代码**

```
我经常逛[Github][1]，[知乎][2]以及[简书][3]
[知乎][2]是个不错的[讨论社区][]
[1]:http://github.com "github"
[2]:http://www.zhihu.com "知乎"
[3]:http://www.jianshu.com "简书"
[写作社区] :http://www.jianshu.com

```

**效果：**

我经常逛[Github][1]，[知乎][2]以及[简书][3]
[知乎][2]是个不错的[讨论社区][]

[1]:http://github.com "github"
[2]:http://www.zhihu.com "知乎"
[3]:http://www.jianshu.com "简书"

[写作社区] :http://www.jianshu.com

#### 3.3自动连接

**代码**

```
<http://steam.imwork.com>
<xxxx@eg.com>
```

**效果:**

<http://steam.imwork.com>
<xxxx@eg.com>

### 4.锚点

*锚点即页内超链接，可以跳转到页内某个位置*

*注意* Markdown Extra 只支持在标题后插入锚点,其他地方无效

**语法描述**

在你准备跳转到的指定标题后插入锚点{#标记},然后再文档的其他地方写道连接到锚点的链接。

**代码**

```
## 0. 目录{#index}
					
					
					
					//中间这块留空区域当作页内其他内容



跳转到[目录](#index)	
```

**效果**

跳转到[目录](#index)

### 5.列表

####  5.1无序列表

使用 *,+，- 表示无序列表（在第一个列表后敲回车将自动生成第二个·并换行，以此类推）。

**代码**:

```
- 无序列表一
- 无序列表二
- 无序列表三

+ 无序列表四

*无序列表五
```

**效果**

+ 无序列表一
+ 无序列表二
+ 无序列表三



+ 无序列表四



* 无序列表五

#### 5.2有序列表

*游戏列表使用数字接着一个英文句点（在第一个列表后敲回车将自动生成第二个序号并换行，以此类推）*

**代码**

```
1. 有序列表一
2. 有序列表二
3. 有序列表三
```

**效果**



1. 有序列表一
2. 有序列表二
3. 有序列表三

#### 5.3 避免列表的错误出现

*有时列表会不小心产生，如下*

```
1986.what a great season.
```

*显示成*

1986. What a great season.

*避免方法：*

```
1986\.What a great season.
```

*效果*

1986\.What a great season.

### 6.引用

**语法说明：**
 引用需要在被引用的文本前加上>符号。

**代码：**



```undefined
> 这是一个有两段文字的引用,
>无意义的占行文字1.
>无意义的占行文字2.
>
>无意义的占行文字3.
>无意义的占行文字4.
```

**显示效果：**

> 这是一个有两段文字的引用,
>  无意义的占行文字1.
>  无意义的占行文字2.
>
> 无意义的占行文字3.
>  无意义的占行文字4.

Markdown 也允许你偷懒只在整个段落的第一行最前面加上 >：

**显示效果：**

> 这是一个有两段文字的引用,
>  无意义的占行文字1.
>  无意义的占行文字2.

> 无意义的占行文字3.
>  无意义的占行文字4.

#### 6.1 引用的多层嵌套

区块引用可以嵌套（例如：引用内的引用），只要根据层次加上不同数量的 >：

**代码：**



```ruby
>>> 请问 Markdwon 怎么用？ - 小白

>>自己看教程！ - 愤青

>教程在哪？ - 小白
```

**显示效果：**

> > > 请问 Markdwon 怎么用？ - 小白

> > 自己看教程！ - 愤青

> 教程在哪？ - 小白

#### 6.2引用其它要素

引用的区块内也可以使用其他的 Markdown 语法，包括标题、列表、代码区块等：
 **代码：**



```kotlin
> 1.   这是第一行列表项。
> 2.   这是第二行列表项。
>
> 给出一些例子代码：
> 
>     return shell_exec("echo $input | $markdown_script");
```

**显示效果：**

> 1. 这是第一行列表项。
> 2. 这是第二行列表项。
>
> 给出一些例子代码：
>
> 
>
> ```kotlin
> return shell_exec("echo $input | $markdown_script");
> ```

### 7.  插入图像

图片的创建方式与超链接相似，而且和超链接一样也有两种写法，行内式和参考式写法。

语法中图片Alt的意思是如果图片因为某些原因不能显示，就用定义的图片Alt文字来代替图片。 图片Title则和链接中的Title一样，表示鼠标悬停与图片上时出现的文字。 Alt 和 Title 都不是必须的，可以省略，但建议写上。

#### 7.1. 行内式

**语法说明：** `![图片Alt](图片地址 "图片Title")`

**代码：**



```ruby
快乐学习： 
![快乐学习](http://upload-images.jianshu.io/upload_images/1001659-7535c9e3fe16240d?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240 "快乐学习")
```

**显示效果：**

快乐学习：



![img](https:////upload-images.jianshu.io/upload_images/1001659-7535c9e3fe16240d?imageMogr2/auto-orient/strip|imageView2/2/w/600/format/webp)

快乐学习

#### 7.2. 参考式

**语法说明：**
 在文档要插入图片的地方写![图片Alt][标记]

在文档的最后写上[标记]:图片地址 "Title"

**代码：**



```ruby
快乐学习：
![快乐学习][study]

[study]:http://upload-images.jianshu.io/upload_images/1001659-7535c9e3fe16240d?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240 "快乐学习"
```

**显示效果：**
 快乐学习：

![img](https:////upload-images.jianshu.io/upload_images/1001659-7535c9e3fe16240d?imageMogr2/auto-orient/strip|imageView2/2/w/600/format/webp)

快乐学习

### 8.内容目录 

在段落中填写 `[TOC]` 以显示全文内容的目录结构。

效果参见最上方的目录

### 9. 注脚

**语法说明：**

在需要添加注脚的文字后加上脚注`[^注脚名字]`,称为加注。 然后在文本的任意位置(一般在最后)添加脚注，脚注前必须有对应的脚注名字。

注意：经测试注脚与注脚之间必须空一行，不然会失效。成功后会发现，即使你没有把注脚写在文末，经Markdown转换后，也会自动归类到文章的最后。

**代码：**



```css
使用 Markdown[^1]可以效率的书写文档, 直接转换成 HTML[^2], 你可以使用简书或者支持Markdown的编辑器进行书写。

[^1]:Markdown是一种纯文本标记语言

[^2]:HyperText Markup Language 超文本标记语言
```

**显示效果：**

使用 Markdown[[1\]](#fn1)可以效率的书写文档, 直接转换成 HTML[[2\]](#fn2), 你可以使用简书或者支持Markdown的编辑器进行书写。

**注：脚注自动被搬运到最后面，请到文章末尾查看，并且脚注后方的链接可以直接跳转回到加注的地方。**

### 10.数学公式

#### 10.1. $ 表示行内公式： 

**代码：**



```ruby
质能守恒方程可以用一个很简洁的方程式 $E=mc^2$ 来表达。
```

**显示效果：**
 质能守恒方程可以用一个很简洁的方程式 ![E=mc^2](https://math.jianshu.com/math?formula=E%3Dmc%5E2) 来表达。

#### 10.2 $$ 表示整行公式：

**代码：**



```ruby
$$\sum_{i=1}^n a_i=0$$

$$f(x_1,x_x,\ldots,x_n) = x_1^2 + x_2^2 + \cdots + x_n^2 $$

$$\sum^{j-1}_{k=0}{\widehat{\gamma}_{kj} z_k}$$
```

**显示效果：**
 ![\sum_{i=1}^n a_i=0](https://math.jianshu.com/math?formula=%5Csum_%7Bi%3D1%7D%5En%20a_i%3D0)
 ![f(x_1,x_x,\ldots,x_n) = x_1^2 + x_2^2 + \cdots + x_n^2](https://math.jianshu.com/math?formula=f(x_1%2Cx_x%2C%5Cldots%2Cx_n)%20%3D%20x_1%5E2%20%2B%20x_2%5E2%20%2B%20%5Ccdots%20%2B%20x_n%5E2)
 ![\sum^{j-1}_{k=0}{\widehat{\gamma}_{kj} z_k}](https://math.jianshu.com/math?formula=%5Csum%5E%7Bj-1%7D_%7Bk%3D0%7D%7B%5Cwidehat%7B%5Cgamma%7D_%7Bkj%7D%20z_k%7D)

访问 [MathJax](http://meta.math.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference) 参考更多使用方法。

### 11 .表格

**语法说明：**

1. 不管是哪种方式，第一行为表头，第二行分隔表头和主体部分，第三行开始每一行为一个表格行。
2. 列于列之间用管道符|隔开。原生方式的表格每一行的两边也要有管道符。
3. 第二行还可以为不同的列指定对齐方向。默认为左对齐，在-右边加上:就右对齐。

**代码：**

简单方式写表格：



```ruby
学号|姓名|分数
-|-|-
小明|男|75
小红|女|79
小陆|男|92
```

原生方式写表格：



```ruby
|学号|姓名|分数|
|-|-|-|
|小明|男|75|
|小红|女|79|
|小陆|男|92|
```

为表格第二列指定方向：



```ruby
产品|价格
-|-:
Leanote 高级账号|60元/年
Leanote 超级账号|120元/年
```

**显示效果：**
 简单方式写表格：

| 学号 | 姓名 | 分数 |
| ---- | ---- | ---- |
| 小明 | 男   | 75   |
| 小红 | 女   | 79   |
| 小陆 | 男   | 92   |

原生方式写表格：

| 学号 | 姓名 | 分数 |
| ---- | ---- | ---- |
| 小明 | 男   | 75   |
| 小红 | 女   | 79   |
| 小陆 | 男   | 92   |

为表格第二列指定方向：

| 产品           |     价格 |
| -------------- | -------: |
| 为知笔记VIP    |  60元/年 |
| 有道云笔记会员 | 198元/年 |

### 12. 分隔线

你可以在一行中用三个以上的星号、减号、底线来建立一个分隔线，行内不能有其他东西。你也可以在星号或是减号中间插入空格。下面每种写法都可以建立分隔线：

**代码：**



```undefined
* * *

***

*****

- - -

---------------------------------------
```

**显示效果都一样：**

### 13. 代码

对于程序员来说这个功能是必不可少的，插入程序代码的方式有两种，一种是利用缩进(Tab), 另一种是利用“`”符号（一般在ESC键下方）包裹代码。

**语法说明：**

1. 插入行内代码，即插入一个单词或者一句代码的情况，使用`code`这样的形式插入。
2. 插入多行代码，可以使用缩进或者``` code ```,具体看示例。

**注意： 缩进式插入前方必须有空行**

#### 13.1. 行内式

**代码：**



```cpp
C语言里的函数 `scanf()` 怎么使用？
```

**显示效果：**

C语言里的函数 `scanf()` 怎么使用？

#### 13.2. 缩进式多行代码

缩进 4 个空格或是 1 个制表符

一个代码区块会一直持续到没有缩进的那一行（或是文件结尾）。

**代码：**



```cpp
    #include <stdio.h>
    int main(void)
    {
        printf("Hello world\n");
    }
```

**显示效果：**



```cpp
#include <stdio.h>
int main(void)
{
    printf("Hello world\n");
}
```

#### 13.3. 用六个`包裹多行代码

**代码：**

\```
 \#include <stdio.h>
 int main(void)
 {
 printf("Hello world\n");
 }
 \```

**显示效果：**



```cpp
#include <stdio.h>
int main(void)
{
    printf("Hello world\n");
}
```

#### 13.4. 代码高亮

代码高亮示例:



```javascript
/**
* nth element in the fibonacci series.
* @param n >= 0
* @return the nth element, >= 0.
*/
function fib(n) {
  var a = 1, b = 1;
  var tmp;
  while (--n >= 0) {
    tmp = a;
    a += b;
    b = tmp;
  }
  return a;
}
 
document.write(fib(10));
```



```python
class Employee:
   empCount = 0
 
   def __init__(self, name, salary):
        self.name = name
        self.salary = salary
        Employee.empCount += 1
```

### 14. todo list 

代码：



```css
近期任务安排:
- [x] 整理Markdown手册
- [ ] 改善项目
   - [x] 优化首页显示方式
   - [x] 修复闪退问题
   - [ ] 修复视频卡顿
- [ ] A3项目修复
   - [x] 修复数值错误
```



效果：

近期任务安排:

- [x] 整理Markdown手册
- [ ] 改善项目
  - [x] 优化首页显示方式
  - [x] 修复闪退问题
  - [ ] 修复视频卡顿
- [ ] A3项目修复
  - [x] 修复数值错误



### 15.本md文件下载地址&markdown撰写工具下载

*可以使用Typora来撰写.md文档*

官方下载地址<https://www.typora.io/#windows>

*本md文件下载&预览地址（）:<https://github.com/immersky/MarkdownLearning/blob/main/README.md>*
*在这里看比较舒服，不会出现不支持显示效果的情况*





------

1. Markdown是一种纯文本标记语言 [↩](#fnref1)
2. HyperText Markup Language 超文本标记语言 [↩](#fnref2)





*全文参考,转载自<https://www.jianshu.com/p/8c1b2b39deb0>
