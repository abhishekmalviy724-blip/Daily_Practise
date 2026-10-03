# Daily_Practise
# Day 1.
students = {
    "Rahul": {"math": 80, "python": 90, "sql": 70},
    "Aman": {"math": 60, "python": 55, "sql": 65},
    "Priya": {"math": 95, "python": 88, "sql": 92},
    "Rohit": {"math": 45, "python": 50, "sql": 40},
    "Rohit": {"math": 80, "python": 90, "sql": 90}
}
for i,j in students.items():
    a=list(j.values())
    avg=sum(a)/len(a)
print(avg)
_____________________________________________________________________________________________________________________________________________________________________________________________________________________________

# Day 2.
a = [1,2,3,4,5,5,6,6,7,7,8]
new = []
for i in a:
    if a.count(i)==1 and i not in new:
        new.append(i)
print(new)
_____________________________________________________________________________________________________________________________________________________________________________________________________________________________
# Day 2.
a = [1,2,3,4]
sum = 0
for i in a:
    sum+=i
    avg = sum/len(a)
print(avg)
_____________________________________________________________________________________________________________________________________________________________________________________________________________________________
# Day 2.
a = [1,2,3,4,4,3,2,1,4,5,6,7,8]
b = {i: a.count(i) for i in a}
print(b)

a = [1,2,1,2,3,1,4,5,43,5,7,8,6,4,6]
new = []
for i in a:
    if a.count(i)>1 and i not in new:
        new.append(i)
print(new)
_____________________________________________________________________________________________________________________________________________________________________________________________________________________________

# Day 3.
# a = "abhishek malviy"
# b=[f"{i[0].upper()}{i[1:]}" for i in a.split()]
# print(" ".join(b))
_____________________________________________________________________________________________________________________________________________________________________________________________________________________________
# s = [1, 2, 2, 3, 3, 3, 4]
# print({i:s.count(i) for i in s})
# fre1={}
# for i in s:
#     fre1[i]=fre1.get(i,0)+1
# print(fre1)
_____________________________________________________________________________________________________________________________________________________________________________
# students = [("Amit", 85), ("Priya", 92), ("Raj", 78)]
# new=sorted(students, key=lambda x:x[1],reverse=True)
# print(new)
_______________________________________________________
# s = [10, 15, 22, 33, 40, 55, 68]
# print([i for i in s if i%2==0 and i>20])
____________________________________________

# def a(*arg):
#     sum=0
#     for i in arg:
#         sum+=i
#         avg = sum/len(arg)
#     return avg
# print(a(2, 4, 6, 8))
______________________________
a = "mada," 
rev = ""
for i in a:
    rev = i + rev
if rev == a:
    print("P")
else:
    print("No")
_________________________________
employees = [
    {"name": "Amit", "dept": "IT", "salary": 50000},
    {"name": "Priya", "dept": "HR", "salary": 40000},
    {"name": "Raj", "dept": "IT", "salary": 60000},
    {"name": "Neha", "dept": "HR", "salary": 45000},
]
new={i["dept"]: i["salary"]/len(employees) for i in employees}
print(new)
___________________________________________________________________
nums = [4, 2, 5, 2, 4, 7, 5, 9]
new = []
for i in nums:
    if i not in new:
        new.append(i)
print(new)
_____________________________________
try:
    a=int(input("Enter"))
    b=int(input("Enter"))
    print(a/b)
except ZeroDivisionError:
    print("Error: Division by zero")
    
except ValueError:
    print("Error: Invalid input")
________________________________________

s = "programming"
new =[]
for i in s:
    if s.count(i)>1 and i not in new:
        print(i)
        new.append(i)
_____________________________________________________________________________________________________________________________________________________________________________________________________________________________

# Day 4.
def fact(n):
    if n==0 | n==1:
        return 1
    else:
        return n* fact(n-1)
# print(fact(5))
_____________________________
list1 = [1, 2, 3, 4] 
list2 = [3, 4, 5, 6]
print(set(list1)&set(list2))
________________________________
words = ["apple", "banana", "kiwi", "fig", "mango"]
print(list(filter(lambda x:len(x)>4,words)))
_______________________________________________________
data = ["10", "20", "abc", "30", "xyz"]
for i in data:
    try:
        int(i)
        print(i)
    except ValueError:
        pass
_____________________________________________________________________________________________________________________________________________________________________________________________________________________________

