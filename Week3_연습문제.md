# Week3 연습문제(2022116624 강민정) 

1. 다음과 같이 사용자로부터 3개의 임의의 정수를 입력으로 받아서 가장 작은 수부터 큰 수가지 나열하는 프로그램을 if-else 문을 사용하여 작성하시오. 


```python
a,b,c=map(int,input("세 정수를 입력하시오:").split())
if a>b:
     if a>c:
          if b>c:
               print(c,b,a)
          else:
               print(b,c,a)
     else:
          print(c,a,b)
else:
     if b>c:
          if a<c:
               print(a,c,b)
          else:
               print(c,a,b)
     else:
          print(a,b,c)

```

    세 정수를 입력하시오:9 12 4
    4 9 12
    


```python
a,b,c=map(int,input("세 정수를 입력하시오:").split())
if a>b:
     if a>c:
          if b>c:
               print(c,b,a)
          else:
               print(b,c,a)
     else:
          print(c,a,b)
else:
     if b>c:
          if a<c:
               print(a,c,b)
          else:
               print(c,a,b)
     else:
          print(a,b,c)

```

    세 정수를 입력하시오:99 12 4
    4 12 99
    

2. 사용자로부터 x,y 좌표를 가진 한 점을 입력으로 받아서 이 점이 1,2,3,4 분면의 어디에 속하는지를 알려주는 프로그램을 작성하시오. 


```python
x,y=map(int,input("점의 좌표 x,y를 입력하시오 : ").split())
if x>0 and y>0:
     print("1사분면에 있음")
elif x<0 and y>0:
     print("2사분면에 있음")
elif x<0 and y<0:
     print("3사분면에 있음")
else:
     print("4사분면에 있음")

```

    점의 좌표 x,y를 입력하시오 : 2 4
    1사분면에 있음
    


```python
x,y=map(int,input("점의 좌표 x,y를 입력하시오 : ").split())
if x>0 and y>0:
     print("1사분면에 있음")
elif x<0 and y>0:
     print("2사분면에 있음")
elif x<0 and y<0:
     print("3사분면에 있음")
else:
     print("4사분면에 있음")

```

    점의 좌표 x,y를 입력하시오 : -2 -4
    3사분면에 있음
    

3. 사용자로부터 점수를 입력받은 다음 게임 사용자의 게임점수(game_score)가 1000점 이상이면 '고수입니다.'를 출력하고 1000점 미만이면 '입문자입니다.'를 출력하는 프로그램을 if-else문을 이용하여 작성하시오. 


```python
game_score=int(input("게임점수를 입력하시오 : "))
               
if game_score>=1000:
     print("고수입니다.")
else:
     print("입문자입니다.")

```

    게임점수를 입력하시오 : 4222
    고수입니다.
    


```python
game_score=int(input("게임점수를 입력하시오 : "))
               
if game_score>=1000:
     print("고수입니다.")
else:
     print("입문자입니다.")

```

    게임점수를 입력하시오 : 4
    입문자입니다.
    

4. 다음의 프로그램은 어떤 결과 값을 출력하는가? 출력결과를 미리 예측한 후 타이핑하여 그 결과가 맞는지 확인해 보도록 하자. 

1) 예측결과 
Python
is
Fun!
Python
is
Fun!
Python
is
Fun!



```python
#실행
for i in range(3):
     print('Python')
     print('is')
     print('FUN!')

```

    Python
    is
    FUN!
    Python
    is
    FUN!
    Python
    is
    FUN!
    

2)예측결과
FUN!


```python
#실행
print('FUN!')
```

    FUN!
    

5. 소수란 양의 자연수 중에서 1과 자기 자신이외의 약수를 가지지 않는 수를 말한다. 사용자로부터 양의 정수 n을 입력받은 후 이 숫자가 소수인지 아닌지를 판별하는 프로그램을 작성하시오. 이때 수행 속도를 개선하기 위하여 2로 나누어 본 후 나누어지지 않을 경우 3, 5, 7, … 과 같은 홀수로 나눗셈을 시도하도록 코딩하여라.


```python
n=int(input("숫자를 입력하세요 : "))
a=0


for i in range(2,n):
     if n%i==0:
          a=1
   


if a==0:
     print(n,"는 소수입니다.")
else:
     
     print(n,"는 소수가 아닙니다.")
     
```

    숫자를 입력하세요 : 5
    5 는 소수입니다.
    


```python
n=int(input("숫자를 입력하세요 : "))
a=0


for i in range(2,n):
     if n%i==0:
          a=1
   


if a==0:
     print(n,"는 소수입니다.")
else:
     
     print(n,"는 소수가 아닙니다.")
     
```

    숫자를 입력하세요 : 9
    9 는 소수가 아닙니다.
    

6.	암스트롱 수란 세 자리의 정수 중에서 각 자리의 수를 세제곱한 수의 합과 자신이 같은 수를 말한다. 구체적인 예를 들면 153은 1 + 125 + 27 의 합으로 구성될 수 있는데 이러한 수가 암스트롱 수이다. 세 자리 정수들 중에서 모든 암스트롱 수를 구하여 다음과 같이 출력하여라.


