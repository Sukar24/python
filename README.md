
##def count_string(abc):
##    count = 0
##    for char in abc:
##        count += 1
##    return count
##print(count_string("sukatttt"))
##
##def func(file_obj):
##    str="test"
##    file_obj.write(str)
##
##def main():
##    f=open("test.txt", 'w')
##    func(f)
##    f.close()
##
##if __name__=='__main__':
##    main()


####
####l=['a','b','c','d','f']
####x=['b','d','l','o','p']
####
####for i in l:
####    if i in x:
####        x.remove(i)
####        print(i)
##
####x = [1,3,4]
####f = [1,11,22,33,44,3,4]
####
####result = set(f) - set(x) # correct elements, but not yet in sorted order
####print(sorted(result)) # sort and print
##
##
##array = [['a','b'], ['a', 'b','c'], ['d']]
##result = set(x for l in array for x in l)
##print(result)

#Write a Python program to count the number of characters (character frequency) in a string.

def num_characters(str1):                                     
    dict ={}
    for d in str1:
        keys = dict.keys()
        if d in keys:
            dict[d] += 1
        else:
            dict[d] = 1
    return dict
print(num_characters("gfjgvcjv"))
                  
        
def char_frequency(str1):
    dict = {}
    for n in str1:
        keys = dict.keys()
        if n in keys:
            dict[n] += 1
        else:
            dict[n] = 1
    return dict
print(char_frequency('google.com'))



def file_name(fname):
    count =0
    file_to_read = open("test.txt")
    print(file_to_read.read())
    print("-----------------------ok-------------------")
    for char in fname:
        count += 1
    return count

print(file_name('fname'))

##import re  
##f=open("demo.txt") or with open(filename) as f:
##while True:
##        read_characters = f.read(15)
##        if not read_characters:
##            print("end of the file")
##            break
##        print("Read characters :",read_characters)
##        findpattern =re.compile(r'sukar',read_characters)
##        regx =re.findall(findpattern,read_characters)
##        print(regx)
   


##
##def append_file(demo):
##    with open("demo.txt","w") as fc:
##        fc.write("sukar is good boy \n")
##        fc.write("ok cool")
##        txt = open("demo.txt")
##        print(txt.read())
##(append_file('test.txt'))


#3. Write aPython program to get a string made of the first 2 and the last 2 chars from a given a string. If the string length is less than 2, return instead of the empty string

def get_string(str1):
    if len(str1) <2:
        return ''
    return str1[:2]+str1[-2:]
print(get_string('sukarkk23'))


#4. Write a Python program to get a string from a given string where all occurrences of its first char have been changed to '$', except the first char itself.

def get_string(str1):
    char =str1[0]
    length =len(str1)
    str1 =str1.replace(char, '$')
    str1 = char + str1[1:]
    return str1
print (get_string("rukarisgudboy"))


#5. Write a Python program to get a single string from two given strings, separated by a space and swap the first two characters of each string.

def swap(str1,str2):
    new_str1 = str2[:2]+str1[2:]
    new_str2 = str1[:2]+str2[2:]
    return new_str1 + ' ' + new_str2
print(swap("123", "xyz"))
##
##x =raw_input("enter a string: ")
##y =raw_input("enter another string: ")
##new_x = y[:2]+x[2:]
##new_y = x[:2]+y[2:]
##swap = new_x + '  ' + new_y
##print(swap)

#6. Write a Python program to add 'ing' at the end of a given string (length should be at least 3). If the given string already ends with 'ing' then add 'ly' instead. If the string length of the given string is less than 3, leave it unchanged    

str1 = raw_input("enter the a string : ")
length =len(str1)
if length > 2:
    if str1[-3:] == 'ing' :
        str1 += 'ly'
    else:
        str1 += 'ing'
    print(str1)

#7  Write a Python program to find the first appearance of the substring 'not' and 'poor' from a given string, if 'bad' follows the 'poor', replace the whole 'not'...'poor' substring with 'good'. Return the resulting string

def apper(str1):
    sn = str1.find('not')
    sb = str1.find('poor')
    if sb > sn :
        str1 = str1.replace(str1[sn:(sb+5)], 'good')
    return str1
print(apper("lyrics are not poor"))
        
#8 Write a Python function that takes a list of words and returns the length of the longest one

def words(lists):
    word_len=[]
    for n in lists:
        word_len.append((len(n),n))
        word_len.sort()
    return word_len[-1][1]
print(words(['php','sukar','hkjhjhj']))


#9 Write a Python program to remove the nth index character from a nonempty string.
                                        
def remove_n(str1,n):
    first = str1[:n]
    last = str1[n+1:]
    return first+last
print(remove_n("sukarman",0))


#10 Write a Python program to change a given string to a new string where the first and last chars have been exchanged.

