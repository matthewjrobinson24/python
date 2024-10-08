```
.append()                  #appends on dlist.append('!')
.join()                    #join '*'.join(dlist)
.split()                   #splits on specified .split(':')
range                      #list(range(0,10,1)) start/stop/step or just range(10)
len                        #len(variable) gives the length of the values inside the variable
slicing                    #variable[0::] also start/stop/step
```
____________________________________________________________________________________________________________________________________________________________________
```
list                       #mutable
tuple                      #immutable
lst = []                   #blank list
tup = ()                   #blank tuple
```
  ```
  1 lst = []
  2 a = email.split('@')
  3 b = a[1].split('.')
  4 
  5 lst.append(a[0])
  6 lst.append(b[0])
  7 lst.append(b[1])
  8 print(lst)
  ```
____________________________________________________________________________________________________________________________________________________________________ 
```
  1 email = 'name@domain.com'
  2 '''
  3 a = email.split('@')
  4 b = '.'.join(a)
  5 c = b.split('.')
  6 print(c)
  7 '''
  8 print(('.'.join(email.split('@'))).split('.'))
```
```    
>>> email
'name@domain.com'
>>> a = email.split('@')
>>> email
'name@domain.com'
>>> a
['name', 'domain.com']
>>> b = '.'.join(a)
>>> b
'name.domain.com'
>>> c = b.split('.')
>>> c
['name', 'domain', 'com']
>>>
```
__________________________________________________________________________________________________________________________________________________________________
```
input()                            #takes user input
```
  ```
 1 usr = input('Type something:\n')
 2 print(type(usr))

 1 usr = input('Pick a team:\n')
 2 if usr == 'Cowboys' or 'Chiefs':
 3     print('The {} suck'.format(usr))
 4 elif usr == 'Broncos':
 5     print('Go Bo')
 6 else:
 7     print('Pick a different team!')
  ```
  ```
 1 num = int(input('Type a positive number:\n'))
 2 if num >= 0 and num <= 10:
 3     print('{} is between 0 and 10'.format(num))
 4 elif num > 10:
 5     print('{} is greater than 10'.format(num))
 6 else:
 7     print('Type a positive number please!')
  ```
