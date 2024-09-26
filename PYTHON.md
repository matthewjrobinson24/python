Day1
ssh Command

This command will login to our Linops as student: ssh student@10.x.x.x -X
For Loop

This is a for loop example "Print each fruit in a list"

fruits = ["apple", "banana", "cherry"]
for x in fruits:
  print(x)

Set up Vim

vim $HOME/.vimrc:

syntax enable
set tabstop=4
set shiftwidth=4
set expandtab
set number
filetype indent on
set autoindent

URL for Handbook

This is the URL: https://git.cybbh.space/programming/python/public.git
Split

>>> 'user:passwd'.split(':')
['user', 'passwd']

Join

>>> ''.join(l)
'jello'
>>> '.'.join(l)
'j.e.l.l.o'
>>> '::'.join(l)  # The separator can be multiple characters
'j::e::l::l::o'

String Manipulation .format()

Examples of this are:

>>> 'Hello. My name is {}.'.format('Albert')
'Hello. My name is Albert.'

and

>>> a = 'Albert'
>>> b = 'today'
>>> 'Hello {}. How are you {}?'.format(a,b)
'Hello Albert. How are you today?'

Activity 'Email Splitting'
Instructions: Given an email address of the form name@somewhere.com, create a list consisting of the 3 portions (i.e. ['name','somewhere','com']).

Example1:

email = 'name@domain.com'
part1 = email.split('@')
part2 = '.'.join(part1)
part3 = part2.split('.')
print(part3)

Example2:

email = 'name@domain.com'
a = email.split('@')
a = a[0]
b = email.split('@')
b = b[1]
b = b.split('.')
email_list = [a, b[0], b[1]]
print(email_list)

Day 2
For Loop with Incorporated if Statement

def count_sheeps(array_of_sheep):
  count = 0
  for sheep in array_of_sheep:
      if sheep:
          count += 1 
  return count

Append
You are adding a name to the pre-established list.

>>> fellowship = []
>>> fellowship.append('Frodo')
>>> fellowship.append('Sam')
>>> fellowship.append('Pip')
>>> fellowship.append('Marry')
>>> fellowship
['Frodo', 'Sam', 'Pip', 'Marry']

Input
You are asking the user for an input.

Examples of this Include:

>>> input('Please type something:')
Please type something:Xavier
'Xavier'

and

>>> var = int(input('Type something:\n'))
Type something:
1

For Loop Iteration

Syntax:

for item in <iterable>:
  <code block>

Example:

>>> for hobbit in fellowship:
...     print(hobbit + ' is in the fellowship')
Frodo is in the fellowship
Sam is in the fellowship
Pip is in the fellowship
Marry is in the fellowship

Branching Statements

Syntax:

if <condition>:
    <indented code block>
elif <condition>:
    <indented code block>
elif <condition>:
    <indented code block>
else:
    <indented code block>

Example:

fellowship = ['Frodo', 'Sam', 'Pip', 'Marry']

for hobbit in fellowship:
    if hobbit == 'Sam':
        print(hobbit + ' is wise')
    elif hobbit == 'Pip':
        print(hobbit + ' is a Took')
    else:
        print(hobbit + ' is a hobbitess')

Output of code listed above:

Frodo is a hobbitess
Sam is wise
Pip is a Took
Marry is a hobbitess

While Loops

Syntax:

while <condition>:
  <code block>

Example of a loop that never executes:

while False:
  print('This code never executes')

Example of an infinite loop:

while True:
  print('This will print over and over and never terminate')

Example of using a control variable:

a = 0
while a <=5:
  print(a)
  a += 1

Output:

0
1
2
3
4
5

Break, Pass, and Continue

To end the current iteration and begin the next, use the CONTINUE statement. To end a loop early, issue the BREAK command to exit the loop. The PASS keyword is used to provide a statement when required syntactically. It does nothing.

