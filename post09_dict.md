---
layout: single
title:  "08 set"
---

>## **dict**

<br/>

딕셔너리(사전) 자료형은 연관되어있는 데이터를 하나의 쌍으로 묶어서 관리하는 자료형입니다.
<br/>

다음과 같이 학생 정보는 번호와 이름으로 구성되어 있습니다.
<br/>

|**번호**|**이름**|
|:--:|:--:|
|12345|이인환|
|12346|김민정|
|12350|정민수|
|12390|정지훈|
|12398|박지혜|

<br/>

위와 같은 학생정보를 저장하기 위해서는 딕셔너리를 사용하면 편리합니다.  
<br/>

딕셔너리는 { } 안에  
<font color="orange">키</font>와 <font color="orange">값</font>이 쌍으로 되도록 작성합니다.
<br/>  


|**딕셔너리**|
|:--|
|딕셔너리 이름 = {‘키’: 값1, 값2, 값3, ... }|

<br/>

### **1. 빈 딕셔너리 만들기**  

<br/>

빈 딕셔너리를 만들 때는 { } 또는 dict() 함수를 사용합니다.
<br/>


***빈 딕셔너리 만들기***  

```python
emptyDict1 = dict()
emptyDict2 = {}

print(emptyDict1, type(emptyDict1))
print(emptyDict2, type(emptyDict2))
```

```
{} <class 'dict'>
{} <class 'dict'>
```

<br/><br/>


### **2. 데이터가 있는 딕셔너리 만들기**  

<br/>

{ } 를 사용해서 데이터가 있는 딕셔너리를 만들 수 있습니다.  


***데이터가 있는 딕셔너리 만들기***
```
dic = {'name':'홍길동', 'age': 20, 'phone':'010-1234-5678'}

print(dic)
```  


```
{'name': '홍길동', 'age': 20, 'phone': '010-1234-5678'}
```  

<br/><br/>


### **3. 딕셔너리 사용하기**  

<br/>

#### **(1) 데이터 추가 및 수정하기**

<br/>

키를 phone으로 하고 010-1234-5678을 값으로 해서  
딕셔너리에 데이터를 추가하는 예제입니다.  
<br/>

***데이터 추가하기***  

```python
dic = {'name':'홍길동', 'age': 20}

# 키는 phone, 값은 010-1234-5678
dic['phone'] = '010-1234-5678'

print(dic)
```  

```
{'name': '홍길동', 'age': 20, 'phone': '010-1234-5678'}
```  

<br/>

다음과 같이 딕셔너리에 있는 키를 넣게 되면  
기존에 있는 데이터를 수정하게 됩니다.  
<br/>

***데이터 수정하기***  

```python
dic = {'name':'홍길동', 'age': 20, 'phone':'010-1234-5678'}
dic['name'] = '이순신' # 홍길동을 이순신으로 수정

print(dic)
```  

```
{'name': '이순신', 'age': 20, 'phone': '010-1234-5678'}
```  

<br/><br/>


#### **(2) 데이터 삭제하기**

<br/>

|**데이터 삭제**|
|:--|
|del 딕셔너리 이름[키]|
|del 딕셔너리 이름|  

<br/>

***데이터 삭제하기***  
```python
score = {'kor':80, 'eng':90, 'mat':97}

# 키가 eng인 데이터를 딕셔너리에서 삭제합니다.
del score['eng']

print(score)
```  

```
{'kor': 80, 'mat': 97}
```  

<br/>


***딕셔너리를 통째로 삭제***  
```python
score = {'kor':80, 'eng':90, 'mat':97}
del score
```

<br/><br/>



### **4. 딕셔너리 메소드**  

<br/>

문자열, 리스트, 튜플, 집합 메소드와 같이  
딕셔너리에서만 사용 가능한 집합 메소드가 있습니다.  

<br/>

#### **(1) 데이터 추가하기 / 가져오기**  

<br/>


|**setdefault(키)**|
|:--|
|딕셔너리 이름.setdefault(키, 값)|
|딕셔너리 이름.setdefault(키)|  

<br/>

***데이터 추가하기 1***  

```pyton
score = {'kor':80, 'eng':90, 'mat':97}
score.setdefault('computer', 100)

print(score)
```  

```
{'kor': 80, 'eng': 90, 'mat': 97, 'computer': 100}
```  

<br/>

***데이터 추가하기 2***  

```python
score = {'kor':80, 'eng':90, 'mat':97}
score.setdefault('computer')

print(score)
```  

```
{'kor': 80, 'eng': 90, 'mat': 97, 'computer': None}
```  

<br/><br/>


#### **(2) 데이터 삭제하기**  

<br/>

|**pop(키)**|
|:--|
|딕셔너리 이름.pop(키)|

<br/>

***데이터 삭제하기***  

```python
score = {'kor':80, 'eng':90, 'mat':97, 'computer':100}
score.pop('computer')

print(score)
```  

```
{'kor': 80, 'eng': 90, 'mat': 97}
```  

<br/><br/>


#### **(3) 딕셔너리 비우기**  

<br/>


|**clear()**|
|:--|
|딕셔너리 이름.clear()|

<br/>

***데이터 모두 삭제하기***  

```python
score = {'kor':80, 'eng':90, 'mat':97, 'computer':100}
score.clear()

print(score)
```  

```
{}
``` 

<br/>

#### **(4) 특정 키에 대한 값 가져오기**  

<br/>

|**get(키)**|
|:--|
|딕셔너리 이름.get(키)|

<br/>

***데이터 가져오기***  

```python
score = {'kor':80, 'eng':90, 'mat':97, 'computer':100}
data = score.get('computer')

print(data)
```  

```
100
```  

<br/>


#### **(5) 키를 모두 가져오기**  

<br/>

|**keys()**|
|:--|
|딕셔너리 이름.keys()|

<br/>

***모든 키를 가져오기***  

```python
score = {'kor':80, 'eng':90, 'mat':97, 'computer':100}
scoreList = list(score.keys())

print(scoreList)
```  

```
['kor', 'eng', 'mat', 'computer']
```  

<br/>

#### **(6) 값을 모두 가져오기**  

<br/>

|**values()**|
|:--|
|딕셔너리 이름.values()|

<br/>

***모든 값을 가져오기***  

```python
score = {'kor':80, 'eng':90, 'mat':97, 'computer':100}
scoreList = list(score.values())

print(scoreList)
```  

```
[80, 90, 97, 100]
```  

<br/>


#### **(7) 키와 값을 모두 가져오기**  

<br/>

|**items()**|
|:--|
|딕셔너리 이름.items()|

<br/>

***모든 키와 값을 가져오기***  

```python
score = {'kor':80, 'eng':90, 'mat':97, 'computer':100}
scoreList = list(score.items())

print(scoreList)
```  

```
[('kor', 80), ('eng', 90), ('mat', 97), ('computer', 100)]
```

<br/>
