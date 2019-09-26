# 序列之列表

```
# 1、通过[] 创建列表
alist = [1,2,'abc']
# print(alist, type(alist))

#2、通过list()创建列表
blist = list('abc')
# print(blist, type(blist))

clist = [1,2,3,4,5,6,7,8,9,10]
dlist = list('qwret')  # 类型转换
print(clist, dlist)

# 3、列表推导式创建列表
a1 = [i*2 for i in range(1,34)]
print(a1)

a2 = [i for i in range(1,67) if i % 2 == 0]
print(a2)
---------------------------------
a3 = ['a',1,2,3,4,5,6]
# print(a3[0])   # 查看

# a3[0] = 'b'  # 赋值
# print(a3)

# a3.append('abc')  # 尾部追加一个元素
# print(a3)

# a3.insert(0,'123')  # 指定位置插入数据
# print(a3)

# print(a3, id(a3))  # 查看内存地址
# a3.extend([1,2,3,4,5])  # 尾部添加多个数据（扩展）
# print(a3, id(a3))


# a = 'a'
# print(a, id(a))
# a = 'b'
# print(a, id(a))

--------------------------------------
balls = []  # 创建空列表

for i in range(1,4):
    a = int(input('请输入第{}个数字'.format(i)))
    balls.append(a)   # 添加到列表内
print('添加后列表：{}'.format(balls))

# 把a插入到列表
balls.insert(1,'a')
print('插入a后列表{},地址为{}'.format(balls, id(balls)))

# 把1，2，3添加到列表内
balls.extend([1,2,3])
print('扩展后列表：{}， 地址为：{}'.format(balls, id(balls)))
---------------------------------
balls = [i for i in range(1,6)]
# print(balls)
# balls.pop(0)  # 删除指定下标（默认最后一个）
# print(balls)
#
# balls.remove(5)  # 删除指定元素
# print(balls)
#
# balls.clear()  # 清空列表
# print(balls)

# del balls  # 删除列表
# print(balls)

del balls[0]  # 删除指定元素
print(balls)
------------------------------------
balls = [1,2,8,6,2,4]
# balls.sort()  # 对原数据从小到大排序
# print(balls)

# b = sorted(balls)  # 从小到大排序不修改原数据
# print(balls, b)

# balls.sort(reverse=True) # 从大到小排序
# print(balls)

balls.reverse()   # 反转
print(balls)
---------------------------------
balls = [1,2,8,6,2,4]

# for i in balls:  # 遍历所有元素
#     print(i)

# for i in range(len(balls)):  # 通过索引获取遍历
#     print(balls[i])

# for j in enumerate(balls):  # 通过枚举返回元组遍历
#     print(j)

for index, j in enumerate(balls):  # 通过枚举获取索引和元素
    print(index, j)
----------------------------------

balls = list()  # 创建一个空列表
for i in range(5):   # 循环5次输入数据
    a = int(input('请输入一个数字:'))
    balls.append(a)  # 添加数据
print(balls)

ma = max(balls)   # 最大值
mi = min(balls)  # 最小值
av = sum(balls) / len(balls)  # 求和/个数 = 平均值
print('最大值：{}， 最小值：{}， 平均值{}'.format(ma, mi, av))

-------------------------------------
balls = []  # 创建空列表

n = 1  # 定义第几个数字
while True:
    a = int(input('请输入你选择的第{}个数字'.format(n)))

    if a in balls:  # 输入的球在列表内退出当前循环
        print('已经输入过{}，请重新输入！'.format(a))
        continue
    else:  # 输入的球不在列表内，添加到列表内
        balls.append(a)
        n += 1

    if len(balls) == 6:   # 球存6个退出循环
        break
print('您的号码是：', balls)
--------------------------------------
balls = []  # 创建空列表
for i in range(1,7):
    a = int(input('请输入第{}个数：'.format(i)))
    balls.append(a)

print('您的号码是', balls)
-----------------------------------
a = [0,1,2,3,4,5]
print(a[::-2])

s = 'abcdabcd'
b = s.find('a', 2, 5)
print(b)

c = s.index('a', 2, 5)
print(c)

```



