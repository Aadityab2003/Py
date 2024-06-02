1]

#Practical 1 Program to calculate area of triangle, rectangle, circle date:9-2-2024

def rectangle():

  l=float(input("enter length of rectangle:"))
  b=float(input("enter breadth of rectangle"))
  area=l*b
  return area

def triangle():
    b=float(input("enter breadth of triangle:"))
    h=float(input("enter height of triangle"))
    area=1/2*height*breadth;
    return area


def circle():
  r=float(input("enter radius of circle:"))
  area=3.14*r*r;
  return area


print("Enter your choice:")
ch=int(input("press 1 for rectangle\n press 2 for triangle\n press 3 for circle\n:"))

if ch==1:
  a=rectangle()
  print(a)

elif ch==2:
  a=triangle()
  print(a)

elif ch==3:
 a=circle()
 print(a)

else :
  print("invalid")


************************************************************************************************************

2]

'''a)Program to find the union of two lists
b)Program to find the intersection of two lists'''
list1=[]
list2=[]


def dispunion(list1,list2):
  list3=list1+list2
  return list3

def intersection(list1,list2):
    common_items=[]

    for item in list1:

        if item in list2 and item not in common_items:
            common_items.append(item)

    return common_items

a=int(input("enter number of elements in a  first list:"))

print("enter element:")
for i in range(0,a):
  value=int(input())
  list1.append(value)
print("list1:",list1)

b=int(input("enter number of elements in a  second list:"))

print("enter element:")
for i in range(0,b):
  value=int(input())
  list2.append(value)
print("List2:",list2)


print("union of lists:",dispunion(list1,list2))
print("intersection of lists:",intersection(list1,list2))



************************************************************************************************************
3]


#Program to remove the “i” th occurrence of the given word in a
#list where words repeat 1-3-24
a=[]
n= int(input("Enter the number of elements in list:"))
for x in range(0,n):
    element=input("Enter element" + str(x+1) + ":")
    a.append(element)
print(a)
c=[]
count=0
b=input("Enter word to remove: ")
n=int(input("Enter the occurrence to remove: "))
print("original",a)

#tqprint("updated",a)
for i in a:
    if(i==b):
        count=count+1
        if(count!=n):
            c.append(i)
    else:
        c.append(i)
if(count==0):
    print("Item not found ")
else:
    print("The number of repetitions is: ",count)
    print("Updated list is: ",c)










*********************************************************************************************************************
4]

#a) Program to count the occurrences of each word in a given
#string sentence,

str="This is a test string with some words this is THE string with words worf"
w=str.lower().split()

w_count={}

for word in w:
  if word in w_count:
    w_count[word]+=1
  else:
    w_count[word]=1


print("Word counts")
for word, count in w_count.items():
  print(word, ":",count )



#b)Program to check if a substring is present in a given string date 12-4-24

def checksubstr(str,substr):
  if substr in str :
    print(f" {substr} :is substring present in string")
  else:
    print(f"{substr}: is not present in string")

str=input("Enter str:")
print(str)
substr=input("enter substr:")
print(substr)

checksubstr(str,substr)

*********************************************************************************************************

5]
#a)Program to map two lists into a dictionary


def createlist():
  a=[]
  b=[]
  n=int(input("Enter the total number of elements in list:"))
  for x in range(0,n):
    c=int(input("enter key"))
    d=int(input("enter value"))
    a.append(c)
    b.append(d)
    print("List of keys :",a)
    print("List of values:",b)

    e=dict(zip(a,b))
    print("Mapped function:",e)
print(createlist())


#b) Program to count the frequency of words appearing in a
#string using a dictionary. date 5-4-24
d={}
str=input("Enter input:")
print(str)
l=str.lower().split()
print(l)

for word in l:
  if word in d:
    d[word]+=1
  else:
    d[word]=1

print(d)
**************************************************************************************************************

6]
#Program to create a dictionary with key as first character and
#value as words starting with that character. date 12-4-24


