# Week3 LAB(2022116624 강민정) 

1. LAB 3-1
1) 게임 사용자의 게임점수(game_score)가 1000점 이상이면 '당신은 고수입니다'를 출력하는 프로그램을 if 문을 이용하여 작성하시오. 이때 다음과 같이 game_score값을 화면에 출력하여라. game_score에 800점,1300점을 각각 입력하여 출력문을 확인하시오. 


```python
game_score=int(input("game_score = "))
if game_score >= 1000:
    print ("당신은 고수입니다")
```

    game_score = 1300
    당신은 고수입니다
    

2) num_a와 num_b에 할당된 값이 같으면 '두 값이 일치합니다.'를 출력하는 프로그램을 if 문을 이용하여 작성하시오. num_a와 num_b에 각각 100과 200이 할당되어 있는 경우와 num_a와 num_b에 300과 300이 할당되어 있는 경우에 대하여 각각 코드를 작성하고 출력문을 확인하시오. 


```python
num_a=100
num_b=200

if num_a==num_b:
    print('두 값이 일치합니다.')
```


```python
num_a=300
num_b=300

if num_a==num_b:
    print('두 값이 일치합니다.')
```

    두 값이 일치합니다.
    

2. LAB 3-2
1) 1에서 100 사이의 임의의 정수 n을 입력받아서 1) n을 화면에 출력한 후, 2) n이 짝수이면 "...은(는) 짝수입니다."를 다음과 같이 출력하는 프로그램을 작성하여라. 


```python
n=int(input("정수를 입력하세요 : "))
print("n = ",n)
if n%2==0:
    print(n,"은(는) 짝수입니다.")

```

    정수를 입력하세요 : 50
    n =  50
    50 은(는) 짝수입니다.
    


```python
n=int(input("정수를 입력하세요 : "))
print("n = ",n)
if n%2==0:
    print(n,"은(는) 짝수입니다.")
```

    정수를 입력하세요 : 75
    n =  75
    

2) -100에서 100 사이의 임의의 정수 x를 입력받아서 1) x를 화면에 출력한 후, 2) x가 0보다 큰 정수이면 "...은(는) 자연수입니다."를 다음과 같이 출력하는 프로그램을 작성하여라. 그렇지 않을 경우 x=-10과 같이 x를 단순 출력하여라.


```python
x=int(input("정수를 입력하세요 : "))
print("x = ",x)
if x>0:
    print(x,"은(는) 자연수입니다.")
```

    정수를 입력하세요 : 50
    x =  50
    50 은(는) 자연수입니다.
    


```python
x=int(input("정수를 입력하세요 : "))
print("x = ",x)
if x>0:
    print(x,"은(는) 자연수입니다.")
```

    정수를 입력하세요 : -10
    x =  -10
    

3. LAB 3-3
1) 게임 사용자의 게임점수(game_score)을 입력받아서 1000점 이상이면 '고수입니다.'를 출력하고 1000점 미만이면 '입문자입니다.'를 출력하는 프로그램을 if-esle 문을 이용하여 작성하시오. 


```python
game_score=int(input("게임점수를 입력하시오 : "))
print("game_score =", game_score)
if game_score >= 1000:
    print ("고수입니다")
else:
    print("입문자입니다.")
```

    게임점수를 입력하시오 : 800
    game_score = 800
    입문자입니다.
    


```python
game_score=int(input("게임점수를 입력하시오 : "))
print("game_score =", game_score)
if game_score >= 1000:
    print ("고수입니다")
else:
    print("입문자입니다.")
```

    게임점수를 입력하시오 : 1300
    game_score = 1300
    고수입니다
    

2) 두 정수를 입력받아 같을 경우 '두 값이 일치합니다.'를 출력하고 값이 다르면 '두 값이 일치하지 않습니다.'를 출력하는 프로그램을 if 문을 이용하여 작성하시오. 두 정수에 각각 100과 200이 할당되어 있는 경우와 300과 300이 할당되어 있는 경우의 출력문을 확인 하시오. 