def string(str1):
    #length =len(str1)
    new_str = str1[-1:]+ str1[1:-1]+ str1[:1]
    return new_str
print(string("sukaro"))

#11 Write a Python program to remove the characters which have odd index values of a given string

def remove_char(str1):
    results =''
    for i in range(len(str1)):
        if i % 2 == 0:
            results = results + str1[i]
    return results
print (remove_char("sukara"))

l = [i for i in range(1,5) if i %2 == 0]
print(l)

#12 Write a Python program to count the occurrences of each word in a given sentence.
        
def word_count(str1):
    dicts ={}
    words = str1.split()
    for word in words:
        if word in dicts:
            dicts[word] += 1
        else:
            dicts[word] = 1
    return dicts
print (word_count ("sukar is good boy ok sukar good boy"))

#13. Write a Python script that takes input from the user and displays that input back in upper and lower case

x = raw_input("enter a string :")
new = x.upper()
print(new)
lower =x.lower()
print(lower)

#14 Write a Python program that accepts a comma separated sequence of words as input and prints the unique words in sorted form (alphanumerically).

    
x =raw_input("enter the colors")
words = [word for word in x.split(",")]
print(",".join(sorted(list(set(words)))))

#15  Write a Python function to create the HTML string with tags around the word(s)

def create_htmltags(tag,word):
    return "<%s><%s><%s>" %(tag,word,tag)
print(create_htmltags("i","python"))

#16 Write a Python function to insert a string in the middle of a string.

def insert_string(str1,word):
    return str1[:2]+ word + str1[2:]
print(insert_string("[[]]",'python'))

#17 Write a Python function to get a string made of 4 copies of the last two characters of a specified string (length must be at least 2).


def specified_string(str1):
    sub_str = str1[-2:]
    return sub_str*4
print(specified_string("python"))

#18 Write a Python function to get a string made of its first three characters of a specified string. If the length of the string is less than 3 then return the original string. 

def three_characters(str1):
    if len(str1) > 3:
       return  str1[:3]
    else:
       return str1
print(three_characters("su"))

#19 Write a Python program to get the last part of a string before a specified character.

str1 = 'http://www.w3resource.com/python-exercises/string'
print(str1.rsplit('/',1)[0])
print(str1.rsplit('-',1)[0])


#20 Write a Python function to reverses a string if it's length is a multiple of 4

def reverses(str1):
    if len(str1)*4:
     return str1[::-1]
print(reverses("sukar iiiii 0000"))

#21 Write a Python function to convert a given string to all uppercase if it contains at least 2 uppercase characters in the first 4 characters.


def converts(str1):
    def_uppercase = 0
    for letters in str1[:4]:
        if letters.upper() == letters:
            def_uppercase += 1
    if def_uppercase >= 2:
        return str1.upper()
    return str1          
print(converts("srTQspu"))
print(converts("sukaraa"))

#22 Write a Python program to sort a string lexicographically.

def lexicograph(s):
    return sorted(sorted(s),key=str.upper )
print(lexicograph("lsjgljlkjfxlkhbj"))

#23 Write a Python program to remove a newline in Python

x ="sukar kkk \n"
print(x)
print(x.rstrip())

#24 Write a Python program to check whether a string starts with specified characters.

stri = "iphone sold by eggs"
result =stri.startswith("iphone")
print(result)

#25 check a given string is palindrome or not .

##def palindrome(str1):
##    length =len(str1)
##    if str1[::-1] == str1[::]:
##         print("the given string is palindrome")
##    else:
##             print("not a p :") 
##print(palindrome("madam"))
      

while True:
    palin = raw_input("enter a string :  ")
    if palin[::-1] == palin[::]:
        print("successfully ")
        break
else:
    print("enter the a palin ")
    
    
#26 factors

x = int(raw_input("enter the number : "))
for i in range(1,x+1):
    if x%i ==0:
        print(i)

# 27 factorial python


x = int(raw_input("enter the number : " ))
facts = 1
if x < 0:
    print(" for negative number no factorials will be avalible : ")
elif x == 0:
        print(" factorial for 0 is 1 ")
else:
   for i in range (1,x+1):
      fact = facts*i
print(" factorial on x is : ",x , "is",fact )
                
# change the value for a different result
#num = 7

# uncomment to take input from the user
num = int(input("Enter a number: "))

factorial = 1

# check if the number is negative, positive or zero
if num < 0:
   print("Sorry, factorial does not exist for negative numbers")
elif num == 0:
   print("The factorial of 0 is 1")
else:
   for i in range(1,num + 1):
       factorial = factorial*i
   print("The factorial of",num,"is",factorial)
        
        
# count the highest number

dup_list = set(1)
unix_list = []
for x in dup_list:
    if x not in dup_list:
        unix_list.append(x)
        dup_list.add(x)
print(dup_items)

        
