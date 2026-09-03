# python库
## 分为自带库和外部库
自带库可以直接调用。
外部库需要执行代码 python -m pip install + 库名称

import + 库

```
import random  #  导入随机数模块，用于后续的随机抽取  
  
#  初始化基础暴击率，0.3 代表 30%
hero = 0.3  
  
# 将暴击率放大100倍，变成整数 30，方便后续放入100个格子的“池子”中  
bj = hero * 100  
  
# 开启一个死循环，不断模拟暴击判定  
while True:  
    list = []  # 每次循环都清空列表，准备重新构建暴击池  
  
    #  循环100次，生成一个包含100个元素的列表（即暴击池）  
    for i in range(100):  
        isBj = False  #  默认每个元素都是 False（不暴击）  
  
        #  如果 i 小于当前的暴击率 bj（比如 bj=30，那么 0~29）  
        if i < bj:  
            isBj = True  #  就把这个元素设为 True（暴击）  
  
        list.append(isBj)  #  将结果放入暴击池  
  
    # 统计暴击率：遍历暴击池，数一数里面有多少个 True    number = 0  
    for i in list:  
        if i:  # 如果当前元素是 True            
        number = number + 1  #  计数器加 1  
    #  在控制台打印当前的暴击率  
    print("当前暴击率是：" + str(number) + "%")  
  
    #  从 0 到 99 中随机抽取一个数字（相当于在池子里盲抓一个球）  
    r = random.randint(0, 100 - 1)  
  
    #  判定：如果抓到的这个球是 True    
    if list[r]:  
        print("暴击成功了！")  
        bj = hero * 100  # 暴击成功，把暴击率重置回初始值（30）  
        break  #  跳出死循环，测试结束  
    else:  
        print("暴击失败了...")  
        bj = bj + 10  #  暴击失败，暴击率增加 10%（即 bj 增加 10）  
  
    input("按回车键进行下一次判定...")  # 暂停程序，等待你按回车键，再进行下一次判定
```
# 时间戳

```
import time  # 导入库
startTime = int(time.time())  # 查看 1970年1月1日 到现在的秒数（适合做运算）

可加运行代码

endtime = int(time.time())
print("程序运行时间为：" +  str(endtime - startTime) + "秒")  # 输出结果
```

# 函数

```
函数，为了将代码的各个功能分离开，我们会用到函数

# 第一种语法结构（最基础的）

def 函数名(参数1, 参数2):
 """这里是函数的说明（可选）
 """ 代码块... 
 return 返回值 # (可选)
 
 #第二种写法（没有参数，没有返回值）
 
 def say_hello(): 
 print("勇士，欢迎回到游戏！") 
 say_hello()   # 调用函数（直接喊名字） 

#第三种写法

# 定义一个打招呼的函数，name 就是参数（食材）
def say_hello(name):
print(f"{name}，欢迎回到游戏！") # 调用函数时，把具体的名字传进去 say_hello("亚索") 
say_hello("提莫")

#第四种写法

def jia(a)
	c = a + 1
	retrun c
m = jia(100)
print("结果为：", m)  #给值后代入计算中

def checkAtk(hero,bz): #定义函数名称，然后括号，加冒号 函数不仅能定义一个，他能定义多个

    bj = hero * 100    # 如果你啥也没传，并且他还没有默认值，那么他就会被None占位，然后这里运算的时候，就会报错

    while True:

        list = []

        for i in range(100):

            isBj = False

  

            if i < bj:

                isBj = True

  

            list.append(isBj)

  

        number = 0

        for i in list:

            if i:

                number = number + 1

        print("当前暴击率是：" + "" +  str(number) + "%")

  

        r = random.randint(0,100 -1)

  

        if list[r]:

            print("暴击成功了")

            # 如果暴击成功了，需要把补正给他踢回去

            bj = hero * 100

            return True

  

        else:

            print("暴击失败了")

            bj = bj + bz

        input("")
        
checkAtk(0.1, 1) #传入参数的值        
```


## 使用别的文件下的函数

```
# 1.py 

from test import add,sub    #导入
print(add(1,2))     #传参
print(sub(4, 3))



#   test.py文件
def add(a,b):  

    return  a + b

  
  

def sub(a,b):

    return a -b
```

# 总结

```
#库

python中提供一些简单的内部库，也有需要下载的库

#函数

1、函数的作用就是将功能分割，可以复用，也可以传参
2、def"定义函数"  test"函数名称"  ()"表示该出为函数，并允许在括号中定义参数"    : "和if 一样，表示到这里截止"
3、函数的返回
```