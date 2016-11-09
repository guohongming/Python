# python学习二

## 一些常用函数



```
1.cmp()
内建函数 cmp()用于比较两个对象 obj1 和 obj2， 如果 obj1 小于 obj2, 则返回一个负整
数，如果 obj1 大于 obj2 则返回一个正整数， 如果 obj1 等于 obj2， 则返回 0。它的行为非常
类似于 C 语言的 strcmp()函数。比较是在对象之间进行的，不管是标准类型对象还是用户自定
义对象。如果是用户自定义对象， cmp()会调用该类的特殊方法__cmp__()。在第 13 章会详细
介绍类的这些特殊方法。下面是几个使用 cmp()内建函数的对数值和字符串对象进行比较的例
子。
>>> a, b = -4, 12
>>> cmp(a,b)
-1
>>> cmp(b,a)
1
>>> b = -4
>>> cmp(a,b)
0
>>>
>>> a, b = 'abc', 'xyz'
>>> cmp(a,b)
-23
>>> cmp(b,a)
23
>>> b = 'abc'
>>> cmp(a,b)
0

2.str()和 repr() (及 `` 运算符)
内建函数 str() 和 repr() 或反引号运算符(``) 可以方便的以字符串的方式获取对象的
内容、类型、数值属性等信息。str()函数得到的字符串可读性好， 而 repr()函数得到的字符
串通常可以用来重新获得该对象, 通常情况下 obj == eval(repr(obj)) 这个等式是成立的。
这两个函数接受一个对象做为其参数， 返回适当的字符串。在下面的例子里， 我们会随机取
一些 Python 对象来查看他们的字符串表示。
>>> str(4.53-2j)
'(4.53-2j)'
>>>
>>> str(1)
'1'
>>>
>>> str(2e10)
'20000000000.0'
>>>
>>> str([0, 5, 9, 9])
'[0, 5, 9, 9]'
>>>
>>> repr([0, 5, 9, 9])
'[0, 5, 9, 9]'
>>>
>>> `[0, 5, 9, 9]`
'[0, 5, 9, 9]'


3.type() 和 isinstance()
type()返回对象的类型
isinstance（）  

4.abs()
	abs() 返回绝对值
	
5.pow() 和**
	指数运算
	
6.enumerate（）
	enumerate（） 将一个iter 变成一个 带index 的 iter
	
7.len()
	返回长度
	
8.zip（）
	>>> s, t = 'foa', 'obr'
	>>> zip(s, t)
	[('f', 'o'), ('o', 'b'), ('a', 'r')]
	
9.sorted() and reversed()
>>> s = ['They', 'stamp', 'them', 'when', "they're", 'small']
>>> for t in reversed(s):
... print t,
...
small they're when them stamp They
>>> sorted(s)
['They', 'small', 'stamp', 'them', "they're", 'when']
初学者使用字符串， 应该注意是如何把单引号和双引号的使用矛盾和谐掉.同时还要注意字
符串排序使用的是字典序,而不是字母序(字母'T'的 ASCII 码值要比字母'a'的还要靠前)

10.sum()
>>> a = [6, 4, 5]
>>> reduce(operator.add, a)
15
>>> sum(a)
15
>>> sum(a, 5)
20
>>> a = [6., 4., 5.]
>>> sum(a)
15.0


11.
List Method Operation
list.append(obj) 向列表中添加一个对象 obj
list.count(obj) 返回一个对象 obj 在列表中出现的次数
list.extend(seq)a 把序列 seq 的内容添加到列表中
list.index(obj, i=0,
j=len(list)) 返回 list[k] == obj 的 k 值,并且 k 的范围在 i<=k<j;否则
引发 ValueError 异常.
list.insert(index, obj) 在索引量为 index 的位置插入对象 obj.
list.pop(index=-1)a 删除并返回指定位置的对象,默认是最后一个对象
list.remove(obj) 从列表中删除对象 obj
list.reverse() 原地翻转列表
list.sort(func=None,key=None,reverse=False)b 以指定的方式排序列表中的成员,如果 func 和 key 参数指定,
则按照指定的方式比较各个元素,如果 reverse 标志被置为
True,则列表以反序排列.
>>> music_media = [45]
>>> music_media
[45]
>>>
>>> music_media.insert(0, 'compact disc')
>>> music_media
['compact disc', 45]
>>>
>>> music_media.append('long playing record')
>>> music_media
['compact disc', 45, 'long playing record']
>>>
>>> music_media.insert(2, '8-track tape')
>>> music_media
['compact disc', 45, '8-track tape', 'long playing record']
在前面的例子中,我们用一个元素初始化了一个列表,然后当向列表插入元素，或在尾部追
加新的元素后，都会去检查这个列表.现在确认一下一个值是否在我们的列表中,并看看如何找
出元素在列表中的索引值.我们用 in 操作符和 index()方法实现这两个需求.
>>> 'cassette' in music_media
False
>>> 'compact disc' in music_media
True
>>> music_media.index(45)
1
>>> music_media.index('8-track tape')
2
>>> music_media.index('cassette') Traceback (innermost last):
File "<interactive input>", line 0, in ? ValueError: list.index(x): x not in list
噢！最后一个例子怎么出错了?呃，看起来用 index()来检查一个元素是否存在于一个 list
中并不是个好主意,因为我们出错了.应该先用 in 成员关系操作符(或者是 not in)检查一下,然
后在用 index()找到这个元素的位置。我们可以把最后几个对 index()调用放到一个单独的 for
循环里面,像这样:
for eachMediaType in (45, '8-track tape', 'cassette'):
if eachMediaType in music_media:
print music_media.index(eachMediaType)
这个方案避免了我们上面犯的错误,因为在确认一个元素属于该列表之前 index()方法是不
会被调用的.稍后我们将会发现该如何处理这种错误,而不是这样的一出错，程序就崩溃了。
接下来我们测试 sort()和 reverse()方法,它们会把列表中的元素排序,然后翻转.
>>> music_media
['compact disc', 45, '8-track tape', 'long playing record']
>>> music_media.sort()
>>> music_media
[45, '8-track tape', 'compact disc', 'long playing record']
>>> music_media.reverse()
>>> music_media
['long playing record', 'compact disc', '8-track tape', 45]


```

