---
title: "[정보처리기사] C언어"
layout: single
categories: Certificate
tag: [정보처리기사]
toc: true
toc_sticky: true
toc_icon: "bars"
toc_label: "Table of Contents"
use_math: true
---

# 포맷 스트링
변수 상세 출력 : 포맷 스트링을 이용해 정렬, 0 채우기, 출력할 공간 확보, 소수점 자릿수 표기를 지정할 수 있다.
- `％[-][0][전체자리수].[소수점자리수]스트링`
  - [-]를 붙이면 왼쪽 정렬
  - [-]를 붙이지 않고, [전체자리수]가 정해져 있을 경우 오른쪽 정렬
  - [0]을 붙이면 전체 자릿수에서 앞에 빈공간 만큼 0으로 채움
  - [전체자리수] 만큼 공간이 확보됨, 소수점(.)도 한 자릿수로 포함됨
  - .[소수점자리수]만큼 소수점이 출력됨, 실수형일 때만 적용됨
- 개념 예제
```c
#include <stdio.h>
void main( ){
  float a = 1.234;         // a라는 이름의 float(실수)형 변수를 선언하고, a는 1.234로 초기화
  int b = 10;              // b라는 이름의 int(정수)형 변수를 선언하고, b는 10으로 초기화
  printf( "%.2f\n", a);    // 소수점 둘째자리까지 표시
  printf( "%5.1f\n", a);   // 전체공간 다섯자리수가 정해져있으니 오른쪽 정렬, 소숫점 첫째 자리까지 표시
  printf( "%05.1f\n", a);  // 위에서 0을 채움
  printf( "%-05.1f\n", a); // 위에서 -만 붙였으니 왼쪽정렬
  printf( "%5d\n", b);     // 전체공간 5자리, 정수출력
  printf( "%05d\n", b);    // 전체공간 5자리, 정수출력, 앞에 0 채움
  printf( "%-5d\n", b);    // -가 붙었으니 왼쪽정렬
  printf( "%-05d\n", b);   // -가 붙었으니 왼쪽정렬(0은 무시)
}
```
- 출력  
１．２３  
　　１．２  
００１．２  
１．２  
　　　１０  
０００１０  
１０  
１０  

---

# 연산자
## 증감 연산자
1. printf 함수 내에서의 증감 연산자
```c
#indude <stdio.h>
void main(){
  int x=3, y=3,
  printf("%d", x++); // x의 값인 3을 먼저 출력하고, 이후에 x의 값을 1 증가시킴, 이제 x=4
  printf("%d", x);
  printf("%d", ++y); // y의 값을 1 증가시킨 후에 y의 값인 4를 출력 
  printf("%d", y);
}
```
- 출력  
3444

2. 다른 연산자와 함께 사용하는 증강 연산자 
```c
#indude <stdio.h>
void main(){
  int x=3, y=3;
  int z = x++ + ++y;           // x의 3을 연산에 사용하고 x를 증가시키고 , y의 값을 1 증가시킨 후에 y의 값인 4를 사용 3+4=7이 z에 저장됨
  printf("%d %d %d", x, y, z);
}
```
- 출력  
447

3. 증감 연산자 단독 사용
```c
#indude <stdio.h>
void main(){
  int x=3, y=3,
  x++; // x를 사용하고 x를 1증가, 이후 x=4
  ++y, // 4
  printf("%d %d", x, y); 
}
```
- 결과  
44


## 산술 연산자
```c
#include <stdio.h>
void main( ){
  int x=3, y=2,
  float z=2.0,
  printf("%d %d\n", x%y, y%x);
  printf("%d %.2f", x/y, x/z); 
}
```
- 출력  
1 2  
1 1.50


## 시프트 연산자
- `<<` : 왼쪽 값을 오른쪽 값만큼 비트를 왼쪽으로 이동하는 연산자
- `>>` : 왼쪽 값에 오른쪽 값만큼의 부호 비트를 채우면서 오른쪽으로 이동하는 연산자

```c
#include <stdio.h>
void main( ){
  int x=11;           // 11을 2진수로 바꾸면 1011
  printf("%d", x<<3), // 왼쪽으로 3비트 이동, 1011000을 다시 10진수로 변경, 64+16+8=88
  printf("%d", x>>1); // 오른쪽으로 1비트 이동, 101(맨 뒤에 한자리는 사라짐)을 다시 10진수로 변경, 4+1=5
}
```
- 출력  
885


## 관계 연산자
관계 연산자는 참이면 1을 , 거짓이면 0을 반환한다.  
C언어에서 논리식을 계산할 때, 0이면 거짓으로 인식 , 0이 아니면 참(1)으로 인식합니다.
```c
#include <stdio.h>
void main( ){
  printf("%d\n", 3==3);
  printf("%d\n", 3!=3); 
}
```
- 출력  
1  
0