while True:
    usr = input('Type pass, break, or continue:\n')
    if usr == 'pass':
        pass 
        print('This is pass')
    elif usr == 'break':
        break
        print('This is break')
    elif usr == 'continue':
        continue
        print('This is continue')
    else:
        print('Please choose a valid option\n')

Activity 'Fizzbuzz'
Instructions: Modify deliverable.py so that it takes a number from the user and prints it (the number) if it isn’t divisible by 3 or 5. For multiples of 3 print 'fizz' instead. For multiples of 5 print 'buzz' instead. For multiples of 3 and 5 print 'fizzbuzz'. (note: divisiblie or multiples use %).

Example:

#!/usr/bin/env python3
x = int(input('Input Number:\n'))
if x  %3 == 0 and x %5 == 0:
    print('fizzbuzz')
elif x %3 == 0:
    print('fizz')
elif x %5 == 0:
    print('buzz')
else:
    print(x)

Day 3
ord() and chr()
ord() returns the number associated with the ASCII character. chr() returns the character representation of the numeric argument.

Example of use:

>>> ord('a')
97
>>> ord('z')
122
>>> ord('A')
65
>>> ord('Z')
90
>>> chr(97)
'a'
>>> chr(122)
'z'
>>> chr(65)
'A'
>>> chr(90)
'Z'

range()
range() produces a sequence from start inclusive to stop exclusive, incrementing by step.

>>> range(10)
range(0, 10)
>>> list(range(10))
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
>>> list(range(5,10))
[5, 6, 7, 8, 9]
>>> list(range(5,11,2))
[5, 7, 9]
>>> for num in range(2,11,2):
...     print(num)
... 
2
4
6
8
10
>>> list(range(2,11,2))
[2, 4, 6, 8, 10]
>>> [start,stop(and go back 1),step]

len()
len() returns the length of the argument.

Example1

>>> len(list(range(2,11,2)))
5

Example2

>>> fellowship
['Frodo', 'Sam', 'Pip', 'Marry']
>>> range(len(fellowship))
range(0, 4)
>>> list(range(len(fellowship)))
[0, 1, 2, 3]
>>> for hobbit in range(len(fellowship)):
...     print(fellowship[hobbit])
... 
Frodo
Sam
Pip
Marry
>>> list(range(len(fellowship)))
[0, 1, 2, 3]

Sliceing
sequence[start:stop:step]

Example1

>>> lst = list(range(0,11,1))
>>> lst
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
>>> lst[0]
0
>>> lst[-1]
10
>>> lst[0:2]
[0, 1]
>>> lst[2:4]
[2, 3]
>>> lst[0:6:2]
[0, 2, 4]
>>> lst[:6:2]
[0, 2, 4]
>>> lst[::2]
[0, 2, 4, 6, 8, 10]

To copy all except the last item from a sequence, use -1 as the end. This works to exclude any number of items from the end of a sequence.

>>> lst[:-1]
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

Slicing can also be used to create a reversed copy of a sequence. Change the step to -1 and leave the start and stop as their defaults.

>>> lst[::-1]
[10, 9, 8, 7, 6, 5, 4, 3, 2, 1, 0]

Activity 'Practical exercise 0-3'
Instructions: Modify deliverable.py and implement guess_number so that it repeatedly asks the user for a number between 0 and 100 inclusive. If the user correctly guesses the value of the given argument n, print "WIN" and exit out of the loop. Otherwise indicate whether the guess was "too high" or "too low". Test the deliverable manually or run python3 check.py to run the supplied unit tests.

#!/usr/bin/env python3

def guess_number(n):
    x = True
    while x == True:
        i = int(input('input a number between 0 and 100:\n'))
        if i > n:
            print('too high')
        elif i < n:
            print('too low')
        elif i == n:
            print('WIN')
            break

guess_number(23)

Dictionaries
There are two types of items in a dictionary, keys and values. Keys are used as an identifier to store a value and is also used to retrieve a value. Keys must be hashable, meaning they are required to be immutable. Values are the other item in a dictionary. Values are allowed to be mutable or immutable and are retrieved from the dictionary using the key that was associated with the value when storing the value. Keys must be unique but values can be duplicated.

