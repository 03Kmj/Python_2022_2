# Week_13 Hands On Lab

* LAB 10-1 :  일반 함수와 람다 함수의 정의와 호출

1. 두 수의 차를 구하여 반환하는 sub라는 이름의 함수를 정의하여 호출하여라. sub(200, 100)을 이용하여 함수를 호출하고 그 반환 값을 다음과 같이 출력하여라.


```python
def sub(x,y):
    return x-y

print("200 - 100 =", sub(200,100))
```

    200 - 100 = 100
    

2. 1번 문제에서 정의한 sub() 함수를 람다 함수를 이용하여 구현하여라. 그리고 그 반환 값을 다음과 같이 출력하여라. 


```python
sub=lambda x,y: x-y
print('200 - 100 =',sub(200,100))
```

    200 - 100 = 100
    

* LAB 10-2 : 람다 함수의 응용

1. 정수 요소 값을 가진 n_list = [1,2,3,4,5,6,7,8,9,10]라는 리스트가 있다. n_list에서 짝수 값 항목만을 가진 even_list라는 리스트를 람다 함수를 이용하여 아래와 같이 생성해 보자.


```python
n_list = [1,2,3,4,5,6,7,8,9,10]
even_list=list(filter(lambda x:x%2==0,n_list))
print("even_list =",even_list)
```

    even_list = [2, 4, 6, 8, 10]
    

2. 1번 문제에서 사용한 n_list 리스트에 람다 함수를 이용하여 홀수 값 항목만을 가진 다음과 같은 odd_list를 생성해 보자.


```python
n_list = [1,2,3,4,5,6,7,8,9,10]
even_list=list(filter(lambda x:x%2!=0,n_list))
print("even_list =",even_list)
```

    even_list = [1, 3, 5, 7, 9]
    

* LAB 10-3 : map() 함수의 응용

1. ['a', 'b', 'c', 'd']와 같은 영문 소문자가 들어있는 a_list라는 이름의 리스트를 ['A', 'B', 'C', 'D']와 같이 영문 대문자가 들어있는 upper_a_list라는 이름의 리스트로 변환시키는 map() 함수를 작성하여라.


```python
n_list = [1,2,3,4,5,6,7,8,9,10]
even_list=list(filter(lambda x:x%2==0,n_list))
print("even_list =",even_list)
```

    even_list = [2, 4, 6, 8, 10]
    

2. [10, 20, 30]과 같은 값을 가진 n_list라는 이름의 리스트를 map() 함수에 넣은 후의 결과는 각각 다음과 같다. 


```python
n_list = [10, 20, 30]
twice_list = list(map(lambda x:x*2,n_list))
triple_list = list(map(lambda x:x*3,n_list))
print('입력 값의 두 배 :',twice_list)
print('입력 값의 세 배 :',triple_list)
```

    입력 값의 두 배 : [20, 40, 60]
    입력 값의 세 배 : [30, 60, 90]
    

* LAB 10-4 : reduce() 함수의 응용

1. reduce() 함수를 사용하여 1에서 100까지 정수의 합을 구하여라. 이 때 range(1,101)을 입력으로 사용하여라.


```python
from functools import reduce

a=[]
for i in range(1,101):
     a.append(i)

n=reduce(lambda x,y: x+y,a)
print('1에서 100까지의 합 :',n)
```

    1에서 100까지의 합 : 5050
    

2. reduce() 함수를 사용하여 10!을 구하여라. 이 때 range(1,11)을 입력으로 사용하여라.


```python
from functools import reduce

a=[]
for i in range(1,11):
     a.append(i)

n=reduce(lambda x,y: x*y,a)
print('10! =',n)
```

    10! = 3628800
    

* LAB 10-5 : 리스트의 축약기능

1. 리스트의 축약기능을 이용하여 1에서 10 사이 정수의 세제곱 값을 가지는 리스트 cubic를 다음과 같이 생성하여라.


