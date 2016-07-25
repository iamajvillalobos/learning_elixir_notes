### Elixir Basics

#### Integers
- 42
- 1_000_000
- you can add underscore for formatting

#### Floats
- 50.24
- 12.45

#### Atoms
- :this_is_an_atom
- :"This is also an atom"
- name constants
- like ruby `Symbol`
- Module name is an atom
- `ModuleName` == `:ModuleName`
- `true` == `:true`
- `nil` == :nil

#### Binaries
- `<<104, 101, 108, 108, 111>>`
- `"Hello"`

#### Strings
- `"I am a string"`
- are just binaries written in `""`

#### Maps
- works like ruby `Hash`
```
person = %{
  name: "Arman Jon Villalobos",
  gender: "Male"
}
```
- you can access it in two ways:
`person.name` #=> "Arman Jon Villalobos"
`person[:gender]` #=> "Male"

