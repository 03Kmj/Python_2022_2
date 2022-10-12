# Week_06_Hands On Lab (2022116624 강민정)

## 4장 함수와 입출력

* LAB 4-1: 함수 정의와 호출

1. 코드 [4-1]의 함수 호출문을 삭제하면 어떻게 되는가?
->출력문이 출력되지 않음.


```python
def print_star():
    print("************************")
```

2. [코드 4-2]를 수정하여 6줄의 별표를 출력해 보시오. 이때 함수 호출을 6회 하시오.


```python
def print_star():
    print("************************")
    
print_star()
print_star()
print_star()
print_star()
print_star()
print_star()
```

    ************************
    ************************
    ************************
    ************************
    ************************
    ************************
    

* LAB 4-2: 함수 정의와 호출

1. 코드 [4-3]을 수정하여 함수 호출 두 번으로 10줄의 별표를 출력해 보시오. 


```python
def print_star5():
    print("*************************")
    print("*************************")
    print("*************************")
    print("*************************")
    print("*************************")

print_star5()
print_star5()
```

    *************************
    *************************
    *************************
    *************************
    *************************
    *************************
    *************************
    *************************
    *************************
    *************************
    

* LAB 4-3: 함수 정의와 호출

1. 코드 [4-4]를 수정하여 해시마크(#)를 한 줄 출력하는 print_hash() 함수를 추가로 구현하시오. 


```python
def print_star():
    print("**************")
def print_plus():
    print("++++++++++++++")
def print_hash():
    print("##############")
    
print_star()
print_plus()
print_hash()
```

    **************
    ++++++++++++++
    ##############
    

2. print_star(), print_plus, print_hash() 함수를 모두 이용하여 다음과 같은 출력이 나타나도록 함수를 호출하시오.ㅇㅇ


```python
def print_star():
    print("**************")
def print_plus():
    print("++++++++++++++")
def print_hash():
    print("##############")
    
print_hash()
print_star()
print_plus()
print_plus()
print_star()
print_hash()
```

    ##############
    **************
    ++++++++++++++
    ++++++++++++++
    **************
    ##############
    

* LAB 4-4: 다양한 별표와 패턴 출력

1. [코드 4-5]를 수정하여 별표(*)줄이 10개 출력되도록 인자를 변경하시오.


```python
def print_star(n):
    for _ in range(n):
        print("************************")
        
print_star(10)
```

    ************************
    ************************
    ************************
    ************************
    ************************
    ************************
    ************************
    ************************
    ************************
    ************************
    

2. [코드 4-5]를 수정하여 별표(*) 표시 대신 해시마크(#)가 출력되도록 하시오. 이를 위해 함수 이름을 print_hash(n)으로 수정하고 수정된 함수를 print_hash(!0)과 같이 호출하시오. 


```python
def print_hash(n):
    for _ in range(n):
        print("########################")
        
print_hash(10)
```

    ########################
    ########################
    ########################
    ########################
    ########################
    ########################
    ########################
    ########################
    ########################
    ########################
    

3. print_hash(6)을 호출하여 다음과 같은 출력이 나타나도록 하여라. 다음 화면과 같이 매번 해시가 출력될 때마다 앞 칸에 줄 번호를 0부터 표시하도록 하여라. 


```python
def print_hash(n):
    for _ in range(n):
        print(_, "########################")
print_hash(6)
```

    0 ########################
    1 ########################
    2 ########################
    3 ########################
    4 ########################
    5 ########################
    

* LAB 4-5: 두 수 연산을 수행하는 함수

1. 두 개의 매개변수 a, b를 받아서 두 수의 차를 구하여 출력하는 print_sub(a, b) 함수를 구현하여라. print_sum(10, 20)을 호출한 결과 다음과 같은 출력이 나타나도록 하여라. 

> 10과 20의 차는 -10입니다. 


```python
def print_sub(a,b):
    print(a,"과",b,"의 차는",a-b,"입니다.")
    

print_sub(10,20)
```

    10 과 20 의 차는 -10 입니다.
    

2. 두 개의 매개변수 a,b를 받아서 두 수의 곱을 구하여 print_mult(a,b) 함수를 구현하여라. print_mult(10, 20)을 호출한 결과 다음과 같은 출력이 나타나도록 하여라. 

> 10과 20의 곱은 200입니다. 


```python
def print_sub(a,b):
    print(a,"과",b,"의 곱은",a*b,"입니다.")
    

print_sub(10,20)
```

    10 과 20 의 곱은 200 입니다.
    

* 4-6: 함수의 사용

1. 다음 2차 방정식의 근을 [코드 4-10]의 함수를 사용하여 출력하여라.

> (1) x^2 +4x - 21 = 0   
> (2) x^2 -6x + 8 = 0


```python
def print_root(a, b, c):
    r1 = (-b + (b ** 2 - 4 * a * c) ** 0.5) / (2 * a)
    r2 = (-b - (b ** 2 - 4 * a * c) ** 0.5) / (2 * a)
    print('해는', r1, '또는', r2)

print_root(1, 4, -21)
print_root(2, -6, +8)
```

    해는 3.0 또는 -7.0
    해는 (1.5+1.3228756555322954j) 또는 (1.5-1.3228756555322954j)
    

2. 삼각형의 면적을 구하기 위하여 밑변과 높이를 사용하려고 한다. 두 개의 매개변수 width, height를 받아서 삼각형의 면적을 출력하는 함수 print_area(width, height)를 구현하여라. 이때 print_area(10, 20)을 호출하여 다음과 같은 출력이 나타나도록 하여라. 


```python
area=0
def print_area(width, height):
    area=width*height
    print("밑변 {}, 높이 {}인 삼각형의 면적은 : {}". format(width, height, area))

print_area(10,20)
```

    밑변 10, 높이 20인 삼각형의 면적은 : 200
    

* LAB 4-7: 원의 면적과 둘레를 반환하는 함수

1. 원의 면적과 둘레를 구하기 위하여 원의 반지름을 사용하려고 한다. 이 때 사용할 circle_area_circum(radius) 함수는 다음과 같이 반지름(radius) 10을 입력으로 받아서 면적(area)과 둘레(circum)의 두 값을 반환하도록 구현하여라. 


```python
pi=3.14
def circle_area_circum(radius):
    area=pi*radius**2
    circum=2*pi*radius
    return area, circum

radius=10
area, circum=circle_area_circum(radius)
print("반지름 {}인 원의 면적은 {}, 원의 둘레는 {:.1f}".format(radius, area, circum))
```

    반지름 10인 원의 면적은 314.0, 원의 둘레는 62.8
    

* LAB 4-8: 다수의 결과를 반환하는 함수 만들기

1. 어떤 정수 n과 m을 입력하면, n의 배수 m개를 반환하는 multiples(n,m) 함수를 구현하고 다음과 같이 호출하여 결과를 출력하여라. 


```python
def multiples(n,m):
    myList = []
    for i in range(1,m+1):
        myList.append(i*n)
    return tuple(myList)

r1,r2,r3,r4=multiples(3,4)
print(r1,r2,r3,r4)
r1,r2,r3,r4,r5=multiples(2,5)
print(r1,r2,r3,r4,r5)
```

    3 6 9 12
    2 4 6 8 10
    

* 4-9: 키워드 인자

1. 다음과 같이 성(last name)과 이름(first name), 존칭(honorifics)을 매개변수로 받아서 출력하는 함수 print_name이 있다. 


```python
def print_name(honorifics, first_name, last_name):
    ''' 키워드 인자를 이용한 출력용 프로그램 '''
    print(honorifics, first_name, last_name)
```

a) 다음과 같은 함수 호출의 결과는 무엇인가?   


```python
print_name(first_name="Gildong", last_name="Hong", honorifics="Dr.")
```

    Dr. Gildong Hong
    

b) 다음과 같은 함수 호출의 결과는 무엇인가?


