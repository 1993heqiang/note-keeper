# 官网文档

## 速览

- 如果不希望前置 `\` 的字符转义成特殊字符，可以使用 *原始字符串*，在引号前添加 `r` 即可：
  
  ```python
  print('C:\some\name')  # 这里 \n 表示换行符！
  print(r'C:\some\name')  # 请注意引号前的 rname
  ```

- 在多行文本中，可以通过`\`避免第一行空行加入到文本中
  
  ```python
  print("""\
  Usage: thingy [OPTIONS]
       -h                        Display this usage message
       -H hostname               Hostname to connect to
  """)
  ```

- 内建方法实现为空
  
  举例：`len(str)` 和 `str.__len__`
  
  `len(str)`是内建方法，全局通用。当str对象内部有`__len__`实现时才会生效，否则抛出异常

- input方法
  
  阻塞执行，要求输入
  
  ```python
  a = input('Please input a number.')
  ```

- 

## 更多控制流工具

- 循环的 `else` 子句
  
  > 在 `for` 或 `while` 循环中 `break` 语句可能对应一个 `else` 子句。 如果循环在未执行 `break` 的情况下结束，`else` 子句将会执行
  
  ```python
  for n in range(2, 10):
      for x in range(2, n):
          if n % x == 0:
              print(n, 'equals', x, '*', n//x)
              break
      else:
          # 循环到底未找到一个因数
          print(n, 'is a prime number')
  ```

- `pass` 语句: 可以理解为函数体或者实现为空
  
  ```python
  class MyEmptyClass:
      pass
  
  def initlog(*args):
      pass   # 记得实现这个！
  ```

- `*args`和`**kwargs`
  
  - `*args`:可变位置参数
  
  - `**kwargs`：可变关键字参数
  
  ```python
  def func(a, b, *args, kwarg1="default", **kwargs):
      print(f"a: {a}")
      print(f"b: {b}")
      print(f"args: {args}")
      print(f"kwarg1: {kwarg1}")
      print(f"kwargs: {kwargs}")
  
  # 调用函数时传递位置参数和关键字参数
  func(10, 20, 30, 40, 50, kwarg1="changed", extra="extra_value", another="another_value")
  ```
  
  output:
  
  ```textile
  a: 10
  b: 20
  args: (30, 40, 50)
  kwarg1: changed
  kwargs: {'extra': 'extra_value', 'another': 'another_value'}
  ```

- match语句[Link](https://docs.python.org/zh-cn/3.13/tutorial/controlflow.html#match-statements)
  
  - `__match_args__`:Python 3.10引入的新特性，它告诉 Python 在进行模式匹配时，应该将类实例的哪些属性作为匹配的依据。没有 `__match_args__` 属性，Python 会默认将类的所有属性用于模式匹配。
  
  - 

- 特殊参数 [Link](https://docs.python.org/zh-cn/3.13/tutorial/controlflow.html#special-parameters)
  
  函数定义如下：
  
  ```tex
  def f(pos1, pos2, /, pos_or_kwd, *, kwd1, kwd2):
        -----------    ----------     ----------
          |             |                  |
          |        位置或关键字   |
          |                                - 仅限关键字
           -- 仅限位置
  ```

- 解包实参列表
  
  数组用`*`解包
  
  ```python
  list(range(3, 6))            # 附带两个参数的正常调用
  
  args = [3, 6]
  list(range(*args))            # 附带从一个列表解包的参数t(**d)
  ```
  
  字典用`**`解包
  
  ```python
  def parrot(voltage, state='a stiff', action='voom'):
      print("-- This parrot wouldn't", action, end=' ')
      print("if you put", voltage, "volts through it.", end=' ')
      print("E's", state, "!")
  
  d = {"voltage": "four million", "state": "bleedin' demised", "action": "VOOM"}
  parrot(**d)
  ```

- Lambda 表达式
  
  - 普通匿名函数
  
  ```python
  def make_incrementor(n):
      return lambda x: x + n
  ```
  
  - 匿名函数用作传递的实参
  
  ```python
  pairs = [(1, 'one'), (2, 'two'), (3, 'three'), (4, 'four')]
  pairs.sort(key=lambda pair: pair[1])
  ```

- 函数注解
  
  ```python
  def f(ham: str, eggs: str = 'eggs') -> str:
      print("Annotations:", f.__annotations__)
      print("Arguments:", ham, eggs)
      return ham + ' and ' + eggs
  
  f('spam')
  ```
  
  输出：
  
  ```tex
  Annotations: {'ham': <class 'str'>, 'return': <class 'str'>, 'eggs': <class 'str'>}
  Arguments: spam eggs
  'spam and eggs'
  ```

## 数据结果

- 列表详解
  
  - 列表推导式
    
    ```python
    squares = [x**2 for x in range(10)]
    
    [(x, y) for x in [1,2,3] for y in [3,1,4] if x != y]
    ```
  
  - 嵌套的列表推导式
    
    ```python
    [[row[i] for row in matrix] for i in range(4)]
    ```

- del 语句
  
  - 列表中删除条目
    
    ```python
    a = [-1, 1, 66.25, 333, 333, 1234.5]
    del a[0]
    
    del a[2:4]
    
    del a[:]
    ```
  
  - 删除变量
    
    ```python
    del a
    ```

- 元组: 不可变
  
  ```python
  t = 12345, 54321, 'hello!'
  
  u = t, (1, 2, 3, 4, 5)
  
  v = ([1, 2, 3], [3, 2, 1])
  
  empty = ()
  singleton = 'hello',    # <-- 注意末尾的逗号
  len(empty)
  
  len(singleton)
  ```

- 集合
  
  ```python
  basket = {'apple', 'orange', 'apple', 'pear', 'orange', 'banana'}
  print(basket)                      # 显示重复项已被移除
  
  'orange' in basket                 # 快速成员检测
  
  'crabgrass' in basket
  
  # 演示针对两个单词中独有的字母进行集合运算
  
  a = set('abracadabra') # {'d', 'b', 'c', 'a', 'r'}
  b = set('alacazam') # {'m', 'l', 'c', 'z', 'z'}
  ```

- 字典
  
  ```python
  tel = {'jack': 4098, 'sape': 4139} 
  dict([('sape', 4139), ('guido', 4127), ('jack', 4098)]) 
  {x: x**2 for x in (2, 4, 6)} 
  dict(sape=4139, guido=4127, jack=4098)
  ```

- 循环的技巧
  
  - 字典执行循环
    
    ```python
    knights = {'gallahad': 'the pure', 'robin': 'the brave'}
    for k, v in knights.items():
        print(k, v)
    ```
  
  - 序列中循环
    
    ```python
    for i, v in enumerate(['tic', 'tac', 'toe']):
        print(i, v)
    ```
  
  - 多个序列循环
    
    ```python
    questions = ['name', 'quest', 'favorite color']
    answers = ['lancelot', 'the holy grail', 'blue']
    for q, a in zip(questions, answers):
        print('What is your {0}?  It is {1}.'.format(q, a))
    ```

- 

## 模块

- 模块搜索路径
  
  - `sys.builtin_module_names`
  
  - `sys.path`

- dir()函数
  
  ```python
  import fibo, sys
  dir(fibo)
  dir(sys)
  
  import builtins
  dir(builtins)
  ```

## 输入与输出

- 更复杂的输出格式
  
  str() 函数返回供人阅读的值，repr() 则生成适于解释器读取的值。大多数情况下，希望：`eval(repr(obj)) == obj`
  
  - 格式化字符串
    
    `print(f'The value of pi is approximately {math.pi:.3f}.')`
  
  - format()
    
    `print('We are the {} who say "{}!"'.format('knights', 'Ni'))`
  
  - 旧式方法（**不推荐**）
    
    `print('The value of pi is approximately %5.3f.' % math.pi)`

- 读写文件
  
  ```python
  with open('workfile', encoding="utf-8") as f:
      read_data = f.read()
  ```

- json
  
  ```python
  import json
  x = [1, 'simple', 'list']
  json.dumps(x)
  
  json.dump(x, f)
  x = json.load(f)
  ```



## 错误与异常

- `try...except`语句可选else语句
  
  ```python
  for arg in sys.argv[1:]:
      try:
          f = open(arg, 'r')
      except OSError:
          print('cannot open', arg)
      else:
          print(arg, 'has', len(f.readlines()), 'lines')
          f.close()
  ```
  
  

- 触发异常
  
  ```python
  try:
      raise NameError('HiThere')
  except NameError:
      print('An exception flew by!')
      raise
  ```
  
  

- 异常链
  
  - `raise...from`语句：表明一个异常是另一个异常的直接后果
    
    ```python
    def func():
        raise ConnectionError
    
    try:
        func()
    except ConnectionError as exc:
        raise RuntimeError('Failed to open database') from exc
    ```
    
    
  
  - 使用 `from None` 表达禁用自动异常链
    
    ```python
    try:
        open('database.sqlite')
    except OSError:
        raise RuntimeError from None
    ```
    
    
  
  - 

- 预定义的清理操作：`with...`
  
  ```python
  with open("myfile.txt") as f:
      for line in f:
          print(line, end="")
  ```
  
  

- ExceptionGroup
  
  - 示例1
    
    ```python
    def f():
        excs = [OSError('error 1'), SystemError('error 2')]
        raise ExceptionGroup('there were problems', excs)
    
    try:
        f()
    except Exception as e:
        print(f'caught {type(e)}: e')
    ```
    
    
  
  - 示例2：使用 `except*` 代替 `except`，提取了某种类型的异常
    
    ```python
    def f():
        raise ExceptionGroup(
            "group1",
            [
                OSError(1),
                SystemError(2),
                ExceptionGroup(
                    "group2",
                    [
                        OSError(3),
                        RecursionError(4)
                    ]
                )
            ]
        )
    
    try:
        f()
    except* OSError as e:
        print("There were OSErrors")
    except* SystemError as e:
        print("There were SystemErrors")
    ```
    
    
  
  - 示例3：嵌套在一个异常组中的异常必须是实例，而不是类型
    
    ```python
    excs = []
    for test in tests:
        try:
            test.run()
        except Exception as e:
            excs.append(e)
    
    if excs:
       raise ExceptionGroup("Test Failures", excs)
    ```
    
    
  
  - 

- 用注释细化异常情况
  
  - 示例1：单一异常
    
    ```python
    try:
        raise TypeError('bad type')
    except Exception as e:
        e.add_note('Add some information')
        e.add_note('Add some more information')
        raise
    ```
    
    
  
  - 异常组
    
    ```python
    def f():
        raise OSError('operation failed')
    
    excs = []
    for i in range(3):
        try:
            f()
        except Exception as e:
            e.add_note(f'Happened in Iteration {i+1}')
            excs.append(e)
    
    raise ExceptionGroup('We have some problems', excs)
    ```
    
    
  
  - 



## 类

- 作用域：
  
  global：语句用于表明特定变量在全局作用域里，并应在全局作用域中重新绑定。
  
  nonlocal：语句表明特定变量在外层作用域中，并应在外层作用域中重新绑定。
  
  查看全局变量：`print(globals())`
  
  查看局部变量：`print(locals())`
  
  ```python
  def scope_test():
      def do_local():
          spam = "local spam"
  
      def do_nonlocal():
          nonlocal spam
          spam = "nonlocal spam"
  
      def do_global():
          global spam
          spam = "global spam"
  
      spam = "test spam"
      do_local()
      print("After local assignment:", spam)
      do_nonlocal()
      print("After nonlocal assignment:", spam)
      do_global()
      print("After global assignment:", spam)
  
  scope_test()
  print("In global scope:", spam)
  ```
  
  输出：
  
  ```tex
  After local assignment: test spam
  After nonlocal assignment: nonlocal spam
  After global assignment: nonlocal spam
  In global scope: global spam
  ```
  
  

- `isinstance(...)`和`issubclass(...)`

- 继承
  
  - 单继承
    
    ```python
    class DerivedClassName(BaseClassName):
        <语句-1>
        .
        .
        .
        <语句-N>
    ```
    
    
  
  - 多继承
    
    ```python
    class DerivedClassName(Base1, Base2, Base3):
        <语句-1>
        .
        .
        .
        <语句-N>
    ```
    
    

- `dataclass`
  
  ```python
  from dataclasses import dataclass
  
  @dataclass
  class Employee:
      name: str
      dept: str
      salary: int
  ```
  
  

- 迭代器
  
  - 迭代器示例
    
    ```python
    for element in [1, 2, 3]:
        print(element)
    for element in (1, 2, 3):
        print(element)
    for key in {'one':1, 'two':2}:
        print(key)
    for char in "123":
        print(char)
    for line in open("myfile.txt"):
        print(line, end='')
    ```
    
    
  
  - 实现自定义迭代器
    
    ```python
    class Reverse:
        """对一个序列执行反向循环的迭代器。"""
        def __init__(self, data):
            self.data = data
            self.index = len(data)
    
        def __iter__(self):
            return self
    
        def __next__(self):
            if self.index == 0:
                raise StopIteration
            self.index = self.index - 1
            return self.data[self.index]
    ```
    
    

- 生成器
  
  ```python
  def reverse(data):
      for index in range(len(data)-1, -1, -1):
          yield data[index]
  ```
  
  

- 生成器表达式
  
  ```python
  sum(i*i for i in range(10))                 # 平方和
  
  
  xvec = [10, 20, 30]
  yvec = [7, 5, 3]
  sum(x*y for x,y in zip(xvec, yvec))         # 点乘
  
  
  unique_words = set(word for line in page  for word in line.split())
  
  valedictorian = max((student.gpa, student.name) for student in graduates)
  
  data = 'golf'
  list(data[i] for i in range(len(data)-1, -1, -1))
  ```
  
  

## 标准库简介

- 操作系统接口
  
  ```python
  import os
  import shutil
  
  os.getcwd()      # 返回当前工作目录
  os.chdir('/server/accesslogs')   # 改变当前工作目录
  os.system('mkdir today')   # 在系统 shell 中运行 mkdir 命令
  
  dir(os) # 返回由模块的所有函数组成的列表
  help(os) # 返回根据模块文档字符串创建的详细说明页面
  
  
  shutil.copyfile('data.db', 'archive.db')
  shutil.move('/build/executables', 'installdir')
  ```
  
  

- 文件通配符
  
  ```python
  import glob
  glob.glob('*.py') # 使用通配符搜索文件列表
  ```
  
  

- 命令行参数
  
  ```python
  import sys
  import argparse
  
  print(sys.argv)
  
  parser = argparse.ArgumentParser(
      prog='top',
      description='Show top lines from each file')
  parser.add_argument('filenames', nargs='+')
  parser.add_argument('-l', '--lines', type=int, default=10)
  args = parser.parse_args()
  print(args)
  ```
  
  

- 错误输出重定向和程序终止
  
  ```python
  import sys
  
  # stdin ， stdout 和 stderr
  sys.stderr.write('Warning, log file not found starting a new one\n')
  
  sys.exit() # 终止脚本
  ```
  
  

- 数学
  
  - math
    
    ```python
    import math
    math.cos(math.pi / 4)
    
    math.log(1024, 2)
    ```
    
    
  
  - random
    
    ```python
    import random
    random.choice(['apple', 'pear', 'banana'])
    
    random.sample(range(100), 10)   # 无替代的取样
    
    random.random()    # [0.0, 1.0) 区间的随机浮点数
    
    random.randrange(6)    # 从 range(6) 中随机选取的整数
    ```
    
    
  
  - statistics
    
    ```python
    import statistics
    data = [2.75, 1.75, 1.25, 0.25, 0.5, 1.25, 3.5]
    statistics.mean(data)
    
    statistics.median(data)
    
    statistics.variance(data)
    ```
    
    

- 互联网访问
  
  示例: urllib.request（URL请求） 和 smtplib（用于发邮件）
  
  ```python
  from urllib.request import urlopen
  with urlopen('http://worldtimeapi.org/api/timezone/etc/UTC.txt') as response:
      for line in response:
          line = line.decode()             # 将字节串转换为字符串
          if line.startswith('datetime'):
              print(line.rstrip())         # 去除末尾换行符
  
  
  
  import smtplib
  server = smtplib.SMTP('localhost')
  server.sendmail('soothsayer@example.org', 'jcaesar@example.org',
  """To: jcaesar@example.org
  From: soothsayer@example.org
  
  Beware the Ides of March.
  """)
  server.quit()
  ```
  
  

- 日期与时间
  
  
  
  ```python
  # 方便地构造和格式化日期值
  from datetime import date
  now = date.today()
  now
  
  now.strftime("%m-%d-%y. %d %b %Y is a %A on the %d day of %B.")
  
  # 日期值支持日历运算
  birthday = date(1964, 7, 31)
  age = now - birthday
  age.days
  ```
  
  

- 数据压缩
  
  常见的数据存档和压缩格式由模块直接支持，包括：zlib, gzip, bz2, lzma, zipfile 和 tarfile
  
  ```python
  import zlib
  s = b'witch which has which witches wrist watch'
  len(s)
  
  t = zlib.compress(s)
  len(t)
  
  zlib.decompress(t)
  
  zlib.crc32(s)
  ```
  
  

- 性能测量
  
  timeit 精细粒度级， profile 和 pstats 模块提供了用于在较大的代码块中识别时间关键部分的工具。
  
  ```python
  from timeit import Timer
  Timer('t=a; a=b; b=t', 'a=1; b=2').timeit()
  
  Timer('a,b = b,a', 'a=1; b=2').timeit()
  ```
  
  

- 质量控制
  
  - `doctest`：文档字符串嵌入测试
    
    ```python
    def average(values):
        """计算数字列表的算术平均值
    
        >>> print(average([20, 30, 70]))
        40.0
        """
        return sum(values) / len(values)
    
    import doctest
    doctest.testmod()   # 自动验证嵌入式测试
    ```
    
    
  
  - `unittest`: 单独测试
    
    ```python
    import unittest
    
    class TestStatisticalFunctions(unittest.TestCase):
    
        def test_average(self):
            self.assertEqual(average([20, 30, 70]), 40.0)
            self.assertEqual(round(average([1, 5, 7]), 1), 4.3)
            with self.assertRaises(ZeroDivisionError):
                average([])
            with self.assertRaises(TypeError):
                average(20, 30, 70)
    
    unittest.main()  # 从命令行调用时会执行所有测试
    ```
    
    

- batteries-included
  
  Python有“batteries-included”的理念。通过其包的复杂和强大功能可以最好地看到这一点。例如:
  
  - [`xmlrpc.client`](https://docs.python.org/zh-cn/3.13/library/xmlrpc.client.html#module-xmlrpc.client "xmlrpc.client: XML-RPC client access.") 和 [`xmlrpc.server`](https://docs.python.org/zh-cn/3.13/library/xmlrpc.server.html#module-xmlrpc.server "xmlrpc.server: Basic XML-RPC server implementations.") 模块使得实现远程过程调用变成了小菜一碟。 尽管存在于模块名称中，但用户不需要直接了解或处理 XML。
  
  -  [`email`](https://docs.python.org/zh-cn/3.13/library/email.html#module-email "email: Package supporting the parsing, manipulating, and generating email messages.") 包是一个用于管理电子邮件的库，包括MIME和其他符合 [**RFC 2822**](https://datatracker.ietf.org/doc/html/rfc2822.html) 规范的邮件文档。与 [`smtplib`](https://docs.python.org/zh-cn/3.13/library/smtplib.html#module-smtplib "smtplib: SMTP protocol client (requires sockets).") 和 [`poplib`](https://docs.python.org/zh-cn/3.13/library/poplib.html#module-poplib "poplib: POP3 protocol client (requires sockets).") 不同（它们实际上做的是发送和接收消息），电子邮件包提供完整的工具集，用于构建或解码复杂的消息结构（包括附件）以及实现互联网编码和标头协议。
  
  -  [`json`](https://docs.python.org/zh-cn/3.13/library/json.html#module-json "json: Encode and decode the JSON format.") 包为解析这种流行的数据交换格式提供了强大的支持。 [`csv`](https://docs.python.org/zh-cn/3.13/library/csv.html#module-csv "csv: Write and read tabular data to and from delimited files.") 模块支持以逗号分隔值格式直接读取和写入文件，这种格式通常为数据库和电子表格所支持。 XML 处理由 [`xml.etree.ElementTree`](https://docs.python.org/zh-cn/3.13/library/xml.etree.elementtree.html#module-xml.etree.ElementTree "xml.etree.ElementTree: Implementation of the ElementTree API.") ， [`xml.dom`](https://docs.python.org/zh-cn/3.13/library/xml.dom.html#module-xml.dom "xml.dom: Document Object Model API for Python.") 和 [`xml.sax`](https://docs.python.org/zh-cn/3.13/library/xml.sax.html#module-xml.sax "xml.sax: Package containing SAX2 base classes and convenience functions.") 包支持。这些模块和软件包共同大大简化了 Python 应用程序和其他工具之间的数据交换。
  
  -  [`sqlite3`](https://docs.python.org/zh-cn/3.13/library/sqlite3.html#module-sqlite3 "sqlite3: A DB-API 2.0 implementation using SQLite 3.x.") 模块是 SQLite 数据库库的包装器，提供了一个可以使用稍微非标准的 SQL 语法更新和访问的持久数据库。
  
  - 国际化由许多模块支持，包括 [`gettext`](https://docs.python.org/zh-cn/3.13/library/gettext.html#module-gettext "gettext: Multilingual internationalization services.") ， [`locale`](https://docs.python.org/zh-cn/3.13/library/locale.html#module-locale "locale: Internationalization services.") ，以及 [`codecs`](https://docs.python.org/zh-cn/3.13/library/codecs.html#module-codecs "codecs: Encode and decode data and streams.") 包。



## 标准库简介-第二部分

- 格式化输出
  
  - reprlib
    
    reprlib 模块提供了一个定制化版本的 repr() 函数，用于缩略显示大型或深层嵌套的容器对象
    
    ```python
    import reprlib
    reprlib.repr(set('supercalifragilisticexpialidocious'))
    ```
    
    
  
  - pprint
    
    pprint 模块提供了更加复杂的打印控制，其输出的内置对象和用户自定义对象能够被解释器直接读取
    
    ```python
    import pprint
    t = [[[['black', 'cyan'], 'white', ['green', 'red']], [['magenta',
        'yellow'], 'blue']]]
    
    pprint.pprint(t, width=30)
    ```
    
    
  
  - textwrap
    
    textwrap 模块能够格式化文本段落，以适应给定的屏幕宽度:
    
    ```python
    import textwrap
    doc = """The wrap() method is just like fill() except that it returns
    a list of strings instead of one big string with newlines to separate
    the wrapped lines."""
    
    print(textwrap.fill(doc, width=40))
    ```
    
    
  
  - locale
    
    locale 模块处理与特定地域文化相关的数据格式
    
    ```python
    import locale
    locale.setlocale(locale.LC_ALL, 'English_United States.1252')
    
    conv = locale.localeconv()          # 获取语言区域设置的映射
    x = 1234567.8
    locale.format_string("%d", x, grouping=True)
    
    locale.format_string("%s%.*f", (conv['currency_symbol'],
                         conv['frac_digits'], x), grouping=True)
    ```
    
    
  
  - 

- 模板
  
  - `substitute()`、`safe_substitute()`
    
    ```python
    from string import Template
    t = Template('${village}folk send $$10 to $cause.')
    t.substitute(village='Nottingham', cause='the ditch fund')
    
    d = dict(village='unladen swallow')
    t.safe_substitute(d)
    ```
    
    
  
  - 自定义分隔符
    
    ```python
    import time, os.path
    photofiles = ['img_1074.jpg', 'img_1076.jpg', 'img_1077.jpg']
    class BatchRename(Template):
        delimiter = '%'
    
    fmt = input('Enter rename style (%d-date %n-seqnum %f-format):  ')
    
    t = BatchRename(fmt)
    date = time.strftime('%d%b%y')
    for i, filename in enumerate(photofiles):
        base, ext = os.path.splitext(filename)
        newname = t.substitute(d=date, n=i, f=ext)
        print('{0} --> {1}'.format(filename, newname))
    ```
    
    

- 使用二进制记录格式 [Link](https://docs.python.org/zh-cn/3.13/tutorial/stdlib2.html#working-with-binary-data-record-layouts)
  
  struct 模块提供了 pack() 和 unpack() 函数

- 多线程：threadiing
  
  ```python
  import threading, zipfile
  
  class AsyncZip(threading.Thread):
      def __init__(self, infile, outfile):
          threading.Thread.__init__(self)
          self.infile = infile
          self.outfile = outfile
  
      def run(self):
          f = zipfile.ZipFile(self.outfile, 'w', zipfile.ZIP_DEFLATED)
          f.write(self.infile)
          f.close()
          print('Finished background zip of:', self.infile)
  
  background = AsyncZip('mydata.txt', 'myarchive.zip')
  background.start()
  print('The main program continues to run in foreground.')
  
  background.join()    # 等待背景任务结束
  print('Main program waited until background was done.')
  ```
  
  

- 日志记录
  
  ```python
  import logging
  logging.debug('Debugging information')
  logging.info('Informational message')
  logging.warning('Warning:config file %s not found', 'server.conf')
  logging.error('Error occurred')
  logging.critical('Critical error -- shutting down')
  ```
  
  

- 弱引用
  
  ```python
  import weakref, gc
  class A:
      def __init__(self, value):
          self.value = value
      def __repr__(self):
          return str(self.value)
  
  a = A(10)                   # 创建一个引用
  d = weakref.WeakValueDictionary()
  d['primary'] = a            # 不创建引用
  d['primary']                # 如果对象仍然存在则获取它
  
  del a                       # 移除一个引用
  gc.collect()                # 立即运行垃圾回收
  
  d['primary']                # 条目会被自动移除
  ```
  
  

- 用于操作列表的工具
  
  - `array`
    
    ```python
    from array import array
    a = array('H', [4000, 10, 700, 22222])
    sum(a)
    
    a[1:3]
    ```
    
    
  
  - `collections`
    
    ```python
    from collections import deque
    d = deque(["task1", "task2", "task3"])
    d.append("task4")
    print("Handling", d.popleft())
    ```
    
    
    
    ```python
    unsearched = deque([starting_node])
    def breadth_first_search(unsearched):
        node = unsearched.popleft()
        for m in gen_moves(node):
            if is_goal(m):
                return m
            unsearched.append(m)
    ```
    
    
  
  - `bisect`
    
    ```python
    import bisect
    scores = [(100, 'perl'), (200, 'tcl'), (400, 'lua'), (500, 'python')]
    bisect.insort(scores, (300, 'ruby'))
    scores
    ```
    
    
  
  - `heapq`
    
    ```python
    from heapq import heapify, heappop, heappush
    data = [1, 3, 5, 7, 9, 2, 4, 6, 8, 0]
    heapify(data)                      # 将列表重新调整为堆顺序
    heappush(data, -5)                 # 添加一个新条目
    [heappop(data) for i in range(3)]  # 获取三个最小的条目
    ```
    
    

- 十进制浮点运算
  
  `decimal.Decimal`适用于:
  
  - 财务应用和其他需要精确十进制表示的用途，
  
  - 控制精度，
  
  - 控制四舍五入以满足法律或监管要求，
  
  - 跟踪有效小数位，或
  
  - 用户期望结果与手工完成的计算相匹配的应用程序。
