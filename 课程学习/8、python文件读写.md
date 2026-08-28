
# 相对路径和绝对路径

路径符 ： windows的是\   linux的是/   但在编程中都是用/,\为转义符， \w 表示空格 \n 表示换行相对路径 ：./表示相对路径，就是从当前程序运行的位置寻找文件。  
绝对路径 ：表示从根路径一层一层到目标的。

# 读取、写入、追加写入、with语法


```
#%%读取%%

r = open("D:/git笔记/study_vault/课程学习/4、linux熟悉.md", "r", encoding="utf-8")   # 绝对路径写法  
print(r.read())  
r.close()                   # 文件一定要关闭，会占用资源

#%%写入%%

s = "jdskjflsj"    # 写入的内容
w = open("wang/1.txt", "w", encoding="utf-8")  #相对路径 
print(w.write(s))  
w.close()

#%%追加写入%%

s = "\nwwwwwwww"    \n 为空格，转义符
a = open("wang/1.txt", "a", encoding="utf-8")   
a.write(s)  
a.close()





```