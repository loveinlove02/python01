---
layout: single
title:  "17 datetime 연습"
---

<br/>

>## **1 날짜 출력하기** 

<br/>

### **날짜 출력**  
<br/>
  

```python
import datetime

# date() 생성자에 2001, 8, 17 인자로 넣어 객체생성
d = datetime.date(2021, 8, 17)

print(d)
```

```
2021-08-17
```  

<br/>




### **요일 출력**  
<br/>

```python
import datetime

# date() 생성자에 2001, 8, 17 인자로 넣어 객체생성
d = datetime.date(2021, 8, 17)

# weekday() 메소드
# 월요일 0
print(d.weekday())  # 해당 날짜가 무슨 요일인지를 파악 
```

```
1
```  

<br/><br/>


### **요일을 문자로 출력**  
<br/>


>y = {0:'월', 1:'화', 2:'수', 3:'목', 4:'금', 5:'토', 6:'일'} 

<br/>

```python
import datetime

# 요일 딕셔너리를 만든다
y = {0:'월', 1:'화', 2:'수', 3:'목', 4:'금', 5:'토', 6:'일'}

# date() 생성자에 2001, 8, 17 인자로 넣어 객체생성
d = datetime.date(2021, 8, 17)

# 딕셔너리의 키로 요일 번호를 넣어서 요일을 출력
print(y[d.weekday()]) 
```

```
화
```  

<br/><br/>

>## **2 시간 출력하기**

<br/>




### **날짜 + 시간 출력**  
<br/>


```python
import datetime

# datatime() 생성자에 인자를 넣어서 객체를 생성
d = datetime.datetime(2021, 8, 17, 13, 11, 0)

print(d) 
```

```
2021-08-17 13:11:00
```  
<br/><br/>


### **시간만 출력**  
<br/>

```python
import datetime

# time() 생성자에 시,분,초를 인자로 넣어서 객체를 생성
d = datetime.time(13, 11, 19)

print(d) 
```

```
13:11:19
```  
<br/><br/>


### **현재 날짜와 시간 출력**  
<br/>

```python
import datetime

# datetime 클래스에는 객체를 생성하지 않고도 
# 바로 클래스에서 사용할 수 있는 클래스 메소드가 있습니다.

# 현재 날짜와 시각을 출력하는 now() 메소드
d = datetime.datetime.now()

print(d) 
 
```

```
2021-08-17 13:15:57.099250
```  
<br/><br/>



### **오늘 날짜와 시간 출력**  
<br/>

```python
import datetime

d = datetime.datetime.today()

print(d)  
```

```
2021-08-17 13:16:54.825394
```  
<br/><br/>




>## **3 연습**

<br/>


### **오늘 날짜 중 년도만 출력하라**  
<br/>

```python
from datetime import date

d = date.today()    # 오늘 날짜
# print(d)

print(d.year)       # 년도만 출력
```

```
2021
```  
<br/>


### **오늘 날짜와 2일을 출력하라**  
<br/>

```python
from datetime import date
from datetime import timedelta

# datetime 내장 모듈의 timedelta 클래스는
# 기간을 표현하기 위해서 사용됩니다.

t = timedelta(days=2)   # 2일 간 이라는 뜻
d = date.today()        # 오늘 날짜

print(d)
print(t)
```

```
2021-08-17
2 days, 0:00:00
```  
<br/>


### **오늘 날짜로 부터 1000일이 지난 날짜는?**  
<br/>

```python
from datetime import date
from datetime import timedelta

# datetime 내장 모듈의 timedelta 클래스는
# 기간을 표현하기 위해서 사용됩니다.

t = timedelta(days=100)  # 100일
d = date.today()         # 오늘 날짜

print(d+t)
```

```
2021-11-25
```  
<br/>


<br/>


## **2021년 12월 25일까지 얼마나 남았나?**
```python
from datetime import date

d = date.today()            # 오늘 날짜
d2 = date(2021, 12, 25)     # date 객체 생성

print(d2-d)
```

```
130 days, 0:00:00
```  
<br/>



### **시, 분, 초 출력**  
<br/>

```python
import datetime

# time() 객체 생성
d = datetime.time(11, 20, 10)
print(d.hour)
print(d.minute)
print(d.second)
```

```
11
20
1
```  
<br/>

