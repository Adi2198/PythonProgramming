

# PythonProgramming

## A python program that can iterate through any type of iterable with having any value

`Code()`
```
def check_data_type(ca): # To check data type and return value
    if type(ca) == int:
        return ca
    elif type(ca) == float:
        return ca
    elif type(ca) == complex:
        return ca
    elif type(ca) == str:
        return ca
    else:               # if not float,int,complex,str the return False
        return False
        

def mydict(dic): # TO check the type of iterable
    if type(dic) == dict:
        for key,value in dic.items():
            if not check_data_type(value):
                mydict(value)
            else:
                print(check_data_type(value))
    elif type(dic) == list:
        for value in dic:
            mydict(value) # recursive checking of type 
            #print(value)
    elif type(dic) == set:
        for value in dic:
            mydict(value)
            #print(value)
    elif type(dic)== tuple:
        for value in dic:
            mydict(value)
            #print(dic)
    elif not check_data_type(dic):
        mydict(dic)
    else:
        print(check_data_type(dic))
     

```
