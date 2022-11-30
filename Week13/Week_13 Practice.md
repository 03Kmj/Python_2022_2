# Week_13 Practice

1. 다음과 같이 10개의 정수를 가진 n_list에서 12의 배수를 모두 찾아서 new_list라는 리스트에 저장하여라.   
>n_list = [44, 66, 34, 24, 144, 98, 38, 568, 234, 345]   
>new_list = [24, 144]


```python
n_list = [44, 66, 34, 24, 144, 98, 38, 568, 234, 345]   
new_list = list(filter(lambda x:x%12==0,n_list))
print("new_list =", new_list)
```

    new_list = [24, 144]
    

2. 다음과 같은 문장으로 된 lyrics라는 문자열이 있다. 이 문자열을 각 단어별로 구분한 후, 아래 실행 결과와 같이 이 단어와 이 단어에 대한 대문자 튜플 쌍으로 바꾸어 출력하여라.   
> lyrics = 'Half of my heart is in Havana'


```python
lyrics='Half of my heart is in Havana'
up_tuple=lyrics.split(' ')
result=[(x, x.upper()) for x in up_tuple]
print(result)
```

    [('Half', 'HALF'), ('of', 'OF'), ('my', 'MY'), ('heart', 'HEART'), ('is', 'IS'), ('in', 'IN'), ('Havana', 'HAVANA')]
    

3. 다음과 같이 6개의 숫자를 가진 n_list에서 양의 실수 값을 가지는 항목을 추출하여 정수로 변환하여 new_list에 담아서 출력하여라.


```python
n_list = [-22.3, 29.44, 902.2, 45.7, -887.1, -56.3]
new_list=[int(x) for x in n_list if x>0]
print("n_list =", n_list)
print("new_list =",new_list)
```

    n_list = [-22.3, 29.44, 902.2, 45.7, -887.1, -56.3]
    new_list = [29, 902, 45]
    

4. 1에서 100 사이의 정수 값들 중에서 6의 배수를 new_list에 담아서 다음과 같이 출력하여라. 


```python
new_list=[x for x in range(1,101) if x%6==0]
print("new_list =", new_list)
```

    new_list = [6, 12, 18, 24, 30, 36, 42, 48, 54, 60, 66, 72, 78, 84, 90, 96]
    

5. 1에서 100 사이의 정수 값들 중에서 6과 7의 배수를 new_list에 담아서 다음과 같이 출력하여라.


```python
new_list=[x for x in range(1,101) if x%6==0 and x%7==0]
print("new_list =", new_list)
```

    new_list = [42, 84]
    