```python
for i in range(100,1000):
     a=i//100
     b=(i%100)//10
     c=((i%100)%10)

     total=(a**3)+(b**3)+(c**3)

     if(i==total):
          print("세 자리의 암스트롱 수:", i)

```

    세 자리의 암스트롱 수: 153
    세 자리의 암스트롱 수: 370
    세 자리의 암스트롱 수: 371
    세 자리의 암스트롱 수: 407
    

7.	다음과 같이 사용자로부터 1에서 9사이의 숫자를 입력받아 입력받은 숫자의 절에 해당하는 구구단을 출력하는 프로그램을 for문과 while 문을 사용하여 작성하여라. 만일 1에서 9 이외의 숫자가 입력되면 ‘1에서 9까지의 수를 다시 입력하세요’라는 안내문을 출력하여라.


```python
num=int(input("1에서 9까지의 수를 입력하세요:"))

while num<1 or num>9:
     num=int(input("1에서 9까지의 수를 다시 입력하세요:"))

for i in range(1,10):
    n=num*i
    print(num,"*",i,"=",n)
 

```

    1에서 9까지의 수를 입력하세요:11
    1에서 9까지의 수를 다시 입력하세요:134
    1에서 9까지의 수를 다시 입력하세요:2
    2 * 1 = 2
    2 * 2 = 4
    2 * 3 = 6
    2 * 4 = 8
    2 * 5 = 10
    2 * 6 = 12
    2 * 7 = 14
    2 * 8 = 16
    2 * 9 = 18
    

8.	맛나 식당의 메뉴 주문 프로그램을 개발하고자 한다. 이를 위해 사용자에게 다음과 같은 메뉴를 보여주고 이중에서 메뉴에 대응되는 하나의 알파벳을 선택하도록 하자. 이때 메뉴에 없는 알파벳이 입력되면 ‘메뉴를 다시 입력하세요:  ’가 출력되도록 한 후 다시 입력을 받도록 하자


```python
print("맛나 식당에 오신 것을 환영합니다. 메뉴는 다음과 같습니다.")
print("- 삼겹구이 (입력 s)")
print("- 오삼불고기 (입력 o)")
print("- 된장찌개 (입력 d)")
menu=input("메뉴를 선택하세요(알파벳 s,o,d 입력) : ")
while True:
     if menu=="s":
          print("삼겹구이를 선택하였습니다.")
          break
     elif menu=="o":
          print("오삼불고기를 선택하였습니다. ")
          break
     elif menu=="d":
          print("된장찌개를 선택하였습니다. ")
          break
     else:
          menu=input("메뉴를  다시 입력하세요(알파벳 s,o,d 입력) : ")
```

    맛나 식당에 오신 것을 환영합니다. 메뉴는 다음과 같습니다.
    - 삼겹구이 (입력 s)
    - 오삼불고기 (입력 o)
    - 된장찌개 (입력 d)
    메뉴를 선택하세요(알파벳 s,o,d 입력) : o
    오삼불고기를 선택하였습니다. 
    

9.	이중 for 문을 사용하여 숫자를 입력 받아 다음과 같은 삼각형을 출력하는 프로그램을 작성하시오. 이때 아래 결과와 같이 숫자 10이 입력되면 높이가 10이고 제일 마지막 줄의 별이 10개가 삼각형 형태로 나타나도록 하시오


```python
n=int(input("숫자를 입력하세요 : "))


for i in range(1,n+1):
     for j in range(n-i):
          print(" ", end="")
     for j in range(i):
          print("*",end="")
     print()

     

```

    숫자를 입력하세요 : 10
             *
            **
           ***
          ****
         *****
        ******
       *******
      ********
     *********
    **********
    

10.	사용자로부터 숫자 1보다 크고 10보다 작은 값 n을 입력으로 받아서 다음과 같이 뱀의 몸통처럼 증가하는 이차원 배열을 출력하여라. (이 배열은 마치 뱀의 몸통처럼 ‘ㄹ’과 같은 패턴을 그리며 수가 1씩 증가하는 형태의 배열이다.) 


```python
n=int(input("n을 입력하시오 : "))

c=0
a=[[0]*n for i in range(n)]

for j in range(n):
     for k in range(n):
          c+=1
          a[j][k]=c
          print("%3d"%(a[j][k]),end=" ")
     print("\n")
     

```

    n을 입력하시오 : 5
      1   2   3   4   5 
    
      6   7   8   9  10 
    
     11  12  13  14  15 
    
     16  17  18  19  20 
    
     21  22  23  24  25 
    
    


```python
n=int(input("n을 입력하시오 : "))

c=0
a=[[0]*n for i in range(n)]

for j in range(n):
     for k in range(n):
          c+=1
          a[j][k]=c
          print("%3d"%(a[j][k]),end=" ")
     print("\n")
     

```

    n을 입력하시오 : 7
      1   2   3   4   5   6   7 
    
      8   9  10  11  12  13  14 
    
     15  16  17  18  19  20  21 
    
     22  23  24  25  26  27  28 
    
     29  30  31  32  33  34  35 
    
     36  37  38  39  40  41  42 
    
     43  44  45  46  47  48  49 
    
    


```python

```