# Day 5.
students = [
    ("Amit", 78),
    ("Ravi", 92),
    ("Amit", 85),
    ("Meena", 88),
    ("Ravi", 76),
    ("Meena", 95)
]
new={}
for name,marks in students:
    if name not in new:
        new[name]=[]
    new[name].append(marks)
print(new)
____________________________________________________________________
words = ["python", "java", "python", "sql", "java", "python", "ml"]
print({i: words.count(i) for i in words if words.count(i)>=2})
___________________________________________________________________
nums = [10, 20, 10, 30, 20, 40, 50, 30]
print(list(dict.fromkeys(nums)))
___________________________________________________________________
text = "python is easy and python is powerful and python is popular"
print({i: text.count(i) for i in text.split() if text.count(i)>=2})
_____________________________________________________________________
students = {
    "Amit": 78,
    "Ravi": 92,
    "Meena": 65,
    "Rahul": 88,
    "Priya": 55
}
print({name: marks+5 for name,marks in students.items() if marks>=70})
______________________________________________________________________
from functools import reduce
nums = [10, 15, 20, 25, 30, 35, 40]
print(reduce(lambda x,y:x*y, filter(lambda x:x%2==0,nums)))
_____________________________________________________________________________________________________________________________________________________________________________________________________________________________

# Day 6. 
from collections import defaultdict
def group_angra(words):
    group = defaultdict(list)
    for i in words:
        key = "".join(sorted(i))
        group[key].append(i)
    return list(group.values())
print(group_angra(["eat", "tea", "tan", "ate", "nat", "bat"]))
_______________________________________________________________
students = [
    {"name": "Amit", "marks": [78, 85, 90]},
    {"name": "Rahul", "marks": [45, 55, 60]},
    {"name": "Priya", "marks": [90, 92, 88]},
    {"name": "Neha", "marks": [65, 70, 72]},
    {"name": "Ravi", "marks": [35, 40, 45]}
]
for i in students:
        avg=sum(i["marks"])/len(i["marks"])
        if avg>70:
            print(i["name"])

_____________________________________________________________________________________________________________________________________________________________________________________________________________________________
# Day 7.
n = int(input("Enter N: "))

primes = []

for num in range(2, n + 1):
    is_prime = True

    for i in range(2, int(num ** 0.5) + 1):
        if num % i == 0:
            is_prime = False
            break

    if is_prime:
        primes.append(num)

print("Prime numbers:", primes)
print("Count:", len(primes))
print("Sum:", sum(primes))
_____________________________________________________________________________________________________________________________________________________________________________________________________________________________

# Day 8.
employees = [
    {"name": "Amit", "salary": 25000, "department": "IT"},
    {"name": "Rahul", "salary": 35000, "department": "HR"},
    {"name": "Priya", "salary": 45000, "department": "IT"},
    {"name": "Neha", "salary": 30000, "department": "Sales"},
    {"name": "Ravi", "salary": 50000, "department": "IT"}
]
for i in employees:
    if i["salary"]>30000 and i["department"]=="IT":
     print(i["name"],i["salary"])
___________________________________________________________
products = [
    {"name": "Laptop", "price": 55000, "stock": 3},
    {"name": "Mouse", "price": 800, "stock": 15},
    {"name": "Keyboard", "price": 1500, "stock": 0},
    {"name": "Monitor", "price": 12000, "stock": 5},
    {"name": "Webcam", "price": 3000, "stock": 0}
]
for i in products:
    if i["stock"]>0 and i["price"]>10000:
        print(i["name"],i["price"])
____________________________________________________________
sales = [
    {"product": "Laptop", "quantity": 2, "price": 50000},
    {"product": "Mouse", "quantity": 5, "price": 800},
    {"product": "Keyboard", "quantity": 3, "price": 1500},
    {"product": "Monitor", "quantity": 2, "price": 12000},
    {"product": "Webcam", "quantity": 4, "price": 3000}
]
for i in sales:
    total = i["quantity"] * i["price"]
    if total > 70000:
        print(i["product"], total)
_______________________________________________________________
students = [
    {"name": "Amit", "marks": [78, 85, 90]},
    {"name": "Rahul", "marks": [65, 72, 68]},
    {"name": "Priya", "marks": [90, 92, 88]},
    {"name": "Neha", "marks": [82, 79, 85]},
    {"name": "Ravi", "marks": [70, 75, 80]}
]
high_marks = 0
for i in students:
    avg = sum(i["marks"])/len(i["marks"])
    if avg>high_marks:
        high_marks=avg
        name = i["name"]