## 비트 연산자
- `&`: AND 연산자
  - 두 값을 비트로 연산하여 같은 비트의 값이 모두 1이면 해당 비트 값이 1이 되고, 그렇지 않으면 0이 되는 연산자
- `|`: OR 연산자
  - 두 값을 비트로 연산하여 같은 비트의 값이 하나라도 1이면 해당 비트 값이 1이 되고, 그렇지 않으면 0이 되는 연산자
- `^`: XOR 연산자
  - 두 값을 비트로 연산하여 같은 비트의 값이 서로 다르면 해당 비트 값이 1이 되고, 그렇지 않으면 0이 되는 연산자
- `~`: NOT 연산자
  - 모든 비트의 값을 반대로 바꾸는 반전 기능을 하는 연산자(부호를 반대로 바꾼 값에 1을 뺀 값)

```c
#include <stdio.h>
void main( ){
  printf("%d" , 12 & 10); // 1100 & 1010 = 1&1=1, 1&0=0, 0&1=0, 0&0=0이므로 1000, 10진수로 변환하면 8
  printf("%d", 12 | 10);  // 1100 | 1010 = 1|1=1, 1|0=1, 0|1=1, 0|0=0이므로 1110, 10진수로 변환하면 14
  printf("%d", 12 ^ 10);  // 1100 ^ 1010 = 1^1=0, 1^0=1, 0^1=1, 0^0=0이므로 0110, 10진수로 변환하면 6
  printf("%d", ~12);      // NOT 연산은 부호를 반대로 바꾼 값 12 → -12에서 1을 뺀 값인, -13
}
```
- 출력  
8146-13

## 논리 연산자
논리 연산자는 참이면 1을, 거짓이면 0을 반환한다.
- `&&`: AND 연산자, 두 개의 논릿값이 모두 참이면 참을 반환하고 , 그렇지 않으면 거짓을 반환하는 연산자
- `||`: OR 연산자, 두 개의 논릿값 중 하나라도 참이면 참을 반환하고, 그렇지 않으면 거짓을 반환하는 연산자
- `!`: NOT 연산자, 한 개의 논릿값이 참이면 거짓을 반환하고, 거짓이면 참을 반환하는 연산자

```c
#include <stdio.h>
void main( ){
  int x=5, y=3;
  printf("%d", x>5 && y>=3); // x>5는 거짓, y>=3은 참, && 연산은 둘 다 참이 아니면 거짓이므로 거짓에 해당하는 0을 출력 
  printf("%d", x>5 || y>=3); // x>5는 거짓, y>=3은 참, || 연산은 둘 중 하나라도 참이면 참이므로 참에 해당하는 1을 출력 
}
```
- 출력  
01


## 삼항 연산자
조건식 ? 참일때값 : 거짓일때값;

```c
#include <stdio.h>
void main( ){
  int a = 26, b = 91;
  int x = a < b ? a : b; // 조건식: a < b는 참이므로 a 값인 26을 x에 대입
  printf('%d' , x); 
}
```
- 출력  
26


## 대입 연산자
- `=`: 왼쪽의 변수에 오른쪽의 값을 대입하는 연산자
- `+=`: 왼쪽의 변수에 오른쪽의 값을 더한 후, 그 결괏값을 왼쪽의 변수에 대입하는 연산자
- `-=`: 왼쪽의 변수에 오른쪽의 값을 뺀 후, 그 결괏값을 왼쪽의 변수에 대입하는 연산자
- `*=`: 왼쪽의 변수에 오른쪽의 값을 곱한 후, 그 결괏값을 왼쪽의 변수에 대입하는 연산자
- `/=`: 왼쪽의 변수를 오른쪽의 값으로 나눈 후, 그 결괏값을 왼쪽의 변수에 대입하는 연산자
- `%=`: 왼쪽의 변수를 오른쪽의 값으로 나눈 후, 그 나머지를 왼쪽의 변수에 대입하는 연산자 

```c
#include <stdio.h>
void main( ){
  int a = 17;
  a += 1; // 17+1 = 18, a=18
  a -= 2; // 18-2 = 16, a=16
  a *= 3; // 16*3 = 48, a=48
  a /= 4; // 48/4 = 12, a=12
  a %= 5; // 12/5의 나머지인 2를 저장
  printf("%d", a); 
}
```
- 출력  
2


