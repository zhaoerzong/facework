**1. 简要写一下 lxml 模块的使用方法框架**

**答：**

**from lxml import html**

**source='''**

<div class="nam"><span>中国</span></div>

**root=html.fromstring(source)**

**_content=root.xpath("string(//div[@class='nam'])")**

**if _content and isinstance(_content,list)：**

​    **content=_content[0]** 

**elif isinstance(_content,str)：**

​    **content=_content**    

**print(content)**



**2. 在 requests 模块中，requests.content 和 requests.text 什么区别**

**答： requests.content 获取的是字节，requests.text 获取的是文本内容。**

 

**3. 使用 Python 实现一个斐波那契数列**

**答： 斐波那契数列：数列从第 3 项开始，每一项都等于前两项之和。**

**def fbonacci(num)：**

​    **"""**

​    **获取指定位数的列表**

​    **：param num：**

​    **：return：**

​    **"""**

​    **a, b = 0, 1**

​    **l = []**

​    **for i in range(num)：**

​        **a, b = b, a + b**

​        **l.append(b)**

​    **return l**

**if __name__ == '__main__'：**

​    **print(fibonacci(10))**



**4. 找出列表中的重复数字** 

**答：**

**"""**

**从头扫到尾，只要当前元素值与下标不同，就做一次判断,numbers[i]与 numbers[numbers[i]]，**

**相等就认为找到了重复元素，返回 true,否则就交换两者，继续循环。直到最后还没找到认为没找到重复元素。**

**"""**

**# -\*- coding：utf-8 -\*-**

**class Solution:**

​    **def duplicate(self, numbers):**

​        **"""**

​        **:param numbers:**

​        **:return:**

​        **"""**

​        **if numbers is None or len(numbers) <= 1:**

​            **return False**

​        **use_set = set()**

​        **duplication = {}**

​        **for index, value in enumerate(numbers):**

​            **if value not in use_set:**

​                **use_set.add(value)**

​            **else:**

​                **duplication[index] = value**

​        **return duplication**

**if __name__ == '__main__':**

​    **s = Solution()**

​    **d = s.duplicate([1, 2, -3, 4, 4, 95, 95, 5, 2, 2, -3, 7, 7, 5])**

​    **print(d)**



**5. 找出列表中的单个数字**

**答：**

**def find_single(l ：list)：**

​    **result = 0**

​    **for v in l：**

​        **result ^= v**

​    **if result == 0：**

​        **print("没有落单元素")**    

​    **else：**

​        **print("落单元素" ,result)**

**if __name__ == '__main__'：**

​    **l = [1,2,3,4,5,6,2,3,4,5,6]**

​    **find_single(l)**        