print(name,high_marks)
_______________________________________________________________
employees = {
    "Amit": {"age": 22, "salary": 30000},
    "Rahul": {"age": 25, "salary": 45000},
    "Priya": {"age": 23, "salary": 38000},
    "Neha": {"age": 27, "salary": 52000}
}
for name,info in employees.items():
    if info["salary"]>40000:
        print(name,info["salary"])
_______________________________________________________
nums = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
new=[]
for i in nums:
    if i%2==0:
        even = i**2
        new.append(even)
    else:
        if i!=3:
            odd=i**3
            new.append(odd)
print(new)
_____________________________________________________________________________________________________________________________________________________________________________________________________________________________
# Day 9.
nums = [4, 2, 4, 5, 2, 7, 4]
new = []
for i in nums:
    if i in new:
        pass   
    else:
        new.append(i)
print(new)
_________________________________________________________
data = [{"name": "A", "age": 25},
        {"name": "B", "age": 20}, 
        {"name": "C", "age": 30}]
print(sorted(data,  key=lambda x:x["age"]))
______________________________________________________
keys = ["a", "b", "c"]
values = [1, 2, 3]
print({k: f"{k}:{v}" for k,v in zip(keys,values)})
_____________________________________________________________________________________________________________________________________________________________________________________________________________________________
# Day 10.
class Employee:
    def __init__(self,name,salary,department):
        self.name=name
        self.salary=salary
        self.department=department
    def display(self):
        print(self.name,self.salary,self.department)
onj1=(Employee("Abhishek",1500000,"MLE"))
onj2=(Employee("Ankit",1500000,"B.Pharma"))
onj3=(Employee("Ayush",1500000,"B.Com"))
onj1.display()
onj2.display()
onj3.display()
_____________________________________________________
class BankAccount:
    def __init__(self,account_holder,balance):
        self.account_holder=account_holder
        self.balance=balance
    def deposit(self, amount):
        self.balance +=amount
    def withdraw(self, amount):
        self.balance -=amount
    def show_balance(self):
        print(self.balance)
obj = BankAccount("Abhishek",500000)
obj.withdraw(70)
obj.show_balance()
____________________________________________________
class Student:
    def __init__(self, name, marks):
        self.name = name
        self.marks = marks

    def average(self):
        total = 0

        for i in self.marks:
            total += i

        return total / len(self.marks)

    def result(self):
        avg = self.average()

        if avg >= 60:
            return "Pass"
        else:
            return "Fail"

    def display(self):
        print(self.name)
        print(self.average())
        print(self.result())

obj = Student("Abhishek", [78, 89, 65])

obj.display()
________________________________________________________________
class Person:
    def __init__(self, name,age):
        self.name=name
        self.age=age
    def display_person(self):
        print(self.name,self.age)
class student(Person):
    def __init__(self, name, age, course, marks):
        super().__init__(name, age)
        self.course=course
        self.marks=marks
    def display_student(self):
        print(self.name,self.age, self.course, self.marks)
obj = student("Abhishek",20,"B.E",80)
obj.display_person()
______________________________________________________________-
class Animal:
    def __init__(self,name):
        self.name=name
    def sound(self):
        print("Aminal makes a sound!")
class Dog(Animal):
    def __init__(self, name):
        super().__init__(name)
    def sound(self):
        print(self.name)
obj = Dog("Bark")
obj.sound()
_____________________________________________________________________________________________________________________________________________________________________________________________________________________________
def two_sum(nums, target):
    seen = {}

    for i, num in enumerate(nums):
        needed = target - num

        if needed in seen:
            return [seen[needed], i]

        seen[num] = i

    return []


nums = [2, 7, 11, 15]
target = 9

print(two_sum(nums, target))
_____________________________________________________________________________________________________________________________________________________________________________________________________________________________
students = [
    {"name": "Aman", "marks": [78, 85, 92, 67, 88]},
    {"name": "Riya", "marks": [91, 76, 89, 95, 84]},
    {"name": "Rahul", "marks": [55, 62, 48, 71, 59]},
    {"name": "Priya", "marks": [88, 93, 90, 87, 95]},
    {"name": "Karan", "marks": [45, 52, 61, 39, 58]}
]
sum=0
highest_average = students[0]
for i in students:
    for marks in i["marks"]:
        sum+=marks
        Total_marks = sum
        avg=sum/len(i["marks"])
    print(sum)
    print(avg)
    if avg>=90:
        print("A+")
    elif avg>80 and avg<89:
        print("B")
    elif avg>70 and avg<79:
        print("C")
    elif avg>60 and avg<69:
        print("D")
    else:
        print("F")
    if avg>=60:
        print("Pass")
    else:
        print("Fail")
