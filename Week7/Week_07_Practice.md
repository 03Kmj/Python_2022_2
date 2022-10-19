# Week_07 연습문제

1.로미오와 줄리엣 두 사람이 주사위를 던져서 높은 숫자가 나오면 이기는 게임을 만들어 보자. 로미오와 줄리엣의 주사위는 모두 다음과 같이 random 모듈의 randrange()를 통해서 생성한 난수를 바탕으로 한다. 출력 결과는 다음과 같이 로미오가 이기거나, 줄리엣이 이기거나, 비기는 결과가 나와야 한다. 


```python
import random as rd

a_=rd.randrange(1,7)
b_=rd.randrange(1,7)

def dice(a,b):
     if a>b:
          print("로미오가 이겼습니다.")
     elif a<b:
          print("줄리엣이 이겼습니다.")
     elif a==b:
          print("무승부")
          print("게임을 다시 시작합니다.")
          dice(a,b)
print("로미오의 주사위 숫자는 {} 입니다.".format(a_))
print("줄리엣의 주사위 숫자는 {} 입니다.".format(b_))
dice(a_,b_)
```

    로미오의 주사위 숫자는 5 입니다.
    줄리엣의 주사위 숫자는 1 입니다.
    로미오가 이겼습니다.
    

2. 랜덤 숫자 맞추기 게임 프로그램을 작성하라. 먼저 랜덤하게 1~20까지의 숫자 x를 하나 생성시키고 사용자는 숫자를 하나씩 입력하면서 생성된 숫자 x와 비교해 큰지 작은지를 보고 숫자를 맞춰가는 게임이다. 컴퓨터는 사용자가 입력한 숫자가 정답보다 큰지 작은지를 알려주어야 한다. 그리고 사용자가 시도를 할 때 마다 시도한 횟수가 n에 저장되도록 한다. 만일 입력한 숫자와 x가 일치하면 “정답입니다!”라는 메시지를 출력한다. 이때 3번 이하로 입력하여 숫자를 맞추면 “n번 만에 맞춘 당신은 천재!”, 3번 이상 6번 이하로 입력하여 숫자를 맞추면 “n번 만에 맞추셨네요. 잘 했어요^^”, 7번 이상으로 숫자를 입력하여 맞추면 “n번 만에 맞추다니 쩝쩝…”이라고 출력하라.


```python
import random as rd

x=rd.randint(1,20)
count=0
while 1:
    in_=int(input("1~20까지의 숫자를 입력하세요 : "))
    count+=1
    if in_>x:
        print("{}보다 작습니다.".format(in_))
    elif in_<x:
        print("{}보다 큽니다.".format(in_))
    else:
        print("정답입니다!")
        break
if count>=7:
    print("{}번 만에 맞추다니 쩝쩝...".format(count))
elif count>=3:
    print("{}번 만에 맞추셨네요. 잘했어요^^".format(count))
else:
    print("{}번 만에 맞춘 당신은 천재!".format(count))

```

    1~20까지의 숫자를 입력하세요 : 10
    10보다 큽니다.
    1~20까지의 숫자를 입력하세요 : 15
    15보다 작습니다.
    1~20까지의 숫자를 입력하세요 : 13
    13보다 작습니다.
    1~20까지의 숫자를 입력하세요 : 12
    12보다 작습니다.
    1~20까지의 숫자를 입력하세요 : 11
    정답입니다!
    5번 만에 맞추셨네요. 잘했어요^^
    

3. 1부터 1,000,000까지 정수의 합을 구하여 반환하는 함수 sum1to1000000()을 작성하고 함수를 100번 호출하여 함수 수행 시간을 다음과 같이 초단위로 구하여 출력하여라. (소수점 4자리까지 표현할 것.)


```python
import time

def sum1to1000000():
    start=1
    while start<1000000:
        start+=1
st=time.time()
for i in range(100):
    sum1to1000000()
finish=time.time()
print("{:.4f}".format(finish-st))
```

    19.4033
    

4. 0부터 1,000,000까지의 임의의 정수를 10개 연속적으로 출력하는 의사난수 함수 myRand()를 생성하여라.


```python
import random as rd

def myRand():
    print(rd.randint(1,1000000))

for _ in range(10):
    myRand()
```

    120173
    897012
    348738
    211183
    666069
    886136
    860751
    89353
    437531
    220007
    

10. math 모듈을 사용하여 0도에서 180도까지 10도 단위로 sin, cos, tan 값을 구하여 다음과 같이 출력하여라.


```python
import math as m

def sin_(degree):
    return m.sin(m.pi*(degree/180))

def cos_(degree):
    return m.cos(m.pi*(degree/180))

def tan_(degree):
    return m.tan(m.pi*(degree/180))

for degree in range(0,181,10):
    print("sin({:3}) = {:7.3f}, cos({:3}) = {:7.3f}, tan({:3}) = {:7.3f}".format(degree,sin_(degree),degree,cos_(degree), degree,tan_(degree)))

```

    sin(  0) =   0.000, cos(  0) =   1.000, tan(  0) =   0.000
    sin( 10) =   0.174, cos( 10) =   0.985, tan( 10) =   0.176
    sin( 20) =   0.342, cos( 20) =   0.940, tan( 20) =   0.364
    sin( 30) =   0.500, cos( 30) =   0.866, tan( 30) =   0.577
    sin( 40) =   0.643, cos( 40) =   0.766, tan( 40) =   0.839
    sin( 50) =   0.766, cos( 50) =   0.643, tan( 50) =   1.192
    sin( 60) =   0.866, cos( 60) =   0.500, tan( 60) =   1.732
    sin( 70) =   0.940, cos( 70) =   0.342, tan( 70) =   2.747
    sin( 80) =   0.985, cos( 80) =   0.174, tan( 80) =   5.671
    sin( 90) =   1.000, cos( 90) =   0.000, tan( 90) = 16331239353195370.000
    sin(100) =   0.985, cos(100) =  -0.174, tan(100) =  -5.671
    sin(110) =   0.940, cos(110) =  -0.342, tan(110) =  -2.747
    sin(120) =   0.866, cos(120) =  -0.500, tan(120) =  -1.732
    sin(130) =   0.766, cos(130) =  -0.643, tan(130) =  -1.192
    sin(140) =   0.643, cos(140) =  -0.766, tan(140) =  -0.839
    sin(150) =   0.500, cos(150) =  -0.866, tan(150) =  -0.577
    sin(160) =   0.342, cos(160) =  -0.940, tan(160) =  -0.364
    sin(170) =   0.174, cos(170) =  -0.985, tan(170) =  -0.176
    sin(180) =   0.000, cos(180) =  -1.000, tan(180) =  -0.000
    


```python

```
