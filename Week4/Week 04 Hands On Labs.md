# Week 04 Hands On Labs

## Chapter 5. 리스트

**LAB 5-1: 리스트의 생성

1. 1부터 10까지의 숫자 중에서 짝수를 요소로 가지는 even_list라는 리스트를 생성하여라(10을 포함). print 함수를 사용하여 이 리스트를 다음과 같이 출력하여라. 


```python
even_list=[2,4,6,8,10]
print("even_list = ",even_list)
```

    even_list =  [2, 4, 6, 8, 10]
    

2. range() 함수를 이용하여 1번의 문제를 다시 풀어보시오.


```python
even_list=list(range(2,11,2))
print("even_list = ",even_list)
```

    even_list =  [2, 4, 6, 8, 10]
    

3. 'Korea', 'China', 'India', 'Nepal'의 네 원소를 가지는 nations라는 리스트를 생성하여라. print() 함수를 사용하여 이 리스트를 다음과 같이 출력하여라. 


```python
nations=['Korea', 'China', 'India', 'Nepal']
print("nations = ",nations)
```

    nations =  ['Korea', 'China', 'India', 'Nepal']
    

4. 여러분의 친한 친구 5명의 이름을 원소로 가지는 friends라는 리스트를 생성하여라. 그리고 다음과 같이 출력하여라.


```python
friends=['길동','철수','은지','지은','영민']
print("friends = ",friends)
```

    friends =  ['길동', '철수', '은지', '지은', '영민']
    

5. 'XYZ' 문자열을 이용하여 'X', 'Y', 'Z'라는 요소를 가지는 string이라는 이름의 리스트를 생성하고 다음과 같이 출력하여라.


```python
string=['X','Y','Z']
print("string = ",string)
```

    string =  ['X', 'Y', 'Z']
    

** LAB 5-2: 리스트의 생성과 인덱싱

1. 2부터 10까지의 수중에서 소수를 원소로 가지는 prime_list라는 리스트를 생성하여라. 그리고 이 리스트의 가장 첫 원소를 리스트 인덱싱을 
이용하여 다음과 같이 출력하여라.


```python
prime_list=[2,3,5,7]
print("prime_list의 첫 원소: ", prime_list[0])
```

    prime_list의 첫 원소:  2
    

2. 문제 1.의 prime_list의 가장 마지막 원소를 양수 인덱스를 사용하여 출력하여라.


```python
prime_list=[2,3,5,7]
print("prime_list의 마지막 원소:", prime_list[3])
```

    prime_list의 마지막 원소: 7
    

3. 문제 1.의 prime_list의 가장 마지막 원소를 음수 인덱스를 사용하여 출력하여라.


```python
prime_list=[2,3,5,7]
print("prime_list의 첫 원소:", prime_list[-1])
```

    prime_list의 첫 원소: 7
    

4. 'Korea', 'China', 'Russia', 'Malaysia'를 원소로 가지는 nations라는 리스트를 생성하여라. 그리고 이 리스트의 가장 첫 원소를 print() 함수를 이용하여 출력하여라. 


```python
nations=['Korea', 'China', 'Russia', 'Malaysia']
print("nations의 첫 원소 :", nations[0])
```

    nations의 첫 원소 : Korea
    

5. 4번에서 생성한 nations 리스트의 가장 마지막 원소를 음수 인덱스를 사용하여 출력하여라.


```python
nations=['Korea', 'China', 'Russia', 'Malaysia']
print("nations의 마지막 원소 :", nations[-1])
```

    nations의 마지막 원소 : Malaysia
    

6. 4번에서 생성한 nations 리스트의 가장 마지막 원소를 len(nations)-1 인덱스를 사용하여 출력하여라.


```python
nations=['Korea', 'China', 'Russia', 'Malaysia']
print("nations의 마지막 원소 :", nations[-1+len(nations)])
```

    nations의 마지막 원소 : Malaysia
    

**LAB 5-3: 리스트의 삽입과 삭제, in 연산자

1. 1부터 10까지의 수들 중에서 소수 원소를 가지는 prime_list라는 리스트를 생성하시오. 그리고 append() 메소드를 사용하여 11을 추가하시오. 이 때 추가 전과 추가 후의 결과를 다음과 같이 출력하시오. 