```python
a=int(input("한 정수를 입력하시오 :"))
b=int(input("다른 정수를 입력하시오 :"))
if a==b:
    print("두 값이 일치합니다.")
else:
    print("두 값이 일치하지 않습니다.")
```

    한 정수를 입력하시오 :100
    다른 정수를 입력하시오 :200
    두 값이 일치하지 않습니다.
    


```python
a=int(input("한 정수를 입력하시오 :"))
b=int(input("다른 정수를 입력하시오 :"))
if a==b:
    print("두 값이 일치합니다.")
else:
    print("두 값이 일치하지 않습니다.")
```

    한 정수를 입력하시오 :300
    다른 정수를 입력하시오 :300
    두 값이 일치합니다.
    

3) if 문의 복합 조건식을 이용해서 다음과 같은 기능을 수행하는 프로그램을 만들어보자. 
1)우선 '당신은 성인인가요(성인이면 1, 미성년이면 0)' 문을 통해서 성인인지 미성년인지를 구한다음 미성년이면(0이 입력되면) '당신은 미성년자입니다.'를 출력하고 프로그램을 종료한다.  


```python
a=int(input("당신은 성인인가요(성인이면 1, 미성년이면 0):"))
if a==0:
    print("당신은 미성년자입니다.")
```

    당신은 성인인가요(성인이면 1, 미성년이면 0):0
    당신은 미성년자입니다.
    


```python
a=int(input("당신은 성인인가요(성인이면 1, 미성년이면 0):"))
if a==0:
    print("당신은 미성년자입니다.")

elif a==1:
    b=int(input("결혼은 하셨나요(기혼이면 1, 미혼이면 0):"))
    if b==1:
        print("당신은 결혼한 성인입니다.")
    else:
        print("당신은 결혼하지 않은 성인입니다.")
```

    당신은 성인인가요(성인이면 1, 미성년이면 0):1
    결혼은 하셨나요(기혼이면 1, 미혼이면 0):1
    당신은 결혼한 성인입니다.
    


```python
a=int(input("당신은 성인인가요(성인이면 1, 미성년이면 0):"))
if a==0:
    print("당신은 미성년자입니다.")

elif a==1:
    b=int(input("결혼은 하셨나요(기혼이면 1, 미혼이면 0):"))
    if b==1:
        print("당신은 결혼한 성인입니다.")
    else:
        print("당신은 결혼하지 않은 성인입니다.")
```

    당신은 성인인가요(성인이면 1, 미성년이면 0):1
    결혼은 하셨나요(기혼이면 1, 미혼이면 0):0
    당신은 결혼하지 않은 성인입니다.
    

4. LAB 3-4 
1) and 연산자를 사용하여 num 변수가 1과 10사이의 값을 가지면 True를 출력하는 부울식을 완성하여라.

num=int(input("num="))
if num>=1 and num<=10:
    print("True")

2) and 연산자를 사용하여 age가 10보다 크고 19보다 작으면 '청소년입니다.'를 출력하는 부울식을 작성하여라. 그리고 age에 9와 12를 넣어서 그 결과를 다음과 같이 확인하여라


```python
num=int(input("age ="))
if num>10 and num<19:
    print("청소년입니다.")
```

    age =10
    


```python
num=int(input("age ="))
if num>10 and num<19:
    print("청소년입니다.")
```

    age =12
    청소년입니다.
    

5. LAB 3-5 
1) 사용자로부터 자동차의 속도(speed)를 km/h 단위의 정수로 입력받도록 하자. 자동차의 속도가 100km/h 이상이면 '고속', 100km/h 미만 60km/h 이상이면 '중속', 60km/h 미만이면 '저속'을 출력하는 프로그램을 if-elif-else 문을 이용하여 작성하여라.


```python
speed=int(input("자동차의 속도를 입력하세요(단위 : km/h ): "))
if speed>=100:
    print("고속")
elif speed>=60 and speed<100:
    print("중속")
else:
    print("저속")
```

    자동차의 속도를 입력하세요(단위 : km/h ): 13
    저속
    


```python
speed=int(input("자동차의 속도를 입력하세요(단위 : km/h ): "))
if speed>=100:
    print("고속")
elif speed>=60 and speed<100:
    print("중속")
else:
    print("저속")
```

    자동차의 속도를 입력하세요(단위 : km/h ): 130
    고속
    

