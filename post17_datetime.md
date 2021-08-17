---
layout: single
title:  "16 datetime"
---

<br/>

## **datetime 패키지**  

1. 날짜와 시간을 함께 저장하는 datetime 클래스  
2. 날짜만 저장하는 date 클래스  
3. 시간만 저장하는 time 클래스  
4. 시간 구간 정보를 저장하는 timedelta 클래스 등을 제공한다.

<br/><br/>


> ## **1. datetime 클래스**  
<br/><br/>


패키지 이름과 클래스 이름이 datetime으로 같기 때문에 사용할 때 주의해야 합니다.  
다른 클래스와 달리 클래스 이름이 대문자로 시작하지 않습니다.  
<br/>

datetime 클래스에는 객체를 생성하지 않고도 바로 클래스에서 사용할 수 있는 클래스 메서드라는 것을 제공합니다.  

<br/>

가장 대표적인 것이 현재 시각을 출력하는 now() 메서드입니다.  
<br/>


```python
import datetime

now = datetime.datetime.now()
print(now)
```

```
2021-08-17 13:38:47.401368
``` 


<br/><br/>



now 클래스 메서드는 컴퓨터의 현재 시각을 datetime 클래스 객체로 만들어 반환한다.  
datetime 클래스 객체는 다음과 같은 속성을 가진다.  
<br/>

- year: 연도
- month: 월
- day: 일
- hour: 시
- minute: 분
- second: 초
- microsecond: 마이크로초(micro seconds, 백만분의 일초)
<br/>

```python
import datetime

now = datetime.datetime.now()
print(now.year, now.month, now.day, now.hour, now.minute, now.second, now.microsecond)
```

```
2021 8 17 13 42 14 904432
```  
<br/><br/>



다음과 같은 메서드도 제공합니다.  
<br/>

- weekday: 요일 반환 (0:월, 1:화, 2:수, 3:목, 4:금, 5:토, 6:일)
- strftime: 문자열 반환
- date: 날짜 정보만 가지는 date 클래스 객체 반환
- time: 시간 정보만 가지는 time 클래스 객체 반환

<br/><br/>

**weekday : 요일 반환 (0:월, 1:화, 2:수, 3:목, 4:금, 5:토, 6:일)**    

```python
import datetime

now = datetime.datetime.now()
day = now.weekday()
print(day)
```

```
1
```

<br/><br/>

**strftime: 문자열 반환**  
<br/>

날짜와 시간 정보를 문자열로 바꿔주는 strftime 메소드.  
<br>

|날짜 및 시간 지정 문자열|의미|
|--|--|
|%Y|앞의 빈자리를 0으로 채우는 4자리 연도 숫자|
|%m|앞의 빈자리를 0으로 채우는 2자리 월 숫자|
|%d|앞의 빈자리를 0으로 채우는 2자리 일 숫자|
|%H|앞의 빈자리를 0으로 채우는 24시간 형식 2자리 시간 숫자|
|%M|앞의 빈자리를 0으로 채우는 2자리 분 숫자|
|%S|앞의 빈자리를 0으로 채우는 2자리 초 숫자|
|%A|영어로 된 요일 문자열|
|%B|영어로 된 월 문자열|

<br/>


```python
import datetime

now = datetime.datetime.now()
day1 = now.strftime('%A %d. %B %Y')
print(day1)

day2 = now.strftime('%H시 %M분 %S초')
print(day2)
```

```
Tuesday 17. August 2021
13시 55분 37초
```

<br/><br/>

반대로 문자열로부터 날짜와 시간 정보를 읽어서 datetime 클래스 객체를 만들기  

```python
import datetime

now = datetime.datetime.strptime("2021-08-16 13:57", "%Y-%m-%d %H:%M")
print(now)
```

```
2021-08-16 13:57:00
```


<br/><br/>



> ## **2 date 클래스**  
<br/><br/>

datetime 내장 모듈의 date 클래스는 날짜를 표현하는데 사용됩니다.  
date 클래스의 생성자는 연, 월, 일 데이터를 인자로 받습니다.  
<br/>



```python
import datetime

now = datetime.date(2021, 1, 1)
print(now)
```

```
on01/a.py"
2021-01-01
```

<br/><br/>



오늘 날짜를 얻고 싶다면 date 클래스의 today() 메서드를 사용합니다.  
<br/>

```python
import datetime

now = datetime.date.today()
print(now)

```

```
2021-08-17
```

<br/><br/>


date 클래스의 isoformat() 메서드는  
date 객체를 YYYY-MM-DD 형태의 문자열로 변환해줍니다.  
<br/>

```python
import datetime

now = datetime.date.today()
print(now, type(now))

now_str = datetime.date.today().isoformat()
print(now_str, type(now_str))
```

```
2021-08-17 <class 'datetime.date'>
2021-08-17 <class 'str'>
```

<br/><br/>


반대로 date 클래스의 fromisoformat() 메서드는  
YYYY-MM-DD 형태의 문자열을 date 객체로 변환해줍니다.  
<br/>

```python
import datetime

now = datetime.date(2021, 1, 2)
print(now)
print(type(now))
```

```
2021-01-02
<class 'datetime.date'>
```

<br/><br/>


date 객체가 보관하고 있는 연, 월, 일 데이터는 각각 year, month, day 속성을 통해 접근할 수 있습니다.  
<br/>



```python
import datetime

today = datetime.date.today()
print(today)
print(today.year)
print(today.month)
print(today.day)
```

```
2021-08-17
2021
8
17
```  

<br/><br/>


date 클래스의 weekday()  
해당 날짜가 무슨 요일인지를 파악하기 위해서 사용됩니다.  
월요일이 0으로 시작  
<br/>

date 클래스의 isoweekday()  
해당 날짜가 무슨 요일인지를 파악하기 위해서 사용됩니다.  
월요일이 1로 시작
<br/>


```python
import datetime

today = datetime.date.today()
print(today)
print(today.weekday())     
print(today.isoweekday())
```

```
2021-08-17
1
2
```  