Example1

>>> romanNumerals = {'I':1, 'V':5, 'X':10, 'L':50} #sets keys and values for dictionary
>>> romanNumerals
{'I': 1, 'V': 5, 'X': 10, 'L': 50}
>>> romanNumerals['I'] #access value by inputting the key
1
>>> romanNumerals['V']
5
>>> romanNumerals['I'] + 5
6
>>> romanNumerals['C'] = 100 #adding keys and values
>>> romanNumerals['D'] = 500
>>> romanNumerals['M'] = 1000
>>> romanNumerals
{'I': 1, 'V': 5, 'X': 10, 'L': 50, 'C': 100, 'D': 500, 'M': 1000}
>>> romanNumerals['C']
100
>>> romanNumerals['D']
500
>>> romanNumerals['M']
1000
>>> del romanNumerals['C'] #deleting a key
>>> romanNumerals
{'I': 1, 'V': 5, 'X': 10, 'L': 50, 'D': 500, 'M': 1000}

Example2

>>> for key in romanNumerals:
...     print('{} = {}'.format(key, romanNumerals[key]))
... 
I = 1
V = 5
X = 10
L = 50
D = 500
M = 1000

Example3

>>> order = [('LotR',4),('Poke',1)]
>>> for i in order:
...     print(i)
... 
('LotR', 4)  
('Poke', 1)
>>> order
[('LotR', 4), ('Poke', 1)]
>>> order[0]  #references first index position in order
('LotR', 4)
>>> order[0][1]  #references first element position in the first index
4
>>> order[0][1]*inventory[order[0][0]]  #multiplies value set for 'LotR' by 4
240.0
>>> order[0][0]
'LotR'

Example4

inventory = {'LotR':60.0, 'Poke':61, 'Step Bros':19}
order = [('LotR',4),('Poke',1)]
total = 0
for i in order:
    total += (inventory[i[0]]*i[1])
print(total) 

Output

301.0

arg

Example1

def myFun(*args):
    total = 0
    for num in args:
        print(num)
        total += num 
    print(total)
    
    

myFun(1,2,3,4,5)

Output

1
2
3
4
5
15

File IO
Opening Files

Example1

with open("test.txt") as fp:
    pass

Different Parameters for Opening:

'r' Read (default)
'w' Write
'a' Write, append to the end
'x' Creation only (Fails if file exists)
'r+' Read and write
't' Text mode (default)
'b' Binary mode

Writing Files and Reading Files

Example1

with open('test.txt', 'w') as fp:
    fp.write('First line\n')   #writes the contents of string to the file
    lines = ['Second line\n', 'Third line\n', 'Fourth line\n', 'Last line\n']
    fp.writelines(lines)   #write all lines in a file including '\n' into a list

Output

11

Example2

with open('test.txt', 'r') as fp:
    fp.read()  #prints entire contents of file

Output

'First line\nSecond line\nThird line\nFourth line\nLast line\n'

Example3

with open('test.txt') as fp:
    fp.read(5) #prints first 5 characters of file

Output

'First'

Example4

with open('test.txt') as fp:
    fp.readline() #reads a line from a file

Output

'First line\n'

Example5

with open('test.txt') as fp:
    for line in fp:
        print(line, end='')

Output

First line
Second line
Third line
Fourth line
Last line

Question1: The textfile, travel_plans.txt, contains the summer travel plans for someone with some commentary. Find the total number of characters in the file and save to the variable num. (Answer: 316)

num = 0
with open('travel_plans.txt') as fp:
        num = len(fp.read())

Question2: We have provided a file called emotion_words.txt that contains lines of words that describe emotions. Find the total number of words in the file and assign this value to the variable num_words. (Answer: 48)

with open('emotion_words.txt') as fp:
    num_words = len(fp.read().split())

Question4: Assign the first 30 characters of school_prompt.txt as a string to the variable beginning_chars. (Answer: first 30 characters)

