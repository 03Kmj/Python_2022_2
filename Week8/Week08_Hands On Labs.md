# Week_08 Hands On Labs

* LAB 8-1 : 다음 코드는 각각 어떤 예외를 발생시키는가?

1. 다음 코드는 각각 어떤 예외를 발생시키는가?


```python
a=[10,20,300]
a[3]
```


    ---------------------------------------------------------------------------

    IndexError                                Traceback (most recent call last)

    Input In [6], in <cell line: 2>()
          1 a=[10,20,300]
    ----> 2 a[3]
    

    IndexError: list index out of range



```python
n=int("20%")
```


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    Input In [7], in <cell line: 1>()
    ----> 1 n=int("20%")
    

    ValueError: invalid literal for int() with base 10: '20%'



```python
a=100+"200"
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Input In [8], in <cell line: 1>()
    ----> 1 a=100+"200"
    

    TypeError: unsupported operand type(s) for +: 'int' and 'str'


2. 위의 문제 1번 코드를 try - except 문으로 감싸고 Exception e를 출력하여 어떤 출력문이 나오는지 확인하고 적으시오. 


```python
try:
    a=[10,20,30]
    a[3]
except Exception as e:
    print("error:",e)
```

    error: list index out of range
    


```python
try:
    n=int("20%")
   
except Exception as e:
    print("error:",e)
```

    error: invalid literal for int() with base 10: '20%'
    


```python
try:
    a=100+'200'
except Exception as e:
    print("error:",e)
```

    error: unsupported operand type(s) for +: 'int' and 'str'
    

* LAB 8-2: 다음 코드는 어떤 예외를 발생시키는가?

1. 다음 코드가 있을 경우 이 코드에 적합한 예외 처리문을 만드시오.

>10 * ( 30 / 0 )


```python
try:
    a, b, c= input('세 수를 입력하시오: ').split()
    result = int(a) * int(b) / int(c)
except ZeroDivisionError:
    print('오류 : 0으로 나눔을 시도했습니다.')
```

    세 수를 입력하시오: 10 30 0
    오류 : 0으로 나눔을 시도했습니다.
    

> x = int(input("정수 x를 입력하세요: "))


```python
try:
    x = int(input("정수 x를 입력하세요: "))
except ValueError:
    print('오류 : 입력 값이 정수나 실수가 아닙니다.')
```

    정수 x를 입력하세요: 이십
    오류 : 입력 값이 정수나 실수가 아닙니다.
    

>import sys   
f = open('myfile.txt')   
s = f.readline()


```python
try:
    import sys   
    f = open('myfile.txt')   
    s = f.readline()
except Exception as e:
    print("error: ",e)
    
```

    error:  [Errno 2] No such file or directory: 'myfile.txt'
    

* LAB 8-3: 예외의 생성과 처리

1. [1, 2, 3, 4, 5]의 다섯개의 요소를 가진 리스트 a가 있을 때 다음과 같이 사용자로부터 정수를 입력 받은 후 이에 해당하는 인덱스를 출력하도록 하자.

> a = [1, 2, 3, 4, 5]   
a의 요소를 하나 선택하시오 :   
2 은(는) 두 번째 요소입니다.

>a=[1, 2, 3, 4, 5]   
a의 요소를 하나 선택하시오 :   
1 은(는) 첫 번째 요소입니다.


```python
a=[1, 2, 3, 4, 5]
inNum=int(input("a의 요소를 하나 선택하시오: "))
if (inNum==a[0]):
    print("{} 은(는) 첫 번째 요소입니다.".format(inNum))
elif (inNum==a[1]):
    print("{} 은(는) 두 번째 요소입니다.".format(inNum))
elif (inNum==a[2]):
    print("{} 은(는) 세 번째 요소입니다.".format(inNum))
elif (inNum==a[3]):
    print("{} 은(는) 네 번째 요소입니다.".format(inNum))
elif (inNum==a[4]):
    print("{} 은(는) 다섯 번째 요소입니다.".format(inNum))
else:
    print("다시 입력하세요.")
```

    a의 요소를 하나 선택하시오: 1
    1 은(는) 첫 번째 요소입니다.
    

2. 다음과 같이 '삼'이 입력되면 try - except 문을 통해 '오류 : 입력 값이 정수나 실수가 아님'을 출력하시오.

>a = [1, 2, 3, 4, 5]   
a의 요소를 하나 선택하시오: 삼   
오류 : 입력 값이 정수나 실수가 아님   


```python
try:
    a=[1, 2, 3, 4, 5]
    inNum=int(input("a의 요소를 하나 선택하시오: "))
    if (inNum==a[0]):
        print("{} 은(는) 첫 번째 요소입니다.".format(inNum))
    elif (inNum==a[1]):
        print("{} 은(는) 두 번째 요소입니다.".format(inNum))
    elif (inNum==a[2]):
        print("{} 은(는) 세 번째 요소입니다.".format(inNum))
    elif (inNum==a[3]):
        print("{} 은(는) 네 번째 요소입니다.".format(inNum))
    elif (inNum==a[4]):
        print("{} 은(는) 다섯 번째 요소입니다.".format(inNum))
