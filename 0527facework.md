1、python2和python3区别？列举5个 

1、Python3 使用 print 必须要以小括号包裹打印内容，比如 print('hi') 

Python2 既可以使用带小括号的方式，也可以使用一个空格来分隔打印内容，比如 print 'hi' 

2、python2 range(1,10)返回列表，python3中返回迭代器，节约内存 

3、python2中使用ascii编码，python中使用utf8编码 

4、python2中unicode表示字符串序列，str表示字节序列python3中str表示字符串序列，byte表示字节序列 

5、python2中为正常显示中文，引入coding声明，python3中不需要 

6、python2中是raw_input()函数，python3中是input()函数 



2、10个Linux常用命令 

ls pwd cd touch rm mkdir tree cp mv cat more grep echo 



3、简述with方法打开处理文件帮我我们做了什么？ 

打开文件在进行读写的时候可能会出现一些异常状况，如果按照常规的f.open 

写法，我们需要try,except,finally，做异常判断，并且文件最终不管遇到什么情况，都要执 

行finally f.close()关闭文件，with方法帮我们实现了finally中f.close 



4、简述面向对象中__new__和__init__区别 

__init__是初始化方法，创建对象后，就立刻被默认调用了，可接收参数，如图 

1、__new__至少要有一个参数cls，代表当前类，此参数在实例化时由Python解释器自动识 

别

2、__new__必须要有返回值，返回实例化出来的实例，这点在自己实现__new__时要特别注 

意，可以return父类（通过super(当前类名, cls)）__new__出来的实例，或者直接是object 

的__new__出来的实例 

3、__init__有一个参数self，就是这个__new__返回的实例，__init__在__new__的基础上可以 

完成一些其它初始化的动作，__init__不需要返回值 

4、如果__new__创建的是当前类的实例，会自动调用__init__函数，通过return语句里面调用 

的__new__函数的第一个参数是cls来保证是当前类实例，如果是其他类的类名，；那么实际 

创建返回的就是其他类的实例，其实就不会调用当前类的__init__函数，也不会调用其他类的 

__init__函数。



5、python内建数据类型有哪些 

整型int 

布尔型bool字符串str 

列表list 

元组tuple 

字典dict 