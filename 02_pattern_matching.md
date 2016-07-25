### Pattern Matching

#### Introduction
- `=` is called a match operator. In the case of `a = 1`, left-hand side is a
variable and the right-hand side is an integer literal. Elixir can make the
match `true` by binding the variable `a` to value `1`.

- A pattern(left side) is `matched` if the values(right side) have the same
structure and if each term in the pattern can be matched to the corresponding
term in the values.

#### Ignoring values
- You can ignore a value when matching with `_`.
```
[1, _, _] = [1, "cats", "dogs"]
```
- It will match as long as the first value is `1`.

#### Variables bind once (per match)
- In a match process, once the variable is bind to a value, you cannot point
to it again.
```
[a,a] = [1,2]
```
will give a match error.


