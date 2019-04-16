# python

## Containers

### Lists

方括号创建：`xs = [3, 1, 2]`，或用range函数`nums = list(range(5))`

append函数增加一个元素，pop函数删除最后一个元素

slice：`print(nums[:-1])`，-1等价于最后一位数

Loops：`for animal in animals`，若显示每个元素的标号

~~~python
for idx, animal in enumerate(animals):
    print('#%d: %s' % (idx + 1, animal))
~~~

List comprehensions：`even_squares = [x ** 2 for x in nums if x % 2 == 0]`

### Dictionaries

元素对应标签，大括号创建：`d = {'cat': 'cute', 'dog': 'furry'}`

get函数获取元素对应标签：`print(d.get('fish', 'N/A'))`

Loops、List comprehensions

### Sets

无序，大括号创建：`animals = {'cat', 'dog'}`

Loops、List comprehensions

### Tuples

Tuples can be used as keys in dictionaries and as elements of sets, while lists cannot.

圆括号创建：`t = (5, 6)`

~~~python
d = {(x, x + 1): x for x in range(10)}
print(d[t])       # Prints "5"
~~~

## Function

`def hello(name, loud=False):`

## Classes

~~~python
class Greeter(object):

    # Constructor
    def __init__(self, name):
        self.name = name  # Create an instance variable

    # Instance method
    def greet(self, loud=False):
        if loud:
            print('HELLO, %s!' % self.name.upper())
        else:
            print('Hello, %s' % self.name)

g = Greeter('Fred')  # Construct an instance of the Greeter class
g.greet()            # Call an instance method; prints "Hello, Fred"
g.greet(loud=True)   # Call an instance method; prints "HELLO, FRED!"
~~~

