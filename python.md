
2021.03.17
- split()

split은 정적 메소드(인듯)
a, b = input().split('분류 기준')
인풋을 받아올 때 바로 스플릿해서 넣어줄 수 있음
입력예시 : 15:08
a, b = input().split(':')
print(a)
print(b)
결과
15
08

- sep='기준' (seperator의 약자)

스플릿은 서로 다른 두개의 변수를 기준으로 이어 붙여 준다
a = 'a'
b = 'b'
print(a, b, sep='-')
결과
a-b


 - %d, %s, %x formating 문자열 포매팅   
 %s : string   
 %d : integer   
 %f : float   
 %o : 8진수(Octa)    
 %x : 16진수(heXadeciaml)        
 %% : % (%라는 문자 자체를 출력하기 위해선 \(백슬래시)가 아니라 %%로 써야한다.         
         
 문자열에 문자가 아닌 다른 값을 넣기 위해서 포매팅을 한다        
 예시)           
 "I have %s apples" % 3 #이경우 3이라는 숫자는 %s때문에 string으로 변환되어 입력된다          
 
 기본적으로 f-string을 파이썬 3.6부터 지원하기때문에 잘 쓰지 않는 기능이지만         
 파이썬이 아닌 다른 문법은 위와같은 포매팅만 지원하는거 같으니 알아두어야겠다          
 
 그리고 8진수 16진수의 경우는          
 n = input(number)          
 "%x"%n #이런 형식으로 작성하면 숫자 n을 %x(16진수)로 변환해준다.         

- chr   
아스키 코드 값을 *입력* 받아 문자로 변환시켜 준다.   
>>> chr(97)   
>>> 'a'   

- ord   
chr험수와 반대로 문자 -> 아스키코드 로 변환해준다   

- list comprehension   
```python
list = [i for i in range(10) if i % 2 == 0]
# [0, 2, 4, 6, 8]

**You should use list comprehension to make Two-dimensional array**
dimension_array = [[0] * 4 for i in range(3)]
# [[0, 0, 0, 0], [0, 0, 0, 0], [0, 0, 0, 0]]

- 파이썬 고정 소수점 출력   
print('%.3f'%n)   
.3은 소수점 4째 자리에서 반올림해서 3째자리 까지만 출력한다.   
n은 출력하고 싶은 숫자   


- 2의 거듭제곱 출력   
```python   
a = 2
b = 10
print(a<<b)
# 결과 : 1024
# <<, >>비트단위 시프트 연산자라고 해서 비트로 (2진수)로 연결된 값에 number << 1 이면 01010을 010100으로 전체 숫자 뒤에0을 붙이고 다른것들을 이동시킨다
```   

- for문 안에서 글로별 변수를 이용한 포맷팅
```python
a1 = 'A'
a2 = 'B'
a3 = 'C'

char_list = []

for i in range(1, 4):
    char_list.append(globals()[f"a{i}"]
```
a1, a2, a3처럼 단순히 숫자로만 구분되어진 변수를 반복문에서 처리하는데   
for문 안에서 생성되는 변수 i와 문자a를 합쳐서 a1, a2, a3로 자동으로 처리해줄 방법을 고민하다 globals()를 이용했다.   
globals()는 전역변수 초기화에 주로 사용되는데 위와 같이 특별한 값을 입력해주지 않으면
전역'변수'이름으로 간주된다
