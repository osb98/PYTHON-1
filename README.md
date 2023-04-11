# PYTHON

## 자료형
#### 숫자형
* 정수 : 123, -20. 0   
* 실수 : 123.45, -4321.5, 6.08e9  
* 8진수 : 0o456, 0o123  
* 16진수 : 0xFF, 0x00, 0x0A  

~~~
a = 10
b = 20
c = a + b
d = b - a
print(c, d)
~~~

~~~
a = 10
b = 3
# 나눗셈
c = a/b # 나눗셈
d = a//b # 몫
e = a%b # 나머지
# 곱셈
f = a*b # 곱셈
g = a**b # 제곱
print(c,d,e,f,g)
~~~

#### 문자열
1. 큰 따옴표 : "Hello World!
It's"  
2. 작은 따옴표 : '대한민국'  
3. 큰따옴표 3 : """Hello!"""  
4. 작은 따옴표 3 : 
'''Life is too short, You need  
python''' 

#### 변수
* 문자 또는 밑줄로 시작(beta, _kim)
* 대소문자를 구분한다.(sum, Sum, SUM)
* 영문자, 숫자, 밑줄(A-z,0-9,_)
* 파이썬 키워드는 사용 불가

~~~
myName = "Jiho Ahn" # 낙타 표기법(camel)
my_name = "안지호" # 뱀 표기법(snake)
MyName = "joe" # 파스칼 표기법
_my_name = "korea" 
MYNAME = "God is love"  
my2name = "12345"
# 2myname = '9876'
# my-name = "hoitkuma"
# my name = "joe"
myStr = '123' # str
myNum = 123 # int

print(myStr, myNum)
print(type(myStr))
print(type(myNum))
~~~

#### 여러개 변수 할당

~~~
x,y,z = "포도","딸기","수박"
print(x)
print(y)
print(z)
~~~

~~~
a = b = c = "오렌지"
print(a)
print(b)
print(c)
~~~

~~~
fruits = "포도", "딸기", "수박"
z,y,z = fruits
print(x)
print(y)
print(z)
~~~

~~~
x = "Life"
y = "is"
z = "Beutiful"
print(x,y,z)
print(x+y+z)
~~~

~~~
a = 1
b = 2
c = 3
print(a,b,c)
print(a+b+c)
~~~

#### 데이터 유형


*   텍스트
*   숫자
*   불(bool)

~~~
a = 100
b = 200
result = a + b
print(a, '+', b, '=', result)
result = a - b
print(a, '-', b, '=', result)
result = a * b
print(a, '*', b, '=', result)
result = a / b
print(a, '/', b, '=', result)
~~~

~~~
a = int(input("첫번째 숫자를 입력하세요; "))
b = int(input("두번째 숫자를 입력하세요; "))
result = a + b
print(a, '+', b, '=', result)
result = a - b
print(a, '-', b, '=', result)
result = a * b
print(a, '*', b, '=', result)
result = a / b
print(a, '/', b, '=', result)
# 제곱, 몫, 나머지
~~~

~~~
a = int(input("첫번째 숫자를 입력하세요; "))
b = int(input("두번째 숫자를 입력하세요; "))
# 제곱
result = a ** b
print(a, '**', b, '=', result)
# 몫
result = a // b
print(a, '//', b, '=', result)
# 나머지
result = a % b
print(a, '%', b, '=', result)
~~~

~~~
num1 = input("숫자입력1: ")
num2 = input("숫자입력2: ")
result = num1 + num2
print(type(num1))
print(num1, '+', num2, '=', result)
~~~

~~~
a = 25
b = 27
c = 54
d = 60
result = a + b + c + d
print(a, '+', b, '+', c, '+', d, '=', result)
~~~

~~~
a = input("이름을 입력하세요")
b = str(input("전화번호를 입력하세요"))
c = int(input("무게를 입력하세요"))
result = c * 10

print("이름", a, "전화번호", b,
      "무게에 따른 금액",result )
~~~

## **2. print() 서식 출력**

~~~
print("%d" % 123)
print("%5d" % 123)
print("%05d" % 123)

print("%f" % 123.45)
print("%7.1f" % 123.45)
print("%7.3f" % 123.45)

print("%s" % "대한민국")
print("%8s" % "대한민국")
~~~

#### **Format 함수: 순서 지정 가능**

