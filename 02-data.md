# 💾 자료 (Data)

* 컴퓨터에 전달하려는 정보(자료, data)
* 자료의 형태
  * 숫자, 문자, 문자열, 불
* 자료의 구조
  * 리스트, 튜플, 딕셔너리, 집합



## 자료형(데이터타입, data type)

* 컴퓨터에 전달하려는 정보(자료, data)의 형태 (데이터를 나타내는 방법)

* 리스트, 튜플, 딕셔너리, 집합, 불 (몇몇은 자료구조)



### 자료의 형태는 왜 구분할까?

* 실생활에서 자료의 형태
* 학번, 영화관 매표소에서의 줄, 사전, 공동체, 바이러스감염orNot
* 데이터의 처리를 편리하게 하기 위해
* 문제 환경에 따라 데이터의 처리를 편리하게 하기 위해



### 자료는 어떻게 저장할까? (변수, variable)

* 변수명 = 자료
* var = "oh"
* var = 123
* type(123)
* type("oh")
* type(var)



## 숫자형 (Numbers)

* 숫자를 나타내는 자료
* 정수, 실수, 8진수, 16진수
* 연산
  * 덧셈, 뺄셈, 곱셈, 나눗셈
  * 제곱, 몫, 나머지

* 직접 해보자

```
3 + 4
3.5 - 10
a = 3
b = 4
a + b
a - b
a * b
a / b
a // b
a % b
a ** b
```

* 몫과 나머지 구하기는 언제 쓰일까?
  * 몫, 나머지 따로 구할 때
  * 짝수, 홀수 구분?
  * 2의 배수?



## 문자열 (String)

* 문자로 구성된 자료

```
"Just do it"
'Just do it'


"Let's do it"
'Let's do it' -> 'Let\'s do it'


'say "hi"'
"say "hi"" -> "say \"hi\""


''' 
산책하기 딱인 온도와
그녀의 발엔 Nike 운동화
I like your style, baby
'''


"""
회색 hoodie 위 가방은 네이비 색
찰랑이는 머릿결은 wavin' flag
그녀의 걸음걸이, 느낌 있게
"""


```



### 이스케이프 코드 (escape)

* print("nike \n 운동화")
* 대표 이스케이프 코드 [^escape]

| 코드   | 설명                                                    |
| :----- | :------------------------------------------------------ |
| `\n`   | 문자열 안에서 줄을 바꿀 때 사용                         |
| `\t`   | 문자열 사이에 탭 간격을 줄 때 사용                      |
| `\\`   | 문자 `\`를 그대로 표현할 때 사용                        |
| `\'`   | 작은따옴표(`'`)를 그대로 표현할 때 사용                 |
| `\"`   | 큰따옴표(`"`)를 그대로 표현할 때 사용                   |
| `\r`   | 캐리지 리턴(줄 바꿈 문자, 현재 커서를 가장 앞으로 이동) |
| `\f`   | 폼 피드(줄 바꿈 문자, 현재 커서를 다음 줄로 이동)       |
| `\a`   | 벨 소리(출력할 때 PC 스피커에서 '삑' 소리가 난다)       |
| `\b`   | 백 스페이스                                             |
| `\000` | 널 문자                                                 |

* 아래 문자열을 한 줄의 명령으로 출력하세요.

> 나는 취미가 '파이썬'입니다. 
>
> 미래에 		"구글"에		들어갈거에요.
>
> 문자열에서 '줄바꿈'은 \n 이래요.



### 문자열 연산

* 문자열 더하기 (문자열 연결)
* 문자열 반복 (같은 문자열 반복)

```
print("Just" + "do" + "it" + "!")
print("Just" + " " + "do" + " " + "it" + "!")
print("Just" + " " + "do" + " " + "it" + "!" * 5)

head = "Python"
tail = " is fun!"
head + tail

head * 2

print("=" * 50)
print("hello world!")
print("=" * 50)

