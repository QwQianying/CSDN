> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [www.runoob.com](https://www.runoob.com/python3/python3-list.html) [Python3 字符串](https://www.runoob.com/python3/python3-string.html "Python3 字符串") [Python3 元组](https://www.runoob.com/python3/python3-tuple.html "Python3 元组")

序列是 Python 中最基本的数据结构。

序列中的每个值都有对应的位置值，称之为索引，第一个索引是 0，第二个索引是 1，依此类推。

Python 有 6 个序列的内置类型，但最常见的是列表和元组。

列表都可以进行的操作包括索引，切片，加，乘，检查成员。

此外，Python 已经内置确定序列的长度以及确定最大和最小的元素的方法。

列表是最常用的 Python 数据类型，它可以作为一个方括号内的逗号分隔值出现。

列表的数据项不需要具有相同的类型

创建一个列表，只要把逗号分隔的不同的数据项使用方括号括起来即可。如下所示：

```
list1 = ['Google', 'Runoob', 1997, 2000]
list2 = [1, 2, 3, 4, 5 ]
list3 = ["a", "b", "c", "d"]
list4 = ['red', 'green', 'blue', 'yellow', 'white', 'black']
```

访问列表中的值
-------

与字符串的索引一样，列表索引从 `0` 开始，第二个索引是 `1`，依此类推。

通过索引列表可以进行截取、组合等操作。

![](https://www.runoob.com/wp-content/uploads/2014/05/positive-indexes-1.png)

```
#!/usr/bin/python3

list = ['red', 'green', 'blue', 'yellow', 'white', 'black']
print( list[0] )
print( list[1] )
print( list[2] )
```

以上实例输出结果：

```
red
green
blue
```

索引也可以从尾部开始，最后一个元素的索引为 `-1`，往前一位为 `-2`，以此类推。

![](https://www.runoob.com/wp-content/uploads/2014/05/negative-indexes.png)

```
#!/usr/bin/python3

list = ['red', 'green', 'blue', 'yellow', 'white', 'black']
print( list[-1] )
print( list[-2] )
print( list[-3] )
```

以上实例输出结果：

```
black
white
yellow
```

使用下标索引来访问列表中的值，同样你也可以使用方括号 `[]` 的形式截取字符，如下所示：

![](https://www.runoob.com/wp-content/uploads/2014/05/first-slice.png)

```
#!/usr/bin/python3

nums = [10, 20, 30, 40, 50, 60, 70, 80, 90]
print(nums[0:4])
```

以上实例输出结果：

```
[10, 20, 30, 40]
```

使用负数索引值截取：

```
#!/usr/bin/python3

list = ['Google', 'Runoob', "Zhihu", "Taobao", "Wiki"]

# 读取第二位
print ("list[1]: ", list[1])
# 从第二位开始（包含）截取到倒数第二位（不包含）
print ("list[1:-2]: ", list[1:-2])
```

以上实例输出结果：

```
list[1]:  Runoob
list[1:-2]:  ['Runoob', 'Zhihu']
```

更新列表
----

你可以对列表的数据项进行修改或更新，你也可以使用 append() 方法来添加列表项，如下所示：

```
#!/usr/bin/python3

list = ['Google', 'Runoob', 1997, 2000]

print ("第三个元素为 : ", list[2])
list[2] = 2001
print ("更新后的第三个元素为 : ", list[2])

list1 = ['Google', 'Runoob', 'Taobao']
list1.append('Baidu')
print ("更新后的列表 : ", list1)
```

**注意：**我们会在接下来的章节讨论 [append()](https://www.runoob.com/python3/python3-att-list-append.html) 方法的使用。

以上实例输出结果：

```
第三个元素为 :  1997
更新后的第三个元素为 :  2001
更新后的列表 :  ['Google', 'Runoob', 'Taobao', 'Baidu']
```

删除列表元素
------

可以使用 del 语句来删除列表中的元素，如下实例：

```
#!/usr/bin/python3
 
list = ['Google', 'Runoob', 1997, 2000]
 
print ("原始列表 : ", list)
del list[2]
print ("删除第三个元素 : ", list)
```

以上实例输出结果：

```
原始列表 :  ['Google', 'Runoob', 1997, 2000]
删除第三个元素 :  ['Google', 'Runoob', 2000]
```

**注意：**我们会在接下来的章节讨论 remove() 方法的使用

Python 列表脚本操作符
--------------

列表对 + 和 * 的操作符与字符串相似。+ 号用于组合列表，* 号用于重复列表。

如下所示：

<table><tbody><tr><th>Python 表达式</th><th>结果</th><th>描述</th></tr><tr><td>len([1, 2, 3])</td><td>3</td><td>长度</td></tr><tr><td>[1, 2, 3] + [4, 5, 6]</td><td>[1, 2, 3, 4, 5, 6]</td><td>组合</td></tr><tr><td>['Hi!'] * 4</td><td>['Hi!', 'Hi!', 'Hi!', 'Hi!']</td><td>重复</td></tr><tr><td>3 in [1, 2, 3]</td><td>True</td><td>元素是否存在于列表中</td></tr><tr><td>for x in [1, 2, 3]: print(x, end=" ")</td><td>1 2 3</td><td>迭代</td></tr></tbody></table>

Python 列表截取与拼接
--------------

Python 的列表截取与字符串操作类似，如下所示：

```
L=['Google', 'Runoob', 'Taobao']
```

操作：

<table><tbody><tr><th>Python 表达式</th><th>结果</th><th>描述</th></tr><tr><td>L[2]</td><td>'Taobao'</td><td>读取第三个元素</td></tr><tr><td>L[-2]</td><td>'Runoob'</td><td>从右侧开始读取倒数第二个元素: count from the right</td></tr><tr><td>L[1:]</td><td>['Runoob', 'Taobao']</td><td>输出从第二个元素开始后的所有元素</td></tr></tbody></table>

```
>>> L=['Google', 'Runoob', 'Taobao']
>>> L[2]
'Taobao'
>>> L[-2]
'Runoob'
>>> L[1:]
['Runoob', 'Taobao']
>>>
```

列表还支持拼接操作：

```
>>> squares = [1, 4, 9, 16, 25]
>>> squares += [36, 49, 64, 81, 100]
>>> squares
[1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
>>>
```

嵌套列表
----

使用嵌套列表即在列表里创建其它列表，例如：

```
>>> a = ['a', 'b', 'c']
>>> n = [1, 2, 3]
>>> x = [a, n]
>>> x
[['a', 'b', 'c'], [1, 2, 3]]
>>> x[0]
['a', 'b', 'c']
>>> x[0][1]
'b'
```

列表比较
----

列表比较需要引入 `operator` 模块的 `eq` 方法（详见：[Python operator 模块](https://www.runoob.com/python3/python-operator.html)）：

```
# 导入 operator 模块
import operator

a = [1, 2]
b = [2, 3]
c = [2, 3]
print("operator.eq(a,b): ", operator.eq(a,b))
print("operator.eq(c,b): ", operator.eq(c,b))
```

以上代码输出结果为：

```
operator.eq(a,b):  False
operator.eq(c,b):  True
```

Python 列表函数 & 方法
----------------

Python 包含以下函数:

<table><tbody><tr><th>序号</th><th>函数</th></tr><tr><td>1</td><td><a href="python3-att-list-len.html">len(list)</a><br>列表元素个数</td></tr><tr><td>2</td><td><a href="python3-att-list-max.html">max(list)</a><br>返回列表元素最大值</td></tr><tr><td>3</td><td><a href="python3-att-list-min.html">min(list)</a><br>返回列表元素最小值</td></tr><tr><td>4</td><td><a href="python3-att-list-list.html">list(seq)</a><br>将元组转换为列表</td></tr></tbody></table>

Python 包含以下方法:

<table><tbody><tr><th>序号</th><th>方法</th></tr><tr><td>1</td><td><a href="python3-att-list-append.html">list.append(obj)</a><br>在列表末尾添加新的对象</td></tr><tr><td>2</td><td><a href="python3-att-list-count.html">list.count(obj)</a><br>统计某个元素在列表中出现的次数</td></tr><tr><td>3</td><td><a href="python3-att-list-extend.html">list.extend(seq)</a><br>在列表末尾一次性追加另一个序列中的多个值（用新列表扩展原来的列表）</td></tr><tr><td>4</td><td><a href="python3-att-list-index.html">list.index(obj)</a><br>从列表中找出某个值第一个匹配项的索引位置</td></tr><tr><td>5</td><td><a href="python3-att-list-insert.html">list.insert(index, obj)</a><br>将对象插入列表</td></tr><tr><td>6</td><td><a href="python3-att-list-pop.html">list.pop([index=-1])</a><br>移除列表中的一个元素（默认最后一个元素），并且返回该元素的值</td></tr><tr><td>7</td><td><a href="python3-att-list-remove.html">list.remove(obj)</a><br>移除列表中某个值的第一个匹配项</td></tr><tr><td>8</td><td><a href="python3-att-list-reverse.html">list.reverse()</a><br>反向列表中元素</td></tr><tr><td>9</td><td><a href="python3-att-list-sort.html">list.sort(key=None, reverse=False)</a><br>对原列表进行排序</td></tr><tr><td>10</td><td><a href="python3-att-list-clear.html">list.clear()</a><br>清空列表</td></tr><tr><td>11</td><td><a href="python3-att-list-copy.html">list.copy()</a><br>复制列表</td></tr></tbody></table>