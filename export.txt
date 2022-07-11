#q11
def show_stars(row):
    for i in range(row):
        for j in range(0,i+1):
            print('*',end='')
        print('\n')
num=int(input("Enter rows :"))
show_stars(num)

#q12
string=input("Enter the string :")
new=''
for i in string:
    if i not in ('!','@','#','$','%','&','*'):
        new+=i
print(new)

#q13
l=[]
length=int(input("Enter list size :"))
for i in range(0,length):
    e=int(input("Enter element :"))
    l.append(e)

for i in l:
    if i%5==0:
        print(i)

#q14
strg="Hi HiihihiHihiHihihiH HIHIhi Hi"
sub="Hi"

print("No. of times substring appears :",strg.count(sub))

#q15
row=int(input("Enter rows :"))
for i in range(row+1):
        for j in range(0,i):
            print(i,end='')
        print('\n')

#LIST
#q17
l=[]
length=int(input("Enter list size :"))
for i in range(0,length):
    e=int(input("Enter element :"))
    l.append(e)

l[0],l[length-1]=l[length-1],l[0]
print(l)

#q18
l=[45,78]
l[0],l[len(l)-1]=l[len(l)-1],l[0]
print(l)

#q19
l=[34,67,12,98,23]
count=0
for i in l:
    count+=1
    
print("Length of list :",count)

#q20
l=[65,73]
maxor=l[0]
for i in range(0,len(l)):
    if l[i]>maxor:
        maxor=l
        
print("Maximum =",maxor)

#q21
l=[65,73]
print(min(l))

#STRING
#q22
string=input("Enter a string :")
rev=string[::-1]

if string==rev:
    print("It is palindrome")
else:
    print("It is not a palindrome")

#q23
string="You must defeat me, John Romero"
new=''
for i in string.split():
    new+=i[::-1]+' '
    
print(new)

#q26
string=input("Enter a string :")

for i in string.split():
    if len(i)%2==0:
        print(i)

#TUPLE 
#q27
t=(23,76,24,'hello',13)
ln=0
for i in t:
    ln+=1
print("Length of string =",ln)

#q29
t=(6,7,44,3,1,25,86)
s=0
for i in t:
    s+=i
print("Sum of elements in tuple :",s)

#q31
l=[4,5,6]
nl=[]
for i in l:
    nl.append((i,i**3))
print(nl)

#DICTIONARY
#q32
d={5:'Orange',1:'Apple',3:'Banana',2:'Grapes'}
d=dict(sorted(d.items()))
print(d)

#q34
d={'A':56,'B':12,'C':4,'D':67}
summ=0
for i in d.items():
    summ+=i
print(summ)

#SET
#q39
s={'5','6','8','Job','Course'}
print(s)
e=input("Enter element to remove :")
s.remove(e)
print(s)

#q40
s1={23,43,12,56,75}
s2={36,75,21,43,66}
res=s1.intersection(s2)
if len(res)>=1:
    print("Two lists have atleast one common element")
else:
    print("No elements in common")

#MATRIX
#q42
l1=[[1,2,3],[4,5,6],[7,8,9]]
l2=[[9,8,7],[6,5,4],[3,2,1]]
l3=[[0,0,0],[0,0,0],[0,0,0]]
l4=[[0,0,0],[0,0,0],[0,0,0]]
for i in range(0,3):
    for j in range(0,3):
        l3[i][j]=l1[i][j]+l2[i][j]
        
for i in range(0,3):
    for j in range(0,3):
        l4[i][j]=l1[i][j]-l2[i][j]

for i in range(0,3):
    print(l3[i])
print('\n')
for i in range(0,3):
    print(l4[i])

#q43
import itertools as it
l=[1, 3, 5, 1, 3, 2, 5, 4, 2]
l2=[]
res=[list(val) for key, val in it.groupby(sorted(l))] 
print(res)

#FUNCTIONS
#q48
def power(num,expo):
    if expo==0:
        return 1
    else:
        return num*power(num,expo-1)
    
n=int(input("Enter a number :"))
p=int(input("Enter its power :"))
print(power(n,p))

#q50
def fn(**x):
    print(x)
    
fn(a='arg1',b='arg2')