```python
print_name("Gildong", "Hong","Dr.")
```

    Gildong Hong Dr.
    

* 4-10: 가변 인자의 활용

1. 가변 인자를 사용하는 sum_nums() 함수를 수정하여 인자들을 튜플 형식으로 출력한 후 모든 값들의 합과 평균을 다음과 같이 출력하시오.   

>3 개의 인자 (10,20,30)  
합계: 60, 평균: 20.0   


```python
def sum_nums(*num):
    total=0
    avg=0
    for n in num:
        total+=n
        avg=total/len(num)
    print("합계: {}, 평균: {:.1f}".format(total,avg))
sum_nums(10,20,30)
```

    합계: 60, 평균: 20.0
    

>5 개의 인자 (10,20,30,40,50)   
합계: 150, 평균: 30.0


```python
def sum_nums(*num):
    total=0
    avg=0
    for n in num:
        total+=n
        avg=total/len(num)
    print("합계: {}, 평균: {:.1f}".format(total,avg))
sum_nums(10,20,30,40,50)
```

    합계: 150, 평균: 30.0
    

2. 가변 인자를 사용하는 함수 min_nums() 함수를 구현하시오. 이 함수는 정수를 인자로 받을 수 있는데 이 인자의 개수가 가변적이다. 이 함수의 호출문이 다음과 같을 경우

