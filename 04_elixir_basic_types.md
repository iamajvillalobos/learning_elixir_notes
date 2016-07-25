### Value Types

#### Integers
- Integer literals can be written as:
  - decimal(1234)
  - hexadecimal(0xcafe)
  - octal(0o765)
  - binary(0b1010)
- can also contain underscores(1_000_000)

#### Floating-Point Numbers
- 15.0

#### Atoms
- `:this_is_an_atom`
- `:"this/is_@also_an_ atom"
- can be any sequence of letters, digits, underscores and @
- may end with exclamation(!) or question mark(?)
- atom name is it's value

#### Ranges
- represented as `start..end`
- `start` and `end` are integers

### Collection Types

#### Tuples
- ordered collection of values
- `{ 1, 2 }`, `{ :ok, 42, "next" }`, `{ :error, :enoent }`
- typical tuples has two to four elements
- use `Map` or `Struct` if you want to use more than that
- use it in pattern matching
```
{ status, count, action } = { :ok, 42, "next" }
status
:ok
count
42
action
"next"
```
- common for a function to return tuple where first element is the atom `:ok`
- common idom is to wite matches that assume success

#### Lists
- [1,2,3]
- they are not array
- basically a linked data structure
- maybe emtpy or consist or head & tail
- head = value
- tail = list(values are the rest of the list - head)
- easy to traverse linearly
- expensive to memory to access in random order(nth element)
- always cheap to get the head of a list and extract the tail of a list
```
[1,2,3] ++ [4,5,6] # concatenation
[1,2,3,4,5,6]

[1,2,3] -- [1] # difference
[2,3]

1 in [1,2,3,4] # membership
true

"sorry" in [1,3,4]
false
```

#### Keyword Lists
- shortcut to write list of key/value pairs
- elixir converts keyword list to two-value tuples
```
[ name: "AJ", age: 25, job: "programmer" ]
[ {:name, "AJ"}, {:age, 25}, {:job, "programmer"} ]
```
- also if keyword list is the last parameter in a function, you can leave off
the square brackets
```
DB.save record, [use_transaction: true, logging: "high"]
DB.save record, use_transaction: true, logging: "high"
```
- keyword lists are usually use in command-line parameters

#### Maps
- %{ "AL" => "Alabama", "WI" => "Wisconsin" }
- collection of key/value pairs
- you can use expression also
```
name = "Jose Valim"
#=> "Jose Valim"
%{ String.downcase(name) => name }
#=> %{"jose valim" => "Jose Valim" }
```
- to use as an associative array
- if keys are strings, you can access maps using `states["AL"]`
- if keys are atoms, you can access maps using `states[:al]`
