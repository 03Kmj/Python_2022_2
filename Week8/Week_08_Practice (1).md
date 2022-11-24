# Week_08_Practice

1. 다음과 같은 내용을 포함하고 있는 greet.txt 파일을 파이썬의 write() 메소드를 이용하여 작성하시오. 이때 greet.txt 파일이 이미 존재할 경우를 가정하고 이 파일이 쓰기 금지 모드(읽기 모드)로 되어 있을 가능성이 있기 때문에 이를 위한 예외처리 기능을 구현하시오.

![image.png](attachment:image.png)


```python
import sys
try:
    f=open("greet.txt","w")
    f.write('Hi, everyone\nWelcome to Python')
    f.close()
except Exception as e:
    print("ERROR::",e)
```

    ERROR:: [Errno 13] Permission denied: 'greet.txt'
    

2. 다음과 같은 내용을 포함하고 있는 number1to10.txt 파일을 한 줄씩 읽어들이도록 하여라.

> (1) 이 파일을 읽어서 각 행의 정수에 곱하기 10을 수행한 후 다음과 같은 numberby10.txt라는 이름의 파일로 저장하여라.    
<(위) number1to10 & (아래) numberby10.txt>
![image.png](attachment:image.png) ![image-2.png](attachment:image-2.png)


```python
f=open("number1to10.txt","r")
f2=open("numberby10.txt","w")

cnt_=f.readline()
for cnt in cnt_:
    cnt=cnt.strip()
    f2.write("{}\n".format(str(int(cnt)*10)))

f.close()
f2.close()
```


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    Cell In [13], line 7
          5 for cnt in cnt_:
          6     cnt=cnt.strip()
    ----> 7     f2.write("{}\n".format(str(int(cnt)*10)))
          9 f.close()
         10 f2.close()
    

    ValueError: invalid literal for int() with base 10: ''




> 위 두 파일을 읽어서 다음과 같이 각 행의 값을 하나의 내용으로 묶어서 저장하는 프로그램을 작성하여라. 이 파일의 이름은 merge.txt이다.   
![image.png](attachment:image.png)


```python
fp1 = open("number1to10.txt", "r")
fp2 = open("numberby10.txt", "r")
fp3 = open("merge.txt", "w")

lines1 = fp1.readlines()
lines2 = fp2.readlines()
for line1, line2 in zip(lines1, lines2):
    line1 = line1.strip()
    line2 = line2.strip()
    fp3.write("{} : {}\n".format(line1, line2))
fp1.close()
fp2.close()
fp3.close()
```



3. "Hello Python"이라는 문자열을 파일로 저장하기 위하여 my_hello.txt 라는 파일을 열고 쓰기를 시도하였다. 이때 이 파일이 이미 존재하고 있으며 문제 1번의 읽기 모드 설정 방법을 참고하여 이미 이 파일이 읽기 모드로 설정되어 있다고 가정한다.   
(1) 이 상황에서는 어떤 예외가 발생하는지, 실제로 파일을 만들어서 이러한 상황을 테스트하는 프로그램을 작성하여 예외를 출력하여라.   
(2) 이 예외를 처리하는 try-exception 문을 구현하여라.


```python
fp = open("my_hello.txt", "w")
fp.write("Hello Python")
fp.close()
```


```python
try:
    fp = open("my_hello.txt", "w")
    fp.write("Hello Python")
    fp.close()
except Exception as e:
    print("ERROR::", e)
```

4. 다음과 같은 내용을 포함하고 있는 hello.txt 파일을 텍스트 편집기를 이용하여 작성하시오.   
![image.png](attachment:image.png)   
(1)이제 이 파일을 open() 함수를 통해 읽어서 이 파일의 내용을 다음과 같이 화면에 출력하시오.   
![image-2.png](attachment:image-2.png)   
(2)이 파일을 open() 함수를 통해 읽어서 원래 파일의 내용 아래쪽에 'Welcome to Python!'을 추가한 후 저장하시오. 그리고 다시 한 번 파일을 읽어서 다음과 같이 화면에 출력하시오.   
![image-3.png](attachment:image-3.png)


```python
f = open("hello.txt", "r")
print("hello.txt 파일:")
lines = f.readlines()
for line in lines:
    line = line.strip()
    print(line)
```


```python
f = open("hello.txt", "r+")

f.write("\nWelcome to Python!")
print("hello.txt 파일:")
lines = f.readlines()
for line in lines:
    line = line.strip()
    print(line)
```

5. 1에서 10 사이의 랜덤한 숫자를 30개 가진 randint30.txt 라는 파일을 random 모듈을 사용하여 생성하시오. 이 때 생성한 숫자는 다음과 같이 공백으로 구분하여 나열하시오.   
![image.png](attachment:image.png)   

위의 randint30.txt라는 파일을 읽어서 1에서 10까지 정수의 출현횟수를 다음과 같이 출력하여라.   
![image.png](attachment:image.png)


```python
import random as rd

f = open("randint30.txt", "w")
for _ in range(30):
    f.write("{} ".format(str(rd.randint(1, 10))))
f.close()

f = open("randint30.txt", "r")
cnt = [0 for i in range(1, 11)]
nums = f.readline()
nums = nums.split()
for num in nums:
    cnt[int(num)-1] += 1
for i in range(10):
    print("{} : {}개".format(i+1, cnt[i]))
```

    1 : 6개
    2 : 2개
    3 : 4개
    4 : 4개
    5 : 4개
    6 : 5개
    7 : 2개
    8 : 1개
    9 : 1개
    10 : 1개
    


```python

```
