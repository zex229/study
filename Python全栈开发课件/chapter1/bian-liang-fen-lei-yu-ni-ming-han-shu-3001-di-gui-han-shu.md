# 变量分类与匿名函数、递归函数

```
a = 10   # 全局变量
def fun():
    b = 1   # 局部变量
    print('hello')
    print('b:', b)

fun()
print(a)
# print(b)

-----------------------------------

a = 10   # 全局变量
def fun():
    a = 20  # 局部变量
    print('a:', a)

fun()
print(a)
------------------------

a = [1,2]

def fun():
    a.append(3)

fun()
print(a)
----------------------

a = 10  # 全局变量
def fun():
    global a  # 声明调用全局变量
    a = a + 1  # 对全局变量进行修改
    print(a)

fun()
print(a)
---------------------
# def fun(a, b):
#     m = max(a,b)
#     return m
#
# b = fun(1,2)
# print(b)

# lambda x, y : max(x,y)   # 定义匿名函数  lambda  形参: 返回值
# (lambda x, y : max(x,y))(1,2)
print((lambda x, y : max(x,y))(1,2))

print((lambda x,y : x+y)(2,3))

-----------------------------
print((lambda x,y=5 : x+y)(2, 3))
print((lambda x,y=5 : x+y)(2))

f = lambda x, y: x + y
print(f(3,4))
------------------------------
递归
def fun(n):    # n!  = n * (n-1) !
    if n == 0 or n == 1:
        return 1     # 当n=0,1结束递归
    elif n > 1:
        return n * fun(n-1)  # 递归规则  4 * 3!   3 * 2!   2 *1!

print(fun(4))
----------------------------------
def fun(n):  # 求0~n之间的和
    if n == 0:  # 终止条件
        return 0
    elif n > 0:
        return n + fun(n-1)  # 递归规则

print(fun(100))
-------------------------
# 斐波那契数字 1， 1 ， 2，  3， 5， 8


def fun(n):
    if n == 1 or n == 0:   # 第0个和第1个数为1
        return 1
    else:
        return  fun(n-1) + fun(n-2)  # 递归规则为前两个数之和为第三个数
print(fun(5))
-----------------------------------
# 编写一个函数，参数是两个int类型，调用该函数可以获取两个参数之间的斐波那契数
# 斐波那契数字 1， 1 ， 2，  3， 5， 8

def fun(x, y):
    a, b = 0,1  # 定义初始值
    while True:
        a, b = b, a+b  # 循环赋值
        if x <= a <=y:  # 当a在[x,y]区间内则打印结果
            print(a)
        if a > y:  # 当a超过范围，则跳出循环
            break
fun(8,30)

--------------------
# 编写一个函数，参数是两个int类型，调用该函数可以获取两个参数之间的斐波那契数
# 斐波那契数字 1， 1 ， 2，  3， 5， 8

def fun(x, y):
    a, b = 0,1  # 定义初始值
    while True:
        temp = a
        a = b
        b = temp + b
        if a >= x and a <=y:  # 当a在[x,y]区间内则打印结果
            print(a)
        if a > y:  # 当a超过范围，则跳出循环
            break
fun(1,10)

```



