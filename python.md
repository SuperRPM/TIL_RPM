
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
