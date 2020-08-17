## 变量
变量的命名和使用
*在Python中使用变量时，需要遵守一些规则和指南。违反这些规则将引发错误，而指南旨在让你编写的代码更容易阅读和理解。请务必牢记下述有关变量的规则。*

- 变量名只能包含字母、数字和下划线。变量名可以字母或下划线打头，但不能以数字打头，例如，可将变量命名为message_1，但不能将其命名为1_message。
- 变量名不能包含空格，但可使用下划线来分隔其中的单词。例如，变量名greeting_message可行，但变量名greetingmessage会引发错误。
- 不要将Python关键字和函数名用作变量名，即不要使用Python保留用于特殊用途的单词，如print
- 变量名应既简短又具有描述性。例如，name比n好，student_name比s_n好，name_length比length_of_persons_name好。
- 慎用小写字母l和大写字母O，因为它们可能被人错看成数字1和0。
> 注意 就目前而言，应使用小写的Python变量名。在变量名中使用大写字母虽然不会导致错误，但避免使用大写字母是个不错的主意。

字符串操作函数
- string.title()  将一个字符串改变成标题形式(首字母大写)。 fh kong->Fh Kong
- string.upper()  改变成大写
- string.lower()  改变成小写

删除空白  
- string.strip()  删除一个字符串首尾无用的空白
- string.lstrip() 删除一个字符串开头无用的空白
- string.rstrip() 删除一个字符串尾部无用的空白

> 实际程序中，对于检测去除用户输入中的无用字符很有效。

分割
- string.split()  用空格将字符串分割,返回包含所有单词的列表


列表 `[]`  适合于程序运行过程中变化的数据集
列表由一系列按特定顺序排列的元素组成。你可以创建包含字母表中所有字母、数字0~9或所有家庭成员姓名的列表；也可以将任何东西加入列表中，其中的元素之间可以没有任何关系。鉴于列表通常包含多个元素，给列表指定一个表示复数的名称（如letters 、digits 或names ）是个不错的主意。

访问 list[idx]
- 索引从0开始
- 访问最后一个元素也可以用索引-1，在不知道列表长度的情况下，访问最后一个元素

增加
- list.append(element)  添加到列表的尾部
- list.insert(idx,element)  插入新元素的索引和内容

删除
- del list[idx]  删除索引为idx的元素，无法引用
- element = list.pop() 从列表末尾删除一个元素并引用它
- element = list.pop(idx)  从列表删除索引为idx的元素并引用它
- remove(value)  从列表中删除第一次出现的value（根据元素的值删除）

> del 和 pop()的区别在于，从列表中删除后，是否引用它。

排序
- list.sort(reverse=False) 默认对列表正序排序，改变了原列表的顺序
- sorted(list,reverse=False)  临时输出正序列表，不改变原列表的顺序

反序
- list.reverse()  反序整个列表

长度
- len(list)  获取列表的长度

切片
- list[i:j]  访问列表中i到j的元素
- list[:j]   从头开始到j
- list[i:]   从i开始到末尾

检查
- item in list  判断item是否在list中，返回True或者False
- item not in list  判断item是否在list中，返回True或者False



数字列表
创建
- numbers = list(range(start,end,step))

针对数字列表操作的函数
- min(list)  返回列表最小元素
- max(list)  返回列表最大元素
- sum(list)  对列表求和


元组`()` 定义不可改变数据集
(1,2)


字典 `{}` 键值对  
每个键 都与一个值相关联，你可以使用键来访问与之相关联的值。  
与键相关联的值可以是数字、字符串、列表乃至字典。事实上，可将任何Python对象用作字典中的值。   

访问
- dict['key']  返回字典中与key相关联的值

添加
- dict['key'] = value  直接添加键值对 key:value

修改
- dict['key'] = value

删除
- del dict['key']  永远删除键值对key:value

遍历
- for key,value in dict.items() 遍历所有的键值对
- dict.keys()   返回的是一个键列表，可执行sorted函数排序
- dict.values() 返回一个值列表，可能会有重复项，若要去掉重复项可用set(list) 集合去掉，不会改变原来的List

> 注意：字典和列表可以相互嵌套，字典也可以嵌套字典  

```python
student1 = {'name':'kong','id':1}
student2 = {'name':'fan','id':2}
student2 = {'name':'hao','id':3}

student = [student1,student2,stuedet3]
```

```python
student = {
    'kong':['c++','Python'],
    'fan' :['C','matlab'],
    'hao' :['verilog','java']
}
```
```python
student = {
    'kong':{
        'id':1,
        'language':c++,
    },
    'fan':{
        'id':2,
        'language':python,
    }
}
```



输入
- input()
函数input() 让程序暂停运行，等待用户输入一些文本。获取用户输入后，Python将其存储在一个变量中，以方便你使用。  
函数input() 接受一个参数：即要向用户显示的提示 或说明，让用户知道该如何做。  

> 注意：input()函数输入默认是str类型


while value in list: 只要value在list中就循环操作
    do something

while list:  只要列表不空，就循环操作
    do something  


类的操作 略
构造函数__init__(self)
继承
实例化
类中实例化类
取其精华去其糟粕
python 标准库


函数名字的书写用带含义的小写字母 function_name
类的名字书写第一个字母用大写

驼峰命名法

文件和异常
1.open() & close() 和with open() as name:
关键字with在不需要访问文件后将其关闭，用这种方式可以不使用close()函数
使用open()和close()这种方式时，当程序健壮性不够时，不能及时的关闭文件夹，可能导致文件的数据损坏。
所以尽可能的还是使用with open(fileurl) as name:这种方式

函数
- file.read()  读取文件的全部内容（读到文件末尾时会返回一个空字符串）
- file.readlines() 逐行读入文本内容，返回到列表中

> 读取文本文件时，Python将其中的所有文本都读为字符串

写入文件
- open(fileurl,'w') : 普通写入 
- open(fileurl,'a') : 追加写入
- open(fileurl,'r') : 读取文件
- open(fileurl,'r+'): 读取和写入文件



异常
使Python在出现异常时依然能够继续运行
`try-except`代码块处理
try中只放可能引起异常的代码。
1. ZeroDivisionError异常
```python
a = 1
b = 0
try:
    c = a/b
except ZeroDivisionError:
    print("ZeroDivisionError")
else:
    #只有try成功执行后的代码放在else里面
```
2. FileNotFoundError异常
```python
filename = 'fhkong.txt'

try:
    with open(filename,'r') as file_obj:
        contents = file_obj.read()
except FileNotFoundError:
    msg = "Sorry,the file "+filename + " does not exist."
    print(msg)
```


JSON 数据格式 略


测试代码
编写函数或类时，还可为其编写测试。通过测试，可确定代码面对各种输入都能够按要求的那样工作。测试让你信心满满，深信即便有更多的人使用你的程序，它也能正确地工作。在程序中添加新代码时，你也可以对其进行测试，确认它们不会破坏程序既有的行为.
Python的`unittest`库





