# 字符串常用操作

```
s = 'abcd'

print(s[0])
s.encode()
-----------------------------
s1 = 'abcd'
print(s1 + 'a')   # 序列加操作
s2   = s1 * 2   # 序列乘操作
print(s2)

alist = [1,3,5,2,6,8]
# print(max(alist))  # 最大值
# print(min(alist))  # 最小值
# print(sum(alist))  # 求和
# print(len(alist))  # 个数

s1 = 'abA'
# print(max(s1))  # 最大ascii码值

s2 = 'abcdef'
# abc
# ac
s3 = s2[0:3]  # 切片


print(s3, type(s3))  # 数据和数据类型

# for i in s2:     # 遍历
#     print(i)

# print('a' in s2)  # 成员判断

print(isinstance('a', str))  # 类型判断
print(type('a'))  # 输出类型
--------------------------------
# # 倒序九九乘法表
for i in range(9, 0, -1):
    for j in range(1, i+1):
        print('%d * %d = %d' %(j, i ,i*j), end='   ')
    print()
------------------------------------------
'''
          *            1 - 1    3
        * * *          2 - 3    2
      * * * * *        3 - 5    1
    * * * * * * *      4 - 7    0
'''

for i in range(1, 5):
   print('  '*(4-i) + '* ' * (2*i-1))
------------------------------------------
# name = input('请输入名字:')
# age = int(input('请输入年龄: '))
# # print('名字： %s, 年龄：%d ' % (name, age))   # %格式化
# print('名字：{1}， 年龄：{1}'.format(name, age))

'成龙在拍成龙历险记'
# name = '成龙'
# print('{0}在拍{0}历险记'.format(name))  # 方法格式化

# s1 = '  a  bc   '
# print(s1.strip())  # 去前后空格

# s2 = 'abc'
# print(s2.replace('b','a'))  # 替换

# s3 = 'abca'
# print(s3.find('a'))  # 找‘a'出现的下标
# print(s3.index('a'))  # 找'a'出现的下标
# print(s3.count('a'))  # 数‘a’的个数
s4 = 'acccabccccabcd'
print(s4.split('b'))   # ['accca', 'cccca', 'cd']  # 以‘b’切分字符串

s5 = '23'
print(s5.isdigit())  # 是否是数字字符串True

s6 = 'abc'
print(s6.isalpha()) # 是否是英文True

print(s6.islower())  # 是否是全小写True
print(s6.isupper())  # 是否是全大写False

print(s6.upper())  # 转为大写ABC
print(s6.lower())  # 转为小写abc
print(s6.title())  # 首字母大写Abc

s7 = 'abAB'
print(s7.swapcase())  # 大小写转换ABab

s8 = '  abc  '
print(s8.lstrip())  # 去掉左空
print(s8.rstrip())  # 去掉右空
print('*'.join('abc'))  # 插入a*b*c
------------------------------------------

s = '123asqwerAAAA'
dnum = 0  # 记录数字个数
anum = 0  # 记录小写字母个数
Anum = 0  # 记录大写字母格式
enum = 0  # 记录其他字符个数
for i in s:  # 遍历整个字符串
    if i.isdigit():  # 判断是否是数字
        dnum += 1
    elif i.islower():  # 判断是否是小写字母
        anum += 1
    elif i.isupper():  # 判断是否是大写字母
        Anum += 1
    else:  # 其他情况字符
        enum += 1

print('数字：{}，小写：{}，大写：{}'.format(dnum, anum,Anum))
---------------------------------------
import string
import random
d = string.digits   # 生成0123456789字符串
a = string.ascii_letters  # 生成26个大小写字母
s = ''
for i in range(20):
    n = random.choice(a+d)
    s += n
ds = ''  # 定义数字字符串
da = ''  # 定义小写字符串
dA = ''  # 定义大写字符串
for j in s:
    if j.isdigit():  # 是数字字符串
        ds += j
    elif j.isupper():  # 是大写字符串
        dA += j
    elif j.islower():  # 是小写字符串
        da += j

print('数字{}个数{}， 大写字母{}个数{}，小写字母{}个数{}'.format(ds,len(ds),  dA, len(dA),  da, len(da)))
insert into demo_student(name,age,hobby) vaules('张三',12,'丑牛');
insert into demo_student(name,age,hobby, add_time) values('张三',12,'丑牛','2018-01-01');
------------------------------------------------------------

import string
import random
d = string.digits   # 生成0123456789字符串
print(d, type(d))
a = string.ascii_letters  # 生成26个大小写字母
print(a)
ad = a + d   # 把字符串拼接
s = ''  # 存储验证码
for i in range(6):
    n = random.choice(ad)  # 随机出一个字符串
    s += n  # 字符串拼接
print(s)  # 打印最后验证码
------------------------------------------

num = int(input('请输入一个数：'))
bai = num // 100  # 获取百位121 // 100 = 1
shi = num % 100 // 10 # 获取十位121 %100 = 21   21 // 10 = 2
ge = num % 10  # 获取个位  121 % 10 =1

n = ge * 100 + shi*10 + bai  # 合并成新数字

if n == num:  # 判断是否相等
    print('{}是回文数'.format(num))
else:
    print('{}不是回文数'.format(num))

---------------------------------------------
num = input('请输入一个数：')
n = num[::-1]  # 使用切片反转字符串
if n == num:
    print('{}是回文数'.format(num))
else:
    print('{}不是回文数'.format(num))

-------------------------------------
a = 'abcd'
"""
    a   b   c   d
    0   1   2   3
   -4  -3  -2  -1
"""

print(a[-2::-2])
-------------------------------------
a = '123abc中文'
b = a.encode('GBK') # 编码
print(a,b)
c= b.decode('GBK')  # 解码
print(a,b,c)
---------------------------------
# 一、求出1-100的和
s = 0
for i in range(1,101):
    s = s + i

print('结果为', s)
--------------------------------
# 三、求1-100之间的所有偶数
for i in range(1,101):
    if i % 2 == 0:
        print('偶数：', i)
-------------------------------
# 使用切片取出字符串’123qweyuzhongguohao’中’zhongguo’字符串
s = '123qweyuzhongguohao'
s1 = s[8:16:1]
print(s1)

--------------------------------
# 使用join方法实现字符串中z*h*o*n*g*g*u*o的效果
print('*'.join('zhongguo'))


# 6使用replace方法实现把字符串z*h*o*n*g*g*u*o中的*替换成@

print('z*h*o*n*g*g*u*o'.replace('*','@'))
--------------------------------
n = int(input('请输入数字:'))  # 153
bai = n // 100
shi = n % 100 // 10
ge = n % 10
s = bai ** 3 + shi ** 3 + ge ** 3
if s == n:
    print('{}是水仙花'.format(n))
else:
    print('{}不是水仙花'.format(n))

------------------------------
n = int(input('请输入数字:'))  # 153
bai = n // 100
shi = n % 100 // 10
ge = n % 10
num = ge * 100 + shi * 10 + bai
if num == n:
    print('{}是回文数字'.format(n))
else:
    print('{}不是回文数字'.format(n))
```



