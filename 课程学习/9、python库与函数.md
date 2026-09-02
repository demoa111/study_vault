# python库
## 分为自带库和外部库
自带库可以直接调用。
外部库需要执行代码 python -m pip install + 库名称

import + 库

```
import random  #  导入随机数模块，用于后续的随机抽取  
  
#  初始化基础暴击率，0.3 代表 30%hero = 0.3  
  
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
        bj = hero * 100  # 【核心机制】暴击成功，把暴击率重置回初始值（30）  
        break  #  跳出死循环，测试结束  
    else:  
        print("暴击失败了...")  
        bj = bj + 10  #  【核心机制】暴击失败，暴击率增加 10%（即 bj 增加 10）  
  
    input("按回车键进行下一次判定...")  # 暂停程序，等待你按回车键，再进行下一次判定
```
# 时间戳

```
startTime = int(time.time())
print(startTime)
```