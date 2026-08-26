# 基础语法
## 变量

```
a = 1       =的意思是赋值
print(a)
```
## 字符类型

```
name = ""
print(name)
```

## 整数类型、浮点型、布尔类型

```
int 整数类型   1
float 浮点型  12.1
bool 布尔类型   1  true           0  flase
```

## 列表、字典、set集合、None

```
# 列表：

list = []          #排列从0开始 0 1 2 3 ··· 等  
list.append("零")  
list.append("一")  
list.append("二")  
list.append("三")  
num = list[0]  
print(num)  
pop = list.pop(3)    #不加参数 默认删除最后一个，  
print(pop)
```

```
# 字典：   键：值
user = {  
    "name": "wang",  
    "age": 20,  
    "city": "shanghai"  
}  
  
# user["age"] = 11  
# user['id'] = 1       加或改参数
name = user["age"]     取出其中参数数据
print(name)
```

```
# set集合
 
# sets = set ()  
sets = {1,2,3,4,5,6,7,8,9}  
# sets.add (3)  
# sets.add (4)  
# sets.add (5)  
# sets.add (6)  
sets.remove(4)  
# sets.clear()  
print(sets)
```

```
# None
result = None
print(result)  #默认参数，当一个数据没有任何类型的时候就是一个none类型
```

# 类型转换


## 字符串转整数、字符串转浮点数、数字转字符串、布尔转换

```
# 字符串转整数
age = "18"
age_num = int(age)
print(age_num + 1)

# 字符串转浮点数  
age = 12.1  
age_num = float(age)  
print(age_num + 1)

# 数字转字符串  
age = 12.1  
age_num = str(age)  
print(type(age_num))

# bool转换  
print(bool(0))  
print(bool(1))  
print(bool(""))  
print(bool("1"))
```

## 常见错误示列

```
# 错误写法
age = input("Enter your age: ")      input中填写的值为str 
print("Your age is", age)       

#正确写法
age = int(input("Enter your age: "))  
print("Your age is", age + 1)
```

# 算术、比较、逻辑、成员、身份运算符

```
# 算术运算符

+ - * / //(整除) %（取余） **（次方）

# 比较运算符
>  <  >=   <=  ==   !=

# 逻辑运算符 

and  正正得正，正负得负，负负得负
or   正正得正，正负得正，负负得负
not  正得负，负得正

# 成员运算符
in   在
not in   不在

# 身份运算符
is    是
is not   不是

result = None  
if result is None:  
    print("over")

```

# if条件判断

```
# 条件判断  
a = 2  
b = 2  
if a > b:  
    print("a大于b")  
elif a == b:  
  
    print("a等于b")  
else:  
    print("a小于b")  
  
  
a = "python"        
if "a" in a:  
    print("yes")  
else:  
    print("no")
```

# for循环、while循环

```
#for循环





# while循环

b = True                # 开关打开  
while b:                # b是True就继续转  
    pwd = input("请输入密码：")  
    if len(pwd) >= 8:  
        print("密码长度符合要求")  
        b = False        # ← 把开关关上，循环结束  
    else:  
        print("密码太短，请重新输入")

写法二：
        
a = True  
while a:  
    pwd = input("请输入密码")  
    if len(pwd) >= 3:  
        print("yes")  
        break  
    else:  
        print("no")        
```