~~~
print("{0:d} {1:5d} {2:05d}".format(123,456,789))
~~~

~~~
print("{2:d} {1:5d} {0:05d}".format(123,456,789))
~~~

#### **서식 출력**

~~~
print("\n줄바꿈\n연습입니다.")
~~~

~~~
print("\n탭키\t연습")
~~~

~~~
print("글자가 \"강조\"되는 효과1")
print("글자가 \"강조\"되는 효과2")
print("역슬레시 3개 출력\\\\\\")
print(r"\n \t \" \\ \' @를 그대로 출력") #그대로 출력됨
~~~

#### **관계 연산자**

~~~
a,b = 10,20
print(a==b, a!=b, a>b, a<b, a>=b, a<=b)
~~~

#### **논리 연산자**

~~~
a = 99
print((a>100) and (a<200))
print((a>100) or (a<200))
print(not(a==100))
~~~

~~~
if(123):
  print("참이면 보입니다.")
if(0):
  print("거짓이면 안 보입니다.")
~~~

### 퀴즈2 숫자 입력을 받아 동전으로 바꿔주는 프로그램( 500원, 100원, 50원, 10원)나머지는 거스름 돈으로 출력

~~~
# 변수
bill, c500, c100, c50, c10 = 0,0,0,0,0
bill = int(input("바꿀 돈은?"))
c500 = bill // 500 # 몫
bill %= 500 # bill =bill % 500
c100 = bill // 100 # 몫
bill %= 100 # bill =bill % 100
c50 = bill // 50
bill %= 50 # bill =bill % 50
c10 = bill // 10
bill %= 10 # bill =bill % 10

print("500원짜리 %d개" % c500)
print("100원짜리 %d개" % c100)
print("50원짜리 %d개" % c50)
print("10원짜리 %d개" % c10)
print("잔돈 %d원" % bill)
~~~

## **조건문**

~~~
a = 200
if(a<100):
  print("100보다 작음")
else :  
  print("100보다 크다")
print("프로그램 끝")
~~~

~~~
# 홀짝 구분
a = int(input("정수를 입력하세요 : "))
if(a % 2 == 0) :
  print("짝수")
else :
  print("홀수")
~~~

~~~
a = 70
if(a > 50):
  if(a<100):
    print("50<a<100")
  else :
    print("a>100")
else :
  print("a<50")
~~~

~~~
fruit = ['사과', '배', '감', '포도']
fruit.append('딸기')
if '딸기' in fruit : # '딸기' not in fruit :
  print("딸기가 있습니다.")
print(fruit)
~~~

~~~
import random
number =[]
for num in range(0, 9) :
  number. append(random.randrange(0,10))
print("생성된 리스트", number)
~~~

~~~
import random
number =[]
for num in range(0,6) :
  number. append(random.randrange(1,46))
print("생성된 리스트", number)
~~~

## **반복문**

~~~
for i in range(0,3,1): # 시작값, 끝값+1, 증가값
  print("%d 안녕하세요~" % i) # 반복 내용
  print(i)
print("반갑습니다^^*")
~~~

~~~
for i in range(1,9,1):
  print("%d " % i, end="")
print("\n")
for i in range(1,9,1):
  print("%d" % i, end=" ")
~~~

~~~
sum = 0
for i in range(1,11,1):
  sum = sum + i
print("1~10까지 합계 : %d" % sum)
~~~

#### Quiz3 : 숫자 입력을 받아 1부터 입력된 숫자까지도 합을 for문을 활용하여 출력하시오

~~~
sum, num = 0, 0
num = int(input("숫자입력 : "))
for i in range(1,num+1,1):
  sum = sum + i
print("1~n까지 합계 : %d" % sum)
~~~

## **중첩 for문**

~~~
i,j,k = 0,0,0
k = int(input("구구단 단수 입력"))
for i in range(k,10,1):
  for j in range(1,10,1):
    print("%d x %d = %2d" % (k,j,k*j))
  print("")
~~~

~~~
i,j,k = 0,0,0
for i in range(2,10,1):
  for j in range(1,10,1):
    print("%d x %d = %2d" % (i,j,i*j))
  print("")
~~~

#### Quiz 구구단을 2,3,4,5 출력 후 줄 바꿔서 출력하시오

