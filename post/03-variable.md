# 변수 (Variable)

### 변수?

* 데이터를 임시로 저장하는 공간
* 임시로 저장?
  * 현재 코드 안에서만 사용됨 
  * 즉, 코드가 종료되면 (= 프로그램이 종료되면) 변수와 그 안에 있는 데이터는 사라짐
  * 메모리(Main memory a.k.a Random Access Memory)에 저장됨

* 데이터의 형태에 따라 변수의 형태가 결정됨 (예. 숫자형, 문자형, 리스트 등)



### 변수이름?

* 변수의 이름이 임시로 저장되는 공간을 나타냄 (예. 사물함)
  * 실제 메모리에 저장되는 위치는 0x1208AB09 과 같이 숫자 주소로 나타냄
* 0x1208AB09은 너무 투박하니 좀 더 인간이 잘알아 들을 수 있는 단어로 표현하자

```
age = 22
date = '2021-07-30'
order_list = ['apple', 'banana', 'orange']
```



### 변수이름을 만드는 규칙 (naming convention)

* 누가 봐도 어떤 데이터를 가지고 있는지(information) 알 수 있도록 이름을 짓자 (meta-data가 포함되도록)
* 코드를 작성할 때 보다 읽을 때가 더 많다
  * 제대로 이름을 짓지 않으면 🐶 고생
* 변수뿐만 아니라 함수, 클래스 등과 같은 이름을 지을 때에도 동일하게 적용
* Style Guide
  * [Google Python Style Guide](https://google.github.io/styleguide/pyguide.html)



### Python Naming Convention

* [PEP8 Style Guide](https://www.python.org/dev/peps/pep-0008/)
* 대략 알아보자
  * 소문자로 시작
  * 밑줄 '_' 사용 가능
  * 중간 줄 ' - ' 사용 불가
  * 공백 사용 불가
  * 예약어 사용 불가
    * import, for, if 등등
    * 사용하고 싶으면 뒤에 _ (밑줄)을 붙여서 써도 되지만.. 
    * 항상 헷갈리지 않도록 하자
  * 숫자로 시작불가
  * 특수문자 사용불가
  * 대소문자 구별됨
  * 동일한 이름을 변수, 함수, 클래스에 함께 사용 불가
* 함수, 클래스의 이름과 그 안(?)에 있는 변수들의 이름을 지을 때는 또다른 규칙이 적용됨 (차차 알아보자)



### 변수이름 예시

* 데이터가 가지고 있는 정보를 잘 나타내게 하자

```
abc = 31
print("age = ", abc)

age = 31
print("age = ", age)
```



* 줄여쓰지 말자 (모두 알아들을 수 있게)

```
jmt = 'steak'
user_favorite_food = 'steak'
```



* 의미가 불분명한 표현은 쓰지 말자 <sup>[ref](https://towardsdatascience.com/data-scientists-your-variable-names-are-awful-heres-how-to-fix-them-89053d2855be)</sup>

```
# Don't do this
temp = get_house_price_in_usd(house_sqft, house_room_count)
final_value = temp * usd_to_aud_conversion_rate

# Do this instead
house_price_in_usd = get_house_price_in_usd(house_sqft, 
                                            house_room_count)
house_price_in_aud = house_price_in_usd * usd_to_aud_conversion_rate
```



### Letter Case

* Camel Case

```
"theQuickBrownFoxJumpsOverTheLazyDog" or "TheQuickBrownFoxJumpsOverTheLazyDog"
```



* Snake Case

```
"the_quick_brown_fox_jumps_over_the_lazy_dog"
```



* Kebab Case

```
"the-quick-brown-fox-jumps-over-the-lazy-dog"
```



### 자료를 담는 공간 = 변수

* 어떤 자료에 어떤 자료형이 좋을까? 왜?

