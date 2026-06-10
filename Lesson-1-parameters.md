# Lesson 1

## named parameters
print(*object, sep=' ', end="n\")
"sep", "end" are called named parameters

## purpose of function `main()` 
Something different happens when we import a function from another file.
This is a python file called `hello.py`
```Python
def main():
    print(exponential(2,4))
    
def exponential(x,n = 2):
    return x ** n

main()
```
The result is 
```text
16
```
if we import exponential function into a new python file: `calculator.py`
```Python
from hello import exponential
print(exponential(3,8))
```
The result would be:
```text
16
6561
```
that shows that when we import functions from other files, that means python will first execute the top-level code of the original python file , then execute current file. 
`main()` is on the top-level. When we execute `calculator.py`, Python also runs the code `main()`
so if we want to import functions from other files, we can just add the followings in the original file to avoid that problems:
```Python
if __name__ == "__main__":
    main()
```
that means only when we execute python file is not the original one, the top-level codes will not be executed. if we change `hello.py` in this way:
```Python
def main():
    print(exponential(2,4))
    
def exponential(x,n = 2):
    return x ** n

if __name__ == "__main__":
    main()
```
the result of the command `Python calculator.py` will be:
```text
6561
```
### Summary
This function `main()` makes a certain python file usable both as a script and as a import module.