# 조건문
```c
#include <stdio.h>
void main( ){
  int x = 5;
  if(x % 3 == 0)      //  5/3의 나머지 = 2, 2 == 0은 거짓
  printf ("1");
  else if(x % 3 == 1) // 5/3의 나머지 = 2, 2 == 1은 거짓
  printf("2");
  else
  printf("3");       // 출력
}
```
- 출력  
3


# switch문
switch문은 조건에 따라 여러 개의 선택 경로 중 하나를 취하고자 할 때 사용하는 명령어이다.
- switch 문에 식이 어떠한 case의 값도 만족하지 않으면 default로 진입해 명령문을 실행한다.
- break가 존재하지 않을 경우 break를 만날 때까지 switch 문에 있는 다른 문장을 실행한다.

```c
#include <stdio.h>
void main( ){
  int score = 101;
  switch(score/10){     // 101/10 = 10.1, 정수와 정수를 연산하면 정수가 되므로 10이 되고, case 10으로 이동함
    case 10:            // case 10인데 break가 없으므로 다음 문장 실행
    case 9:             // break가 없으므로 계속 실행
    printf("A"); break; // A를 출력하고, break를 만나서 switch 문 종료 
    case 8:
    printf("B"); break;
    default:
    printf("F");
  }
}
```
- 출력  
A


# 반복문
- 반복문은 특정 부분을 조건이 만족할 때까지 실행하도록 하는 명령문이다.
- 반복문을 사용할 때 특별한 조건이 없으면 무한 처리를 반복(무한 루프)하게된다.

1. while 문
```c
#include <stdio.h>
void main( ){
  int i=0, sum = 0;
  while ( i < 2 ){ // 0<2는 참이므로 반복문 수행 | 1<2는 참 | 2<2는 거짓이 되어 반복문 종료
    i++,           // 값을 1 증가시켜 i=1이 됨 | i=2
    sum = sum + i; // 0+1 = 1을 sum에 대입 | 1+2 = 3을 sum에 대입
  }
  printf("%d\n", sum); // sum값인 3을 출력
}
```
- 출력  
3

2. do while 문  
do while 문은 참, 거짓과 관련 없이 무조건 한 번은 실행하고, 그다음부터는 조건이 참인 동안에 해당 분기를 반복해서 실행하는 명령문이다.
```c
#include <stdio.h>
void main( ){
  int i=1, sum = 0;
  do{              // do while 문 진입 (무조건 한 번은 실행!)
    sum = sum + i; // 0+1 = 1을 sum에 대입
    i++,           // i값을 1증가시켜 i는 2가 됨
  }while(i<0);     // 2<0은 거짓이므로 do while 문 종료
  printf("%d\n", sum); // sum값인 1을 출력
}
```
- 출력  
1

3. for 문
for 문은 초기식, 조건식, 증감식을 지정하여 반복하는 명령어이다.
```c
#include <stdio.h>
void main( ){
  int i, sum = 0;
  for(i=1; i<3; i++) // 1<3이니 반복문 실행 | 2<3이니 반복문 실행 | 3<3은 거짓이므로 반복문 종료
    sum = sum + i;   // 0+1 = 1을 sum에 대입 | 1+2 = 3을 sum에 대입
  printf("%d\n", sum); 
}
```
- 출력  
3

4. 이중 for 문  
이중 for 문의 코드가 한 줄이면 다음과 같이 중괄호는 생략할 수 있습니다.
```c
#include <stdio.h>
void main( ){
  int i, j;
  for(i=1; i<3; i++) // 1<3 참이므로 반복문 실행 | 2<3 이므로 실행 | 3<3은 거짓이므로 바깥쪽 반복문 종료
    for(j=1; j<3; j++) // 1<3 이므로 반복분 실행, 2<3 참이므로 실행, 3<3 거짓으로 종료 | 안쪽 반복문 동일하게 실행
      printf("%d\n", i*10+j); // 1*10+1 = 11, 1*10+2 = 12 | 2*10+1 = 21, 2*10+2 = 22
}
```
- 출력  
11  
12  
21  
22

5. 루프 제어 명령어 : break 문  
break 문은 반복문이나 switch 문을 중간에 탈출하기 위해 사용하는 명령어이다.
```c
#include <stdio.h>
void main( ){
  int i=1,
  while ( i < 5 ){   // 1<5 실행 | 2<5 실행 
    i++;
    if ( i == 3 )    // 2 == 3 거짓 | 3 == 3 참
      break;         // break를 실행하여 반복문인 while 종료
    printf("%d", i); // i = 2출력
  }
  printf("%d", i);   // i의 값인 3 출력
}
```
- 출력  
23

