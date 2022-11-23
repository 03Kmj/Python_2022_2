# Week_12 Practice

1. 다음과 같은 기능을 가지는 클래스를 정의하고, 인스턴스를 생성하여라.   


```python
class Dog:
     def __init__(self,name,age):
          self.name=name
          self.age=age
          

     def __str__(self):
          print("이름은 {} , 나이는 {}살 입니다.".format(self.name,self.age))
          
my_dog=Dog('Mango', 3)
my_dog.__str__()
```

    이름은 Mango , 나이는 3살 입니다.
    

2. 다음과 같은 기능을 가지는 Couter 클래스를 정의하고 c1, c2라는 이름의 인스턴스를 생성하여라.


```python
class Counter:
    def __init__(self,number):
        
        
```
