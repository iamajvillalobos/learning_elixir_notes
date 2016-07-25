### Operators

#### Comparison operators
```
a === b                 # strict equality
a !== b                 # strict inequality
a == b                  # value equality
a != b                  # value inequality
a > b                   # normal comparison
a >= b                  # :
a < b                   # :
a <= b                  # :
```

#### Boolean operators
```
a or b                  # true if a is true, otherwise b
a and b                 # false if a is false, otherwise b
not a                   # false if a is true, true otherwise
```

#### Relaxed Boolean operators
```
a || b                  # a if a is truthy, otherwise b
a && b                  # b if a is truthy, otherwise a
!a                      # false if a is truthy, otherwise true
```

#### Arithmetic operators
```
+ - * / div rem
```
- div(a,b) #=> result is an integer
- rem is like %(modulus) in other language

#### Join operators
```
binary <> binary2
string <> string2           # concatenantes two binaries/strings
list1 ++ list2              # concatenantes two lists
list1 -- list2              # returns elements in list1 not in list2
```

#### `in` operator
```
a in enum                   # check if item is in the list/map/range or any enum
```
