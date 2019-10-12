## ===== PROBLEM1 =====
# Exercise 1 - Introduction - Say "Hello, World!" With Python
print("Hello, World!")

# Exercise 2 - Introduction - Python If-Else
n = int(input())
if(n%2!=0): #If n is odd, print Weird
    print("Weird")
if((n%2==0) and (n>=2) and (n<=5)): #If n is even and in the inclusive range of 2 to 5 print Not Weird
    print("Not Weird")
if((n%2==0) and (n>=6) and (n<=20)): #If n is even and in the inclusive range of 6 to 20 print Weird
    print("Weird")
if((n%2==0) and (n>20)): #If n is even and greater than 20 print Not Weird
    print("Not Weird")
    
# Exercise 3 - Introduction - Arithmetic Operators
if __name__ == '__main__':
    a = int(input())
    b = int(input())
    c=a+b
    d=a-b
    e=a*b
    print(c)
    print(d)
    print(e)
# Exercise 4 - Introduction - Python: Division
if __name__ == '__main__':
    a = int(input())
    b = int(input())
    print(a//b)
    print(a/b)
	
# Exercise 5 - Introduction - Loops
if __name__ == '__main__':
    n = int(input())
    for i in range(0,n):
        print(i*i)

# Exercise 6 - Introduction - Write a function
def is_leap(year):
    leap = False    
    if ((year%4==0) and (year%100!=0) or (year%400==0)):
        leap=True
    return leap
# Exercise 7 - Introduction - Print Function
if __name__ == '__main__':
    n = int(input())
    i=1
    for i in range(1,n+1):
        print (i,end='')
# Exercise 8 - Basic data types - List Comprehensions
if __name__ == '__main__':
    x = int(input())
    y = int(input())
    z = int(input())
    n = int(input())
    lstout = [[i, j, k] for i in range(x+1) 
        for j in range(y+1) 
            for k in range(z+1) 
                if i+j+k != n]
    print(lstout)

# Exercise 9 - Basic data types - Find the Runner-Up Score!

n = int(input())
arr = list(map(int, input().split())) #convert the map to list 
arr.sort() # sort the list
uniqueSet=list(set(arr)) # convert it to set first so that we get unique value then to list again 
setLength=len(uniqueSet) # getting the length
if setLength == 1 :
    print (uniqueSet[setLength-1])
elif setLength > 1:
    print (uniqueSet[setLength-2])
	
# Exercise 10 - Basic data types - Nested Lists
marks_list = []
students_count = int(input())
for i in range(students_count):
    marks_list.append([input(), float(input())])
marks_list = sorted(marks_list)
highest = sorted(set([mark_list for name, mark_list in marks_list]))[1]
for i in range(students_count):
        if(marks_list[i][1]==highest):
            print(marks_list[i][0])

# Exercise 11 - Basic data types - Finding the percentage
n = int(input())
student_marks = {}
for _ in range(n):
     name, *line = input().split()
     scores = list(map(float, line))
     student_marks[name] = scores
query_name = input()

total_numbers=0
for student_subject_score in student_marks[query_name]:
    total_numbers+=student_subject_score

print ("{0:.2f}".format(total_numbers/len(student_marks[query_name])))
# Exercise 12 - Basic data types - Lists
# Exercise 13 - Basic data types - Tuples
n = int(input())
t = tuple(list(map(int, input().split())))
print(hash(t))
# Exercise 14 - Strings - sWAP cASE
def swap_case(s):
    lst = []
    for character in s:
        if character.isupper():
            lst.append(character.lower())
        elif character.islower():
            lst.append(character.upper())
        else:
            lst.append(character)
    return ''.join(lst)
# Exercise 15 - Strings - String Split and Join
def split_and_join(line):
    # write your code here
    string_line = line.split(" ")
    return "-".join(string_line)
print (aresult)
# Exercise 16 - Strings - What's Your Name?
def print_full_name(a, b):
    print("Hello " + a +" "+ b + "! You just delved into python.")
	
# Exercise 17 - Strings - Mutations
def mutate_string(string, position, character):
    lst = list(string)
    lst[int(position)] = character
    lst1 = ''.join(lst)
    return (lst1)

# Exercise 18 - Strings - Find a string
def count_substring(string, sub_string):
    count=0
    
    for i in range(0, len(string)-len(sub_string)+1): #start from the end
        if string[i] == sub_string[0]: #check that sub string first character matches
            match=1
            for j in range (0, len(sub_string)):
                if string[i+j] != sub_string[j]: #traverse to see that both matches
                    match=0
                    break
            if match==1:
                count += 1 #if all goes well save it.
    return count
    
# Exercise 19 - Strings - String Validators
stringfull = input()
isExist=False
for s in stringfull:
    if s.isalnum():
        isExist=True
        break
print(isExist)
isExist=False
for s in stringfull:
    if s.isalpha():
        isExist=True
        break
print(isExist)
isExist=False
for s in stringfull:
    if s.isdigit():
        isExist=True
        break
print(isExist)
isExist=False
for s in stringfull:
    if s.islower():
        isExist=True
        break
print(isExist)
isExist=False
for s in stringfull:
    if s.isupper():
        isExist=True
        break
print(isExist)

# Exercise 20 - Strings - Text Alignment

thickness = int(input()) # This must be an odd number
c = 'H'
# Top Cone
for i in range(thickness):
    print((c*i).rjust(thickness-1)+c+(c*i).ljust(thickness-1))

# Top Pillars
for i in range(thickness+1):
    print((c*thickness).center(thickness*2)+(c*thickness).center(thickness*6))

# Middle Belt
for i in range((thickness+1)//2):
    print((c*thickness*5).center(thickness*6))

# Bottom Pillars
for i in range(thickness+1):
    print((c*thickness).center(thickness*2)+(c*thickness).center(thickness*6))

# Bottom Cone
for i in range(thickness):
    print(((c*(thickness-i-1)).rjust(thickness)+c+(c*(thickness-i-1)).ljust(thickness)).rjust(thickness*6))
# Exercise 21 - Strings - Text Wrap
def wrap(string, max_width):
    count=0
    list=[]
    substring=""
    for s in string:
        count+=1
        substring+=s
        if count==max_width: 
            list.append(substring)
            count=0
            substring=""
    if len(substring)>0:
        list.append(substring)
    outputString=""
    for list_item in list:
        if list_item is not None:
            outputString+=list_item+"\n"
    return outputString
# Exercise 22 - Strings - Designer Door Mat
# Exercise 23 - Strings - String Formatting
# Exercise 24 - Strings - Alphabet Rangoli
# Exercise 25 - Strings - Capitalize!
# Exercise 26 - Strings - The Minion Game
# Exercise 27 - Strings - Merge the Tools!
# Exercise 28 - Sets - Introduction to Sets
def average(array):
    average = sum(set(array))/len(set(array))
    return average
# Exercise 29 - Sets - No Idea!
# Exercise 30 - Sets - Symmetric Difference
# Exercise 31 - Sets - Set .add()
# Exercise 32 - Sets - Set .discard(), .remove() & .pop()
# Exercise 33 - Sets - Set .union() Operation
# Exercise 34 - Sets - Set .intersection() Operation
# Exercise 35 - Sets - Set .difference() Operation
# Exercise 36 - Sets - Set .symmetric_difference() Operation
inp_i_len=int(input())
inp_i_set=set(map(int,input().split()))
inp_j_len=int(input())
inp_j_set=set(map(int,input().split()))
compare_i=inp_i_set.difference(inp_j_set)
compare_j=inp_j_set.difference(inp_i_set)

for item in sorted(set(compare_i.union(compare_j))):
    print(item)
# Exercise 37 - Sets - Set Mutations
# Exercise 38 - Sets - The Captain's Room
# Exercise 39 - Sets - Check Subset
# Exercise 40 - Sets - Check Strict Superset
# Exercise 41 - Collections - collections.Counter()
from collections import Counter
articlecount=int(input())
articlesizes=list(map(int,input().split()))
customers=int(input())
earned=0
for i in range(customers):
    article_size_price=list(map(int,input().split()))
    if article_size_price[0] in Counter(articlesizes).keys():
        earned+=article_size_price[1]
        articlesizes.remove(article_size_price[0])
print(earned)