6. 루프 제어 명령어 : continue 문  
continue 문은 반복문에서 다음 반복으로 넘어갈 수 있도록 하는 명령어이다.
```c
#include <stdio.h>
void main( ){
  int i=1,
  while ( i < 5 ){   // 1<5 참 | 2<5 참 | 3<5 참 | 4<5 참 | 5<5는 거짓으로 반복문 종료
    i++;
    if ( i == 3 )    // 2 == 3 거짓 | 3 == 3 참 | 4 == 3 거짓 | 5 == 3 거짓
      continue;      // continue를 만났으므로 다시 while 문 시작 부분으로 이동
    printf("%d", i); // i는 2 출력 | i는 4 출력 | i는 5 출력
  }
  printf("%d" , i);  // i 값인 5를 출력
}
```
- 출력  
2455


# 배열
1. 배열(Array) 개념
- 배열은 **같은 자료형의 변수들로 이루어진 집합**이다.

2. 1차원 배열 선언 및 출력
```c
#include <stdio.h>
void main( ){
  int a[3] = {1, 2};
  int i;
  for(i=O; 1<3; i++)   // 초기값 i=0, i=1, i=2
  printf("%d\n", a[i]);
}
```
- 출력  
1  
2  
0

3. 2차원 배열 선언 및 출력
```c
#include <stdio.h>
void main( ){
  int a[2][3] = {1, 2, 3, 4}; // a 배열의 요소 개수는 2x3개지만, 초깃값은 1, 2, 3, 4만 명시되어 있으므로 나머지 2개의 공간은 0으로 초기화
  int i, j;
  for(i=0; i<2; i++)   // 행 : i=0 | i=1
    for(j=0; j<3; j++) // 열 : j=0, j=1, j=2 | j=0, j=1, j=2
      printf("%d", a[i][j]); // a[0][0], a[0][1], a[0][2], a[1][0], a[1][1], a[1][2]
}
```

- 풀이
```
a[0][0] a[0][1] a[0][2]
a[1][0] a[1][1] a[1][2]

   1       2       3
   4       0       0
```

- 출력  
123400


# 문자열
c언어에서는 문자열은 char 형 배열로 표현한다.

1. 1차원 배열과 문자열
```c
#include <stdio.h>
void main( ){
  char a[8] = "Hello";
  printf("%s\n", a);   // a = a[0][0]부터 NULL을 만나기 전까지 읽음
  printf("%s\n", a+1); // a[1] 부터 NULL을 만나기 전까지 읽음
  a[3] = NULL;         // H e l NULL o
  printf("%s\n", a+1); // a[1] 부터 NULL을 만나기 전까지 읽음
  printf("%s\n", a+4); // a[4] 부터 NULL을 만나기 전까지 읽음
}
```
- 출력  
Hello  
ello  
el  
o

2. 2차원 배열과 문자열  
문자열을 여러 개 정의할 때 char 형 2차원 배열을 사용한다.
```c
#include <stdio.h>
void main( ){
  char a[2][8] = {"Hel1o", "Soojebi"};
  printf("%s\n", a[0]);   // a[0][0]부터 NULL을 만나기 전까지 읽음
  printf("%s\n", a[1]);   // a[1][0]부터 NULL을 만나기 전까지 읽음
  printf("%s\n", a[1]+3); // a[1][3]부터 NULL을 만나기 전까지 읽음
  a[1][4] = NULL;
  printf("%s\n", a[1]+2); // a[1][2]부터 NULL을 만나기 전까지 읽음
}
```

- 풀이
```
a[0][0] a[0][1] a[0][2] a[0][3] a[0][4] a[0][5] a[0][6] a[0][7]
a[1][0] a[1][1] a[1][2] a[1][3] a[1][4] a[1][5] a[1][6] a[1][7]
   H       e        l      l       o      NULL    NULL    NULL
   S       o        o      j       e       b       i      NULL
```

- 출력  
Hel1o  
Soojebi  
jebi  
oj


# 구조체
구조체는 사용자가 기본 자료형을 가지고 새롭게 정의할 수 있는 사용자 정의 자료형이다.
- 구조체는 구조체변수.변수명 형태로 값을 가리킨다.

```c
struct 구조체명{
  자료형 변수명1;
  자료형 변수명2;
};

struct 구조체명 구조체변수;
```

```c
#include <stdio.h>
struct Student {
  car gender;
  int age;
}
void main( ) {
  struct Student s = {'F', 21}; // s라는 이름의 Student 구조체를 선언, S 안에 gender는 F로, S 안에 age는 21로 초기화
  s.gender = 'M';               // s 안에 gender의 값을 M으로 대입
  printf("%c", s.gender);       // s 안에 gender의 값을 출력하므로 M이 출력
  printf("%d", s.age);          // s 안에 age의 값을 출력하므로 21이 출력
```
- 출력  
M21