except ValueError:
    print('오류 : 입력 값이 정수나 실수가 아님')    
```

    a의 요소를 하나 선택하시오: 삼
    오류 : 입력 값이 정수나 실수가 아님
    

* LAB 8-4: 파일 저장하기

1. 다음과 같은 내용을 가지는 numbers.txt 파일을 파이썬의 write() 메소드를 이용하여 작성하여라. 이때 아래와 같이 줄바꿈이 되도록 하자. 

>100   
200   
300   
400


```python
f=open("numbers.txt","w")
f.write("100\n")
f.write("200\n")
f.write("300\n")
f.write("400\n")
f.close()
```

2. 다음과 같은 내용을 가지는 we_will_rock.txt 파일을 파이썬의 write() 메소드를 이용하여 작성하여라. 따옴표의 출력에 주의하여 프로그램을 작성하자.


```python
f=open("we_will_rock.txt","w")
f.write("Buddy, tou're a boy, make a big noise\n")
f.write("Playing in the street, gonna be a big man someday\n")
f.write("You got mud on your face, you big disgrace\n")
f.write("Kicking your can all over the place, singin'\n")
f.write("We will, we will rock you\n")
f.write("We will, we will rock you\n")
```

* LAB 8-5: 파일 읽어오기

1. 다음과 같은 내용을 가지는 numbers.txt 파일을 파이썬의 read() 메소드를 이용하여 출력하시오(힌트 : f.readline().rstrip()을 사용하여라).

>100   
200   
300   
400


```python
f=open("numbers.txt","r")
s=f.readline().rstrip()
print(s)
s=f.readline().rstrip()
print(s)
s=f.readline().rstrip()
print(s)
s=f.readline().rstrip()
print(s)
f.close()
```

    100
    200
    300
    400
    

2. 다음과 같은 내용을 가지는 we_will_rock.txt 파일을 파이썬의 read() 메소드를 이용하여 출력하여라.(힌트 : f.readline().rstrip()을 사용하여라)


```python
f=open("we_will_rock.txt","r")
s=f.readline().rstrip()
print(s)
s=f.readline().rstrip()
print(s)
s=f.readline().rstrip()
print(s)
s=f.readline().rstrip()
print(s)
s=f.readline().rstrip()
print(s)
s=f.readline().rstrip()
print(s)
f.close()
```

    Buddy, tou're a boy, make a big noise
    Playing in the street, gonna be a big man someday
    You got mud on your face, you big disgrace
    Kicking your can all over the place, singin'
    We will, we will rock you
    We will, we will rock you
    

* LAB 8-6: 파일 저장하기

1. 사용자로부터 파일 이름을 입력으로 받은 후 입력받은 파일의 모든 문자를 대문자로 변환한 후 출력하여라. 그리고 이 내용을 [파일명_upper].txt 라는 이름의 파일로 저장하여라(힌트: 문자열의 upper() 메소드를 사용하시오.


```python
fname=input("입력할 파일의 이름: ")
f=open(fname,"r")

f2=open("we_will_rock_upper.txt","w")
cnt=f.readline()
while cnt:
    print(cnt.upper(),end="")
    f2.write(cnt)
    cnt=f.readline()
f.close()
```

    입력할 파일의 이름: we_will_rock.txt
    BUDDY, TOU'RE A BOY, MAKE A BIG NOISE
    PLAYING IN THE STREET, GONNA BE A BIG MAN SOMEDAY
    YOU GOT MUD ON YOUR FACE, YOU BIG DISGRACE
    KICKING YOUR CAN ALL OVER THE PLACE, SINGIN'
    WE WILL, WE WILL ROCK YOU
    WE WILL, WE WILL ROCK YOU
    


```python
fname=input("입력할 파일의 이름: ")
with open(fname,"r") as f:
    cnt=f.readlines()

cnt.reverse()
    
for line in cnt:
    line=line.strip()
    print(line)
    

```

    입력할 파일의 이름: we_will_rock.txt
    We will, we will rock you
    We will, we will rock you
    Kicking your can all over the place, singin'
    You got mud on your face, you big disgrace
    Playing in the street, gonna be a big man someday
    Buddy, tou're a boy, make a big noise
    