a={}
str=input("Enter input:")
print(str)
b=str.lower().split()
print(b)

for word in b:
  if(word[0] not in a.keys()):
    a[word[0]]=[]
    a[word[0]].append(word)
  else:
    if(word not in a[word[0]]):
      a[word[0]].append(word)

for key,value in a.items():
        print(key,":",value)
        
***************************************************************************************************************

7]

#Program to find the length of a list using recursion
#23-2-24

def list_length(l):
  if not l:
    return 0

  else:
    return 1+ list_length(l[1:])


l=[1,2,3,4,5,6,'a']

list_length(l)


***********************************************************************************************************************

8]

#compute the diameter, circumference, and volume of a sphere using class

class Sphere:

  def __init__(self,radius):
    self.radius=radius

  def diameter(self):
    self.dia=2*self.radius
    return self.dia

  def circum(self):
    self.cir=2*3.14*self.radius
    return self.cir

  def volume(self):
    self.vol=(4/3)*3.14*self.radius**3
    return self.vol

  def show(self):
    print(f"diameter of sphere: {ob1.diameter()}")
    print(f"circumference of sphere: {ob1.circum()}")
    print(f"volume of sphere: {ob1.volume()}")

radius=int(input("enter the radius:"))
ob1=Sphere(radius)
ob1.show()


******************************************************************************************************************

9]
Program to read a file and capitalize the first letter of every word in a file.

'''file=open("viva.txt",'w')
print(file)
file.write("Hiii,\n welcome to python programming lab")
file.close()

file=open("viva.txt",'r')
content=file.read(2)
content=file.readline()
content=file.readlines()
print(content)
file.close()'''

f=input("enter file name:")
file=open(f,'a+')
print("what operation you want to perform:")

ch=int(input("press 1.write \n press 2.read \n press 3.capitalize"))

if(ch==1):
        data=input("enter data that you want to store:")
        file.write(data)
        
elif(ch==2):
        file.seek(0)
        content=file.read()
        print(content)
       
       
       
elif(ch==3:
        file.seek(0)
        content=file.read()
        d=content.title()
        print(d)
        #for i in file:
            #print(i)
            
else:
     exit()


print(file.mode)
print(file.name)
print(file.closed)


file.close()        
   
      
        
       

*****************************************************************************************************************************

10]

Program to connect with databases using SQLite and perform add,delete,update,and retrive.

import mysql.connector
try:
    conn=mysql.connector.connect(
        host="localhost",
        user="root",
        password="root",
        database="mysql"
        )
    cursor=conn.cursor()
     #Create table
    employee_create = """CREATE TABLE empolyee100(
       empid INT,
       empname VARCHAR(45) NULL,
       department VARCHAR(45) NULL,
       salary INT NULL,
       PRIMARY KEY (empid))"""

    #cursor.execute(employee_create)
    sql_insert = """INSERT INTO empolyee100(empid,empname,department,salary)VALUES (%s, %s, %s, %s)"""
    val = ("1","pallavi", "Comp", "1000000")
    data1 = [("2","pallavi","Comp","1000000"),("3","Jayashri","Mech","2000000")]
    cursor.execute(sql_insert, val)
    cursor.executemany(sql_insert,data1)
    cs=conn.cursor()
    sql_select = """SELECT * FROM empolyee100"""

    cursor.execute(sql_select)
    employee_data = cursor.fetchall()
    for e in employee_data:
        print(e)
    print(cursor)
    update="""UPDATE employee100
           SET
           empname="abhi",salary="8000"
           WHERE empid=1"""
   
    cursor.execute(update)
    sql_select = """SELECT * FROM empolyee100"""
    cursor.execute(sql_select)
    employee_data = cursor.fetchall()
    for e in employee_data:
        print(e)
    conn.commit()
    conn.close()
    print("connect",conn)

   
 

except Exception as ex:
    print(ex)
    
    
    
***************************************************************************************************