```



### 문자열 길이 구하기

* 문자열에 포함되어 있는 전체 문자 개수(이스케이프 코드 포함)

```
lyric = "더 붉게 타 저 멀리 번져도 돼 깜짝 놀란 나의 맘이 타오르게"
len(lyric)
```



### 문자열 안에 있는 문자에 접근

```
print(lyric[0])
print(lyric[1])
print(lyric[2])
print(lyric[3])
print(lyric[-1])
print(lyric[-2])
```



### 문자열 연산

```
burning_my_mind = lyric[27] + lyric[28] + lyric[29] + lyric[30] + lyric[31] + lyric[32] + lyric[33]
```



### 문자열 자르기

* 문자열변수[시작번호:끝번호]
* 문자열변수[시작번호:]
* 문자열변수[:끝번호]
* 문자열변수[:]

```
surprise = lyric[18:23]
red = lyric[:4]
remove_more = lyric[2:]
verse = lyric[:]
```



### 언제 문자열을 자를까?

* 전처리에 아주 유용

```
messy = "20210724한남"
```

* 날자와 장소를 분리해서 출력해보세요
* 년, 월, 일, 장소를 분리해서 출력해보세요
* 년-월-일 로 출력해 보세요 (예: 2020-07-17)
* 년-월-일, 장소로 출력해 보세요 (예: 2020-07-17, 한남)



## 리스트 (List)

* [ ] 데이터들의 한데 모아 사용할 수 있는 자료형태
* [ ] 로 표현 
* list_name = [] 와 같은 형태로 초기화할 수 있음
  * 초기화 = 빈 값으로 자료를 저장할 공간(변수, 리스트, 딕셔너리 등)을 만드는 것
  * 리스트에서 []는 아무것도 없는 빈 리스트를 의미

```
리스트이름 = [데이터1, 데이터2, 데이터3, ... ]
```



### 리스트의 생김새

```
empty_list = []
num = [1, 2, 3]
words = ['nike', 'shoes', 'on', 'my', 'feet']
mixed = [1, 2, 3, 'nike', 'shoes']
list_in_list = [1, 2, ['리스트', '안에', '리스트']]
empty_list_init = list()
```



### 리스트 인덱싱

```
list_index = [1, 2, 3]
list_index[0]
list_index[1]
list_index[2]
list_index[0] + list_index[1]
list_index[-1]

list_index = [1, 2, 3, ['nike', 'shoes', 'on']]
list_index[0]
list_index[3]
list_index[-1]
list_index[3][0]
list_index[3][1]
list_index[3][2]
list_index[-1][2]

list_index = [1, 2, 3, ['nike', 'shoes', ['on', 'my', 'feet']]]
```

* 가장 마지막 list_index 리스트에서 2를 출력해보자
* nike를 출력해보자
* my를 출력해보자
* feet의 t를 출력해보자



### 리스트 슬라이싱

* 리스트의 내용물을 잘라서 사용할 수 있음

```
slicing_test = [1, 2, 3, 4, 5]
slicing_test[0:2]

slicing_test = "Naive Set Theory"
slicing_test[0:2]

slicing_test = [1, 2, 3, 4, 5]
slicing_result = slicing_test[:2]
slicing_result = slicing_test[2:]
slicing_result = slicing_test[:]
```

* 중간 slicing_test에서 "Set Theory"만 출력되게 해보자
* 가장 마지막 slicing_test에서 2, 3, 4만 출력되게 해보자



### 리스트 연산

* 연산 ( +, * ) 가능

```
list_op1 = [1, 2, 3]
list_op2 = [4, 5, 6]

list_op1 + list_op2
list_op1 * 3
```



### 리스트 길이구하기

* len(리스트) 로 리스트의 길이를 구할 수 있음
* 리스트길이 외에도 다른 자료형 데이터의 길이를 구할 때 사용할 수 있음

```
list_length = [1, 2, 3, 4, 5]
len(list_length)
```



### 리스트의 수정과 삭제

* 리스트 인덱스로 리스트 원소에 직접 접근하여 수정하거나 삭제할 수 있음

```
list_modify = [1, 2, 3]
list_modify[2] = 7
list_modify

del list_modify[1]
list_modify
```



### 리스트 관련 함수들

* 리스트 이름 뒤에 . 을 붙여서 리스트를 수정하거나 변형하는 함수 사용가능
* 리스트에 원소 추가 (append)
  * 리스트의 맨 마지막에 새로운 원소를 추가

```
list_practice = [1, 2, 3]
list_practice.append(4)
list_practice

list_practice.append([5, 6])
list_practice
```



* 리스트 정렬(sort)
  * 리스트의 원소들을 순서대로 정렬함

```
list_practice = [1, 9, 8, 3, 2, 5, 4, 7, 6]
list_practice.sort()
list_practice

