# 四-os模块的使用-创建指定大小的文件



## 话不多说直接贴代码：

```
# coding: utf-8
import os

def create_file(path,size):
    file = open(path,'w')            # 打开一个文件
    file.seek(1024*1024*1024*size)   #定位到1024*1024*1024*size字节，这样就可以创建出sizeGB的文件
    file.write('\x00')               #一定要写入一个字符，否则无效
    file.close()

create_file('testfile2G',2)         

```

###  关于os 的其他函数

```

os.chdir('E://testfile')  #切换目录
os.mkdir('./test10_2G')   #创建文件夹

```