# 함수
## 1. main 함수  
main 함수는 프로그램이 실행하는 모든 프로그램의 시작점이다. main 함수에 있는 명령어를 실행한다.
```c
자료형 main(파라미터){
  명령어;
}
```
- void main()일 경우 반환할 값이 없으므로 return;을 사용하거나 return 자체를 사용하지 않는다.
- int main()일 경우 return 반환값;을 명시해주어야 한다.
```c
int main(){
  return 반환값;
}
```
- main 함수나 사용자 정의 함수는 return을 만나면 그 즉시 함수를 종료한다.

## 2. 사용자 정의 함수  
사용자 정의 함수는 사용자가 직접 새로운 함수를 정의하여 사용하는 방법이다.
- 사용자 정의 함수에서 매개변수나 생성된 변수는 사용자 정의 함수가 종료되면 없어진다.
```c
자료형 함수명(자료형 변수명){
  명령어;
  return 반환값;
}
```
```c
#include <stdio.h>  // 1. stdio.h 헤더 파일을 읽어옴 
  char fn(int num){
  if (num % 2 == 0) // 5/2의 나머지가 0이라면 참
    return 'Y';
  else
    return 'N';
}
void main(){       // 2. main 함수의 시작 부분(프로그램이 제일 처음 실행되는 부분)
  char a = fn(5);  // 3. a라는 이름의 char(문자)형 변수를 선언, a는 fn(5)가 실행한 후에 반환되는 return값으로 초기화
  printf("%c\n" , a);
} 
```
- 출력  
N  

1. 매개변수 전달 방법 구성요소
- ① 전달인자(Argument)
  - 실 매개변수(Actual Parameters)
  - 함수를 호출하는 쪽에서 전달**하는** 변수의 값 또는 변수의 주솟값
- ② 매개변수(Parameter)
  - 형식 매개변수(Formal Parameters)
  - 함수를 호출하는 쪽에서 전달**받는** 변수의 값 또는 변수의 주솟값  
```c
#include <stdio.h>
int fn(int x, int y){ // 매개변수(Parameter)
...
}
void main(){
  int i, j;
  ...
  fn(i, j);            // 전달인자(Argument)
} 
```  

2. 매개변수 전달 방법의 종류
- 1) Call by Value
  - 변수의 값을 넘겨주고, 이 값은 새로운 공간에 할당되어 사용하는 방식
  - 형식 매개변수의 어떠한 변화도 실 매개변수에 아무런 영향을 미치지 않음  
```c
#include <stdio.h>
int fn(int x, int y){ // 형식 매개변수는 변수 선언과 동일하게 작성하고,
...
}
void main(){
  int i, j;
  ...
  fn(i, j);          // 실 매개변수는 변수명을 작성함 
} 
```
- 2) Call by Reference
  - 변수의 값이 아닌 변수가 사용 중인 메모리 공간의 주소를 넘겨주는 방식
  - 실 매개변수의 주소를 형식 매개변수로 보냄  
```c
#include <stdio.h>
int fn(int* x, int* y){ // Call by Reference, 간접값 연산자(*)를 이용해 포인터 변수 선언과 동일하게 작성하고,
...
}
void main(){
  int i, j;
  ...
  fn(&i, &j);          // 실 매개변수는 주소연산자(&)를 이용해 변수의 주솟값을 작성 
} 
```
- Call-by-Value 예제  
```c
#include <stdio.h>
int fn(int n){     // n = 5 파라미터로 사용자 정의 함수 내에서만 사용할 수 있고, 사용자 정의 함수가 종료되면 사라짐(main 함수의 n과 다름)
  n = 7;           // n에 7을 대입
  return n;        // n 값인 7을 fn(5)로 호출한 부분에 전달, return을 만났으므로 사용자 정의 함수가 종료되고, n은 사용자 정의 함수가 종료되었으므로 사라짐
}
void main(){
  int n = 5;       // 해당 n은 main 함수에서 선언했으므로 main 함수에서만 사용할 수 있고, main 함수가 종료되면 사라짐(사용자 정의 함수의 n과 다름)
  fn(n);           // fn(n)은 반환값 7로 바뀌어 7;와 동일하지만, 7을 어디에도 활용하지 않으므로 아무일이 일어나지 않음
  printf("%d", n); // main 함수의 n 값인 5를 출력
} 
```
- 출력  
5  
- Call-by-Reference 예제
```c
#include <stdio.h>
int fn(int* m){    // fn(int* m）에서 m은 main 함수의 변수 n에 대한 주솟값
  *m = 7;          // fn의 m이 가리키는 값(main 함수의 n 값)으로 7을 대입
}
void main(){
  int n = 5;       // 해당 n은 main 함수에서 선언했으므로 main 함수에서만 사용할 수 있고, main 함수가 종료되면 사라짐(사용자 정의 함수의 n과 다름) 
  fn(&n);          // n의 주솟값을 fn 함수에 전달
  printf("%d", n); // n은 7이므로 7을 출력
```
- 출력  
7