_____________________________________________________________________________________________________________________________________________________________________________________________________________________________

employees = [
    {"name": "Aman", "dept": "IT", "salary": 55000, "ratings": [8, 7, 9]},
    {"name": "Riya", "dept": "HR", "salary": 48000, "ratings": [9, 8, 8]},
    {"name": "Karan", "dept": "IT", "salary": 62000, "ratings": [6, 7, 6]},
    {"name": "Neha", "dept": "Sales", "salary": 51000, "ratings": [9, 9, 10]},
    {"name": "Rahul", "dept": "Sales", "salary": 45000, "ratings": [5, 6, 7]},
    {"name": "Priya", "dept": "HR", "salary": 58000, "ratings": [8, 9, 9]}
]


def analyze_employees(employees):

    departments = {}
    excellent = []

    for employee in employees:

        average = sum(employee["ratings"]) / len(employee["ratings"])

        if average >= 8.5:
            performance = "Excellent"
            increment = 0.15
            excellent.append(employee["name"])

        elif average >= 7:
            performance = "Good"
            increment = 0.10

        elif average >= 5:
            performance = "Average"
            increment = 0.05

        else:
            performance = "Poor"
            increment = 0

        new_salary = employee["salary"] + employee["salary"] * increment

        employee["average_rating"] = round(average, 2)
        employee["performance"] = performance
        employee["updated_salary"] = round(new_salary, 2)

        dept = employee["dept"]

        if dept not in departments:
            departments[dept] = []

        departments[dept].append(employee)

    department_salary = {}

    for dept, data in departments.items():

        total_salary = sum(employee["salary"] for employee in data)

        department_salary[dept] = round(
            total_salary / len(data), 2
        )

    department_top = {}

    for dept, data in departments.items():

        top_employee = max(
            data,
            key=lambda employee: employee["average_rating"]
        )

        department_top[dept] = top_employee["name"]

    overall_top = max(
        employees,
        key=lambda employee: employee["average_rating"]
    )

    print("EMPLOYEE PERFORMANCE")

    for employee in employees:
        print(
            employee["name"],
            employee["average_rating"],
            employee["performance"],
            employee["updated_salary"]
        )

    print("\nDEPARTMENT AVERAGE SALARY")

    for dept, salary in department_salary.items():
        print(dept, salary)

    print("\nDEPARTMENT TOP EMPLOYEE")

    for dept, name in department_top.items():
        print(dept, name)

    print("\nEXCELLENT EMPLOYEES")
    print(excellent)

    print("\nOVERALL TOP EMPLOYEE")
    print(overall_top["name"])
    print(overall_top["average_rating"])


analyze_employees(employees)
_____________________________________________________________________________________________________________________________________________________________________________________________________________________________
nums = [12, 5, 8, 12, 3, 8, 15, 5, 20, 3, 7]
new = []
for i in nums:
    if i in new:
        pass
    else:
        new.append(i)
print(new)
_____________________________________________
nums = [2, 4, 7, 2, 9, 4, 7, 7, 3, 9, 2]
new = {i: nums.count(i) for i in nums}
neww = []
for i in new:
    if new[i]==1:
        neww.append (i)
print(neww)
________________________________________________
nums = [10, 20, 30, 20, 40, 10, 50, 30, 60]
new = {i: nums.count(i) for i in nums}
new1 = []
for i in new:
    if new[i]==2:
        new1.append(i)
print(new1)
_____________________________________________________________________________________________________________________________________________________________________________________________________________________________
L = [1,2,3,4,5]
largest = L[0]
smallest = L[0]
for i in L:
    if i>largest:
        largest=i
    elif i<smallest:
        smallest=i
print(largest)
print(smallest)
___________________________________________________
L1 = [1,2,3,4,5]
L2 = [5,6,7,8,9]
for i in L1:
    if i in L2:
        print(i)
_______________________________________________________
nums = [10, 20, 10, 30, 20, 40, 10, 30, 50, 20]
new = {i: nums.count(i) for i in nums}
list = []
for i in new:
    if new[i]==3:
        list.append(i)
