**1. 列举 5 个 Python 中的标准模块**

**答： pathlib：路径操作模块，比 os 模块拼接方便。 urllib：网络请求模块，包括对 url 的结构解析。 asyncio： Python 的异步库，基于事件循环的协程模块。 re：正则表达式模块。 itertools：提供了操作生成器的一些模块。**



**2. Python 中的异常处理，写一个简单的应用场景**

**答： 比如在计算除法中出现为 0 的情况出现异常**

**try：**

​    **1 / 0**

**except ZeroDivisionError as e：**

​    **print(e.args)**



**3. 什么是面向对象的 mro**

**答：Python 是支持面向对象编程的，同时也是支持多重继承的。一般我们通过调用类对象的 mro()方法获取其继承关系。**



**4. isinstance 作用以及应用场景？**

**答：isinstance 是判断一个对象是否为另一个对象的子类的，例如我们知道在 Python3 中 bool 类型其实是 int 的子类，所以我们可以对其检测。**

**print(isinstance(True,int))**



**5. 什么是断言？**

**答：在 Python 中是断言语句 assert 实现此功能，一般在表达式为 True 的情况下，程序才能通过。**