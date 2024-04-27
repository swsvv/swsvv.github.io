## f-string이란?
* 문자열 중간에 변수를 사용하여 문자열을 구성하는 방법


## 사용방법
* 문자열 앞에 f를 붙임
* 문자열 중간에 변수를 넣을 부분에 {변수명}과 같이 사용
* 예시1
    ```
        community = 'sns'
        welcome_sentence = f"이곳은 {community}공동체 입니다!"
        print(welcome_sentence)
    ```
* 예시2
    ```
        community = 'sns'
        group = 'knowing'
        print(f"이 곳은 {community}, {group}입니다!")
    ```