6. LAB 3-6
1) for 반복문에서 언더스코어 루프 제어변수를 사용하여 다음과 같이 Hello, Python!을 5번 출력하는 프로그램을 작성해 보자. 


```python
for i in range(5):
    print('Hello, Python!')
```

    Hello, Python!
    Hello, Python!
    Hello, Python!
    Hello, Python!
    Hello, Python!
    

2) i라는 루프변수를 사용해서 0에서 4까지의 정수를 출력하는 프로그램을 작성하시오. 


```python
for i in range(5):
    print(i)
```

    0
    1
    2
    3
    4
    

7. LAB 3-7
1) range() 함수와 list() 함수를 사용하여 1이상 100이하의 자연수 리스트를 다음과 같이 만드시오. 


```python
print(list(range(0,101)))

```

    [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 64, 65, 66, 67, 68, 69, 70, 71, 72, 73, 74, 75, 76, 77, 78, 79, 80, 81, 82, 83, 84, 85, 86, 87, 88, 89, 90, 91, 92, 93, 94, 95, 96, 97, 98, 99, 100]
    

2) 1 이상 100 이하의 짝수 리스트를 만드시오. 


```python
print(list(range(2,101,2)))
```

    [2, 4, 6, 8, 10, 12, 14, 16, 18, 20, 22, 24, 26, 28, 30, 32, 34, 36, 38, 40, 42, 44, 46, 48, 50, 52, 54, 56, 58, 60, 62, 64, 66, 68, 70, 72, 74, 76, 78, 80, 82, 84, 86, 88, 90, 92, 94, 96, 98, 100]
    

3) 1 이상 100 이하의 홀수 리스트를 만드시오. 


```python
print(list(range(1,101,2)))
```

    [1, 3, 5, 7, 9, 11, 13, 15, 17, 19, 21, 23, 25, 27, 29, 31, 33, 35, 37, 39, 41, 43, 45, 47, 49, 51, 53, 55, 57, 59, 61, 63, 65, 67, 69, 71, 73, 75, 77, 79, 81, 83, 85, 87, 89, 91, 93, 95, 97, 99]
    

4) -100보다 크고 0보다 작은 음수 리스트를 만드시오.


```python
print(list(range(-99,0,1)))
```

    [-99, -98, -97, -96, -95, -94, -93, -92, -91, -90, -89, -88, -87, -86, -85, -84, -83, -82, -81, -80, -79, -78, -77, -76, -75, -74, -73, -72, -71, -70, -69, -68, -67, -66, -65, -64, -63, -62, -61, -60, -59, -58, -57, -56, -55, -54, -53, -52, -51, -50, -49, -48, -47, -46, -45, -44, -43, -42, -41, -40, -39, -38, -37, -36, -35, -34, -33, -32, -31, -30, -29, -28, -27, -26, -25, -24, -23, -22, -21, -20, -19, -18, -17, -16, -15, -14, -13, -12, -11, -10, -9, -8, -7, -6, -5, -4, -3, -2, -1]
    

8. LAB 3-8
1) 앞서 배운 누적 덧셈을 응용하여 1에서 100까지 정수의 합을 구하여 출력하여라.


```python
s=0
for i in range(1,101):
    s=s+i
print(s)
```

    5050
    

2) range() 함수의 step 값을 이용하여 1에서 100까지 정수 중에서 짝수의 합을 구하여 출력하여라. 


```python
s=0
for i in range(0,101,2):
    s=s+i
print(s)
```

    2550
    

3) range() 함수의 step 값을 이용하여 1에서 100까지 정수 중에서 홀수의 합을 구하여 출력하여라. 


```python
s=0
for i in range(1,100,2):
    s=s+i
print(s)
```

    2500
    

9. LAB 3-9
1)이중 for 루프를 이용하여 다음과 같은 패턴을 출력하여라.


```python
n=7
for i in range(n):
    print(' '*(n-(i+1))+"#")
```

          #
         #
        #
       #
      #
     #
    #
    


```python

```
