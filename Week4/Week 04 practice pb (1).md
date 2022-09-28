# Week 04 연습문제

## (1) 리스트

1. n_list라는 리스트에 [10, 20, 30, 50, 60]과 같은 5개의 원소가 있다. 내장 함수 sum(n_list)를 사용하지 않고 n_list의 5개 원소의 합을 구하는 프로그램을 작성하여라.


```python
n_list=[10, 20, 30, 50, 60]
sum=0
for i in range(len(n_list)):
     sum=sum+n_list[i]
print("리스트 원소들:", n_list)
print("리스트 원소들의 합:", sum)
```

    리스트 원소들: [10, 20, 30, 50, 60]
    리스트 원소들의 합: 170
    

2. 임의의 정수 값을 가진 리스트 n_list에서 가장 큰 값을 구하는 프로그램을 max() 함수를 사용하지 말고 구현하여라.


```python
n_list=[10, 20, 30, 50, 60]
b=n_list[0]
cnt=0

for i in range(len(n_list)):
     if b<n_list[i]:
          b=n_list[i]
          cnt+=1
          
print("리스트 원소들:", n_list)
print("리스트 원소들 중 최댓값:",b)
```

    리스트 원소들: [10, 20, 30, 50, 60]
    리스트 원소들 중 최댓값: 60
    

3. 사용자로부터 5개의 수를 입력받은 후 다음과 같이 입력된 값들의 합, 평균, 최댓값, 최솟값을 출력하는 프로그램을 작성하시오. 이때 반드시 입력된 값들은 리스트에 넣어서 sum(), min(), max() 함수를 사용하도록 하시오


```python
number=list(map(int,input("5개의 수를 입력하세요: ").split()))
print("합:", sum(number))
print("평균:", sum(number)/len(number))
print("최댓값:", max(number))
print("최솟값:", min(number))
```

![image.png](attachment:image.png)

4. 다음과 같은 list1, list2가 있을 경우 이중 for 루프를 사용하여 list1과 list2의 각 원소를 곱한 후 원소의 곱셈을 결과와 함께 출력하시오.



```python
list1=[3,5,7]
list2=[2,3,4,5,6]

for i in list1:
     for j in list2:
          print(i,"*",j,"=",i*j)
```

    3 * 2 = 6
    3 * 3 = 9
    3 * 4 = 12
    3 * 5 = 15
    3 * 6 = 18
    5 * 2 = 10
    5 * 3 = 15
    5 * 4 = 20
    5 * 5 = 25
    5 * 6 = 30
    7 * 2 = 14
    7 * 3 = 21
    7 * 4 = 28
    7 * 5 = 35
    7 * 6 = 42
    

5. a=[2,3,4,5,6]이 있을 경우, 이 리스트의 순서를 바꾸는 기능을 for-in 문과 pop() 메소드를 사용하여 구현하시오


```python
a=[2,3,4,5,6]
rev_a=[]
print("a =", a)
for i in range(len(a)):
     rev_a.append(a.pop())

print("rev_a=", rev_a)
     

```

    a = [2, 3, 4, 5, 6]
    rev_a= [6, 5, 4, 3, 2]
    

## (2) 딕셔너리, 튜플, 집합

1. 주어진 튜플은 10일 동안 일일 매장 매출을 기록한 것이다. 매출이 전날보다 감소한 날이 며칠인지 출력하는 코드를 작성하라


```python
sales=(100, 121, 120, 130, 140, 120, 122, 123, 190, 125)

cnt=0

for i in range(len(sales)-1):
     if sales[i]>sales[i+1]:
          cnt=cnt+1

print("일일 매출 기록:",sales)
print("지난 10일 동안 전일대비 매출이 감소한 날은",cnt,"일입니다.")
```

    일일 매출 기록: (100, 121, 120, 130, 140, 120, 122, 123, 190, 125)
    지난 10일 동안 전일대비 매출이 감소한 날은 3 일입니다.
    