list_practice = ['z', 'f', 'a', 'b', 'd', 'e']
list_practice.sort()
list_practice
```



* 리스트 뒤집기(reverse)
  * 리스트의 원소를 역순으로 배열함 (정렬은 하지 않음)

```
list_practice = ['b', 'c', 'z']
list_practice.reverse()
list_practice
```



* 위치 반환(index)

```
list_practice = ['apple', 'banana', 'cereal']
list_practice.index('cereal')
list_practice
```



* 리스트에 원소 삽입(insert)
  * 원하는 위치에 데이터를 삽입
  * insert(a, b) 
  * a 번째 위치에 b를 삽입 (주의. 인덱스는 0부터 시작함)

```
list_practice = [1, 2, 3]
list_practice.insert(0, 4)
list_practice

list_practice.insert(3, 5)
list_practice
```



* 리스트 원소 제거(remove)
  * 원하는 위치의 데이터를 제거
  * remove(인덱스 번호)
  * 해당 인덱스 번호의 원소를 제거

```
list_practice = [1, 2, 3, 4, 5]
list_practice.remove(3)
list_practice

list_practice = ['apple', 'banana', 'cereal']
list_practice.remove(1)
list_practice
```



* 리스트 원소 꺼내기(pop)
  * 리스트의 맨 마지막 원소를 꺼내고 리스트 안에서 그 원소는 삭제함

```
list_practice = [1, 2, 3]
list_practice.pop()
list_practice

pop_result = list_practice.pop()
list_practice
pop_result
```



* 리스트에 포함된 특정 원소의 개수 세기(count)
  * 리스트 안에 해당 원소가 몇 개 있는지 알려줌

```
list_practice = ['apple', 'banana', 'milk', 'cereal', 'orange', 'apple']
list_practice.count('apple')
list_practice = [1, 2, 3, 2, 1]
list_practice.count(1)
list_practice.count(2)
list_practice.count(3)
list_practice.count(4)
```



* 리스트 확장(extend)
  * 리스트에 리스트를 추가함

```
list_practice = [1, 2, 3]
list_practice.extend([4, 5])
list_practice

list_practice.extend([6, 7, 8, 9])
list_practices

list_practice = list_practice + [10, 11]
list_practice
```



### 🔥 해보자

1. 아래 리스트의 4번째 값을 0으로 변경해보자

```
weights = [55.4, 60, 65.2, 'NA', 57.3, 61.1, 56.5]
```

* weight 리스트의 4번째 값을 모든 원소의 평균값으로 변경해보자 (평균은 'NA'를 제외한 모든 원소를 더하고 원소 개수로 나누어 구하자)

* len 함수를 사용하여 weights 리스트의 가장 마지막 값을 60으로 변경해보자

* weight 리스트 값을 크기 순으로 정렬해보자

* 정렬한 리스트 순서를 뒤집어보자



2. 아래 리스트의 마지막에 'Symbol'을 추가해보자

```
stock = ['Region','Exchange','Index','Currency']
```

* stock 리스트에서 2번째 원소를 삭제해보자

* stock 리스트의 길이를 구하고 이를 사용하여 맨 끝에서 두번째와 맨 끝 사이에 'Code'를 넣어보자

* 'Exchange'의 index 값을 출력해보자



3. 아래 리스트에서 'Run'이 몇 번 들어가 있는지 출력해보자

```
sneakers = ['하늘에', '펼쳐', '주문을', '걸어', 'forever', 'young', 'Run', 'Run', 'Run', 'Make', 'a', 'run', 'Run', 'Run', 'Run', '멈추고', '싶지', '않아']
```



4. sneakers 리스트에 아래 extra_verse 리스트를 연결해보자

```
extra_verse = ['고요하게', '어둠', '속에', '잠겨가는', '순간', '빛난', '저', '별과']
```



5. 아래 리스트에서 '\n'의 index번호를 출력해보자

```
ha = ['이끌어', '줘', '\n', 'Fly', 'away']
```

* ha 리스트에서 '\n'을 제거해보자



6. lyric 리스트에서 '\n'이 몇 번 쓰였는지 출력해보자

```
lyric = ['그', '언제나', '상상했던', '\n', '숲으로', '날', '데려가', '\n']
```

* lyric 리스트에서 '\n'을 모두 제거해보자



## 튜플 (Tuple)

* 리스트와 거의 비슷
* ( )로 표현
  * tuple_practice = (1, 2, 3)
  * tuple_practice = ('a', 'b', ('abc', 'def'))
* 리스트와의 차이
  * 리스트는 원소의 값을 바꿀 수 있음
  * 튜플은 원소값을 바꿀 수 없음
  * 프로그램 중간에 값을 바꾸지 않아야할 경우가 있다면 튜플을 써도 되나 리스트를 더 많이 씀 (프로그램 실행 중에 변화되는 경우가 훨씬 많기 때문)



## 딕셔너리 (Dictionary)

* 말그대로 사전과 같은 형태
* 단어 : 뜻 설명
* key를 보고 key가 나타내는 value를 사용할 수 있음
* {}로 표현

| 단어 | 뜻                                                           |
| ---- | ------------------------------------------------------------ |
| 야곱 | 이삭과 리브가의 아들로 쌍둥이 형 에서의 발 뒤꿈치를 잡고 태어났다. |
| 바울 | 예수님의 인격과 사역의 의미를 해석하는 데 있어서 가장 큰 공헌을 한 신약 시대의 인물이다. |
| 하늘 | 지평선이나 수평선 위로 보이는 무한대의 넓은 공간             |



### 딕셔너리 예시

* 앎사전 = { 성별 : 여, 국적 : 한국,  취미 : 파이썬}
* 태킴사전 = { 이름 : itk, 전번 : 01012345678, 직업 : 데이터과학자 }

```
itk_dic = {'name' : 'itk', 'phone' : 01012345678, 'job' : 'data_scientist'}
```

| key   | value          |
| ----- | -------------- |
| name  | itk            |
| phone | 01012345678    |
| job   | data_scientist |



### 딕셔너리를 만드는 방법

* key : value
  * {key1:value1, key2:value2, key3:value3, ...}
  * 키(key) 이름으로 숫자, 문자열 사용 가능
  * 키는 중복되면 안됨 (하나만 인식됨)

```
딕셔너리이름 = {키1 : 값, 키2 : 값, 키3 : 값, ....}
```



### 딕셔너리 쌍 추가, 삭제

* 추가
  * dictionary_name[key] = value
* 삭제
  * del dictionary_name[key]

```
arm_dict = {1 : 'blackberry'}
arm_dict

