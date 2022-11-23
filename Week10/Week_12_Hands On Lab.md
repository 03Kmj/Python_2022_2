# Week_12 Hands On Lab

* LAB 9-1 : 객체와 메소드 호출

1. 다음 메소드 호출의 결과는 무엇인가?


```python
(200).__sub__(100)
```




    100




```python
(200).__mul__(100)
```




    20000




```python
(200).__truediv__(100)
```




    2.0



2. 다음 메소드 호출의 결과는 무엇인가?


```python
[10, 20, 30, 40].pop()
```




    40



3. 다음 중 리스트 객체가 호출할 수 없는 메소드는 무엇인가?   
> 1)pop()   2)keys()   3)remove()   4)get()

4)get() -> 딕셔너리 자료형에서 사용

4. 다음과 같은 방법으로 int 클래스의 메소드와 속성을 조사하여라. 


```python
dir(int)
```




    ['__abs__',
     '__add__',
     '__and__',
     '__bool__',
     '__ceil__',
     '__class__',
     '__delattr__',
     '__dir__',
     '__divmod__',
     '__doc__',
     '__eq__',
     '__float__',
     '__floor__',
     '__floordiv__',
     '__format__',
     '__ge__',
     '__getattribute__',
     '__getnewargs__',
     '__gt__',
     '__hash__',
     '__index__',
     '__init__',
     '__init_subclass__',
     '__int__',
     '__invert__',
     '__le__',
     '__lshift__',
     '__lt__',
     '__mod__',
     '__mul__',
     '__ne__',
     '__neg__',
     '__new__',
     '__or__',
     '__pos__',
     '__pow__',
     '__radd__',
     '__rand__',
     '__rdivmod__',
     '__reduce__',
     '__reduce_ex__',
     '__repr__',
     '__rfloordiv__',
     '__rlshift__',
     '__rmod__',
     '__rmul__',
     '__ror__',
     '__round__',
     '__rpow__',
     '__rrshift__',
     '__rshift__',
     '__rsub__',
     '__rtruediv__',
     '__rxor__',
     '__setattr__',
     '__sizeof__',
     '__str__',
     '__sub__',
     '__subclasshook__',
     '__truediv__',
     '__trunc__',
     '__xor__',
     'as_integer_ratio',
     'bit_count',
     'bit_length',
     'conjugate',
     'denominator',
     'from_bytes',
     'imag',
     'numerator',
     'real',
     'to_bytes']



5. 다음과 같은 방법으로 list 클래스의 메소드와 속성을 조사하여라. 


```python
dir(list)
```




    ['__add__',
     '__class__',
     '__class_getitem__',
     '__contains__',
     '__delattr__',
     '__delitem__',
     '__dir__',
     '__doc__',
     '__eq__',
     '__format__',
     '__ge__',
     '__getattribute__',
     '__getitem__',
     '__gt__',
     '__hash__',
     '__iadd__',
     '__imul__',
     '__init__',
     '__init_subclass__',
     '__iter__',
     '__le__',
     '__len__',
     '__lt__',
     '__mul__',
     '__ne__',
     '__new__',
     '__reduce__',
     '__reduce_ex__',
     '__repr__',
     '__reversed__',
     '__rmul__',
     '__setattr__',
     '__setitem__',
     '__sizeof__',
     '__str__',
     '__subclasshook__',
     'append',
     'clear',
     'copy',
     'count',
     'extend',
     'index',
     'insert',
     'pop',
     'remove',
     'reverse',
     'sort']



* LAB 9-2 : 용어 정리

1. 다음 용어를 정의하여라. 

a) 객체 지향 프로그래밍:모든 데이터를 오브젝트(object;물체)로 취급하여 프로그래밍 하는 방법으로, 처리 요구를 받은 객체가 자기 자신의 안에 있는 내용을 가지고 처리하는 방식   
b) 절차적 프로그래밍:‘순차적인 처리’가 중요시 되며 프로그램 전체가 유기적으로 연결되도록 만드는 프로그래밍 기법   
c) 그래픽 사용자 인터페이스: 사용자가 컴퓨터를 사용할 때 컴퓨터 사용에 관한 명령어를 알아야 할 필요 없이 마우스로 그래픽 아이콘(graphic icon)만 클릭하면 프로그램을 실행할 수 있도록 만든 시스템

2. 객체 지향 프로그래밍 기법과 절차적 프로그래밍 기법의 차이점을 기술하여라. 

절차지향은 데이터를 중심으로 함수를 구현합니다. 이에 반해 객체지향은 기능을 중심으로 메서드를 구현합니다. 

* LAB 9-3 : 용어 정리

1. 다음 용어를 정의하여라.