2. 중복 요소를 가진 튜플 tup에서 중복 요소가 하나만 나타나도록 수정한 튜플을 생성하라.


```python
tup=(1,2,5,4,3,1,1,1,3,2,1,5,7,7)

print("주어진 튜플:",tup)
print("중복 제거 튜플:",tuple(set(tup)))
```

    주어진 튜플: (1, 2, 5, 4, 3, 1, 1, 1, 3, 2, 1, 5, 7, 7)
    중복 제거 튜플: (1, 2, 3, 4, 5, 7)
    

3.	어떤 문자열을 뒤집었을 때에 원래의 문자열과 같은 것을 회문(palindrome)이라고 한다. 예를 들어 ‘mom’은 문자열을 뒤집어도 ‘mom’이 되므로 회문이다. 사용자로부터 임의의 문자열이나 문장을 입력받아서 이 문자열이 회문인지 아닌지 검사하는 코드를 작성하라. 입력으로는 다음과 같은 영문자를 입력으로 받으며, 대문자와 소문자, 공백, 마침표 등은 무시하도록 구현하라.


```python
word = input('문자열을 입력하세요: ')
 
is_palindrome = True                 
for i in range(len(word) // 2):      
    if word[i] != word[-1 - i]:      
        is_palindrome = False        
        break

if is_palindrome==True:
     print("회문입니다.")
else:
     print("회문이 아닙니다")
```

    문자열을 입력하세요: racecar
    회문입니다.
    

4. 튜플 데이터를 이용하면 임시변수를 사용하지 않고 두 변수의 값을 서로 교환(swap)할 수 있다. 이 교환 방법을 이용하여 다음과 같이 주어진 리스트에서 가장 큰 값 12를 제일 마지막으로 옮겨 놓는 프로그램을 작성해 보라.(제약조건: 리스트의 요소를 살펴보기 위해 사용하는 for 문의 인덱스 변수 i를 제외하고는, 주어진 리스트 이외에 다른 어떤 변수도 추가로 사용해서는 안 된다.) 


```python
before = [5, 6, 3, 9, 2, 12, 3, 8, 7]
after = before
print(before)

max_index = 0
for i in range(1, len(before)):
    if before[i] > before[max_index]:
        max_index = i
while max_index != len(before) - 1:
    after[max_index], after[max_index + 1] = after[max_index + 1], after[max_index]
    max_index += 1
print(after)
```

    [5, 6, 3, 9, 2, 12, 3, 8, 7]
    [5, 6, 3, 9, 2, 3, 8, 7, 12]
    

5. 튜플을 요소로 가지는 student_tuple 튜플이 다음과 같이 있다. 이 튜플의 요소가 되는 튜플은 (학번, 이름, 전화번호)로 이루어져 있다. 이를 이용하여 (학번:이름)의 딕셔너리를 만들고 학번을 입력하면 학생의 이름이 나오도록 하라.


```python
student_tuple = (('191101', '홍길동'), ('191102', '임꺽정'), ('191103', '장길산'))

dictionary = dict(student_tuple)
print("학생 정보 :", dictionary)

stdin = int(input("학번을 입력하세요 :"))
while (stdin != -1):
    if str(stdin) in dictionary.keys():
        print(f"{stdin}번 학생은 {dictionary[str(stdin)]}입니다.")
    else:
        print("해당 학번의 학생이 없습니다.")
    stdin = int(input("학번을 입력하세요 :"))
print("프로그램을 종료합니다.")
```

    학생 정보 : {'191101': '홍길동', '191102': '임꺽정', '191103': '장길산'}
    학번을 입력하세요 :191101
    191101번 학생은 홍길동입니다.
    학번을 입력하세요 :191106
    해당 학번의 학생이 없습니다.
    학번을 입력하세요 :-1
    프로그램을 종료합니다.
    