```python
prime_list=[2, 3, 5, 7]
print("소수 목록 :", prime_list)
prime_list.append(11)
print("추가 후 소수 목록 :", prime_list)
```

    소수 목록 : [2, 3, 5, 7]
    추가 후 소수 목록 : [2, 3, 5, 7, 11]
    

2. 1번 문제의 prime_list라는 리스트에 있는 3이라는 원소를 remove() 메소드를 사용하여 제거하시오. 이 때 삭제 전과 삭제 후의 결과를 다음과 같이 출력하시오. 


```python
prime_list=[2, 3, 5, 7, 11]
print("소수 목록 :", prime_list)
prime_list.remove(3)
print("삭제 후 소수 목록 :", prime_list)
```

    소수 목록 : [2, 3, 5, 7, 11]
    삭제 후 소수 목록 : [2, 5, 7, 11]
    

3. 'Korea', 'China', 'Russia', 'Malaysia'라는 국가이름을 원소로 가지는 nations라는 리스트에 append() 메소드를 사용항 'Nepal'을 추가하시오. 이 때 추가 전과 추가 후의 결과를 다음과 같이 출력하시오.


```python
nations=['Korea', 'China', 'Russia', 'Malaysia']
print("국가 목록 :", nations)
nations.append('Nepal')
print("추가 후 국가 목록 :", nations)
```

    국가 목록 : ['Korea', 'China', 'Russia', 'Malaysia']
    추가 후 국가 목록 : ['Korea', 'China', 'Russia', 'Malaysia', 'Nepal']
    

4. 3번 문제의 nations라는 리스트에 'Japan'과 'Russia'가 있는지 검사하여 출력하시오. 이때 in 연산자를 사용하여 리스트에 항목이 있는가 검사하고 출력시에는 if-else 조건문을 사용하시오.


```python
nations=['Korea', 'China', 'Russia', 'Malaysia']
if ('Japan' in nations):
     print("Japan 는(은) 국가 목록에 있습니다")
else:
     print("Japan 는(은) 국가 목록에 없습니다")
if ('Russia' in nations):
     print("Russia 는(은) 국가 목록에 있습니다")
else:
     print("Russia 는(은) 국가 목록에 없습니다")
```

**LAB 5-4: 리스트의 min()과 max(),sum(), len() 함수

1. 1부터 10까지의 수중에서 소수 원소를 가지는 prime_list라는 리스트를 생성하고 이들중 최솟값, 최댓값을 다음과 같이 출력하시오. min()과 max(), sum(), len() 내장함수를 사용하여 다음과 같이 출력하시오. 


```python
prime_list=[2, 3, 5, 7]
print("1에서 10까지의 소수 :", prime_list)
print("최솟값 :", min(prime_list))
print("최댓값 :", max(prime_list))
print("합계 :", sum(prime_list))
print("평균 :", sum(prime_list)/len(prime_list))
```

    1에서 10까지의 소수 : [2, 3, 5, 7]
    최솟값 : 2
    최댓값 : 7
    합계 : 17
    평균 : 4.25
    

2. 'Korea', 'China', 'Russia', 'Malaysia' 원소를 가지는 nations라는 리스트가 있다. 이들 나라 중에서 사전 순서로 가장 먼저 나오는 나라와 가장 뒤에 나오는 나라를 다음과 같이 출력하시오. 


```python
nations=['Korea', 'China', 'Russia', 'Malaysia']
print("국가 목록 :", nations)
print("사전에 가장 먼저 나오는 나라 :", min(nations))
print("사전에 가장 뒤에 나오는 나라 :", max(nations))
```

    국가 목록 : ['Korea', 'China', 'Russia', 'Malaysia']
    사전에 가장 먼저 나오는 나라 : China
    사전에 가장 뒤에 나오는 나라 : Russia
    

**LAB 5-5: 리스트 메소드의 응용

1. a 리스트의 원소 값이 [1, 2, 3]이고 b 리스트의 원소 값이 [10, 20, 30]이다. a 리스트에 append(b) 메소드와 extend(b) 메소드를 각각 호출할 때 어떤 결과가 나타날지 예측하시오. 그리고 실제로 수행한 후의 결과를 각각 적으시오. 

