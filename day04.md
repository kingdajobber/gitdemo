# 标准输入函数 input()
- 作用：接收从终端输入的字符串，然后赋值给变量。
- 格式：str = input("提示输入字符串")

## 练习：任意输入一个数，将其加5并打印
- 答案：  
```  
a = input('please input a number: ')  
result = int(a) + 5  
print('result is: ', result)  
```

# 占位符（字符串格式化）
## 格式：  
 - 格式化字符串 % 参数值  
 - 格式化字符串 % （参数1、参数2、……）  

 ## 实例：
 ```  
 name = '门庆，西'
 age = 38
 print("%s的年龄为%d岁" % (name,age))  
 ```

- %s占位：字符串参数  
- %d占位：整数参数  
- %f占位：浮点数参数(默认6位精度)，%.2f可保留2位精度  

## 练习(用占位符实现)：  
 - 输出姓名：秋香&&年龄：20岁&&毕业薪资：10000.88元  
 【答案】：  
```
name = "秋香"
age = 20
salary = 10000.88
print("姓名：%s&&年龄：%d岁&&毕业薪资：%.2f元" % (name,age,salary))  
```

# 关系运算符  
 **`>,>=,<,<=,!=,==`**  
 - 关系运算符返回值都是布尔类型 True、False  

# if条件语句
- 作用： 让程序根据条件，判断并选择性的去执行某条或某些语句  
- 格式：  
```  
 if 条件1:
     Python语句
 elif 条件2:
     Python语句
 ……
 else:
     Python语句  
 ```

**注意： if条件语句后面必须加 :**  
- elif可以有0个，也可以有多个  
- else 最多只能有一个，也可以没有  

## 实例：  
输入一个数，判断是整数、负数、还是零  
- 答案：  
```  
a = int(input('please input a number: '))
if a > 0:
    print("正数")
elif a == 0:
    print("零")
else:
    print("负数")  
```

## 练习：
 1.输入一个季度 1-4，显示对应季度有那几个月，如果输入不是1-4的整数，提示输入错误。  
- 答案：  
```
print("1.输入一个季度 1-4，显示对应季度有那几个月，\ 如果输入不是1-4的整数，提示输入错误。")
print('\n')

s = int(input('please input a Season num: '))
if s == 1:
    print("Jan,Feb,Mar")
elif s == 2:
    print("Apr,May,Jun")
elif s == 3:
    print("Jul,Aug,Sep")
elif s == 4:
    print("Oct,Nov,Dec")
else :
    print("Not a valid Season! ")
print('\n')  
```

2.输入一个正整数，判断这个数是奇数还是偶数，并打印结果。  
- 答案：  
```  
print("２．输入一个正整数，判断这个数是奇数还是偶数，并打印结果。")
print("\n")

a = int(input('please input a　int num: '))
if a % 2 == 0:
    print('偶数')
elif a % 2 !=0:
    print('奇数')  
```

---

## if 嵌套语句  
- 格式：  
```
if 条件1:
    if 子条件1:
        子条件执行的Python语句
    elif 子条件2:
        子条件执行的Python语句
    else:
        子条件执行的Python语句
elif 条件2:
    Python语句
……
else :
    Python语句  
```

# 逻辑运算符
- and  表示与  
- or 表示或  

## 练习：
输入一个学生的成绩(0-100)，超出范围提示输入不合法，  
0-59提示不及格，60-79为及格，80-89为良好，90-100为优秀

- 答案：  
```
print("输入一个学生的成绩(0-100)，超出范围提示输入不合法，0-59提示不及格，60-79为及格，80-89为良好，90-100为优秀")
print("\n")

score = float(input("Please input one student's score: "))
b = "不及格"
j = "及格"
l = "良好"
y = "优秀"

if score >= 0 and score <= 100:
    if score >= 0 and score <= 59:
        print(b)
    elif score >= 60 and score <= 79:
        print(j)
    elif score >= 80 and score <= 89:
        print(l)
    else:
        print(y)
else:
    print("超出成绩范围！")  
```

## 练习：  
输入一年中的月份1-12，输出这个月属于哪个季度，如果输入其他数则报错。  

- 答案：  
```  
m = float(input("请输入一个月份："))
if m >=1 and m<=12:
    if m <= 3:
        print("本月属于一季度")
    if 4 <= m <= 6:
        print("本月属于二季度")
    if 7 <= m <= 9:
        print("本月属于三季度")
    if 10 <= m <= 12:
        print("本月属于四季度")
else :
    print("不是合法月份输入！")  
```

## 练习：  
给出一个年份，判断是否为闰年  
闰年规则：每四年一润，每百年不润，四百年又润  
- 答案：  
```
year = int(input("Please input a Year number:"))

if (year % 4 == 0) and (year % 100 != 0):
    print("This year is a Leap Year!")
elif (year % 400 == 0):
    print("This year is a Leap Year!")
else:
    print("This year is NOT a Leap Year!")  
```

 
