# Week_07_Hands On Lab

* LAB 7-1: 오늘의 날짜와 현재시간 출력하기

1. datetime 모듈을 사용하여 오늘의 날짜와 시간을 다음과 같이 출력하여라. 이때 hpur 값이 10일 경우 오전 10시, 13이면 오후 1시와 같이 오전/오후 정보를 출력하여라. 


```python
import datetime as dt
today=dt.date.today()
start_time=dt.datetime.now()
print("오늘의 날짜 : {}년 {}월 {}일".format(today.year, today.month, today.day))

if(start_time.hour>12):
    print("현재시간 : 오후 {}시 {}분 {}초".format(start_time.hour-11, start_time.minute, start_time.second))
else:
    print("현재시간 : 오후 {}시 {}분 {}초".format(start_time.hour, start_time.minute, start_time.second))
    
```

    오늘의 날짜 : 2022년 10월 13일
    현재시간 : 오후 3시 48분 40초
    

* LAB 7-2: 남은 날짜 계산하기

1. 앞서 배운 남은 날짜 계산 프로그램을 수정하여 오늘 날짜와 함께 2025년 크리스마스까지의 남은 날짜와 시간을 구해서 출력해 보자.


```python
import datetime as dt
today = dt.date.today()
print('오늘은 {}년 {}월 {}일입니다'.format(today.year, today.month, today.day))
xMas = dt.datetime(2025, 12, 25)
time_gap = xMas - dt.datetime.now()
print('2025년 크리스마스 까지는 {}일 {}시간 남았습니다.'.format( \
time_gap.days,time_gap.seconds // 3600))
```

    오늘은 2022년 10월 13일입니다
    2025년 크리스마스 까지는 1168일 8시간 남았습니다.
    

2. 앞서 배운 남은 날짜 계산 프로그램을 수정하여 2036년 1월 1일까지의 남은 날짜와 시간을 구해서 출력해 보자.


```python
import datetime as dt
today = dt.date.today()
print('오늘은 {}년 {}월 {}일입니다'.format(today.year, today.month, today.day))
newYear = dt.datetime(2036, 1, 1)
time_gap = newYear - dt.datetime.now()
print('2036년 새해 까지는 {}일 {}시간 남았습니다.'.format( \
time_gap.days,time_gap.seconds // 3600))
```

    오늘은 2022년 10월 19일입니다
    2036년 새해 까지는 4821일 2시간 남았습니다.
    

3. 다가오는 자신의 생일까지 남은 날짜와 시간을 출력해 보자. 


```python
import datetime as dt
today = dt.date.today()
print('오늘은 {}년 {}월 {}일입니다'.format(today.year, today.month, today.day))
birth = dt.datetime(2023, 4, 3)
time_gap = birth - dt.datetime.now()
print('2023년 생일까지는 {}일 {}시간 남았습니다.'.format( \
time_gap.days,time_gap.seconds // 3600))
```

    오늘은 2022년 10월 19일입니다
    2023년 생일까지는 165일 2시간 남았습니다.
    

* LAB 7-3: 날짜 계산하기

1. timedelta 클래스를 사용하여 오늘 날짜로부터 1,000일 후의 날짜를 구하시오.


```python
import datetime as dt
th=dt.timedelta(days=1000)
plus1000day=dt.datetime.now()+th
print("오늘 날짜로부터 1,000일 후: ",plus1000day)
```

    오늘 날짜로부터 1,000일 후:  2025-07-15 21:30:37.861990
    

2. timedelta 클래스를 이용하여 커플들을 위한 프로그램을 작성하자. 다음과 같이 처음으로 사귄 연도와 월, 일을 띄어쓰기로 입력하면 100일 기념일을 출력하는 기능이 있다.


```python
import datetime as dt
year, month, date=map(int, input("처음으로 사귄 연도와 월, 일을 입력하시오 : ").split())
first=dt.datetime(year,month,date)
plus100=first+dt.timedelta(days=100)
print("100일 기념일은 : {}월 {}일 {}일입니다.".format(plus100.year, plus100.month,plus100.day-1))
```

    처음으로 사귄 연도와 월, 일을 입력하시오 : 2019 3 30
    100일 기념일은 : 2019월 7일 7일입니다.
    

* LAB 7-4: math 모듈을 이용한 계산

1. math 모듈과 for - in range()를 사용하여 4의 2승부터 10승까지를 화면에 출력하여라.