print(list)
______________________________________________________
nums = [2, 5, 2, 8, 5, 2, 9, 8, 5, 8, 8]
new = {i: nums.count(i) for i in nums}
max_frq = 0
max_num = 0
for key,value in new.items():
    if value>max_frq:
        max_frq=value
        max_num=key
print(max_num)
__________________________________________________
nums = [4, 2, 7, 4, 9, 2, 4, 7, 9, 9, 9]
new = {}
for i in nums:
    if i in new:
        new[i]+=1
    else:
        new[i]=1
print(new)
__________________________________________________________
nums = [10, 15, 20, 10, 25, 15, 30, 20, 10, 35, 15]
dic = {}
for i in nums:
    if i in dic:
        dic[i]+=1
    else:
        dic[i]=1
for j in dic:
    if dic[j]==2:
        print(i)
_____________________________________________________________
nums = [5, 2, 8, 5, 2, 9, 8, 5, 2, 2, 7]
frq = {}
for i in nums:
    if i in frq:
        frq[i]+=1
    else:
        frq[i]=1
max_frq=0
max_num=0
for key,value in frq.items():
    if value>max_frq:
        max_frq=value
        max_num=key
max_frq,max_frq
___________________________________________________
nums = [10, 20, 30, 20, 40, 10, 50, 30, 60]
dic = {}
new=[]
for i in nums:
    if i in dic:
        if dic[i]==1:
            new.append(i)
        dic[i]+=1
    else:
        dic[i]=1
new
__________________________________________________-
nums = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
even = []
for i in nums:
    if i%2==0:
        even.append(i**2)
    else:
        even.append(i**3)
print(even)
____________________________________________________
nums = [12, 5, 8, 21, 10, 7, 16, 3, 14, 9]
{"Even":[i for i in nums if i%2==0],
 "Odd":[i for i in nums if i%2!=0]}
_____________________________________________________________________________________________________________________________________________________________________________________________________________________________
a = [12, 5, 8, 21, 10, 7,0,-1]
[i for i in a if i%2==0]

sum=0
for i in a:
    sum+=1
sum
___________________________
max_num = a[0]
min_num = a[0]
for i in a:
    if i>max_num:
        max_num=i
    elif i<min_num:
        min_num=i
print(min_num)
print(max_num)
______________________________________________
p = 0
n = 0
zero = 0
for i in a:
    if i == 0:
        zero+=1
    elif i<0:
        n+=1
    else:
        p+=1
print(p)
print(n)
print(zero)
________________________________________
a="PythonProgramming"
v=0
c=0
for i in a:
    if i in "AIOUEaioue":
        v+=1
    else:
        c+=1
print(v)
print(c)
_______________________
rev = ""
for i in a:
    rev = i + rev
print(rev)
________________________-
rev = ""
for i in a:
    rev = i + rev
if rev == a:
    print("Palindrome")
else:
    print("Not Palindrome")
__________________________________
a=[1,2,3,4,5,5]
new = []
for i in a:
    if i in new:
        pass
    else:
        new.append(i)
new
_____________________________________
a=[1,2,3,4,3,2,3,4]
{i: a.count(i) for i in a}
____________________________
a=[1,1,2,3,4,5,5,6]
new={i: a.count(i) for i in a}
for key,values in new.items():
    if values==2:
        print(key)
_____________________________________
a=[1,2,3,4]
b=[4,5,6,7]
for i in a:
    if i in b:
        print(i)
______________________________
c=a+b
new = []
for i in c:
    if i in new:
        pass
    else:
        new.append(i)
print(new)
________________________________
a=[1,2,3,4,5,6]
max_1 = a[0]
max_2 = a[0]
for i in a:
    if i>max_2:
        max_2=max_1
        max_1=i
print(max_2)
_________________________________________
a = [3, 1, 4, 2, 5, 6]
min_1 = float('inf')
min_2 = float('inf')

for i in a:
    if i < min_1:
        min_2 = min_1
        min_1 = i

    if i < min_2:
        if i != min_1:
            min_2 = i

print("Smallest:", min_1)
print("Second smallest:", min_2)
____________________________________
a=12345
sum=0
for i in str(a):
    sum+=int(i)
print(sum)
________________________________
a=12345
rev=""
for i in str(a):
    rev = i + rev
rev

_____________________________________________________________________________________________________________________________________________________________________________________________________________________________
