# Variables
- Defines areas in memory in which values (data) are stored
- Unique identifies that retrieve values from the memory addresses at which they are stored
- The value of a variable can change during the execution of the program

# Constant
- An identifier with an associated value which cannot be altered by the program during normal execution

# Data Types + Operators
ceebs ik tthis
```run-python
print("hello")
```


# idk
### Programs that can extract and manipulate substrings
```python
phrase = "Computer Science"
print(phrase[7])
```

```python
#find first char that matches
print(phrase.find("c"))
```

```python
#find last char that matches
print(phrase.rfind("e"))
```

```python
#literally phrase[9:15], so literally substring
print(phrase[slice(9,15)])
```

```python
#replace if not in phrase, wont do anything
print(phrase.replace("Science","Programming"))
```

```python
phrase2 = "is the best"
#string concatenation
finalPhrase = phrase + " " + phrase2
print(finalPhrase)
```

```python
#split by spaces
print(finalPhrase.split())
```