3. 재귀 함수  
재귀 함수는 함수 자신이 자신을 부르는 함수이다.
```c
자료형 함수명(자료형 변수명){
  함수명(변수명)
return 반환값;
}
```
- 예제
```c
#include <stdio.h>
int fn(int n){  // n = 3
  if( n <= 1 ) // 3 <= 1은 거짓이므로 else 문을 실행
    return 1;
  else
    return n*fn(n-1), // 3*fn(3-1), 3*fn(2), 3*2 = 6을 호출한 부분에 전달
}
void main(){
  printf("%d", fn(3));
}
```
- 출력
6

## 3. 표준 함수
### 1) 문자열 함수
1. strcat(String Concatenate) : 문자열끼리 연결하는 함수
- `strcat(dest, src);` : src의 문자열을 dest 문자열 뒤에 붙임
- `strncat(dest, src, maxien);` : src의 문자열에서 maxien의 개수만큼 dest 문자열 뒤에 붙임
- 예제
```c
#include <stdio.h>
#include <string.h>
void main(){
  char a[20] = "Hello";
  char b[10] = "Soojebi";
  char c[20] = "Hello";
  strcat(a, b);
  printf("%s %s\n", a, b);
  strncat(c, b, 3);
  printf("%s %s", C, b); 
}
```
- 출력  
HelloSoojebi Soojebi  
HelloSoo Soojebi

2. strcpy(String Copy) : 문자열을 복사하는 함수
- `strcpy(dest, src);` : src의 문자열을 dest 문자열에 복사
- `strncpy(dest, src, maxien);` : src의 문자열에서 maxien의 개수만큼 dest 문자열에 복사
- 예제
```c
#include <stdio.h>
#include <string.h> // Strcpy 함수와 strncpy 함수를 사용하기 위해 string.h 헤더 파일을 읽어옴
void main(){
  char a[20] = "Hello";
  char b[10] = "Soojebi";
  char c[20] = "Hello";
  strcpy(a, b);            // b의 "Soojebi"가 a에 복사되어 a와 b 모두 Soojebi가 됨
  printf("%s %s\n", a, b);
  strncpy(c, b, 3);        // b의 "Soojebi" 중 3글자가 C에 복사되어 C는 Soolo가 됨
  printf("%s %s", C, b); 
}
```
- 출력  
Soojebi Soojebi  
Soolo Soojebi

3. strcmp(String Compare) : 문자열을 비교하는 함수
- `strcmp(s1, s2);` : s1, s2의 대소를 비교
- `strncmp(s1, s2, maxien);` : maxlen 길이만큼만 s1, s2의 대소를 비교
  - 문자열에 대해서 ASCII 코드를 비교하여 s1이 s2보다 크면 1을, s1과 s2이 같으면 0을, s1이 s2보다 작으면 -1을 반환한다.
  - 사전 배열 방식과 유사, 문자열의 첫 번째 문짜끼리 비교하고, 다르면 아스키 코드 값을 통해 크고 작음을 판별합니다.
  - 문자열의 첫 번째 문자가 같으면 두 번째 문자끼리 비교하괴 그래도 같으면 세 번째 문자끼리 비교하는 식으로해서 마지막 문자까지 같으면 두 문자열은 같다라고 판별합니다.
- 예제
```c
#include <stdio.h>
#include <string.h>
void main(){
  char a[10] = "HelloA";
  char b[10] = "HelloB";
  int c = strcmp(a, b); // A < B이므로 -1을 반환
  printf("%d\n", c);
  c = strncmp(a, b, 3);
  printf("%d", c); 
}
```
- 출력  
-1  
0

4. strlen(String Length) : 문자열의 길이를 알려주는 함수
- `strien(s);` : s의 길이를 알려줌

5. strrev(String Reverse) : 문자열을 거꾸로 뒤집는 함수
- `strrev(str);` : str 내에 문자열을 거꾸로 뒤집음 