(1) 예측결과: [1, 2, 3, [10, 20, 30]]


```python
>>> a=[1,2,3]
>>> b=[10,20,30]
>>> a.append(b)
>>> a
```




    [1, 2, 3, [10, 20, 30]]



(2) 예측결과: [1, 2, 3, 10, 20, 30]


```python
>>> a=[1,2,3]
>>> b=[10,20,30]
>>> a.extend(b)
>>> a
```




    [1, 2, 3, 10, 20, 30]



2. 1부터 10까지의 정수 값을 원소로 가지는 nlist를 생성하여 다음과 같이 출력하여라. 


```python
nlist=[1,2,3,4,5,6,7,8,9,10]
print("nlist =", nlist)
```

    nlist = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
    

3. insert() 메소드를 사용하여 nlist의 제일 앞에 0을 삽입하여 다음과 같이 출력하여라.


```python
nlist.insert(0,0)
print("nlist =", nlist)
```

    nlist = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
    

4. 위의 3번 문제를 통해 만들어진 nlist를 역순으로 다시 배열하여 다음과 같이 출력하여라(reverse() 메소드를 사용할 것).


```python
nlist.reverse()
print("nlist =",nlist)
```

    nlist = [10, 9, 8, 7, 6, 5, 4, 3, 2, 1, 0]
    

5. nlist의 제일 마지막 원소를 pop() 메소드를 사용하여 반환하여 출력하고 삭제한 후의 nlist를 다음과 같이 출력하여라. 


```python
nlist=[10,9,8,7,6,5,4,3,2,1,0]
print("마지막 원소 =", nlist.pop())
print("nlist =", nlist)
```

    마지막 원소 = 0
    nlist = [10, 9, 8, 7, 6, 5, 4, 3, 2, 1]
    

**5-6: 리스트 연산

1. 사용자로부터 정수 n을 입력받아 [1,2,3]이라는 원소를 가지는 리스트를 다음과 같이 지정된 정수 n만큼 반복 출력하여라.


```python
n_list=[1,2,3]
n=int(input("반복할 정수를 입력하시오 :"))
print(n_list*n)
```

    반복할 정수를 입력하시오 :3
    [1, 2, 3, 1, 2, 3, 1, 2, 3]
    


```python
n_list=[1,2,3]
n=int(input("반복할 정수를 입력하시오 :"))
print(n_list*n)
```

    반복할 정수를 입력하시오 :4
    [1, 2, 3, 1, 2, 3, 1, 2, 3, 1, 2, 3]
    

**5-7: 리스트의 슬라이싱

1. range(15) 함수를 사용하여 다음과 같은 리스트를 생성하여라. 


```python
n_list=list(range(15))
print("n_list =", n_list)
```

    n_list = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14]
    

2. 문제 1번의 n_list로부터 슬라이싱을 수행하여 다음과 같은 리스트를 생성하여라

s_list1 = [0, 1, 2, 3, 4]  
s_list2 = [5, 6, 7, 8, 9, 10]  
s_list3 = [11, 12, 13, 14]  
s_list4 = [2, 4, 6, 8, 10]  
s_list5 = [10, 9, 8, 7, 6]  
s_list6 = [10, 8, 6, 4, 2]


```python
print("s_list1 =", n_list[0:5])
```

    s_list1 = [0, 1, 2, 3, 4]
    


```python
print("s_list2 =", n_list[6:11])
```

    s_list2 = [6, 7, 8, 9, 10]
    


```python
print("s_list3 =", n_list[11:15])
```

    s_list3 = [11, 12, 13, 14]
    


```python
print("s_list4 =", n_list[2:11:2])
```

    s_list4 = [2, 4, 6, 8, 10]
    


```python
n_list.reverse()
print("s_list5 =", n_list[4:9])
```

    s_list5 = [10, 9, 8, 7, 6]
    


```python
n_list.reverse()
print("s_list6 =", n_list[4:13:2])
```

    s_list6 = [10, 8, 6, 4, 2]
    

## Chapter 6. 딕셔너리, 튜플, 집합

**LAB 6-1: 딕셔너리의 생성

