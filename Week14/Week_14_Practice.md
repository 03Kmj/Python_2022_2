# Week 14 Practice

1.  1에서 16까지의 정수값을 가지는 4x4 크기의 배열을 만들어서 다음과 같이 출력하시오. 이 때 arange()와 reshape()을 이용하여 배열을 생성하시오.


```python
import numpy as np
print(np.arange(1, 17).reshape(4,4))
```

    [[ 1  2  3  4]
     [ 5  6  7  8]
     [ 9 10 11 12]
     [13 14 15 16]]
    

2. random.random() 함수를 사용하여 10개의 난수값을 생성하여 다음과 같이 출력하시오. 그리고 이 수들 중에서 최댓값, 최솟값, 평균값을 각각 출력하시오.


```python
a = np.random.random(10)
print('a = ', a)
print('최댓값 :', a.max())
print('최솟값 :', a.min())
print('평균값 :', a.mean())
```

    a =  [0.28048981 0.9537085  0.3357324  0.29509148 0.85446814 0.79427005
     0.32002505 0.73614211 0.92124463 0.88962859]
    최댓값 : 0.9537084950774459
    최솟값 : 0.2804898144057193
    평균값 : 0.6380800761250003
    

3. 사용자로부터 2이상의 수 n을 입력으로 받아서, 입력된 수를 바탕으로 다음과 같은 대각선 성분의 값이 1에서 n까지 증가하는 다차원 배열 a를 생성하는 프로그램을 작성하시오. 이때 대각선 성분 이외의 값은 모두 0으로 하시오.


```python
import numpy as np

n = int(input('n을 입력하시오 : '))
a = np.diag(1+np.arange(n),k=0)
print(a)
```

    n을 입력하시오 : 5
    [[1 0 0 0 0]
     [0 2 0 0 0]
     [0 0 3 0 0]
     [0 0 0 4 0]
     [0 0 0 0 5]]
    

4. 다음과 같은 두 배열 a와 b가 있을 경우 a 배열의 원소내에 b 배열의 원소가 있는지 없는지를 판단하여 출력하는 프로그램을 작성하시오. 이 때 a 배열내의 원소가 b에 있을 경우는 True, 없을 경우는 False를 출력하여라.


```python
a = np.array([0, 10, 20, 40, 60, 80])
print('a 배열 :', a)
b = np.arange(0, 30, 20)
print('b 배열 :', b)

t = np.full(a.shape, False)
ind = 0
for x in a:
  if x in b:
    t[ind] = True
  ind += 1
  
print(t)
```

    a 배열 : [ 0 10 20 40 60 80]
    b 배열 : [ 0 20]
    [ True False  True False False False]
    

5. 다음과 같이 사용자로부터 정수 n을 입력으로 받아서 (n, n) shape의 정방행렬을 만드시오.   
1) 이 행렬의 대각선 성분과 그 아래값들이 다음과 같이 모두 1이 되도록 만드시오.   
2) 이 때 모든 행렬의 원소의 합을 구하시오.


```python
import numpy as np

n = int(input('n을 입력하시오 : '))
a = np.full((n, n), 0)

for i in range(n):
  for j in range(n):
    if i >= j:
      a[i, j] = 1
      
print(a)
```

    n을 입력하시오 : 6
    [[1 0 0 0 0 0]
     [1 1 0 0 0 0]
     [1 1 1 0 0 0]
     [1 1 1 1 0 0]
     [1 1 1 1 1 0]
     [1 1 1 1 1 1]]
    


```python
print('행렬의 모든 원소의 합:', a.sum())
```

    행렬의 모든 원소의 합: 21
    
