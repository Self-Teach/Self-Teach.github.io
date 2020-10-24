<center><font face="黑体" size=12 color=green>Python基础知识简要概述</font></center>

# Python Introduce
1. python 是一种**解释型、面向对象**的语言，由Guido van Rossum于1989年发明，1991年正式公布；其官网地址为：[www.python.org](https://www.python.org/)
2. python特性：可读性强、简洁、面向对象、免费开源、可 移植性和跨平台、丰富的库、可扩展性等。
    ```
    python是基于 C 语言开发的。
    ```
3. python应用范围：科学计算、人工智能、web服务端和大型网站、GUI开发（图形用户界面开发）、游戏开发、移动设备、嵌入设备、系统运维、大数据、云计算等。
4. python是解释性语言，性能较低。
5. python版本包含：python2 和 python3 (新学python建议用python3)。
6. python解释器：CPython（用C语言实现），Jython（用Java实现），IronPython（.NET 平台上使用的解释器），PyPy（使用python实现的解释器）。

# Python Downloads and Install
7. python下载地址：[https://www.python.org/downloads](https://www.python.org/downloads)
8. python的安装：通过下载的exe文件 (如python-3.7.3-amd64.exe) 安装即可，基本上一直点下一步就可以了。
    ```
    注意：
        1. 安装中出现Advanced Options时勾选上Add Python to environment variables选项；以免后期在手动添加到环境变量；
        2. python可以安装在自己指定的文件夹下；
        3. python安装好后，通过 cmd 输入 python 就可进入 python 环境。
    ```

# IDE
9. IDE：开发环境（Integrated Development Environment 集成开发环境）
10. 常用的开发环境：IDLE、Pycharm、wingIDE、Eclipse、IPython
11. IDLE是Python官方的标准开发环境，安装好Python后就有可以使用，直接在其中输入代码即可运行调试。
    ```python
    print("hello world!")
    ```

# Basic Introduce
12. python程度基本格式
    1. 恰当的空格，缩进问题：行首的空白决定逻辑缩进层次，决定分组；语句从新行的第一列开始；统一缩进风格；
    2. Python区分大小写；
    3. 注释：行注释用 # ；段注释用 '''xxx'''； 
    4. [PEP-8](https://www.python.org/dev/peps/pep-0008/)官方推荐代码风格；
    5. 代码需要多行输写时使用 \ 行连接符。
13. 学习方法：守、破、离；实战。建立体系为先，不事事求完美。
14. python程度的构成：
    1. python由模块组成；
    2. python程度按模块中的顺序运行。
15. 对象
    1. python中一切均对象；
    2. 对象本质就是一个内在块、拥有特定的值，支持特定类型的相关操作；
    3. 每个对象由：标识（identity）、类型（type）、值（value）组成。
        ```python
        >>> a = 3
        >>> a
        # 3
        >>> id(3)
        # 140724412375760
        >>> type(3)
        # <class 'int'>
        >>> id(a)
        # 140724412375760
        >>> type(a)
        # <class 'int'>
        ```
16. 引用
    1. python中，变量也成为对象的引用，变量存储的就是对象的地址，变量通过地址引用对象；
    2. 变量  位于 **栈** 内存中；对象  位于 **堆** 内存中。
    3. python是动态类型语言，不需要显式声明类型；
    4. python是强类型语言。
17. 标识符
    1. 标识符用于变量、类、模块等的名称；
    2. 区分大小写；
    3. 以字母、下划线开关，其后的字符是字母、数据、下划线；
    4. 不能使用关键字；
    5. 以双下划线开头和结尾的通常有特殊用法，尽量避免这样写；
    6. python标识符命名规则：
        1. 模块名和包名：全小写，尽量简单，多个单词之间用下划线隔开；
        2. 函数名：全小写字母，多个单词之间用下划线隔开；
        3. 类名：首字母大写，采用驼峰原则；
        4. 常量名：全大写字母，多个单词用下划线隔开。
18. 变量声明和赋值
    ```python
    a = 9
    ```
    1. 删除变量： del a 语句；
    2. 垃圾回收机制：对象没有变量引用时，就会清空内存；
    3. 链式赋值：x=y=123 相当于：x=123; y=123 赋值方法；
    4. 系列解包赋值：a, b, c = 4, 5, 6 相当于 a=4, b=5, c=6 赋值方法。
19. 常量
    1. python不支持常量，即没有语法规则限制改变一个常量的值；只能约定常量的命名规则，在程度逻辑上对常量的值不作修改。

# Data
20. 基本的python内置数据类型
    1. 整型
        1. 使用int()实现类型转换，直接将小数部分去掉；
        2. 自动转型：整数和浮点数混合运算时，结果自动转换成浮点数。
    2. 浮点型（float）
        1. 使用float()将其他类型转化为浮点型；
        2. round(value)可以返回四舍五入的值，该方法不改变原值。
    3. 布尔型
        1. 真 True
        2. 假 False
    4. 字符串型
        1. 字符串本质上是字符序列；python的字符串是不可变的；
        2. 字符串编码：python3字符默认16位Unicode编码，ASCII码是Unicode的子集；
        3. ord()函数可以把字符转换成对应的Unicode码；chr()函数把十进制数转换成对应的字符。
        4. 单引号 和 双引号 创建字符串
            ```python
            >>> a = "I'm a student"
            >>> a
            # "I'm a student"
            >>> b = 'my name is "Tom"'
            >>> b
            # 'my name is "Tom"'
            # 用三个单引号 或 三个双引号 创建多行字符串
            ```
        5. 空字符串和len()函数
            ```python
            >>> c = ''
            >>> c
            # ''
            >>> len(c)
            # 0
            ```
        6. 转义字符
            ```python
            # \ 续行符、 \\ 反斜杠符号、 \' 单引号、 \" 双引号
            # \b 退格、 \n 换行、 \t 横向制表符、 \r 回车
            ```
        7. 字符串拼接
            1. 使用 + 将字符串拼接起来；
            2. 也可以将多个字符串直接放在一起拼接；
            2. 如果 + 两边都是字符串，则拼接；
            3. 如果 + 两边都是数字，则加法运算；
            4. 如果 + 两边类型不同，则异常。
        8. 字符串复制
            1. 使用 * 实现字符串复制
            ```python
            >>> a = 'rogy  ' * 3
            >>> a
            # 'rogy  rogy  rogy  '
            ```
        9. 不换行打印
            1. python中调用print()会自动打印一个换行符；
            2. 通过参数 end='任意字符串' 实现末尾添加内容。
            ```python
            >>> print('rogy', end='*')
            >>> print('rogy', end='&&')
            >>> print('rogy')
            # rogy*rogy&&rogy
            ```
        10. 使用```input()```从控制台读取输入的内容
        11. 使用[]提取字符
            1. 字符串本质是字符序列；
            2. 正向从0 到 len(str)-1 对应每个字符的序列号；
            3. 反向从-1 到 -len(str)对应每个字符的序列号。
                ```python
                >>> a= 'adaffknenfe'
                >>> a[0]
                # 'a'
                >>> a[-2]
                # 'f'
                ```
        12. ```replace()```实现字符串替换
            1. 字符串是不可改变的；
            2. ```replace()```对某个字符改变是生成了新的字符串。
                ```python
                >>> a = 'abcdefg'
                >>> a.replace('c', '刘')
                # 'ab刘defg'
                >>> a
                # 'abcdefg'
                ```
        13. 字符串切片```slice```操作
            1. 标准格式：[起始偏移量start:终止偏移量end:步长step]，注意起始与终止偏移量范围；
            2. [:] 提取整个字符串；
            3. [start:] 从start开始到结尾；
            4. [:end] 从头开始到end-1, 不含最后一个；
            5. [start:end] 从start到end-1；
            6. [start:end:step] 从start到end-1，步长step。
                ```python
                >>> a = 'abcdefghigklmn'
                >>> a[2]
                # 'c'
                >>> a[1:5]
                # 'bcde'
                >>> a[1:5:2]
                # 'bd'
                >>> a[-3:]
                # 'lmn'
                >>> a[::-1]
                # 'nmlkgihgfedcba'
                ```
        14. 分割```split()```和合并```join()```
            ```python
            # split()为分割字符串
            >>> a = "to be or not to be"
            >>> a.split() # 默认为按空格分割
            # ['to', 'be', 'or', 'not', 'to', 'be']
            >>> a.split('be')
            # ['to ', ' or not to ', '']
            ```
            ```python
            # join()为拼接字符串
            >>> a = ['rogy', 'ray', 'tom']
            >>> '*'.join(a)
            # 'rogy*ray*tom
            ```

            ```python
            import time

            time1 = time.time()
            a = ""
            for i in range(100000):
                a += "str"

            time2 = time.time()
            print('run time: ' + str(time2 - time1))

            time3 = time.time()
            li = []
            for i in range(100000):
                li.append('str')

            a = "".join(li)
            time4 = time.time()

            print('run time: ' + str(time4 - time3))

            # result 二者效率不同
            # run time: 0.06981348991394043
            # run time: 0.03590226173400879
            ```
        15. 字符串驻留机制
            1. 字符串驻留：仅保留一份相同且不可变字符串的方法，不同的值存放在字符串驻留池中；
            2. python对于符合标识符规则的字符串(仅包含下划线、字母和数字)会启用字符串驻留机制。
                ```python
                >>> a = 'abd_33'
                >>> b = 'abd_33'
                >>> a is b
                # True
                >>> c = 'dd#'
                >>> d = 'dd#'
                >>> c is d
                # False
                >>> str = 'aa'
                >>> str1 = 'aa'
                >>> str2 = 'bb'
                >>> str1 + str2 is 'aabb'
                # False
                ```
        16. 字符串比较
            1. 使用 == ，！= 对字符串是否含有相同的字符进行比较；
            2. 使用is、not is 判断两个对象是否同一个对象，比较的是对象的地址；
            3. 成员操作符：in、not in 查询某个字符是否在字符串中。
        17. 常用查找方法
            1. len(str)
            2. str.startswith('xx')
            3. str.endwith('xx')
            4. str.find('xx')
            5. str.rfind('xx') 最后一次出现指定字符串的位置
            6. str.count('xx')
            7. str.isalnum()
        18. 去除首尾信息
            1. ```strip("xx")```去除首尾指定信息，默认去除空格；
            2. ```lstrip()```去除左边信息；
            3. ```rstrip()```去除右边信息。
        19. 大小写转换
            1. str.capitalize() 产生新的字符串，首字母大写；
            2. str.title() 产生新的字符串，每个单词首字母大写；
            3. str.upper() 产生新的字符串，所有字母大写；
            4. str.lower() 产生新的字符串，所有字母小写；
            5. str.swapcase() 产生新的字符串，所有字母大小写互换。
        20. 格式排版
            1. center() 居中；
            2. ljust() 左对齐；
            3. rjust() 右对齐。
        21. str()实现将数字等类型转型为字符串类型
        22. 字符串格式化
            1. format() 基本用法：接受不限个数参数，位置可以不按顺序。
                ```python
                >>> a = "name is: {0}, age is: {1}"
                >>> a.format('rogy', 27)
                # 'name is: rogy, age is: 27'
                >>> b = "name is: {0}, age is: {1}, {0} is a good man"
                >>> b.format('ray', 28)
                # 'name is: ray, age is: 28, ray is a good man'
                >>> c = "name is: {name}, age is: {age}"
                >>> c.format(age = 28, name = 'Ray')
                # 'name is: Ray, age is: 28'
                ```
            2. 填充与对齐
                ```python
                # ^、<、>分别是居中、左对齐、右对齐，后面带宽度
                # ：后面带填充的字符，只能是一个字符，不指定就默认空格
                >>> c.format(age = 28, name = 'Ray')
                # 'name is: Ray, age is: 28'
                >>> "{:*>8}".format('245')
                # '*****245'
                >>> "I am {0}, I like number{1:*^8}".format('Ray', '666')
                # 'I am Ray, I like number**666***'
                ```
            3. 数字格式化
                1. 浮点数通过 f 、整数通过 d 进行需要的格式化
                    ```python
                    >>> a = "my name is {0}, I have money {1:.2f}"
                    >>> a.format('Ray', 1256.235489)
                    # 'my name is Ray, I have money 1256.24'
                    >>> b = 3.1415926
                    >>> "{:+.2f}".format(b)
                    # '+3.14'
                    >>> "{:.0f}".format(b)
                    # '3'
                    >>> "{:0>2d}".format(5)
                    # '05'
                    >>> "{:0<4d}".format(5)
                    # '5000'
                    >>> "{:,}".format(1000000)
                    # '1,000,000'
                    >>> "{:.2%}".format(0.25)
                    # '25.00%'
                    >>> "{:.2e}".format(10000000)
                    # '1.00e+07'
                    >>> "{:10d}".format(13)
                    # '        13'
                    >>> "{:<10d}".format(13)
                    # '13        '
                    >>> "{:^10d}".format(13)
                    # '    13    '
                    ```

    5. 赋值运算
        ```python
        # +  -  *  /浮点除  %取余  //整除  ** 幂运算
        a += 1
        a = a + 1
        a -= 1
        a = a - 1
        # 比较运算符
        # == 、!= 、 > 、< 、>= 、<=
        # 逻辑运算符
        # or 逻辑或、 and 逻辑与、 not 逻辑非 
        # |  ^  & : 按位或，按位异或、按位与
        # << 、>> 移位
        '''
        x or y: x 为true, 则不计算y，直接返回true; x为false, 则返回y值。
        x and y: x 为true, 则返回y值; x为false, 则不计算y，直接返回false。
        not x: x 为true, 则返回false; x为false，返回true。
        '''
        # 同一运算符
        # is : 判断两个标识符是不是引用同一个对象
        # is not : 判断两个标识符是不是引用不同对象
        # is 与 == 区别: 
        # is判断两个变量引用对象是否为同一个，比较的是对象的地址；
        # == 用于判断引用变量对象的值是否相等，默认调用对象的__eq__()方法。
        >>> a = 1000
        >>> b = 1000
        >>> a == b
        True
        >>> a is b
        False
        >>> id(a)
        2561693013424
        >>> id(b)
        2561693012048
        ```
        [整数缓存问题](http://www.manongjc.com/article/55314.html)：是对比较小的整数对象进行缓存，[-5,256]范围是在命令行中执行时的数据缓存范围；在Pycharm或者保存文件中执行时，因为解释器做了一部分优化，范围是[-5,任意正整数]。
    6. 时间的表示
        1. 计算机中时间的表示是从1970年1月1日 00:00:00（unix时间点）开始，以毫秒进行计算；
        2. ```python```中使用```time.time()```获得当前时刻，返回的值是以秒为单位，带微秒精度的浮点值。
            ```pyton
            >>> import time
            >>> time.time()
            1602314627.59237
            ```
    7. 运算符优先级
        1. 乘除优先加减
        2. 位运算和算术运算 > 比较运算符 > 赋值运算符 > 逻辑运算符

# Sequence
21. python中序列结构有：字符串，列表，元组，字典，集合。  
        <img src="./Pictures/sequence.png">
22. 列表：用于存储任意数目、任意类型的数据集合
    1. 列表的创建方法
        1. ```a = [20, 30, 'ray']```
        2. list() 创建 ```a = list('rafafjk')```
        3. ```range()```创建整数列表：```list(range(3, 15, 2))```
        4. 推导式创建列表：```a = [x*2 for x in range(5)]```
    2. 列表的相关方法
        1. list.append(x) 尾部添加元素x，直接修改原列表，不创建新列表对象；
        2. list.extend(aList) 将列表aList所有元素添加互list尾部，直接修改原列表，不创建新列表对象；
        3. list.insert(index, x) 在列表list指定位置插入元素 X ；
        4. list.remove(x) 删除**首次**出现的元素x，不存在抛出异常;
        5. list.pop([index]) 删除并返回列表指定位置处的元素，默认最后一个元素：```list.pop()```
        6. list.clear() 删除所有元素；```del list[2]```删除指定位置元素;
        7. list.index(x) 返回第一个x的索引位置，不存在抛出异常；语法：```index(value, [start, [end]])```，指定范围;
        8. list.count(x) 返回指定元素x在列表中出现的次数;
        9. len(list) 返回列表中包含元素的个数;
        10. list.reverse() 翻转列表，所有元素原地翻转;
        11. list.sort() 排序，所有元素原地排序，默认升序，不修改原列表；```list.sort(reverse=True)```为降序排列;
        12. list.copy() 浅拷贝，返回列表对象的浅拷贝;
        13. 乘法扩展：生成新列表，新列表是原列表元素的多次重复：```a = ['ray'], b = a*3```
        14. 成员资格判断：```a in list```
        15. random.shuffle(list) 随机排序;
        16. list.sorted() 排序：生成新的列表的排序;
        17. reversed()返回迭代器：```reversed(list)```返回一个逆序的迭代器对象。
    3. 切片 slice 操作
        1. 语法：```list[start: end: step]```
        2. 基本方法：同 字符串 切片操作
    4. 列表的遍历
        ```python
        >>> a = [10, 20, 30, 50, 88]
        >>> for x in a:
            print(x, end=" * ")

        # 10 * 20 * 30 * 50 * 88 *
        ```
    5. 多维列表
        1. 二维列表
            ```python
            >>> a = [
                    ['ray', 28, 12000, '昆明'],
                    ['rogy', 27, 10000, '上海'],
                    ['Tom', 26, 10000, '北京']
                ]
            >>> a[1]
            # ['rogy', 27, 10000, '上海']
            >>> a[1][0]
            # 'rogy'
            ```
23. 元组
    1. 元组是不可变序列，访问与处理速度比列表快；
    2. 创建：```a = (10, 20, 30)``` ; ```tuple('abc')```
    3. 元组的访问、切片等方法同列表，但不能进行修改的操作；
    4. 元组排序：sorted(tupleObj)， 生成新的**列表**；
    5. zip(list1, list2, ...)将多个列表对应位置的元素组合成元组，并返回这个zip对象。
        ```python
        >>> a = [10, 20, 30]
        >>> b = [40, 50, 60]
        >>> c = [70, 80, 90]
        >>> d = zip(a, b, c)
        >>> list(d)
        # [(10, 40, 70), (20, 50, 80), (30, 60, 90)]
        >>> d
        # <zip object at 0x000001F614EF9F48>
        ```
    6. 生成器推导式创建元组
        ```python
        >>> s = (x*2 for x in range(5))
        >>> tuple(s)
        # (0, 2, 4, 6, 8)
        >>> list(s) # 只能访问一次，第二次为空，需要再生成一次
        # []
        # __next__() 方法一个一个元素遍历
        >>> s = (x*2 for x in range(5))
        >>> s.__next__()
        # 0
        >>> s.__next__() # 直到全部遍历完，若再遍历会返回异常
        # 2
        ```
24. 字典
    1. 字典是键值对的**无序**可变序列，包含 键对象 与 值对象；键对象为不可变数据，且不可重复；
    2. 字典通过 ｛｝、dict()创建。
        ```python
        >>> a = {'name':'rogy', 'age':27, 'job': 'student'}
        >>> a
        # {'name': 'rogy', 'age': 27, 'job': 'student'}
        >>> b = dict(name = 'ray', age = 28, job = 'solider')
        >>> b
        # {'name': 'ray', 'age': 28, 'job': 'solider'}
        >>> c = dict([('name', 'Tom'), ('age', 28)])
        >>> c
        # {'name': 'Tom', 'age': 28}
        ```
    3. 通过zip()创建字典对象
        ```python
        >>> k = ['name', 'age', 'job']
        >>> v = ['ray', 28, 'solider']
        >>> d = dict(zip(k,v))
        >>> d
        # {'name': 'ray', 'age': 28, 'job': 'solider'}
        ```
    4. 通过```a = dict.fromkeys(['name', 'age', 'job'])```创建值为空的字典
    5. 字典元素的访问
        ```python
        >>> a = {'name':'rogy', 'age':27, 'job': 'student'}
        >>> a['name'] # 若键不存在，则异常
        # 'rogy'
        >>> a.get('name')
        # 'rogy'
        >>> a.get('sex') # 若键不存在，则返回None
        >>> print(a.get('sex'))
        # None
        >>> a.get('sex', 'man') # 也可指定返回的值
        # 'man'
        ```
    6. 其他方法
        1. 列出所有键值对：a.items()
        2. 列出所有键：a.keys()
        3. 列出所有的值：a.values()
        4. len() 键值对的个数
        5. 键是否在字典中：```name in dictA```
    7. 字典元素的增、删、改
        1. 添加的键值对，如果键已经存在，则覆盖原来的键值对；不存在，则新增键值对；
        2. update()将新字典中所有键值对全部添加互旧字典中，如果键有重复，则直接覆盖；
        3. 字典元素的删除，用del()方法、或clear()方法删除所有键值对；pop()删除指定键值对，并返回对应的值对象；
        4. popitem() 随机删除和返回键值对。
    8. test
        ```python
        r1 = {'name': 'ray', 'age': 28, 'salary': 10000, 'city': '北京'}
        r2 = {'name': 'rogy', 'age': 27, 'salary': 8000, 'city': '昆明'}
        r3 = {'name': 'Tom', 'age': 28, 'salary': 11000, 'city': '上海'}

        tb = [r1, r2, r3]

        # 打印第二行中人的薪资
        print(tb[1].get('salary'))

        # print all the salary
        for i in range(len(tb)):
            print(tb[i].get('salary'))
        ```
    9. 字典核心底层原理
25. 集合
    1. 集合是无序可变，元素不能重复且唯一。实际上，集合底层是字典实现；
    2. 定义：a = {3, 7, 9}
    3. add() 方法向集合中添加元素；
    4. set() 将列表、元组等可迭代对象转成集合；
    5. remove() 删除指定元素，clear() 清空集合；
    6. 集合的并集 | union()、交集 & intersection()、差集 - difference()

# Python Control statement
26. download and install of [PyCharm](https://www.jetbrains.com/pycharm/download/#section=windows)
27. 选择结构
    1. 选择结构有：单分支、双分支、多分支结构
    2. 单分支结构
        ```python
        '''
        # 注意条件表达式为False的情况
        # 条件表达式中不能有赋值符 = 
        if 条件表达式： 
            语句
        '''
        a = input("please input a number which is letter than 10:")
        if int(a) < 10:
            print(a)
        ```
    3. 双分支结构
        ```python
        '''
        if 条件表达式： 
            语句1
        else:
            语句2
        '''
        a = input("please input a number which is letter than 10:")
        if int(a) < 10:
            print(a)
        else:
            print('the number is biger than 10')
        ```
    4. 三元条件运算符
        1. 语法：条件为真时的值  if （条件表达式） else  条件为假时的值
        ```python
        num = input('please input a number:')
        print(num if int(num)<10 else 'number is too big')
        ```
    5. 多分支结构
        ```python
        '''
        if 条件表达式1： 
            语句1
        elif 条件表达式2： 
            语句2
        ......
        else:
            语句
        # 多分支结构的几个分支之间是有逻辑关系的，不能随意颠倒顺序
        '''
        score = int(input('input the score:'))
        grade = ""

        if score < 60:
            grade = '不及格'
        elif score < 80:
            grade = '及格'
        elif score < 90:
            grade = '良好'
        else:
            grade = '优秀'

        print('score is {0}, denji is {1}'.format(score, grade))
        ```
    6. 选择结构嵌套
        1. 选择结构可以嵌套，使用时要注意不同级别代码的缩进量，因为缩进量决定了代码的从属关系。
        2. 语法：
        ```
        if 表达式1：
            语句1
            if 表达式2：
                语句2
            else:
                语句3
        else :
            if 表达式4：
                语句4
        ```
        ```python
        score2 = int(input('please input a score: '))
        grade2 = ""
        if score2 > 100 or score2 < 0:
            score2 = int(input('请输入0-100之间的数字：'))
        else:
            if score2 >= 90:
                grade2 = 'A'
            elif score2 >= 80:
                grade2 = 'B'
            elif score2 >= 70:
                grade2 = 'C'
            elif score2 >= 60:
                grade2 = 'D'
            else:
                grade2 = 'E'
            print("score is {0}, denji is {1}".format(score2, grade2))
        ```
28. while循环结构
    1. 语法
    ```
    while 条件表达式:
        循环体语句
    ```
    ```python
    nums = 0
    sum_all = 0

    while nums <= 100:
        sum_all = sum_all + nums
        nums += 1

    print("1-100累加和: ", sum_all)
    ```
29. for循环
    1. 语法
    ```
    for 变量 in 可迭代对象：
        循环体语句
    ```
    2. 可迭代对象
    ```
    python中可迭代对象有：序列（字符串、列表、元组）、字典、迭代器对象（iterator）、生成器对象（generator）
    ```
    ```python
    for m in range(1, 10):
        for n in range(1, m+1):
            print("{0}*{1}={2}".format(m, n, (m*n)), end="\t")
        print()
    ```
    3. break语句
    ```
    break语句可用于while和for循环，用来结束整个循环，当有嵌套时，break语句只能跳出最近一层的循环。
    ```
    ```python
    while True:
        a = input('please input a str(input Q or q to end)')
        if a.upper() == 'Q':
            print('end')
            break
        else:
            print(a)
    ```
    4. continue语句
    ```
    continue 用来结束本次循环，继续下一次，多个循环嵌套时，continue也是应用于最近的一层循环
    ```
    ```python
    empNum = 0
    salarySum = 0
    salarys = []
    while True:
        s = input('请输入员工的薪资（按Q或q结束）:  ')

        if s.upper() == 'Q':
            print('录入完成，退出！')
            break
        if float(s) < 0:
            continue
        empNum += 1
        salarys.append(float(s))
        salarySum += float(s)

    print("员工数{0}".format(empNum))
    print("录入薪资：", salarys)
    print("平均薪资{0}".format(salarySum/empNum))
    ```
    5. else语句
    ```
    while、for循环可以附带一个else语句，如果while、for语句没有被break语句结束，则会执行else语句，否则不执行。
    ```
    6. 循环代码优化
    ```
    1. 尽量减少循环内部不必要的计算；
    2. 嵌套循环中，尽量减少内层循环的计算，尽可能向外提；
    3. 局部变量查询较快，尽量使用局部变量。
    ```
30. zip()并行迭代
31. 推导式创建序列
    1. 推导式是从一个或者多个迭代器快速创建序列的一种方法，将循环和条件判断结合，避免冗长的代码，是典型的python风格。
    2. 列表推导式
        ```
        [表达式 for item in 可迭代对象]  或  [表达式 for item in 可迭代对象 if 条件判断]
        ```
        ```python
        >>> [x for x in range(1, 5)]
        [1, 2, 3, 4]
        >>> [x*2 for x in range(1, 20) if x%5 == 0]
        [10, 20, 30]
        >>> cells = [(row, col) for row in range(1, 5) for col in range(1, 5)]
        >>> cells
        [(1, 1), (1, 2), (1, 3), (1, 4), (2, 1), (2, 2), (2, 3), (2, 4), (3, 1), (3, 2), (3, 3), (3, 4), (4, 1), (4, 2), (4, 3), (4, 4)]
        ```
    3. 字典推导式
         ```
        ｛key_expression: value_expression for 表达式  in  可迭代对象｝
        ```
        ```python
        >>> my_text = "i love you, i love sxt, i love rogy"
        >>> char_count = {c:my_text.count(c) for c in my_text}
        >>> char_count
        {'i': 3, ' ': 8, 'l': 3, 'o': 5, 'v': 3, 'e': 3, 'y': 2, 'u': 1, ',': 2, 's': 1, 'x': 1, 't': 1, 'r': 1, 'g': 1}
        ```
    4. 集合推导式
        ```
        ｛表达式 for item in 可迭代对象｝  或  ｛表达式 for item in 可迭代对象 if 条件判断｝
        ```
    5. 生成器推导式（生成元组）
        ```
        一个生成器推导式只能运行一次
        ```
        ```python
        >>> gnt = (x for x in range(4))
        >>> gnt
        <generator object <genexpr> at 0x00000191E749FA20>
        >>> tuple(gnt)
        (0, 1, 2, 3)
        >>> tuple(gnt)
        ()
        ```
    6. test
        ```python
        # -*- coding: utf-8 -*-

        import turtle

        t = turtle.Pen()

        for i in range(10):
            t.penup()
            t.goto(0, -i*10)
            t.pendown()
            t.circle(10 + i*10)

        turtle.done() # 程度执行完毕，窗口还在
        # result is the next picture
        ```
        <img src="./Pictures/turtleResult.png">
# Function
32. 函数简介
    1. 一个程度由一个个任务组成，函数就是代表一个任务或一个功能。
    2. 函数是代码复用的通用机制。
    3. python函数的分类
        1. 内置函数
        2. 标准库函数
        3. 第三方库函数
        4. 用户自定义函数
    4. 函数的定义和调用
        ```
        def 函数名([参数列表])：
            '''文档字符串(对函数进行注释)'''
            # help(函数名.__doc__) 查看文档字符串
            函数体/若干语句
        ```
        1. 要点
        ```
        1. 使用def 定义函数，python执行时会创建一个函数对象，并绑定到函数名变量上
        2. 参数列表：圆括号内是形式参数列表，有多个参数则使用逗号隔开；形式参数不需要声明，也不需要指定函数返回值类型； 无参数，也必须保留空的圆括号； 实参列表必须与形参列表一一对应
        3. return返回值： 如果函数体中包含return语句，则结束函数执行并返回值； 如果函数体中不包含return语句，则返回None值。
        4. 调用函数之前，必须要先定义函数，内置函数会自动创建，标准库和第三方库函数，通过import导入模块。
        ```
        ```python
        def fuc_1():
            print('*'*10)
            print('$'*10)

        fuc_1()
        ```
    5. 形参和实参
        ```python
        def printMax(a, b):
            # a, b为形参, 定义函数时使用
            '''实现两个数的比较，返回较大值'''
            if a > b:
                print(a, "bigger")
            else:
                print(b, 'bigger')

        printMax(10, 20) # 10, 20为实参， 实参需要与形参一一对应
        ```
    6. 函数返回值
        ```
        return 作用：返回值； 结束函数的执行
        ```
    7. 变量的作用域：全局变量和局部变量
        ```
        全局变量：
        1. 在函数和类定义之外声明的变量，作用域为定义的模块，从定义位置开始直到模块结束。
        2. 全局变量降低了函数的通用性和可读性，避免使用。
        3. 全局变量一般做常量使用。
        4. 函数内要改变全局变量的值，要用global 声明一下。
        局部变量：
        1. 函数体中声明的变量。
        2. 局部变量的引用比全局变量快，优先考虑使用。
        3. 如果局部变量和全局变量同名，则在函数内隐藏全局变量，只使用同名的局部变量
        ```
        ```python
        a = 3 # 全局变量

        def test01():
            b = 4 # 局部变量
            print(b*10)

            # global a
            a = 300 
            print(a)

        test01()
        print(a)
        # print(b) # 会报错，b没有定义
        ```
        
        ```python
        # 局部变量与全局变量效率测试
        import math
        import time

        def func01():
            start = time.time()
            for i in range(10000000):
                math.sqrt(30)
            end = time.time()
            print('using time: {0}'.format(end-start))

        def func02():
            b = math.sqrt
            start = time.time()
            for i in range(10000000):
                b(30)
            end = time.time()
            print('using time: {0}'.format(end-start))

        func01()
        func02()
        # 运行结果
        # using time: 2.3268659114837646
        # using time: 1.727508544921875
        ```
    8. 参数的传递
        1. 本质上是从实参到形参的赋值操作
        2. 对可变对象进行写操作时，直接作用于原对象本身；可变对象有：字典、列表、集合、自定义的对象等。
        3. 对不可变对象进行写操作时，会产生一个新的对象空间，并用新的值填充这块空间；不可变对象有：数字、字符串、元组、function等。
        ```python
        # 传递可变对象
        a = [10, 20]
        print(id(a))
        print(a)
        print('*'*10)
        def func001(m):
            print(id(m))
            m.append(300)
            print(id(m))

        func001(a)
        print(a)
        # 运行结果
        '''
        1664995844744
        [10, 20]
        **********
        1664995844744
        1664995844744
        [10, 20, 300]
        '''
        ```
        ```python
        # 传递不可变对象
        x = 100
        def f1(n):
            print("n: ", id(n)) # 传递进来的是x对象的地址
            n = n + 200 # 因x是不可变对象，因此创建新的对象n
            print("n: ", id(n)) # n已经变成了新的对象
            print(n)

        f1(x)
        print('x: ', id(x))
        # 运行结果
        '''
        n:  140724600008432
        n:  2155949973328
        300
        x:  140724600008432
        '''
        ```
    9. 浅拷贝copy 和 深拷贝deepcopy
        1. 浅拷贝：不拷贝子对象的内容，只是拷贝子对象的引用。**传递不可变对象时，如果发生拷贝，是浅拷贝。**
        2. 深拷贝：会连子对象的内存也全部拷贝一份，对子对象的修改不会影响源对象。
        ```python
        # 浅拷贝和深拷贝
        import copy

        def testCopy():
            '''测试浅拷贝'''
            a = [10, 20, [5, 6]]
            b = copy.copy(a)

            print("a: ", a)
            print("b: ", b)

            b.append(30)
            b[2].append(7)

            print('浅拷贝后···')
            print("a: ", a)
            print("b: ", b)

        def testDeepCopy():
            '''测试深拷贝'''
            a = [10, 20, [5, 6]]
            b = copy.deepcopy(a)

            print("a: ", a)
            print("b: ", b)

            b.append(30)
            b[2].append(7)

            print('深拷贝后···')
            print("a: ", a)
            print("b: ", b)

        testCopy()
        print('*'*20)
        testDeepCopy()
        # 运行结果
        '''
        a:  [10, 20, [5, 6]]
        b:  [10, 20, [5, 6]]
        浅拷贝后···
        a:  [10, 20, [5, 6, 7]]
        b:  [10, 20, [5, 6, 7], 30]
        ********************
        a:  [10, 20, [5, 6]]
        b:  [10, 20, [5, 6]]
        深拷贝后···
        a:  [10, 20, [5, 6]]
        b:  [10, 20, [5, 6, 7], 30]
        '''
        ```
        浅拷贝原理图  
        <img src="./Pictures/copy.png">  
        深拷贝原理图  
        <img src="./Pictures/deepCopy.png">
33. 基本函数
    1. lambda表达式和匿名函数
        ```
        lambda表达式可以用来声明匿名函数，生成一个函数对象，只允许包含一个表达式，不能包含复杂语句，表达式计算结果就是函数的返回值
        lambda  arg1, arg2, arg3... : <表达式>
        ```
        ```python
        >>> f = lambda a, b, c : a+b+c
        >>> print(f)
        <function <lambda> at 0x0000027316374048>
        >>> print(f(2, 3, 4))
        9
        >>> g = [lambda a:a*2, lambda b:b*3, lambda c:c*4]
        >>> g[0](6), g[1](7), g[2](8)
        (12, 21, 32)
        ```
    2. eval()函数
        1. 功能：将字符串str当成有效的表达式来求值并返回计算结果。
        2. 语法：eval(source[, globals[, locals]]) -> value
        3. 参数：
        ```
        source：一个Python表达式或函数compile()返回的代码对象
        globals: 可选，必须是dictionary
        locals: 可选，任意映射对象
        ```
        ```python
        >>> s = "print('hello world!')"
        >>> eval(s)
        hello world!
        >>> a = 10
        >>> b = 20
        >>> c = eval('a+b')
        >>> c
        30
        >>> dict1 = dict(a=100, b=200)
        >>> d = eval("a+b", dict1)
        >>> d
        300
        ```
    3. 递归函数
        1. 递归函数是自己调用自己的函数，在函数体内直接或间接的自己调用自己。
        2. 终止条件：表示递归什么时候结束，一般用于返回值，不再调用自己。
        3. 递归步骤：把第n步的值和第n-1步相关联。
        4. 递归函数会创建大量的函数对象，对内存和运算能力消耗大。
        5. 先进后出，后进先出。
            ```python
            def test01(n):
                print("test01: ", n)
                if n == 0:
                    print("over!")
                else:
                    test01(n-1)

                print("test01***", n)

            test01(4)
            # result
            '''
            test01:  4
            test01:  3
            test01:  2
            test01:  1
            test01:  0
            over!
            test01*** 0
            test01*** 1
            test01*** 2
            test01*** 3
            test01*** 4
            '''
            ```
        <img src="./Pictures/recurrence.png">

            ```python
            # 阶乘计算
            def factorial(n):

                if n == 1:
                    return 1
                else:
                    return n*factorial(n-1)

            result = factorial(5)
            print(result)
            # 120
            ```
    4. 嵌套函数（内部函数）
        1. 嵌套函数：在函数内部定义的函数
            ```python
            def f1():
                print("f1 is running...")

                def f2():
                    print("f1 is running...")
                
                f2()

            f1()

            # result
            # f1 is running...
            # f1 is running...
            ```
        2. 嵌套函数作用
            ```
            1. 封装 - 数据隐藏：外部无法访问嵌套函数；
            2. 贯彻DRY（don't repeat yourself）原则：在函数内部避免代码重复；
            3. 闭包
            ```
    5. nonlocal关键字：用来声明外层的局部变量
34. LEGB规则
    1. python在查找“名称”时，是按照LEGB规则查找的：local-->enclosed-->global-->built in
        ```
        local: 指的是函数或者类的方法内部
        enclosed: 指的是嵌套函数
        global：指的是模块中的全局变量
        built in: 指的是python为自己保留的特殊名称
        ```
# 面向对象（OOP object oriented programming)
    ```
    1. python中，一切皆对象；python支持面向过程、面向对象、函数式编程等多种编程范式；
    2. 面向对象编程将数据和操作数年相关的方法封装到对象中，组织代码和数据的方式更加接近人的思维，大大提高了编程的效率。
    ```
35. 面向对象与面向过程的区别
    1. 面向过程（procedure oriented）思维
        ```
        更加关注程序的逻辑流程，是一种执行者思维
        ```
    2. 面向对象（object oriented）思维
        ```
        设计者思维，更加关注“软件中对象之间的关系”
        ```
36. 类的定义
    1. 语法：
        ```
        class 类名：
            类体

        1. 方法代码共享，属性数据不共享；
        2. 类名必须符合标识符规则，一般首字母大写，多个单词使用驼峰原则；
        3. 类体中定义属性和方法；
        4. 属性描述数据，方法描述这些数据相关的操作。
        ```
        ```python
        class Student:

            def __init__(self, name, score): # self必须位于第一个参数位置
                self.name = name
                self.score = score

            def say_score(self):
                print("{0} 的分数是：{1}".format(self.name, self.score))


        s1 = Student("rogy", 87)
        s1.say_score()
        # rogy 的分数是：87
        ```
    2. 构造函数__init__()
        1. 创建对象，需要定义构造函数__init__()方法，用于执行实例对象的初始化工作，即对象创建后，初始化当前对象的相关属性，无返回值。
            ```
            __init__()的要点：
            1. 名称固定，必须是__init__()
            2. 第一个参数固定，必须是：self，self指的就是刚创建好的实例对象；
            3. 构造函数通常用来初始化实例对象的实例属性；
            4. 通过 类名 来调用构造函数，调用后，将创建好的对象返回给相应的变量；
            5. ___init__()方法：初始化创建好的对象，即给实例属性赋值；
            6. __new__()方法用来创建对象，一般无需重定义该方法；
            注：python中的self相当于C++中的self指针和JAVA中this关键字；pyhton中self必须是构造函数的第一参数，名字可以任意修改，一般都叫self.
            ```
    3. 实例属性
        1. 实例属性从属于实例对象，也称为 实例变量。
        2. 使用要点
            ```
            1. 实例属性一般在__init__()方法中通过代码：self.实例属性名 = 初始值 来定义
            2. 在本类的其他实例方法中，也是通过self进行访问：self.实例属性名
            3. 创建实例对象后，通过实例对象访问：obj01 = 类名()； obj01.实例属性名 = 值
            ```
    4. 实例方法
        1. 实例方法是从属于实例对象的方法
        2. 定义格式：
            ```
            def 方法名(self, [, 形参列表])：
                函数体
            
            方法的调用格式如下：
                对象.方法名([实参列表])
            
            要点：
            1. 定义实例方法时，第一个参数必须是self，self也指当前的实例对象。
            2. 调用实例方法时，不需要也不能给self传参，self由解释器自动传参。
            ```
    5. 类对象
    6. 类属性
        1. 从属类对象的属性，也称为类变量，可以被所有实例对象共享。
        2. 定义：
            ```
            class 类名：
                类变量名 = 初始值
            
            在类中或者类的外面，可以通过：类名.类变量名 来读写。
            ```
            ```python
            class Student:
                company = 'STX' #类属性
                count = 0 # 类属性

            def __init__(self, name, score):
                self.name = name
                self.score = score # 实例属性
                Student.count += 1

            def say_score(self): # 实例方法
                print("my company is: ", Student.company)
                print(self.name, '的分数是：', self.score)
            
            s1 = Student('ray', 80) # s1是实例对象，自动调用__init__()方法
            s1.say_score()
            print('一共创建{0}个Student对象'.format(Student.count))
            '''
            my company is:  STX
            ray 的分数是： 80
            一共创建1个Student对象
            '''
            ```
    7. 类方法
        1. 从属类对象的方法，类方法通过装饰器@classmethod来定义，格式如下：
            ```
            @classmethod
            def 类方法名(cls, [, 形参列表])：
                函数体
            
            要点：
            1. @classmethod必须位于方法上面一行。
            2. 第一个cls必须有；cls指的就是 类对象 本身。
            3. 调用类方法格式：类名.类方法名（参数列表）；参数列表中，不能给cls传值。
            4. 类方法中访问实例属性和实例方法会导致错误。
            5. 子类继承父类方法时，传入cls是子类对象，而非父类对象。
            ```
        2. 类方法测试
            ```python
            class Student:
                company = 'stx'

                def __init__(self, name, age):
                    self.name = name
                    self.age = age

                @classmethod
                def printCompany(cls):
                    print(cls.company)
                    # print(self.name) # 类方法和静态方法中，不能调用实例变量和实例方法

            Student.printCompany()
            ```
    8. 静态方法
        1. python 中定义的与对象无关的方法，叫静态方法；
        2. 静态方法放到了类的名字空间里面，需要通过类调用；
        3. 静态方法通过装饰器@staticmethod来定义，格式:
            ```
            @staticmethod
            def 静态方法名([形参列表])：
                函数体
            要点：
            1. @staticmethod必须位于方法上面一行
            2. 调用静态方法格式：类名.静态方法（参数列表）
            3. 静态方法中访问实例属性和实例方法会导致错误
            ```
            ```python
            class Student:
                company = 'stx' # 类属性

                @staticmethod
                def add(a, b): # 静态方法
                    print("{0}+{1}={2}".format(a, b, (a+b)))
                    return a+b

            Student.add(20, 30)
            ```
37. 析构函数(__del__方法)和垃圾回收机制
    1. 析构方法：用于实现对象被销毁时所需的操作，如释放对象占用的资源等；
    2. python实现自动的垃圾回收机制，当对象没有被引用时（引用计数为0），由垃圾回收器调用__del__方法；
    3. 也可以通过del语句删除对象，从而保证调用__del__方法；
    4. 系统会自动提供__del__方法，一般不需要自定义析构方法。
        ```python
        # 析构函数
        class Person:

            def __del__(self):
                print("销毁对象：{0}".format(self))

        p1 = Person()
        p2 = Person()

        del p2
        print("程序结束！")
        # 销毁对象：<__main__.Person object at 0x000001FCE210FEB8>
        # 程序结束！
        ```
38. 可调用对象和__call__方法
    1. 定义了__call__方法的对象，称为 可调用对象，即该对象可以像函数一样被调用
        ```python
        class SalaryAccount:
            '''工资计算类'''
            
            def __call__(self, salary):
                print("算工资了....")
                yearSalary = salary * 13
                daySalary = salary // 27.5
                hourSalary = daySalary // 8

                return dict(yearSalary=yearSalary, monthSalary = salary, daySalary=daySalary, hourSalary=hourSalary)

        s = SalaryAccount()
        print(s(11000))
        '''
        算工资了....
        {'yearSalary': 143000, 'monthSalary': 11000, 'daySalary': 400.0, 'hourSalary': 50.0}
        '''
        ```
39. python中方法没有重载
    1. python中，方法的参数没有类型(调用时确定方法的类型)，参数的数量也可以由可变参数控制，因此，python中没有方法的重载，定义一个方法即可有多种调用方式，相当于实现了其他语言中的方法重载；
    2. 如果在python中定义了多个重名的方法，只有最后一个有效。
        ```python
        class Person:

            def say_hi(self):
                print("hello")

            def say_hi(self, name):
                print('{0}, hello!'.format(name))

        man = Person()
        # man.say_hi()
        # TypeError: say_hi() missing 1 required positional argument: 'name'
        man.say_hi('ray')
        # ray, hello!
        ```
40. 方法的动态性
    1. python是动态语言，可以动态的为类添加新的方法，或者动态的修改类的已有方法
        ```python
        # 测试方法的动态性

        class Person:

            def work(self):
                print("working hard!")


        def play_game(s):
            print("{0} is playing game".format(s))
        
        def work2(s):
            print('好好工作，努力上班')

        Person.play = play_game
        p = Person()
        p.work()
        p.play() # Person.Play(p)
        Person.work = work2
        p.work()
        # working hard!
        # <__main__.Person object at 0x0000029061C7FD68> is playing game
        # 好好工作，努力上班
        ```
41. 私有属性和私有方法(实现封装)
    1. Python对于类的成员没有严格的访问控制；
    2. 私有属性和私有方法的要点：
        ```
        1. 两个下划线开关的属性是私有（private），其他的为公共。
        2. 类内部可以访问私有属性（方法）。
        3. 类外部不能直接访问私有属性（方法）。
        4. 类外部可以通过“_类名__私有属性（方法）名”访问私有属性和方法。
        注：方法本质上也是属性。
        ```
        ```python
        # 测试私有属性
        class Employee:

            __company = "programmer"  # 变量也可以私有

            def __init__(self, name, age):
                self.name = name
                self.__age = age # 私有属性

            def __work(self): # 私有方法
                print("working hard, have a good live!")
                print("age: {0}".format(self.__age)) # 类里面自己调用私有属性是没有问题
                print(Employee.__company)

        e = Employee('ray', 28)

        print(e.name)
        # print(e.__age) # 会报错， 'Employee' object has no attribute '__age'，因为age是私有属性。
        print(e._Employee__age) # 私有属性调用
        # e.__work() # 报错：'Employee' object has no attribute '__work'
        e._Employee__work() # 私有方法调用
        # ray
        # 28
        # working hard, have a good live!
        # age: 28
        # programmer
        # programmer
        ```
42. @property装饰器
    1. @property装饰器可以将一个方法的调用方式变成 属性调用；
    2. 用来给属性增加对应的get 和 set 方法。
        ```python
        # 测试@property装饰器的用法

        class Employee:

            @property
            def salary(self):
                print("salary run...")
                return 10000

        emp = Employee()
        # emp.salary()
        print(emp.salary)
        # salary run...
        # 10000
        ```
        ```python
        class Employee:

            def __init__(self, name, salary):
                self.__name = name
                self.__salary = salary

            '''
            def get_salary(self):
                return self.__salary

            def set_salary(self, salary):
                if 1000 < salary < 50000:
                    self.__salary = salary
                else:
                    print("录入错误，薪水在1000—50000之间")
            '''
            
            @property
            def salary(self):
                return self.__salary

            @salary.setter
            def salary(self, salary):
                if 1000 < salary < 50000:
                    self.__salary = salary
                else:
                    print("录入错误，薪水在1000—50000之间!")

        emp = Employee('ray', 11000)

        '''
        print(emp.get_salary())
        emp.set_salary(20000)
        print(emp.get_salary())
        '''
        print(emp.salary)
        emp.salary = -20000
        print(emp.salary)
        ```
43. 面向对象的三大特征：封装、继承、多态
    1. 封装（隐藏）
        ```
        隐藏对象的属性和实现细节，只对外提供必要的方法；
        python可以通过私有属性、方法实现封装。
        ```
    2. 继承
        ```
        继承可以让子类具有父类的特征，提高代码的重用性；
        从设计上是一种增量进化，在父类设计不变的情况下，可以增加新的功能，或改进已有算法。
        
        1. 语法格式：
            class 子类类名（父类类名1 [, 父类类名2...]：
                类体
        2. 在类定义中没有指定父类，则默认父类是object类；
        3. 父类私有的属性子类可以继承，但不能直接使用；
        4. 类成员的继承和重写。
        ```
            ```python
            class Person:

                def __init__(self, name, age):
                    self.name = name
                    self.__age = age # 私有属性

                def say_age(self):
                    print("my age is: ", self.__age)

                def say_introduce(self):
                    print("my name is {0}".format(self.name))

                    
            class Student(Person):

                def __init__(self, name, age, score):
                    Person.__init__(self, name, age) # 必须显示调用父类初始化方法，不然解释器不会调用
                    self.score = score

                def say_introduce(self):
                    '''重写了父类的方法'''
                    print("teacher, my name is: {0}".format.(self.name))


            # print(Student.mro()) # Student.mro()可以输出这个类的继承层次结构
            # [<class '__main__.Student'>, <class '__main__.Person'>, <class 'object'>]

            s = Student('Ray', 27, 90)
            s.say_age()
            s.say_introduce()
            print(s.name)
            # print(s.age) # AttributeError: 'Student' object has no attribute 'age'
            # print(dir(s)) # dir()查看对象属性
            # ['_Person__age', '__class__', '__delattr__', '__dict__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__le__', '__lt__', '__module__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__', '__weakref__', 'name', 'say_age', 'score']
            print(s._Person__age)
            ```
        ```
        5. 重写object的__str__()方法
        ```
            ```python
            class Person:  # 默认继承object类

                def __init__(self, name):
                    self.name = name

                def __str__(self): # 重写object的__str__()方法
                    return "name is :{0}".format(self.name)
                

            p = Person('ray')
            print(p)
            # 没重写前输出的是：<__main__.Person object at 0x000001D6B0F9FCF8>
            # 重写后输出的是：name is :ray
            ```
        ```
        6. 多重继承
            一个子类可以有多个直接父类，具备多个父类的特点；也会导致类的整体层次异常复杂，避免使用。
        7. super()获得父类的定义
        ```
    3. 多态
        ```
        1. 多态指：同一个方法调用由于对象不同会产生不同的行为；
        2. 多态是方法的多态，属性没有多态；
        3. 多态的存在有2个必要条件：继承和方法重写。
        ```
        ```python
        # 多态

        class Man:

            def eat(self):
                print("eating!")


        class Chinese(Man):

            def eat(self):
                print("Chinese use chopsticks to eat!")


        class English(Man):

            def eat(self):
                print("English use fork to eat!")
                

        class Indian(Man):

            def eat(self):
                print("Indian use rightHand to eat!")

        def manEat(m):
            if isinstance(m, Man):
                m.eat() # 多态，一个方法调用，根据对象不同调用不同的方法！
            else:
                print("can not eat!")

        manEat(Chinese())
        manEat(English())
        # Chinese use chopsticks to eat!
        # English use fork to eat!
    ```
44. 组合
    1. is-a关系，可以使用继承，实现子类拥有父类的方法和属性。
    2. has-a关系，可以使用组合，也能实现一个类拥有另一个类的方法和属性。
        ```python
        # 测试组合

        # 继承实现
        class AI:

            def say_ai(self):
                print("ai")


        class BI(AI):
            pass

        b1 = BI()
        b1.say_ai()


        # 组合方法实现

        class A2:

            def say_a2(self):
                print('a2')


        class B2:

            def __init__(self, a):
                self.a = a


        a2 = A2()
        b2 = B2(a2)
        b2.a.say_a2()
        ```
45. 设计模式---工厂模式
    1. 工厂模式：实现了创建者和调用者的分离，使用专门的工厂类将选择实现类、创建对象进行统一管理和控制。
        ```python
        # 测试工厂模式

        class CarFactory:

            def create_car(self, brand):
                if brand == "奔驰":
                    return Benz()
                elif brand == "宝马":
                    return BMW()
                elif brand == "比亚迪":
                    return BYD()
                else:
                    return "未知品牌，无法创建"


        class Benz:

            pass


        class BMW:

            pass



        class BYD:

            pass

        factory = CarFactory()
        c1 = factory.create_car("奔驰")
        print(c1)
        ```
        