6. strchr : 문자열 내에 일치하는 문자가 있는지 검사하는 함수
- `strchr(str, c);` : str 내에 C가 존재하는지 알려줌 
- 예제
```c
#include <stdio.h>
#include <string.h>
void main(){
  char a[20] = "Hello";
  char* p = strchr(a, 'l'); // 첫 번째 'l'이 나온 위치를 반환하여 p라는 포인터 변수에 저장
  printf("%s", p);          // p라는 포인터 변수가 가리키는 문자부터 NULL 전까지 값을 출력 
}
```
- 출력  
llo

### 2) 수학 함수
1. sqrt : 양의 제곱근을 계산하는 함수
- `sqrt(n);` : $\sqrt{n}$ 의 값을 계산
  - 양의 제곱큰은 소수(약수가 1과 자기 자신만 있는 숫자)를 확인할 때도 사용합니다. a라는 값의 소수를 확인할 때는 2 ~ (a-1)의 모든 정수들로 나눴을 때 나누어 떨어지지 않는지 확인해야 합니다. 하지만, sqrt를 이용하면  2 ~ $\sqrt{a}$의 정수들만 나누어 떨어지지 않는지 확인하면 되기 때문에 확인해야 할 숫자가 많이 줄어들어 sqrt를 소수 계산할 때 사용합니다.
  - 101이 소수인지 아닌지 구하기 위해서 2부터 100까지 나누어 떨어지는지 확인할 필요가 없이, 2부터 $\sqrt{101}$(=10.05) 이하의 정수인 10까지 나눠떨어지는지만 확인하면 됩니다.
- 예제
```c
#include <stdio.h>
#include <math.h>
void main(){
  double a;
  a = sqrt(5.1);     // $\sqrt{5.1} 값을 계산해서 값을 반환해줌
  printf("%.2f", a); // a 변수에 저장된 값을 소수점 셋째 자리에서 반올림해서 소수점 둘째자리까지 보여줌
}
```
- 출력  
2.26

2. ceil : 소수점 올림 함수
- `ceil(n);` : 소수점 올림
- 예제
```c
#include <stdio.h>
#include <math.h>
void main() {
  double a = 1.1;
  printf("%.2f", ceil(a)); // ceil(1.1), 1.1을 올림한 값인 2를 반환
}
```
- 출력  
2.00

3. floor : 소수점 내림 함수
- `floor(n);` : 소수점 내림
- 예제
```c
#include <stdio.h>
#include <math.h>
void main() {
  double a = 1.1;
  printf("%.2f", floor(a)); // ceil(1.1), 1.1을 내림한 값인 1을 반환
}
```
- 출력  
1.00


### 3) 유틸리티 함수
1. rand(Random) : 임의의 값을 생성하는 함수
- `rand();` : 임의의 정숫값 1개를 생성
  - rand()는 0~32767 중에 하나의 값을 반환

2. srand(Seed Random) : 난수 생성 알고리즘에 사용하는 seed를 정해주는 함수
- `srand(seed);` : seed 값에 따라 난수 발생기를 초기화한다.
  - 컴퓨터는 난수를 난수 생성 알고리즘에 의해서 만드는데, 난수 생성 알고리즘의 seed 값이 같으면 프로그램을 실행할 때마다 계속 똑같은 패턴의 난수를 만들게 됩니다. 그래서 seed 값을 프로그램 시작할 때마다 다르게 하도록 seed에 fime 함수를 사용합니다.

3. time : 현재 시간을 가져오는 함수  
- 1970년 1월 1일 이후로 몇 초가 경과했는지를 나타낸다.
- `time(NULL);` : time 함수에 파라미터를 NULL로 하면 현재 시간을 리턴 
- 예제
```c
#include <stdio.h>
#include <stdlib.h> // rand 함수를 사용하기 위해 stdlib.h 헤더 파일을 읽어옴
#include <time.h>   // time 함수를 사용하기 위해 time.h 헤더 파일을 읽어옴
void main() {
  int a;
  int i;
  srand(time(NULL));  // srand(time(NULL));을 삭제할 경우 프로그램을 실행할 때마다 똑같은 결과가 나옴
  for(i=0; i<6; i++){ // 0~5
    a = rand()%45+1;  // rand()는 임의의 값을 반환하고, 반환한 값에 45로 나눴을 때 나머지(0~44 중 하나의 값을 가짐)에 1을 더함, 1~45
    printf("%d", a);  // a 변수에는 1~45 중에 임의의 값이 저장됨 
  }
}
```
- 출력  
29 17 28 26 24 26

4. atoi(ASCII to Integer) : 문자열을 정수형으로 변환하는 함수
- `atoi(str);` : 문자열(str)을 정수(int)형으로 변환
- 예제
```c
#include <stdio.h>
#include <stdlib.h>
void main() {
  char *a = "1";     // "1"이라는 문자열 생성한 후에 a 문자형 포인터가 "1"이라는 문자열을 가리킴 
  int num = atoi(a); // a 변수의 문자열 "1"이 숫자 1로 변환되고, 숫자 1을 num에 대입함
  printf("%d", num);
}
```
- 출력  
1