arm_dict[2] = 'writer'
arm_dict

arm_dict['hair'] = 'red'
arm_dict

arm_dict[3] = [1, 2, 3]
arm_dict

del arm_dict[3]
arm_dict

del arm_dict['har']
arm_dict
```



### 딕셔너리는 왜 만들까?

* 딕셔너리
  * 여러 데이터로 구성된 하나의 데이터집합
* 데이터집합을 특징별로 묶을 때 편리함
  * 변수 => 하나의 데이터만 가지고 있음
  * 리스트 => 인덱스 번호로 데이터(원소)를 분류
  * 딕셔너리 => 키(key)로 데이터를 분류할 수 있음 (key로 데이터의 특징을 나타낼 수 있음)



```
순원1 = {
            이름 : 김민주, 
            성별 : 여, 
            번호 : 01012345678,
            전공 : 컴퓨터공학,
            생일 : 2001-02-05
	}

순원2 = {
            이름 : 정수정, 
            성별 : 여, 
            번호 : 010910111213,
            전공 : 수학,
            생일 : 1994-10-24
	}

hanul_futsal = {'팀장' : '한승주', 
								'총무' : '김익태', 
								'매니저' : '최아름', 
								'팀원' : 서성원
	}
```



### 딕셔너리의 활용

* 키로 값을 얻음
* 딕셔너리이름[키]

```
author = {
						'Matthew' : 'Matthew',
						'Mark' : 'Markos',
						'Romans' : 'Paul',
						'Philippians' : 'Paul'
}

author['Romans']
author['Mark']

bible = {
					1 : 'Genesis',
					2 : 'Exodus',
					3 : 'Leviticus',
					4 : 'Numbers'
}

bible[1] # 주의, 키값은 0부터 시작하는 리스트의 인덱스 번호 순서와 다름
bibl3[3] 

bible = {1 : 'Genesis', 2 : 'Exodus', 1 : 'Matthew'}
bible[1] # 주의, 키 값이 같으면 하나만 인식됨
```



### 🔥 해보자

* 자신의 정보에 대한 딕셔너리를 만들고 모든 키에 대한 값을 하나씩 출력해보자
  * name, hobby, birth, phone



### 딕셔너리 관련 함수

* key만 얻기 - keys()
  * 딕셔너리의 키들을 dict_keys라는 이름의 '객체'로 만들어줌
  * dictionary_name.keys()

```
author = {
						'Matthew' : 'Matthew',
						'Mark' : 'Markos',
						'Romans' : 'Paul',
						'Philippians' : 'Paul'
}