1. 다음과 같은 문자열 키-값의 항목을 가지는 capital_dic 딕셔너리를 생성하시오. 그리고 이 capital_dic을 이용하여 다음의 딕셔너리 항목에 대한 조회 결과를 적으시오.


```python
capital_dic={'Korea':'Seoul', 'China':'Beijing', 'USA':'Washington DC'}
```


```python
capital_dic['Korea']
```




    'Seoul'




```python
capital_dic['China']
```




    'Beijing'




```python
capital_dic['USA']
```




    'Washington DC'



2. 다음 키-값의 항목을 요소로 가지는 fruits_dic 딕셔너리를 생성하시오. 그리고 이 딕셔너리를 이용하여 각 과일의 가격을 다음과 같이 출력하여라.


```python
fruits_dic={'apple':5000, 'banana':4000, 'grape':5300, 'melon':6500}
print("apple의 가격은",fruits_dic['apple'],"원 입니다.")
print("banana의 가격은",fruits_dic['banana'],"원 입니다.")
print("grape의 가격은",fruits_dic['grape'],"원 입니다.")
print("melon의 가격은",fruits_dic['melon'],"원 입니다.")
```

    apple의 가격은 5000 원 입니다.
    banana의 가격은 4000 원 입니다.
    grape의 가격은 5300 원 입니다.
    melon의 가격은 6500 원 입니다.
    

**LAB 6-2: 딕셔너리의 항목 추가와 삭제

1. person 딕셔너리에 다음과 같이 '특기' 키와, '분신술' 값을 가지는 새로운 항목을 추가하시오. 


```python
person={'이름':'홍길동', '나이':26, '몸무게':82}
person['특기']='분신술'
person
```




    {'이름': '홍길동', '나이': 26, '몸무게': 82, '특기': '분신술'}




```python
person['아버지']='홍판서'
person
```




    {'이름': '홍길동', '나이': 26, '몸무게': 82, '특기': '분신술', '아버지': '홍판서'}




```python
del person['나이']
person
```




    {'이름': '홍길동', '몸무게': 82, '특기': '분신술', '아버지': '홍판서'}



**LAB 6-3: 딕셔너리와 연산


```python
capital_dic={'Korea':'Seoul', 'China':'Beijing', 'USA':'Washington DC'}
```


```python
'Korea' in capital_dic
```




    True




```python
'China' in capital_dic
```




    True




```python
'Indonesia' in capital_dic
```




    False




```python
'Beijing' in capital_dic
```




    False



**LAB 6-4: 딕셔너리의 활용

1. apple, melon, banana, orange라는 문자열로 된 키와 각각 6000, 3000, 5000, 7000원의 가격을 값으로 가지는 fruits_dic이라는 이름의 딕셔너리를 생성하자. 


```python
fruits_dic={'apple':6000, 'melon':3000,'banana':5000, 'orange':7000}
```

2. fruits_dic 딕셔너리의 모든 키를 keys() 메소드를 사용하여 출력하시오.


```python
fruits_dic.keys()
```




    dict_keys(['apple', 'melon', 'banana', 'orange'])



3. fruits_dic 딕셔너리의 모든 값을 values() 메소드를 사용하여 출력하시오.


```python
fruits_dic.values()
```




    dict_values([6000, 3000, 5000, 7000])



4. fruits_dic 딕셔너리의 ('apple', 6000) 항목을 pop() 메소드를 이용하여 삭제하시오.


```python
fruits_dic.pop('apple')
fruits_dic
```




    {'melon': 3000, 'banana': 5000, 'orange': 7000}



5. fruits_dic 딕셔너리의 모든 항목을 삭제하시오.


```python
fruits_dic.clear()
fruits_dic
```




    {}



**LAB 6-5: 딕셔너리의 활용

1. ('apple', 6000), ('melon', 3000), ('banana', 5000), ('orange', 4000)라는 키와 값의 쌍으로 이루어진 fruits_dic이라는 이름의 딕셔너리를 생성하자. 이제 fruits_dic 딕셔너리의 모든 키를 리스트 형식으로 출력하시오.