>min_nums(20,40,50,20)

다음과 같은 출력이 나타나도록 하시오. 

>최솟값은 10


```python
def min_nums(*num):
    myList= []
    for n in num:
        myList.append(n)
    return min(myList)

print("최솟값은", min_nums(20,40,50,10))   
```

    최솟값은 10
    

* LAB 4-11: format() 메소드의 활용

1. 위의 코드를 수정하여 이름, 나이, 직업, 사는 곳까지 다음과 같이 화면에 출력하려고 한다. 

>당신의 이름을 입력해주세요: 김철수      
 나이를 입력해주세요: 21   
 직업을 입력해주세요: 학생   
 사는 곳을 입력해주세요: 창원시   
 당신의 이름은 김철수, 나이는 21살, 직업은 학생, 사는 곳은 창원시입니다. 

a) 출력문에서 format() 메소드를 사용하여 출력하여라. 


```python
name=input("당신의 이름을 입력해주세요: ")
age=input("나이를 입력해주세요: ")
job=input("직업을 입력해주세요: ")
area=input("사는 곳을 입력해 주세요:")
print("당신의 이름은 {}, 나이는 {}살, 직업은 {}, 사는 곳은 {}입니다.".format(name, age, job, area))
```

    당신의 이름을 입력해주세요: 김철수
    나이를 입력해주세요: 21
    직업을 입력해주세요: 학생
    사는 곳을 입력해 주세요:창원시
    당신의 이름은 김철수, 나이는 21살, 직업은 학생, 사는 곳은 창원시입니다.
    

b) 출력문에서 format() 메소드를 사용하지 말고 쉼표로 구분하여 출력하여라. 


```python
name=input("당신의 이름을 입력해주세요: ")
age=input("나이를 입력해주세요: ")
job=input("직업을 입력해주세요: ")
area=input("사는 곳을 입력해 주세요:")
print("당신의 이름은 ",name, ", 나이는 ",age,"살, 직업은 ",job, ", 사는 곳은 ",area,"입니다.", sep="")
```

    당신의 이름을 입력해주세요: 김철수
    나이를 입력해주세요: 21
    직업을 입력해주세요: 학생
    사는 곳을 입력해 주세요:창원시
    당신의 이름은 김철수, 나이는 21살, 직업은 학생, 사는 곳은 창원시입니다.
    

* LAB 4-12: 문자열의 여러 메소드 활용

1. join() 메소드를 사용하여 'ABCD'의 문자열을 'A_B_C_D'와 같이 출력하여라.


```python
'_'.join('ABCD')
```




    'A_B_C_D'



2. 'My favorite thing is monsters.'라는 문자열 s에 replace() 메소드를 적용하여 'My favorite thing is cartoons.'로 수정된 t 문자열을 얻도록 하여라. 


```python
s='My favorite thing is monsters.'
t=s.replace('monsters','cartoons')
print(t)
```

    My favorite thing is cartoons.
    
