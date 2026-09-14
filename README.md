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
_______________________________________________________________________________________________________________________________________________________________________________

# Day 2.
a = [1,2,3,4,5,5,6,6,7,7,8]
new = []
for i in a:
    if a.count(i)==1 and i not in new:
        new.append(i)
print(new)
____________________________________________________________________________________________________________________________________________________________________________
# Day 2.
a = [1,2,3,4]
sum = 0
for i in a:
    sum+=i
    avg = sum/len(a)
print(avg)
____________________________________________________________________________________________________________________________________________________________________________
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
____________________________________________________________________________________________________________________________________________________________________________

# Day 3.
# a = "abhishek malviy"
# b=[f"{i[0].upper()}{i[1:]}" for i in a.split()]
# print(" ".join(b))

# s = [1, 2, 2, 3, 3, 3, 4]
# print({i:s.count(i) for i in s})
# fre1={}
# for i in s:
#     fre1[i]=fre1.get(i,0)+1
# print(fre1)

# students = [("Amit", 85), ("Priya", 92), ("Raj", 78)]
# new=sorted(students, key=lambda x:x[1],reverse=True)
# print(new)

# s = [10, 15, 22, 33, 40, 55, 68]
# print([i for i in s if i%2==0 and i>20])


# def a(*arg):
#     sum=0
#     for i in arg:
#         sum+=i
#         avg = sum/len(arg)
#     return avg
# print(a(2, 4, 6, 8))
        
a = "mada," 
rev = ""
for i in a:
    rev = i + rev
if rev == a:
    print("P")
else:
    print("No")

employees = [
    {"name": "Amit", "dept": "IT", "salary": 50000},
    {"name": "Priya", "dept": "HR", "salary": 40000},
    {"name": "Raj", "dept": "IT", "salary": 60000},
    {"name": "Neha", "dept": "HR", "salary": 45000},
]
new={i["dept"]: i["salary"]/len(employees) for i in employees}
print(new)

nums = [4, 2, 5, 2, 4, 7, 5, 9]
new = []
for i in nums:
    if i not in new:
        new.append(i)
print(new)

try:
    a=int(input("Enter"))
    b=int(input("Enter"))
    print(a/b)
except ZeroDivisionError:
    print("Error: Division by zero")
    
except ValueError:
    print("Error: Invalid input")
    

s = "programming"
new =[]
for i in s:
    if s.count(i)>1 and i not in new:
        print(i)
        new.append(i)
____________________________________________________________________________________________________________________________________________________________________________

# Day 4.
def fact(n):
    if n==0 | n==1:
        return 1
    else:
        return n* fact(n-1)
# print(fact(5))

list1 = [1, 2, 3, 4] 
list2 = [3, 4, 5, 6]
print(set(list1)&set(list2))

words = ["apple", "banana", "kiwi", "fig", "mango"]
print(list(filter(lambda x:len(x)>4,words)))

data = ["10", "20", "abc", "30", "xyz"]
for i in data:
    try:
        int(i)
        print(i)
    except ValueError:
        pass
____________________________________________________________________________________________________________________________________________________________________________