~~~
m,n=0,0
for m in range(1,10,1):
  for n in range(2,6,1):
      print("%d x %d = %2d" % (n,m,m*n), end='\t')     
  print("")
print("\n")
m,n=0,0
for m in range(1,10,1):
  for n in range(6,10,1):
   print("%d x %d = %2d" % (n,m,n*m), end='\t' )
  print("")
~~~

# CH3 자료형
## 1. 인덱스와 슬라이딩

~~~
L = [0,1,2,3,4,5,6,7,8,9]
print(L[1])
~~~

~~~
L = [0,1,2,3,4,5,6,7,8,9]
print(L[-1])
~~~

~~~
L = [0,1,2,3,4,5,6,7,8,9]
print(L[0:9:2])
~~~

~~~
L = [0,1,2,3,4,5,6,7,8,9]
print(len[L])
print(L[len(L)-1])
~~~

~~~
L = [0,1,2,3,4,5,6,7,8,9]
L[0] = 99
L[9] = '가나다'
L[1] = [1,2,3]
print(L)
print(L[9])
~~~

~~~
a = [1,2,3]
b = [4,5,6]
c = a+b
print(a+b)
print(c)
print(a*3)
~~~

~~~
L = [1,2,3,4,5]
print(L)
L.append(6) #리스트 뒤에 추가
print(L)
L.remove(3) #해당 요소값을 삭제
print(L)
~~~

~~~
k =['a' , 'b' , 'c' , 'd']
k.remove('d')
print(k)
~~~

~~~
k = "God is love!"
print(k[:3])
~~~

~~~
k = "God is love!"
print(k[:3])
print(k[6:])
print(k[-8:-2])
~~~

~~~
k = "God is love!"
print(k.upper())
print(k.lower())
print(k.strip())
~~~

~~~
a = " God, is, love! "
print(a.split(","))
print(k.lower())
print(k.strip()) 
~~~

~~~
a = ["apple", "banana", "cherry"]
a.append("orange") # 맨뒤에 추가
print(a)
~~~

~~~
a = ["apple", "banana", "cherry"]
a.insert(1,"orange") # 지정된 곳에 삽입
print(a)
~~~

~~~
a = ["apple", "banana", "cherry"]
a.remove("banana")
print(a)
~~~

~~~
a = ["apple", "banana", "cherry"]
a.pop() # 맨뒤 삭제
print(a)
a.pop(1) # 지정한 위치 삭제
print(a)
~~~

~~~
a = ["apple", "banana", "cherry"]
del a[0]
print(a)
a.clear() # del a
print(a)
~~~

~~~
fruit = ["apple", "banana", "cherry"]
for x in fruit:
  print(x)
~~~

~~~
fruit = ["apple", "banana", "cherry"]
for i in range(len(fruit)):
  print(fruit)
~~~

#### SORT

~~~
a = [5,3,6,8,1,9,0]
a.sort()
print(a)
~~~

~~~
a = [5,3,6,8,1,9,0,2,4,7]
a.sort(reverse = True)
print(a)
a.sort()
print(a)
~~~

~~~
fruit = ["banana", "apple", "kiwi", "cherry", "Orange"]
fruit.sort() # 대소문자 구분하여 정렬
print(fruit)
fruit.sort(key = str.lower) # 대소문자 구분 없이 정렬
print(fruit)
fruit.reverse() # 항목의 순서를 역으로 바꿈
print(fruit)
~~~

~~~
# list 복사
fruit = ["banana", "apple", "kiwi", "cherry", "Orange"]
myList = fruit.copy()
print(myList)
cpList = list(fruit)
print(cpList)
~~~

### 2.튜플(Tuple)

~~~
l = [1,2,3]
t = (4,5,6)
l[0] = 5
print(l)
# t[0] = 1
print(t)
~~~

~~~
f = ["banana", "apple", "kiwi", "cherry", "Orange"]
print(len(f))
~~~

~~~
t = ("apple",)
print(t)
print(type(t))
f = ("banana") # 튜플로 인식하기 위해서는 ","필요
print(f)
print(type(f))
~~~

~~~
f = ("banana", "apple", "kiwi", "cherry", "Orange")
print(f[:4])
print(f[2:])
~~~

~~~
f = ("banana", "apple", "kiwi", "cherry", "Orange")
if "apple" in f:
  print("Yes, 'apple' is in")
