2021-03-22    
c++에서 4.000 소수점 고정표기 하는 방법 ( fixed notation)   
cout << fixed 또는 << showpoint 입력후 << cout.precision(int number) 입력   
int number가 2라면 4.00까지 출력되고 아래는 반올림 한다.   


2021-03-23   
함수에서 여러개의 값을 리턴 하는 방법   
구조체 생성후 구조체의 멤버에 값을 입력하고 그뒤 방법이 두개   
1. 구조체 선언 및 초기화 하고 같은 함수 내에서 다른 함수에 파라미터로 전달   
2. 구조체 자체를 하나의 구조체 자료형 변수에 넣어준뒤 구조체 자료형 변수를 전달   
참고 : https://okky.kr/article/893651
이런 식으로도 가능하다   
```cpp
int function(int &a, int &b){
  cin >> a;
  cin >> b;

  return 0;
}

int main(){
  int a, b;
  int retn = function(a,b);
  // if retn else end if
  cout << a << endl;
  cout << b << endl;
  return 0;
}
```