with open('school_prompt.txt') as fp:
    beginning_chars = fp.read(30)

*Challenge: Using the file school_prompt.txt, assign the third word of every line to a list called three.

with open("school_prompt.txt") as fp:
    three = []
    for line in fp:
        b = line.split()
        three.append(b[2])

*Challenge: Create a list called emotions that contains the first word of every line in emotion_words.txt.

with open("emotion_words.txt") as fp:
    emotions = []
    for line in fp:
        b = line.split()
        emotions.append(b[0])

*Challenge: Challenge: Using the file school_prompt.txt, if the character ‘p’ is in a word, then add the word to a list called p_words.

p_words = []
with open("school_prompt.txt") as fp:
    for line in fp:
        for word in line.split():
            if 'p' in word:
                p_words.append(word)

.upper() and .lower()

captilizes and lowercases characters in a string
_________________________________________________________________________________________________________________________
# Python Practice:

## Q1

Given the floatstr, which is a comma separated string of floats, return a list with each of the floats in the argument as elements in the list.
```
lst = []
for i in floatstr.split(','):
    lst.append(float(i))
return lst
```
_________________________________________________________________________________________________________________________
## Q2

Given the variable length argument list, return the average of all the arguments as a float.
```
type(args)
    sum = 0 
    for addend in args:
        sum += addend
        avg = sum / float(len(args))
    return avg 
```
_________________________________________________________________________________________________________________________
## Q3

Given a list (lst) and a number of items (n), return a new list containing the last n entries in lst.
```
lst1 = []
    for i in lst[-n:]:
        lst1.append(int(i))
    return lst1
```
_________________________________________________________________________________________________________________________
## Q4

Given an input string, return a list containing the ordinal numbers of each character in the string in the order found in the input string.
```
  lst = []
    for i in strng:
        lst.append(ord(i))
    return lst 
```
_________________________________________________________________________________________________________________________
## Q5

Given an input string, return a tuple with each element in the tuple containing a single word from the input string in order.
```
 arr = []
    arr = strng.split(' ')
    t = tuple(arr)
    return t
```
_________________________________________________________________________________________________________________________
## Q6

Given a dictionary (catalog) whose keys are product names and values are product prices per unit and a list of tuples (order) of product names and quantities, compute and return the total value of the order.
```
 total = 0
    for i in order:
        total += catalog[i[0]]*i[1]
    return total
```
_________________________________________________________________________________________________________________________
## Q7

Given a filename, open the file and return the length of the first line in the file excluding the line terminator.
```
 with open(filename, 'r') as fp:
        i = fp.readline()
        return(len(i)) -1
```
_________________________________________________________________________________________________________________________
## Q8

Given a filename and a list, write each entry from the list to the file on separate lines until a case-insensitive entry of "stop" is found in the list. If "stop" is not found in the list, write the entire list to the file on separate lines.
```
with open(filename, 'w') as fp:
        for word in lst:
            if word.lower() == 'stop':
                break
            else:
                fp.write('{}\n'.format(word))
```
_________________________________________________________________________________________________________________________
## Q9

Given the military time in the argument miltime, return a string containing the greeting of the day. 0300-1159 "Good Morning" 1200-1559 "Good Afternoon" 1600-2059 "Good Evening" 2100-0259 "Good Night"
```
 if miltime >= 300 and miltime <= 1159:
        return "Good Morning"
 elif miltime >= 1200 and miltime <= 1559:
        return "Good Afternoon"
 elif miltime >= 1600 and miltime <= 2059:
        return "Good Evening"
 elif miltime >= 2100 and miltime <= 259:
        return "Good Night"
```
_________________________________________________________________________________________________________________________
## Q10:

Given the argument numlist as a list of numbers, return True if all numbers in the list are NOT negative. If any numbers in the list are negative, return False.
```
 for i in numlist:
        if i < 0:
            return False
 return True    
 ```
