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
  
  

- 