```python
fruits_dic={'apple':6000, 'melon':3000, 'banana':5000,'orange':4000}
list(fruits_dic)
```




    ['apple', 'melon', 'banana', 'orange']



2. fruits_dic 딕셔너리의 모든 값을 리스트 형식으로 출력하시오


```python
list(fruits_dic.values())
```




    [6000, 3000, 5000, 4000]



3. fruits_dic 딕셔너리의 항목의 개수를 len() 함수를 통해서 구한 후, 다음과 같이 출력하시오.


```python
print("fruits_dic 딕셔너리의 항목의 개수 :",len(fruits_dic))
```

    fruits_dic 딕셔너리의 항목의 개수 : 4
    

4. fruits_dic 딕셔너리에 'apple' 키와 'mango' 키가 있는가 검사하여 다음과 같이 출력하시오.


```python
if 'apple' in fruits_dic:
    print("apple is in fruits_dic.")
else:
    print("apple is not in fruits_dic.")
if 'mango' in fruits_dic:
    print("mango is in fruits_dic.")
else:
    print("mango is not in fruits_dic.")
```

    apple is in fruits_dic.
    mango is not in fruits_dic.
    

**LAB 6-6: 튜플의 생성과 패킹, 언패킹

1. (1919, 3, 1)의 요소 값을 가지는 the_day 튜플을 생성하여라. 그리고 이 튜플의 요소를 언패킹을 통해 year, month, day 변수에 할당한 후 다음과 같이 출력하여라. 


```python
the_day=(1919, 3, 1)
year,month,day=the_day
print(year,"년",month,"월",day,"일은 삼일절입니다.")
```

    1919 년 3 월 1 일은 삼일절입니다.
    

2. 10, 20, 30의 순서대로 이루어진 리스트를 튜플로 변환하여 a,b,c에 언패킹한 후 이를 다음과 같이 출력하여라.


```python
list_=[10, 20, 30]
tuple1=tuple(list_)
a,b,c=tuple1
print("a =", a)
print("b =", b)
print("c =", c)
```

    a = 10
    b = 20
    c = 30
    

**LAB 6-7: 튜플의 활용

1. 2019001이라는 학번과 '홍길동'이라는 이름, 179라는 키를 튜플의 요소로 가지는 튜플 객체와 참조 변수 person을 생성하여라.


```python
person=('홍길동', 2019001, 179)
print("person =", person)
```

    person = ('홍길동', 2019001, 179)
    

2. person의 학번을 2019003으로 변경하여라. 어떤 오류가 발생하는가?
>TypeError발생

3. person을 리스트로 변환하여 학번을 2020003으로 변경한 후 이를 다시 튜플로 변환하여 다음과 같이 출력하여라.


```python
person=('홍길동', 2019001, 179)
per=list(person)
per[1]=2020003
person=tuple(per)
print("학번 변동 후 person =",person)
```

    학번 변동 후 person = ('홍길동', 2020003, 179)
    

**LAB 6-9: 집합의 생성

1. 다음 리스트 lst로부터 set() 함수를 사용하여 집합 s1을 생성하여 출력하시오.


```python
lst=['apple','mango','banana']
s1=set(lst)
print("s1 =",s1)
```

    s1 = {'apple', 'banana', 'mango'}
    

2. 다음 문자열 greet으로부터 set() 함수를 사용하여 집합 s2를 생성하여 출력하시오.


```python
greet = 'Good afternoon'
s2=set(greet)
print("s2 =", s2)
```

    s2 = {'t', 'e', 'n', 'r', 'o', 'd', 'G', 'a', 'f', ' '}
    

**LAB 6-10: 집합의 연산

1. 다음 두 집합이 있을 경우 이 집합에 대한 연산결과는 무엇인가?


```python
s1 = {10, 20, 30, 40}
s2 = {30, 40, 50, 60, 70}
```


```python
s1|s2
```




    {10, 20, 30, 40, 50, 60, 70}




```python
s1&s2
```




    {30, 40}




```python
s1-s2
```




    {10, 20}




```python
s1^s2
```




    {10, 20, 50, 60, 70}




```python
s1.issubset(s2)
```




    False




```python
s1.issuperset(s2)
```




    False




```python
s1.isdisjoint(s2)
```




    False