5. atof(ASCII to Floating Point) : 문자열을 실수형으로 변환하는 함수
- `atof(str);` : 문자열(str)을 실수형(float, double)형으로 변환
- 예제
```c
#include <stdio.h>
#include <stdlib.h>
void main() {
  char *str_num = "1.0";      // "1.0“이라는 문자열 생성한 후에 str_num 문자형 포인터가 "1.0"이라는 문자열을 가리킴
  double num = atof(str_num); // str_num 변수의 문자열 "1.0"이 숫자 1.0으로 변환되고, 숫자 1.0을 num에 대입함
  printf("%.2f", num);        // num에 저장된 1.0을 소수점 셋째자리에서 반올림해서 소수점 둘째자리까지 출력
}
```
- 출력  
1.00

6. itoa(Integer to ASCII) : 정수형을 문자열로 변환하는 함수
- `itoa(value, str, radix)` : value를 변환하여 str에 radix 진수로 저장함
- 예제
```c
#include <stdio.h>
#include <stdlib.h>
void main() {
  char buffer[4] = {NULL}; // 초깃값이 명시되지 않은 값들은 문자형일 경우는 NULL로 초기화된다．
  int num = 123;
  itoa( num, buffer, 10 ); // num 값인 123을 10진수 형태로 buffer라는 변수에 문자열로 저장
  printf("%s", buffer); 
}
```
- 출력  
123


# 포인터(Pointer)
1. 포인터 개념  
포인터는 변수의 주솟값을 저장하는 공간이다.

2. 포인터 선언 : `자료형* 포인터_변수명 = ＆변수명;`
- 자료형 뒤에 *를 붙이면 주소를 저장하는 포인터 변수라는 의미이고, 일반변수명에 &를 붙이면 해당 변수명의 주솟값이다.
- int 형 변수를 가리키는 포인터 변수 선언 시 `int*`를, char 형 변수를 가리키는 포인터 변수 선언 시 `char*`를, float 형 변수를 가리키는 포인터 변수 선언 시 `float*`를 사용해야 한다.
- 주소에 해당하는 값을 가리킬 때는 *를 사용한다.
- 주소에 해당하는 값을 가리키는 * 연산과 변수에 주솟값을 나타내는 & 연산은 반대 기능입니다．
그래서 *(&)과 같이 두 연산을 같이 쓰면 서로 상쇄됩니다.
- 예제
```c
#include <stdio.h>
void main() {
  int a = 10;  // a라는 변수에 10이라는 값을 저장
  int* b = &a; // b라는 포인터 변수에 a의 주솟값을 저장
  priritf("%d %d %d", a, *b, *(&a)); // *b는 b라는 포인터 변수가 저장하고 있는 주소에 있는 값을 출력하라는 의미이므로, a의 주솟값에 저장된 값인 a를 출력, b가 가리키는(*) 값은 a이므로 *b와 a는 값이 같음, a의 주솟값인 &a가 가리키는 값은 a가 됨（*과 ＆는 반대 연산으로 서로 상쇄됨)
}
```
- 출력  
10 10 10

3. 배열과 포인터
- "자료형 배열명[요소];"일 때 다음 코드는 동일하다.
  - 배열의 i번지 주소 : `배열+i == ＆배열[i];`
  - 배열의 i번지 값 :  `*(배열+i) == 배열[i];`
- 1차원 배열에서 배열명만 단독으로 사용할 경우 1차원 포인터와 동일하다.
- 1차원 배열일 때는 배열명[요소] 형태, *(배열명＋요소)일 경우 값을 가리키고, 1차원 포인터일 때는 포인터[요소] 형태, (포인터＋요소)일 경우 값을 가리킨다.
- 예제
```c
#include <stdio.h>
void main() {
  int a[3] = {1, 2}; 
  int *p = a;
  printf("%d %d %d\n", a[0], a[1], a[2]);
  printf("%d %d %d\n" , *a, *(a+1), *(a+2)); // a는 &a[0]과 같으므로 *a는 *(&a[0])이 되고, *과 ＆는 반대 연산으로 서로 상쇄되어 a[0] 값을 출력
  printf("%d %d %d\n", *p, *(p+1), *(p+2));
  printf("%d %d %d\n", p[0], p[1], p[2]);
}
```
- 출력  
1 2 0  
1 2 0  
1 2 0  
1 2 0  