else:
  print("No")
~~~

### list<->Tuple

~~~
firm = ['Samsung', 'LG', 'SK']
tdata = tuple(firm)
print(firm)
print(tdata)
~~~

~~~
# tuple에 추가
t = ("banana", "apple", "kiwi", "cherry")
y = list(t)
y.append("Orange")
t = tuple(y)
print(t)
~~~

~~~
t = ("apple", "banana", "cherry")
q = ("kiwi",)
t += q
print(t)
~~~

~~~
t = ('apple', 'banana', 'cherry', 'kiwi')
l = list(t)
l.remove('apple')
t= tuple(l)
print(t)
del t
# print(t)
~~~

### 3.dict 사전자료형

~~~
d = {
    'a':1,
    'b':2,
    'c':3
}
print(d)
print(d.keys())
print(d.values())
print(d.items())
~~~

~~~
car = {
    "brand" : "BMW",
    "model" : "GT",
    "year" : 1988
}
print(car)
print(len(car))
car["year"] = 2000
print(car)
car["item"] = 123456
car.update({"color" : "red"})
print(car)
~~~

~~~
# 항목 제거
car = {
    "brand" : "BMW",
    "model" : "GT",
    "year" : 1988
}
car.pop("model")
print(car) 
~~~

~~~
car = {
    "brand" : "BMW",
    "model" : "GT",
    "year" : 1988
}
car.popitem()
print(car) 
~~~

~~~
car = {
    "brand" : "BMW",
    "model" : "GT",
    "year" : 1988
}
car.clear()
del car 
~~~

#### LOOP

~~~
# 값을 하나씩 인쇄
car = {
    "brand" : "BMW",
    "model" : "GT",
    "year" : 1988
}
for x in car :
  print(car[x])
~~~

~~~
car = {
    "brand" : "BMW",
    "model" : "GT",
    "year" : 1988
}
for x in car.values() :
  print(x)
~~~

~~~
car = {
    "brand" : "BMW",
    "model" : "GT",
    "year" : 1988
}
for x,y in car.items():
  print(x,y)
~~~

~~~
car = {
    "brand" : "BMW",
    "model" : "GT",
    "year" : 1988
}
myCar = car.copy()
print(myCar)
~~~

~~~
car = {
    "brand" : "BMW",
    "model" : "GT",
    "year" : 1988
}
myCar = dict(car)
print(myCar)
~~~

~~~
name1 = {"name" : "홍길동", "year":2001}
name2 = {"name" : "갑돌이", "year":2010}
name3 = {"name" : "갑순이", "year":2003}
family ={
    "name1" : name1,
    "name2" : name2,
    "name3" : name3
}
print(family)
~~~

~~~
##CH4 조건문, 반복문
~~~

~~~
score = int(input("점수를 입력해 주세요 : "))
if (score > 100):
  print("0~100까지의 숫자로 입력하세요.")
else:
  if(score >= 90):
    print("A")
  elif(score >= 80):
    print("B")
  elif(score >= 70):
    print("C")
  elif(score >= 60):
    print("D")
  else: 
    print("F")
print("학점 입니다.")
~~~

~~~
score = int(input("점수를 입력해 주세요 : "))
if (score > 100):
  print("0~100까지의 숫자로 입력하세요.")
else:
  if(score >= 90):
    print("A")
  elif(score >= 80):
    print("B")
  elif(score >= 70):
    print("C")
  elif(score >= 60):
    print("D")
  else: 
    print("F")
print("학점, 점수: %3d" %score)
~~~

~~~
import random

numbers = []
for num in range(0,10):
  numbers.append(random.randrange(0,10))

print("생성된 리스트", numbers)

for num in range(0,10):
  if num not in numbers:
    print("숫자 %d는 리스트에 없습니다." %num)
  else:
    print("숫자 %d는 리스트에 없습니다." %num)
~~~

~~~
select, answer, numStr, num1, num2 = 0,0,"",0,0

select = int(input("1.입력한 수식 계산 2.두수의 합계"))

if select == 1:
  numStr = input("*** 수식을 입력하세요 : ")
  answer = eval(numStr) # 1+2, "string"+"string"
  print(" %s 결과는 %5.1f입니다. " %(numStr,answer))
