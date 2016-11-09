# python 学习三

## 字典



```
方法名字 操作
dict.cleara() 删除字典中所有元素
dict.copya() 返回字典(浅复制)的一个副本
dict.fromkeysc(seq,
Edit By Vheavens
Edit By Vheavens
val=None) c 创建并返回一个新字典，以 seq 中的元素做该字典的键，val 做该字
典中所有键对应的初始值(如果不提供此值，则默认为 None)
dict.get(key,
default=None)a 对字典 dict 中的键 key,返回它对应的值 value，如果字典中不存在此
键，则返回 default 的值(注意，参数 default 的默认值为 None)
dict.has_key(key) 如果键(key)在字典中存在， 返回 True， 否则返回 False. 在 Python2.2
版本引入 in 和 not in 后，此方法几乎已废弃不用了，但仍提供一个
可工作的接口。
dict.items() 返回一个包含字典中(键, 值)对元组的列表
dict.keys() 返回一个包含字典中键的列表
dict.iter()d 方法 iteritems(), iterkeys(), itervalues()与它们对应的非迭代方法
一样，不同的是它们返回一个迭代子，而不是一个列表。
dict.popc(key
[, default]) c 和方法 get()相似，如果字典中 key 键存在，删除并返回 dict[key]，
如果 key 键不存在，且没有给出 default 的值，引发 KeyError 异常。
dict.setdefault(key,
default=None)e 和方法 set()相似，如果字典中不存在 key 键，由 dict[key]=default 为
它赋值。
dict.update(dict2)a 将字典 dict2 的键-值对添加到字典 dict
dict.values() 返回一个包含字典中所有值的列表
```