__________________________________________________________________________________________________________________________________________________________________________
```
  1 #!/usr/bin/env python3
  2 #Modify deliverable.py so that it takes a number from the user and prints it
    #(the number) if it isn’t divisible by 3 or 5. For multiples of 3 print 'fizz' instead. 
    #For multiples of 5 print 'buzz' instead. For multiples of 3 and 5 print 'fizzbuzz'.
  3 def fizzbuzz(): 
  4   num = int(input('Type a positive number:\n'))
  5   if num % 5 == 0 and num % 3 == 0:
  6       print('fizzbuzz')
  7   elif num % 3 == 0:
  8       print('fizz')
  9   elif num % 5 == 0:
 10       print('buzz') 
 11   else:
 12       print(num)
 13 fizzbuzz()
```
__________________________________________________________________________________________________________________________________________________________________________
```  
  1  def test():
  2  while True:
  3    user = input("Type 'Pass', 'Break', 'Continue', or 'Return':\n").lower()
  4    if user == 'pass':
  5      pass
  6      print('This is pass.')
  7    elif user == 'break':
  8      break
  9      print('This is break.')
 10    elif user == 'return':
 11      break
 12      print('This is return.')
 13    else:
 14      print('Please choose a valid option.')
 15  test()
```
__________________________________________________________________________________________________________________________________________________________________________
```
  1 #!/usr/bin/env python3
  2 '''
  3 Modify deliverable.py and implement guess_number,
  4 so that it repeatedly asks the user for a number between 0 and 100 inclusive.
  5 If the user correctly guesses the value of the given argument n,
  6 print "WIN" and exit out of the loop. 
  7 Otherwise indicate whether the guess was "too high" or "too low". 
  8 Test the deliverable manually,
  9 or run python3 check.py to run the supplied unit tests.
 10 ''' 
 11 
 12 def guess_number(n):
 13     while True:
 14         usr = int(input('Type a number:\n'))
 15         if usr == n:
 16             print('WIN')
 17             break
 18         elif usr < n:
 19             print('too low')
 20         elif usr > n:
 21             print('too high')
 22 guess_number(23)
```
__________________________________________________________________________________________________________________________________________________________________________
dictionary
```
  1 catalog = {'Apex':50,'COD':79.99,'MVP':154.49,'Tarkov':200}
  2 order = [('MVP',5),('Tarkov',2)]
  3 total = 0
  4 for i in order:
  5     print(catalog[i[0]] * i[1])
  6     total += catalog[i[0]] * i[1]
  7 print(total)
  8 '''
  9 print(order[0][1] * catalog['MVP'])
 10 '''
 11 '''
 12 for game in catalog:
 13     print('{}: {}'.format(game,catalog[game]))
 14 '''
```
__________________________________________________________________________________________________________________________________________________________________________
```
student@lin-ops:~$ python3
Python 3.6.9 (default, Nov 25 2022, 14:10:45) 
[GCC 8.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> a = 1
>>> print(a)
1
>>> type(a)
<class 'int'>
>>> type(1.0)
<class 'float'>
>>> type('b')
<class 'str'>
>>> b = 'b'
>>> print(b)
b
>>> type(b)
<class 'str'>
>>> a = 1
>>> b = 2
>>> a + b
3
>>> a + 1.1
2.1
>>> 'Hello' + ' ' + 'World!'
'Hello World!'
>>> 
>>> 'Hello ' * 5
'Hello Hello Hello Hello Hello '
>>> 15 / 8
1.875
>>> 15 // 8
1
>>> 15 % 8
7
>>> 15 ** 8
2562890625
>>> 12 ** 2
144
>>> 3 ** 4
81
>>> 
>>> '{} {}!'.format('Hello',' World')
'Hello  World!'
>>> '{} {}!'.format('Hello','World')
'Hello World!'
>>> 
>>> c = str(7)
>>> c
'7'
>>> type(c)
<class 'str'>
>>> 
>>> tuple
>>> list('hello world')
['h', 'e', 'l', 'l', 'o', ' ', 'w', 'o', 'r', 'l', 'd']
>>> tuple('hello world')
('h', 'e', 'l', 'l', 'o', ' ', 'w', 'o', 'r', 'l', 'd')
>>> d = list('hello world')
>>> d
['h', 'e', 'l', 'l', 'o', ' ', 'w', 'o', 'r', 'l', 'd']
>>> d[0]
'h'
>>> d[1]
'e'
>>> d[2]
'l'
>>> d[3]
'l'
>>> d[4]
'o'
>>> 
>>> d[-1]
'd'
>>> d[-2]
'l'
>>> d[-3]
'r'
>>> 
>>> tuple('hello world')[0]
'h'
>>> e = tuple('hello world')
>>> e
('h', 'e', 'l', 'l', 'o', ' ', 'w', 'o', 'r', 'l', 'd')
>>> 
>>> d
['h', 'e', 'l', 'l', 'o', ' ', 'w', 'o', 'r', 'l', 'd']
>>> e
('h', 'e', 'l', 'l', 'o', ' ', 'w', 'o', 'r', 'l', 'd')
>>> dlist = d
>>> etuple = e
>>> dlist
['h', 'e', 'l', 'l', 'o', ' ', 'w', 'o', 'r', 'l', 'd']
>>> etuple
('h', 'e', 'l', 'l', 'o', ' ', 'w', 'o', 'r', 'l', 'd')
>>> 
>>> dlist.append('!')
>>> dlist
['h', 'e', 'l', 'l', 'o', ' ', 'w', 'o', 'r', 'l', 'd', '!']
>>> etuple.append('!')
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
AttributeError: 'tuple' object has no attribute 'append'
>>> a = 'Hello World!'
>>> a
'Hello World!'
>>> a.append('a')
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
AttributeError: 'str' object has no attribute 'append'
>>> 
>>> a
'Hello World!'
>>> a += 'AHHHHHH"
  File "<stdin>", line 1
    a += 'AHHHHHH"
                 ^
SyntaxError: EOL while scanning string literal
>>> a += 'AHHHHHH'
>>> a
'Hello World!AHHHHHH'
>>> a = 'Hello World!'
>>> a
'Hello World!'
>>> 
>>> ''.join(dlist)
'hello world!'
>>> '*'.join(dlist)
'h*e*l*l*o* *w*o*r*l*d*!'
>>> '|'.join(dlist)
'h|e|l|l|o| |w|o|r|l|d|!'
>>> ''.join(dlist)
'hello world!'
>>> ' '.join(dlist)
'h e l l o   w o r l d !'
>>> a = ''.join(dlist)
>>> a = ''.join(dlist)
>>> 
>>> a
'hello world!'
>>> dlist[0] = H
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'H' is not defined
>>> dlist
['h', 'e', 'l', 'l', 'o', ' ', 'w', 'o', 'r', 'l', 'd', '!']
>>> ' '.join(dlist)
'h e l l o   w o r l d !'
>>> dlist[0] = j
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'j' is not defined
>>> dlist[0] = 'j'
>>> dlist
['j', 'e', 'l', 'l', 'o', ' ', 'w', 'o', 'r', 'l', 'd', '!']
>>> dlist[0] = 'H'
>>> dlist
['H', 'e', 'l', 'l', 'o', ' ', 'w', 'o', 'r', 'l', 'd', '!']
>>> 
>>> 
>>> email = 'name@domain.com'
>>> email
'name@domain.com'
>>> email.split()
['name@domain.com']
>>> email.split(' ')
['name@domain.com']
>>> email.split('@','.')
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'str' object cannot be interpreted as an integer
>>> email
'name@domain.com'
>>> email.split('@','.')
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'str' object cannot be interpreted as an integer
>>> 
>>> email
'name@domain.com'
>>> email.split('@','.')
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'str' object cannot be interpreted as an integer
>>> 
>>> lst
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'lst' is not defined
>>> lst = []
>>> lst
[]
>>> tup = ()
>>> tup
()
>>>
```
______________________________________________________________________________________________________________________
Challenge: Using the file school_prompt.txt, assign the third word of every line to a list called three.
```
three = []
with open('school_prompt.txt') as fp:
    for line in fp:
        three.append(line.split()[2])
```
______________________________________________________________________________________________________________________
Challenge: Create a list called emotions that contains the first word of every line in emotion_words.txt.
```
emotions = []
with open('emotion_words.txt') as fp:
    for line in fp:
        emotions.append(line.split()[0])

```
_______________________________________________________________________________________________________________________
Challenge: Using the file school_prompt.txt, if the character ‘p’ is in a word, then add the word to a list called p_words.
```
p_words = []
with open('school_prompt.txt') as fp:
    for line in fp:
        for word in line.split():
            if 'p' in word:
                p_words.append(word)
```
________________________________________________________________________________________________________________________
```
with open('text.txt') as outfile:
    with open('007.txt','w') as infile:
        for line in outifle:
            if 'Third' in line.split():
                infile.write('Third')
```
_________________________________________________________________________________________________________________________















__________________________________________________________________________________________________________________________________________________________________________
