# Week_06_JumpToPython

1. 주어진 자연수가 홀수인지 짝수인지 판별해 주는 함수(is_odd)를 작성해 보자.


```python
def is_odd(n):
    if n%2==0:
        print("{} is even".format(n))
    else:
        print("{} is odd".format(n))      
        
is_odd(2)
```

    2 is even
    

2. 입력으로 들어오는 모든 수의 평균값을 계산해주는 함수를 작성해 보자. 


```python
def avg(*nums):
    myList=[]
    for n in nums:
        myList.append(n)
    return sum(myList)/len(myList)
```

3. 다음은 두 개의 숫자를 입력받아 더하여 돌려주는 프로그램이다. 


```python
input1 = input("첫번째 숫자를 입력하세요:")
input2 = input("두번째 숫자를 입력하세요:")

total = input1 + input2
print("두 수의 합은 %s 입니다" % total)
```

이 프로그램을 수행해보자. 


```python
input1 = input("첫번째 숫자를 입력하세요:")
input2 = input("두번째 숫자를 입력하세요:")

total = input1 + input2
print("두 수의 합은 %s 입니다" % total)
```

    첫번째 숫자를 입력하세요:3
    두번째 숫자를 입력하세요:6
    두 수의 합은 36 입니다
    

3과 6을 입력했을 때 9가 아닌 36이라는 결괏값을 돌려주었다. 이 프로그램의 오류를 수정해 보자.


```python
input1 = int(input("첫번째 숫자를 입력하세요:"))
input2 = int(input("두번째 숫자를 입력하세요:"))

total = input1 + input2
print("두 수의 합은 %s 입니다" % total)
```

    첫번째 숫자를 입력하세요:3
    두번째 숫자를 입력하세요:6
    두 수의 합은 9 입니다
    

4. 다음 중 출력 결과가 다른 것 한 개를 골라보자.
>1. print("you" "need" "python")   
 2. print("you"+"need"+"python")   
 3. print("you", "need", "python")   
 4. print("".join(["you", "need", "python"]))

정답: C


```python
print("you" "need" "python")   
print("you"+"need"+"python")   
print("you", "need", "python")   
print("".join(["you", "need", "python"]))
```

    youneedpython
    youneedpython
    you need python
    youneedpython
    


```python

```
