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
         self._number=number
         if self._number>=100 or self._number<=-1:
              self._number=0
        

    def inc(self): 
        self._number+=1
        if self._number>=100:
             self._number=0

    def __str__(self):
         return f"C({self._number})"
          

    
c1 = Counter(10) 
c1.inc() 

print("c1 = ", c1)

print()
```

    c1 =  C(11)
    
    

3. 다음과 같은 기능을 가지는 은행계좌의 클래스 BankAccount 클래스를 구현한 뒤, 인스턴스를 생성하여 실행해 보아라.


```python
class BankAccount:
    def __init__(self, name, accountnum):
        self._name = name
        self._accountnum = accountnum
        self._balance = 0

    def __str__(self):
        return f"{self._name}님의 계좌 {self._accountnum}의 잔고는 {self._balance}원입니다."
    
    def get_name(self):
        return self._name

    def get_account_num(self):
        return self._accountnum

    def get_balance(self):
        return self._balance

    def deposit(self, money):
        self._balance += money
        print(f"{money}원이 입금되었습니다. 잔고는 {self._balance}원입니다.")

    def withdraw(self, money):
        if money > self._balance:
            print(f"계좌 잔고는 {self._balance}원으로 인출 요구 금액 {money}원 보다 작습니다.")
        else:
            self._balance -= money


account1 = BankAccount('홍길동', '1234-0001')
print(account1)
account1.deposit(2000)
print(account1)
account1.withdraw(500)
print(account1)
account1.withdraw(5000)

```

    홍길동님의 계좌 1234-0001의 잔고는 0원입니다.
    2000원이 입금되었습니다. 잔고는 2000원입니다.
    홍길동님의 계좌 1234-0001의 잔고는 2000원입니다.
    홍길동님의 계좌 1234-0001의 잔고는 1500원입니다.
    계좌 잔고는 1500원으로 인출 요구 금액 5000원 보다 작습니다.
    

4. 다음과 같은 기능을 가지는 Student라는 학생 클래스를 구현하여라. 그리고 인스턴스를 생성하여 실행해보아라.


```python
class Student:
    def __init__(self, name, student_id):
        self._name = name
        self._student_id = student_id
        self._korean_quiz = 0
        self._math_quiz = 0
        self._science_quiz = 0
        self._total_quiz = 0

    def __str__(self):
        return f"이름: {self._name}, 학번: {self._student_id}\n" \
               f"국어성적: {self._korean_quiz}, 수학성적: {self._math_quiz}, 과학성적: {self._science_quiz}\n" \
               f"합계: {self._total_quiz}, 평균: {self._total_quiz / 3}"

    def get_name(self):
        return self._name

    def get_student_id(self):
        return self._student_id

    def get_korean_quiz(self):
        return self._korean_quiz

    def get_math_quiz(self):
        return self._math_quiz

    def get_science_quiz(self):
        return self._science_quiz

    def set_korean_quiz(self, score):
        self._korean_quiz += score
        self._total_quiz += self._korean_quiz

    def set_math_quiz(self, score):
        self._math_quiz += score
        self._total_quiz += self._math_quiz

    def set_science_quiz(self, score):
        self._science_quiz += score
        self._total_quiz += self._science_quiz

    def get_total_score(self):
        return self._total_quiz

    def get_avg_score(self):
        return self._total_quiz / 3


name = input('학생의 이름을 입력하세요 : ')
student_id = input('학생의 학번을 입력하세요 : ')

student = Student(name, student_id)

korean_quiz = int(input('학생의 국어 성적을 입력하세요 : '))
math_quiz = int(input('학생의 수학 성적을 입력하세요 : '))
science_quiz = int(input('학생의 과학 성적을 입력하세요 : '))
student.set_korean_quiz(korean_quiz)
student.set_math_quiz(math_quiz)
student.set_science_quiz(science_quiz)
print(student)

```

    학생의 이름을 입력하세요 : 강민정
    학생의 학번을 입력하세요 : 20220302
    학생의 국어 성적을 입력하세요 : 85
    학생의 수학 성적을 입력하세요 : 90
    학생의 과학 성적을 입력하세요 : 95
    이름: 강민정, 학번: 20220302
    국어성적: 85, 수학성적: 90, 과학성적: 95
    합계: 270, 평균: 90.0
    

6. 다음과 같은 기능을 가지는 Rectangel 클래스를 구현하여라. 그리고 이 클래스를 이용하여 인스턴스를 생성하여라. 이 클래스는 다음과 같은 속성과 동작을 가진다. 


```python
class Rectangle():
    def __init__(self, x, y, width, height):
        self.x = x
        self.y = y
        self.width = width
        self.height = height

    def __str__(self):
        return f"(x = {self.x}, y = {self.y}, h = {self.height}), 면적: {self.width * self.height}"

    def set_x(self, x):
        self.x = x

    def set_y(self, y):
        self.y = y

    def set_width(self, width):
        self.width = width

    def set_height(self, height):
        self.height = height

    def get_x(self):
        return self.x

    def get_y(self):
        return self.y

    def get_width(self):
        return self.width

    def get_height(self):
        return  self.height

    def area(self):
        return self.width * self.height

r1 = Rectangle(0, 0, 100, 100)
r2 = Rectangle(0, -10, 10, 10)
r3 = Rectangle(-100, 0, 120, 100)

print('r1 = ', r1)
print('r2 = ', r2)
print('r3 = ', r3)

```

    r1 =  (x = 0, y = 0, h = 100), 면적: 10000
    r2 =  (x = 0, y = -10, h = 10), 면적: 100
    r3 =  (x = -100, y = 0, h = 100), 면적: 12000
    