_________________________________________________________________________________________________________________________
# Python Practice 2:
```
def q1(radius):
    # Given the radius of a sphere, calculate and return 
    # its surface area. Surface area is given by the following:
    # A = 4*PI*(r**2) where PI is the constant 3.14159 and r
    # is the radius of the sphere.

    return 4*3.14159*(radius**2)

    pass
```
_________________________________________________________________________________________________________________________
```
def q2(addr):
    # Given an IPv4 address as a string in dotted decimal notation,
    # return True if the address is multicast, otherwise return False.
    # IPv4 multicast addresses are those in the range 224.0.0.0 to
    # 239.255.255.255.
    # ipaddress.IPv4Address has been disabled for this function.
    counter = 0
    arr = addr.split('.')
    if int(arr[0]) >= 224 and int(arr[0]) <= 239:
        return True
    else:
        return False
    if counter == 1:
        return True


    #pass
```
_________________________________________________________________________________________________________________________
```
def q3():
    # Return the well-known ports as a list of integers.
    # Ports 0 through 1023 are considered well-known.

    arr = []
    for x in range(1024):
        arr.append(x)
    return arr

    pass
```
_________________________________________________________________________________________________________________________
```
def q4(number):
    # Given a string for a number spelled out as a word,
    # return the number as an integer. The number will
    # only be 'zero','one','two','three', or 'four'.

    if number == 'zero':
        return 0
    elif number == 'one':
        return 1
    elif number == 'two':
        return 2
    elif number == 'three':
        return 3
    elif number == 'four':
        return 4


    pass
```
_________________________________________________________________________________________________________________________
```
def q5():
    # Read a string from the user and return the integer conversion of it.
    # Ensure the conversion is successful by removing any non-numeric characters.
    # You may assume that the input will contain at least 1 numeric character.
    bruh = ''
    arr = ['0','1','2','3','4','5','6','7','8','9']
    a = input()
    for x in list(a):
        if x in arr:
            bruh += x
        else:
            continue
    return int(bruh)


    pass
```
_________________________________________________________________________________________________________________________
```
def q6(first,middle,last,domain):
    # Given a name and domain, print to the screen their email address.
    # The address should take the form: 
    # <first>.<middle initial>.<last>@<domain>.com
    # Only include a middle initial (the first letter of the middle name).
    # Ensure the address is all lowercase.
    # Append '.com' to the given domain.
    
    print(f'{first.lower()}.{middle[0]}.{last.lower()}@{domain}.com')


    pass
```
_________________________________________________________________________________________________________________________
```
def q7(infile,outfile):
    # Copy the contents of the file whose filename is given in 
    # infile to the file whose name is given in outfile. Overwrite
    # outfile if it already exists.
    # shutil.copyfile, copy, and copy2 have been disabled for this function.
    with open(infile, 'r+') as fp, open(outfile, 'w') as out:
        out.write(fp.read())
            

    pass
```
_________________________________________________________________________________________________________________________
```
def q8(address):
    # Given an email address of the form:
    # <first>.<middle initial>.<last>@<domain>.com
    # return the 4 elements of the address as a tuple in the order
    # that they appear in the address.
    # For example, if given 'nicholas.r.yost@somedomain.com,
    # ('nicholas','r','yost','somedomain') should be returned.

    
    return tuple((address.replace('.com','')).replace('@','.').split('.'))

    pass
```
_________________________________________________________________________________________________________________________
```
def q9(strng):
    # Given a string, return a dictionary whose keys are the set of
    # unique characters within the string and whose values are the
    # count of occurances of each character.
    # For example, if given 'hello', the returned dictionary should be
    # { 'l':2, 'h':1, 'e':1, 'o':1 }
    # collections.Counter has been disabled for this function.
    count = 0
    dict = {}
    for x in list(strng):
        dict[x] = strng.count(x)
    return dict
    
    pass    
```
_________________________________________________________________________________________________________________________
```
def q10():
    # Return your last name as a string. Use all lowercase letters.
    pass

    return 'hunt'

if __name__ == '__main__':
    pass
```