```python
cubic=[x**3 for x in range(1,11)]
print("cubic =",cubic)
```

    cubic = [1, 8, 27, 64, 125, 216, 343, 512, 729, 1000]
    

2. 리스트 축약기능을 이용하여 ['welcome', 'to', 'the', 'python', 'world']라는 항목을 가지는 리스트 a로부터 첫 알파벳을 추출한 first_a 리스트를 생성하여라.


```python
a=['welcome', 'to', 'the', 'python', 'world']
first_a = [x[:1] for x in a]
print('a =',a)
print('first_a =',first_a)
```

    a = ['welcome', 'to', 'the', 'python', 'world']
    first_a = ['w', 't', 't', 'p', 'w']
    

* LAB 10-6 : 리스트의 축약기능과 조건식

1. 리스트 축약기능과 조건식을 사용하여 1에서 10사이 정수의 세제곱 값 중에서 500 이하인 값만을 가진 cubic 리스트를 다음과 같이 생성하여라. 


```python
cubic=[x**3 for x in range(1,11) if x**3<500]
print('cubic =',cubic)
```

    cubic = [1, 8, 27, 64, 125, 216, 343]
    

2. st = 'Hello 1234 Python'라는 문자열이 있다. 리스트 축약기능과 조건식을 사용하여 이 문자열로부터 ['1', '2', '3', '4']를 추출하여 다음과 같이 출력하여라(힌트 : isdigit()메소드를 사용함.)


```python
st='Hello 1234 Python'
s_list=[x for x in st if x.isdigit()==True]
print(s_list)
```

    ['1', '2', '3', '4']
    

* LAB 10-7 : 반복자 객체 만들기

1. 짝수를 순차적으로 반환하는 __next__() 메소드를 가진 EventCounter라는 이름의 클래스를 정의하고 my_even 객체를 생성하여라. 이 객체의 __next__()메소드를 호출하여 다음과 같이 출력하여라. 


```python
class EvenCounter:
     def __init__(self, n=0):
          self.n=n
     def __iter__(self):
          return self
     def __next__(self):
          temp=self.n
          self.n+=2
          return temp

my_counter = EvenCounter()
print(next(my_counter))
print(my_counter.__next__())
print(my_counter.__next__())
print(my_counter.__next__())
print(my_counter.__next__())
```

    0
    2
    4
    6
    8
    

2. 1번 문제를 통해 생성한 my_even 객체를 이용하여 for 문에서 다음과 같이 20 이하의 짝수를 출력하여라. 


```python
class EvenCounter:
     def __init__(self, n=0):
          self.n=n
     def __iter__(self):
          return self
     def __next__(self):
          temp=self.n
          self.n+=2
          return temp

my_counter = EvenCounter()
for x in my_counter:
     if x>20:
          break
     print(x,end= ' ')
```

    0 2 4 6 8 10 12 14 16 18 20 

* LAB 10-8 : split()과 join()

1. 다음 코드의 실행 결과는 무엇인가?


```python
txt = 'Welcome to Busan Metropolitan City'
txt.split()
```




    ['Welcome', 'to', 'Busan', 'Metropolitan', 'City']



2. 다음 코드의 실행 결과는 무엇인가?


```python
greet = 'Hello, My name is DongMin, Good to see you again'
greet.split(',')
```




    ['Hello', ' My name is DongMin', ' Good to see you again']



3. 다음 코드와 같이 '|'로 구분된 과일의 이름을 가진 fruits 문자열이 있다. 이 문자열을 split()을 이용하여 구분하여 ['Apple', 'Banana', 'Melon', 'Orange']와 같은 문자열의 리스트로 만드시오.


```python
fruits = 'Apple|Banana|Melon|Orange'
fruits_list = fruits.split('|')
print("fruits =",fruits)
print(fruits_list)
```

    fruits = Apple|Banana|Melon|Orange
    ['Apple', 'Banana', 'Melon', 'Orange']
    
