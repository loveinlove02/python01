---
layout: single
title:  "01 파이썬 출력"
---

>## **print()**

<br/>

|자료형|의미|예시|기호|
|:--:|:--:|:--:|:--:|
|int|정수|1, 0, 100, -1|%d|
|float|실수|1.0, 1.23, -1.2|%f|
|str|문자열|'hello', '123'|%s|


<br/>

```python
# 숫자를 출력 : 정수
print(123)    

# 숫자를 출력 : 실수
print(1.23)

# 글자를 출력할 때는 '' 따옴표 또는 "" 사이에 적는다.
print('안녕하세요.')
print("hello world")

# 숫자를 따옴표 안에 적으면 글자로 취급
print('123')
print('1.23')
```   

```
123
1.23       
안녕하세요.
hello world
123
1.23
```   
<br/>

```python
# 변수 : 데이터(100, 1.23, 'hello')를 저장하는 그릇
# 저장된 값을 바꿀 수 있다. 가져와서 사용할 수 있다

a = 10      # 변수 a에 10을 넣는다. (대입)
print(a)

b = 1.23    # 변수 b에 1.23을 넣는다. (대입)
print(b)

c = 'hello' # 변수 c에 글자 hello를 넣는다. (대입)
print(c)

print(a, b, c)  # 한 줄에 출력
```   

```
10
1.23
hello        
10 1.23 hello
```   
<br/>

```python
a = 10       # 변수 a에 10을 넣는다. (대입)
b = 1.23     # 변수 b에 1.23을 넣는다. (대입)
c = 'hello'  # 변수 c에 글자 hello를 넣는다. (대입)

print('a는', a, '입니다')
print('b는', b, '입니다')
print('c는', c, '입니다')
```   

```
a는 10 입니다
b는 1.23 입니다
c는 hello 입니다
```  


<br/>


>int   - %d  
float - %f  
str   - %s  

<br/>

```python
print('' %() )
```   

<br/>


```python
print('%d %f %s' %(100, 1.23, 'hello'))
```   

```
100 1.230000 hello
```  

<br/>


```python
a = 10
b = 1.23
c = 'hello'

print('%d %f %s' %(a, b, c))
```   

```
10 1.230000 hello
```  

<br/>


```python
a = 10
b = 1.23
c = 'hello'

print('a : %d' %(a))
print('b : %f' %(b))
print('c : %s' %(c))
```   

```
a : 10
b : 1.230000
c : hello
```  
<br/>

```python
a = 1.23

# %d로 출력하면 1만 출력 됨
print('a : %d' %(a))

# %f로 출력하면 소수 6자리까지 출력    
print('a : %f' %(a))

# %.2f의 의미는 반올림 해서 소수 2자리까지 출력    
print('a : %.2f' %(a))  
```   

```
a : 1
a : 1.230000
a : 1.23
```  

<br/>


```python
a = 10
b = 1.23
c = 'hello'

# 10칸을 확보하고 오른쪽에서부터 출력
print('%10d' %(a))

# 10칸을 확보하고 오른쪽에서부터 출력(소수 2자리)      
print('%10.2f' %(b))

# 10칸을 확보하고 오른쪽에서부터 출력    
print('%10s' %(c)) 
```   

```
        10
      1.23
     hello
```  
