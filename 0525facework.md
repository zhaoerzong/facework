**1. lambda 表达式格式以及应用场景？**

**答：lambda 表达式其实就是一个匿名函数,在函数编程中经常作为参数使用。 例子如下**

**a = [('a',1),('b',2),('c',3),('d',4)]**

**a_1 = list(map(lambda x：x[0],a))**



**2. 新式类和旧式类的区别**

**答：Python 2.x 中默认都是经典类，只有显式继承了 object 才是新式类，Python 3.x 中默认都是新式类，经典类被移除，不必显式的继承 object。 新式类都从 object 继承，经典类不需要。 新式类的 MRO(method resolution order 基类搜索顺序)算法采用 C3 算法广度优先搜索，而旧式类的 MRO 算法是采用深度优先搜索。 新式类相同父类只执行一次构造函数，经典类重复执行多次。**



**3. dir()是干什么用的？**

**答：当在使用某一个对象不知道有哪些属性或者方法可以使用时，此时可以通过 dir() 方法进行查看。**



**4. 一个包里有三个模块，demo1.py、demo2.py、demo3.py，但使用 from tools import \*导入模块时，如何保证只有 demo1、demo3 被导入了。**

**答： 增加_init_.py 文件，并在文件中增加：**

**__all__ = ['demo1','demo3']**



**5. 列举 5 个 Python 中的异常类型以及其含义**

**答：**

**AttributeError 对象没有这个属性**

**NotImplementedError 尚未实现的方法**

**StopIteration 迭代器没有更多的值**

**TypeError 对类型无效的操作**

**IndentationError 缩进错误**