a) 클래스: 객체를 정의하고 만들기 위한 변수와 메소드의 집합   
b) 객체: 클래스에 의해 생성된 것   
c) 인스턴스: 클래스의 객체가 소프트웨어에 실체화된 것

* 9-4 : Dog 클래스와 인스턴스 생성

1. 다음 기능을 가진 Dog 클래스와 객체를 생성하라. 


```python
class Dog:
     def bark(self):
          print("멍! 멍!")

my_dog=Dog()
my_dog.bark()

```

    멍! 멍!
    

* LAB 9-5 : Dog 클래스와 인스턴스 생성

1. 다음 기능을 가진 Dog 클래스를 생성하고 인스턴스와 메소드를 호출하여라.


```python
class Dog:
     def __init__(self,name):
          self.name=name
          

     def bark(self):
          print("내 이름은 {} , 멍! 멍!".format(self.name))
          
my_dog=Dog('Jindo')
my_dog.bark()
```

    내 이름은 Jindo , 멍! 멍!
    

* LAB 9-6 : Dog 클래스와 문자열화 메소드

1. 다음 기능을 가진 Dog 클래스를 생성하고 인스턴스와 메소드를 호출하여라.


```python
class Dog:
     def __init__(self,name):
          self.name=name
          

     def __str__(self):
          return 'my_dog의 정보 : Dog(name ='+self.name+')'
          
my_dog=Dog('Jindo')
print(my_dog)
```

    my_dog의 정보 : Dog(name =Jindo)
    

* LAB 9-7 : 정수 객체의 is 연산

1. 다음 코드의 수행 결과는 무엇인가? 결과를 적고 그 이유를 설명하여라


```python
n=100
m=100
if n is m:
    print("n is m")
else:
    print("n is not m")
```

    n is m
    

* LAB 9-8 : 특수 메소드의 응용

1. 앞서 배운 __mul__()과 truediv__() 메소드를 이용하여 두 벡터의 곱셈과 나눗셈 기능을 구현하여라. v1이 (30, 40)이고 v2가 (10, 20)이라고 가정하고 다음과 같은 결과가 나타나도록 출력문을 작성하여라. 

> v1 * v2 = (300, 800)   
  v1 / v2 = (3.0, 2.0)


```python
class Vector2D:
     def __init__(self, x, y):
          self.x = x
          self.y = y
     def __mul__(self, other):
          return Vector2D(self.x * other.x, self.y * other.y)
     def __truediv__(self, other):
          return Vector2D(self.x / other.x, self.y / other.y)
     def __str__(self):
          return "({}, {})".format(self.x, self.y)
     
v1 = Vector2D(30, 40)
v2 = Vector2D(10, 20)
v3 = v1 * v2
print('v1 * v2 =', v3)
v4 = v1 / v2
print('v1 / v2 =', v4)
```

    v1 * v2 = (300, 800)
    v1 / v2 = (3.0, 2.0)
    

2. 앞서 배운 __neg__() 메소드를 이용하여 벡터의 음의 벡터를 구하시오. v1이 (10, 20)일 경우 출력 값은 다음과 같다. 

> -v1 = (-10, -20)


```python
class Vector2D:
     def __init__(self, x, y):
          self.x = x
          self.y = y
     def __neg__(self):
          return Vector2D(- self.x, -self.y)
     def __str__(self):
          return "({}, {})".format(self.x, self.y)
     
v1 = Vector2D(10, 20)
v2 = - v1 
print('-v1 =', v2)
```

    -v1 = (-10, -20)
    

* LAB 9-9 : 벡터의 크기 비교하기

1. 앞서 배운 비교 연산자에 해당하는 특수 메소드를 이용하여 두 벡터의 크기를 비교하는 프로그램을 작성하시오. v1이 (30, 40)이고 v2가 (10, 20)이라고 가정하면 다음과 같은 결과가 나타나도록 출력문을 작성하여라. 

> v1 > v2 = True   
  v1 >= v2 = True   
  v1 < v2 = False   
  v1 <= v2 = False


```python

```

* LAB 9-10 : __dict__를 이용한 인스턴스변수의 조회

1. 코드의 수행 결과는 무엇인가?


```python
class Rect:
     def __init__(self, width, height):
          self.width = width
          self.height = height

r1=Rect(100,200)
print(r1.__dict__)
print(r1.__dict__['width'])
```

    {'width': 100, 'height': 200}
    100
    

2. 코드의 수행 결과는 무엇인가?


```python
class Rect:
     def __init__(self, width, height):
          self.__width = width
          self.__height = height

r1=Rect(100,200)
print(r1.__dict__)
print(r1.__dict__['_Rect__width'])
```

    {'_Rect__width': 100, '_Rect__height': 200}
    100
    
