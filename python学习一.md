# python学习一

## 字符串

```

1. string.capitalize() 把字符串的第一个字符大写

2.string.center(width) 返回一个原字符串居中,并使用空格填充至长度 width 的新字符串

3. string.count(str, beg=0,
end=len(string)) 返回 str 在 string 里面出现的次数，如果 beg 或者 end 指定则返回指定范围内 str 出现的次数

4. string.decode(encoding='UTF-8',
errors='strict') 以 encoding 指定的编码格式解码 string，如果出错默认报一个
ValueError 的 异 常 ， 除 非 errors 指 定 的 是 'ignore' 或 者
'replace'

5. string.encode(encoding='UTF-8',
errors='strict')a 以 encoding 指定的编码格式编码 string，如果出错默认报一个ValueError 的异常，除非 errors 指定的是'ignore'或者'replace'
/ decode()是解码，decode('utf-8')表示 把utf-8的解码成unicode。
/python3.X中 str就是unicode

6. string.endswith(obj, beg=0,
end=len(string))b,e检查字符串是否以 obj 结束，如果 beg 或者 end 指定则检查指定的范围内是否以 obj 结束， 如果是， 返回 True,否则返回 False.

7.string.expandtabs(tabsize=8)把字符串 string 中的 tab 符号转为空格， 默认的空
格数 tabsize 是 8.

8. string.find(str, beg=0,
end=len(string)) 检测 str 是否包含在 string 中，如果 beg 和 end 指定范围，
则检查是否包含在指定范围内，如果是返回开始的索引值，否则
返回-1

9. string.index(str, beg=0,
end=len(string)) 跟 find()方法一样，只不过如果 str 不在 string 中会报一个异常.

10. string.isalnum()a, b, c R 如果 string 至少有一个字符并且所有字符都是字母或数字则返
回 True,否则返回 False

11. string.isalpha()a, b, c 如果 string 至少有一个字符并且所有字符都是字母则返回 True,
否则返回 False
12. string.isdecimal()b, c, d 如果 string 只包含十进制数字则返回 True 否则返回 False.# 后开被删了？2.7.10没这个啊。

13. string.isdigit()b, c 如果 string 只包含数字则返回 True 否则返回 False.

14. string.islower()b, c 如果 string 中包含至少一个区分大小写的字符，并且所有这些(区分
大小写的)字符都是小写，则返回 True，否则返回 False

15. string.isnumeric()b, c, d 如果 string 中只包含数字字符，则返回 True，否则返回 False

16. string.isspace()b, c 如果 string 中只包含空格，则返回 True，否则返回 False.

17. string.istitle()b, c 如果 string 是标题化的(见 title())则返回 True，否则返回 False

20. string.isupper()b, c 如果 string 中包含至少一个区分大小写的字符， 并且所有这些(区分
大小写的)字符都是大写，则返回 True，否则返回 False

21. string.join(seq) Merges (concatenates)以 string 作为分隔符，将 seq 中所有的元素
(的字符串表示)合并为一个新的字符串 

22. string.ljust(width)返回一个原字符串左对齐,并使用空格填充至长度 width 的新字符串

23. string.lower() 转换 string 中所有大写字符为小写.

24. string.lstrip() 截掉 string 左边的空格

25. string.partition(str)e 有点像 find()和 split()的结合体,从 str 出现的第一个位置起,
把 字 符 串 string 分 成 一 个 3 元 素 的 元 组
(string_pre_str,str,string_post_str),如果 string 中不包含
str 则 string_pre_str == string.

26. string.replace(str1, str2,
num=string.count(str1))把 string 中的 str1 替换成 str2,如果 num 指定，
则替换不超过 num 次.

27. string.rfind(str, beg=0,end=len(string))类似于 find()函数， 不过是从右边开始查
找.

28. string.rindex( str, beg=0,end=len(string)) 类似于 index()， 不过是从右边开始.

29. string.rjust(width)返回一个原字符串右对齐,并使用空格填充至长度 width 的新字符串

30. string.rpartition(str)e 类似于 partition()函数,不过是从右边开始查找.

31. string.rstrip()删除 string 字符串末尾的空格.

32. string.split(str="", num=string.count(str)) 以 str 为分隔符切片 string，如果 num
有指定值，则仅分隔 num 个子字符串

33. string.splitlines(num=string.count('\n'))b, c 按照行分隔， 返回一个包含各行作为元素
的列表， 如果 num 指定则仅切片 num 个
行.

34. string.startswith(obj, beg=0,end=len(string))b, e检查字符串是否是以 obj 开头，是则返回 True，否则返回 False。如果
beg 和 end 指定值，则在指定范围内
Edit By Vheavens
Edit By Vheavens
检查.

35. string.strip([obj]) 在 string 上执行 lstrip()和 rstrip()

36. string.swapcase() 翻转 string 中的大小写

37. string.title()b, c 返回"标题化"的 string,就是说所有单词都是以大写开始，其余
字母均为小写(见 istitle())

38. string.translate(str, del="") 根据 str 给出的表(包含 256 个字符)转换 string 的字符,
要过滤掉的字符放到 del 参数中

39. string.upper() 转换 string 中的小写字母为大写

40. string.zfill(width) 返回长度为 width 的字符串，原字符串 string 右对齐，前面填充
0
```







## 列表

```

```