```python
import math as m

for i in range(2,11):
    print("4**{:2} = {:9.1f}".format(i,m.pow(4,i)))
```

    4** 2 =      16.0
    4** 3 =      64.0
    4** 4 =     256.0
    4** 5 =    1024.0
    4** 6 =    4096.0
    4** 7 =   16384.0
    4** 8 =   65536.0
    4** 9 =  262144.0
    4**10 = 1048576.0
    

2. 일반각도 0도에서 180도를 10도 단위로 출력하여라. 이때 이 일반각도에 대응되는 라디안 각도 값을 함께 출력하라. 


```python
import math as m

for i in range(0,181,10):
    print("{:3} degree = {:.3f} radian".format(i,m.radians(i)))
```

      0 degree = 0.000 radian
     10 degree = 0.175 radian
     20 degree = 0.349 radian
     30 degree = 0.524 radian
     40 degree = 0.698 radian
     50 degree = 0.873 radian
     60 degree = 1.047 radian
     70 degree = 1.222 radian
     80 degree = 1.396 radian
     90 degree = 1.571 radian
    100 degree = 1.745 radian
    110 degree = 1.920 radian
    120 degree = 2.094 radian
    130 degree = 2.269 radian
    140 degree = 2.443 radian
    150 degree = 2.618 radian
    160 degree = 2.793 radian
    170 degree = 2.967 radian
    180 degree = 3.142 radian
    

3. math 모듈과 for 문을 사용하여 일반각도 sin 0도에서 부터 180도까지의 값을 10도 간격으로 출력하여라. 


```python
import math as m
for i in range(0,181,10):
    print("sin({:4d}) = {:.2f}".format(i,m.sin(m.radians(i))))
```

    sin(   0) = 0.00
    sin(  10) = 0.17
    sin(  20) = 0.34
    sin(  30) = 0.50
    sin(  40) = 0.64
    sin(  50) = 0.77
    sin(  60) = 0.87
    sin(  70) = 0.94
    sin(  80) = 0.98
    sin(  90) = 1.00
    sin( 100) = 0.98
    sin( 110) = 0.94
    sin( 120) = 0.87
    sin( 130) = 0.77
    sin( 140) = 0.64
    sin( 150) = 0.50
    sin( 160) = 0.34
    sin( 170) = 0.17
    sin( 180) = 0.00
    

* LAB 7-5: 랜덤 번호 생성기

1. random 모듈의 randrange() 함수를 이용하여 0에서 100 이하의 정수 중에서 5의 배수 값을 임의로 3개 선택하여 리스트 형식으로 출력해 보시오.


```python
import random as rd

myList=[]
for i in range(3):
    myList.append(rd.randrange(0,100,5))
print("0에서 100 이하의 정수 중에서 5의 배수")
print(rd.sample(myList,3))

```

    0에서 100 이하의 정수 중에서 5의 배수
    [70, 25, 55]
    

2. 1에서 10 사이의 정수 중 임의의 정수 3개를 sample() 함수를 이용하여 출력하시오.


```python
import random as rd
numlist=list(range(1,11))
print("1에서 10사이의 임의의 정수 :", rd.sample(numlist,3))
```

    1에서 10사이의 임의의 정수 : [7, 8, 5]
    

*  랜덤 주사위 게임(수업 중 과제)

>A와 B 두 사람이 있다. 이 두 사람이 주사위를 굴려서 높은 숫자를 얻은 사람이 이기는 주사위 게임을 할 때, 이긴 사람이 누구인지 출력하고 무승부일 경우 승부가 날 때까지 게임을 하는 프로그램을 만들어보자


```python
import random as rd

a_=rd.randrange(1,7)
b_=rd.randrange(1,7)

def dice(a,b):
     if a>b:
          print("a가 이겼습니다.")
     elif a<b:
          print("b가 이겼습니다.")
     elif a==b:
          print("무승부")
          print("게임을 다시 시작합니다.")
          dice(a,b)
print("a:{}, b:{}".format(a_,b_))
dice(a_,b_)
```

    a:3, b:2
    a가 이겼습니다.
    

* 7.5.2 로또 번호 만들기(수업 중 과제)

> 파이썬의 random 모듈을 활용하여 로또 번호를 자동으로 생상하여 출력하는 프로그램 만들어보기.


```python
import random as rd

numlist=list(range(1,46))
rd.shuffle(numlist)
numlist=numlist[:6]
numlist.sort()
print("이번 주의 추천 로또번호: ",numlist)
```

    이번 주의 추천 로또번호:  [2, 20, 33, 34, 35, 41]
    