author.keys()
```



* value만 얻기 - values()
  * 딕셔너리의 값(value)들만 dict_values라는 이름의 객체로 만들어줌

```
author.values()
```



* key, value 함께 얻기 - items()
  * dictionary_name.items()

```
author.items()
```



* key, value 쌍 모두 지우기 - clear()
  * 딕셔너리의 key, value를 모두 지움
  * 빈 값 {} 반환 (딕셔너리는 {}로 표현된다는 것을 기억하자)

```
author.clear()
author
```



* key값 가져오기 - get()
  * dictionary_name[key] 와 같음
  * 없는 key를 가져오려고할 경우 반환되는 값이 다름
    * dictionary_name[key]일 경우 에러
    * dictionary_name.get(key)일 경우 None



* 특정 Key가 딕셔너리 안에 있는지 조사 - in
  * 'key_name' in dictionary_name

```
'Jerusalem' in author
'조선왕조실록' in author
'Matthew' in author
```



### 딕셔너리의 또다른 생성방법(초기화)

* dictionary_name = dict() 와 같은 형태로 생성할 수 있음
* 생성된 딕셔너리는 빈 값 {} 을 가짐
* 인덱스번호로 딕셔너리 값을 추가할 수 있음 (리스트처럼 사용가능)

```
dataset = dict()
dataset

dataset[0] = {'no':1, 'artist':'하성운', 'title':'sneakers'}
dataset[1] = {'no':2, 'artist':'NCT Dream', 'title':'Hot Sauce'}
dataset[2] = {'no':3, 'artist':'여자친구', 'title':'MAGO'}
dataset
dataset[0]
dataset[0]['artist']
dataset[0]['title']
dataset[1]['artist']
dataset[2]['title']
```



### 🔥 해보자

1. 아래 표를 딕셔너리로 만들어보자

| no   | artist | title    | lyrics          |
| ---- | ------ | -------- | --------------- |
| 1    | 하성운 | 스니커즈 | eh oh yeah yeah |

  

* 만든 딕셔너리의 모든 key 를 출력해보자
* 모든 value를 출력해보자
* key와 value를 모두 출력해보자
* Title key의 value를 출력해보자
* Currency key의 value를 출력해보자
* 각 딕셔너리에 'comment' key가 있는지 확인해보자

  

2. 아래 표를 딕셔너리로 만들어보자 

| Region        | Exchange                | Index | Currency |
| ------------- | ----------------------- | ----- | -------- |
| United States | New York Stock Exchange | NYA   | USD      |
| Europe        | Euronext                | N100  | EUR      |
| Korea         | Korea Exchange          | KS11  | KRW      |

  



## 불 (Bool)

* 참 또는 거짓을 나타내는 자료형
  * 참, 거짓
  * 있다, 없다
  * 0, 1
* True 또는 False로 표현함
  * 글자 그대로 '진짜' 또는 '거짓'으로만 생각하면 안됨
  * ''맞다' 또는 '틀리다'
  * '있다' 또는 '없다' 
  * 이런 의미일 수도 있음
* True, False도 예약어 이므로 변수, 함수, 클래스 등의 이름으로 사용할 수 없음

```
bool_data = True
type(bool_data)

bool_data = False
type(bool_data)
```

* 대소비교 예시

```
1 == 1
2 > 1

alps = 4808
rocky = 4398
taebaek = 1708

alps < taebaek
alps > rocky
rocky == taebaek
```

* 조건 예시
  * "어떠한 조건이 True이면 이것을 False이면 저것을 해라"
  * "어떠한 조건이 1이면 이것을 0이면 저것을 해라"

```
how_bool_works = [1, 2, 3, 4, 5]

while how_bool_wokrs:
	print(how_bool_works.pop())
```

```
if []:
	print("참")
else:
	print("거짓")
```

```
if [1, 2, 3]:
	print("참")
else:
	print("거짓")
```



### 불연산

* True 또는 False를 판단하는 연산
* 0 또는 1를 판단하는 연산
* '있다' 또는 '없다'를 판단하는 연산

```
bool(True)
bool('python')
bool('')
bool("")
bool([])
bool()
bool(123)
```



### References

[^escape]: https://wikidocs.net/13