elif select == 2:
  num1 = int(input("*** 첫번째 숫자를 입력하세요 : "))
  num2 = int(input("*** 두번째 숫자를 입력하세요 : "))
  for i in range(num1,num2+1):
    answer = answer + i
  print("%d+...+%d는 %d입니다. " %(num1,num2,answer))
else:
  print("1또는 2만 입력해야 합니다.")
~~~

~~~
##for&while 반복문
~~~

~~~
for i in range(0,3,1):
  print("안녕!")
~~~

~~~
for i in [0,3,1]:
  print("안녕@")
~~~

~~~
for i in range(0,3,1):
  for j in range(0,2,1):
    print("i:%d, j:%d" %(i,j))
~~~

~~~
i,j = 0,0
for i in range(2,10,1):
  for j in range(1,10,1):
    print("%d x %d = %2d " %(i,j,i*j), end='' )
  print("")
~~~

~~~
i =0 
while i<3:
  print("%d : while문" %i)
  i = i+1
~~~

~~~
#Q 1부터 10까지 합계를 while, for문으로
i, hap=0,0
i = 1
while i<11:
  hap = hap + i
  i=i+1

print("1부터 10까지의 합계: %d" %hap)
~~~

~~~
#while True:
print("무한루프ㅠㅠ", end='')
~~~

~~~
#break
for i in range(1,100):
  print("for문 %d번 실행" %i)
  break
print("break 빠짐")
~~~

~~~
hap = 0
a,b = 0,0
while True:
  a = int(input("덧셈 첫번째 수 입력: "))
  if a==0:
    break
  b = int(input("덧셈 두번째 수 입력: "))
  hap = a + b
  print("%d + %d = %d" %(a,b,hap))

print("break로 탈출")
~~~

~~~
# continue
hap, i = 0,0
for i in range(1,11):
  if i % 3 ==0:
    continue
  hap += i

print("1~100 합계(3의 배수 제외): %d" %hap)
~~~

~~~
fruits = ["사과", "바나나","체리"]
for x in fruits:
  if x =="바나나":
    continue
  print(x)
~~~

~~~
for x in range(6):
  print(x)
else:
  print("끝")
~~~

~~~
for x in range(6):
  if x ==3:break
  print(x)
else:
  print("끝")
~~~

~~~
for x in [0,1,2]:
  pass
~~~

~~~
## 함수
~~~

~~~
# 두수를 더하는 함수
def plus(v1,v2):
  result = 0
  result = v1 + v2
  return result

hap = 0
hap = plus(10,20)
print("10+20 plus() 처리 결과는 %d" %hap)
hap = plus(20,30)
print("20+30 plus() 처리 결과는 %d" %hap)
~~~

~~~
#계산기 코드
def calc(v1,v2,op):
  result = 0
  if op =='+':
    result = v1 + v2
  elif op == '-':
    result = v1 - v2
  elif op == '*':
    result = v1 * v2
  elif op == '/':
    result = v1 / v2
  return result

rst = 0
var1, var2, opr = 0,0,""

opr = input("(+,-,*,/) 입력: ")
var1 = int(input("1번째 수 입력: "))
var2 = int(input("2번째 수 입력: "))
rst = calc(var1,var2,opr)
print("계산기 %d %s %d = %d" %(var1, opr, var2, rst))
~~~

~~~
## Q 0으로 나누려고하면 메시지 출력 계산되지 않게, ** 제곱연산자 추가(숫자1, 연산자, 숫자2)
~~~

~~~
#계산기 코드
def calc(v1,v2,op):
  result = 0
  if op =='+':
    result = v1 + v2
  elif op == '-':
    result = v1 - v2
  elif op == '*':
    result = v1 * v2
  elif op == '/':
    result = v1 / v2
  elif op == '**':
    result = v1 ** v2
  return result

rst = 0
var1, opr, var2 = 0,0,""

opr = input("(+,-,*,/,**) 입력: ")
var1 = int(input("1번째 수 입력: "))
var2 = int(input("2번째 수 입력: "))
rst = calc(var1,opr,var2)
~~~

~~~
#전역 변수와 지역변수
def func1():
  a = 10 # 지역변수
  print("func1()에서 a값 %d" %a)

def func2():
  print("func2()에서 a값 %d" %a)

a = 20 # 전역 변수

func1()
func2()
~~~
