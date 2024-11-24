# Differences from Python
* Type must be set
* The variable name must be preceded by a `ct` (constant, unmodifiable) or `lt` (variable, modifiable) declaration.
* Private functions must be described at the time of declaration as `priv fn`.
* No need to include `:` in function or class or for, if definitions
* `print` is `out
* `self` is `this` (need not be defined as an argument)
* To use this language you need to drink mocha coffee :)
# Example
## Value
```
# const
ct text: String = "Hello"

# variable
lt text: String = "Hello"
```

## Function
```
fn greet() -> String
  return `Hello, World!`

# With assignment
fn greet(name: String) -> String
  return `Hello, ${name}!`
```

## For
```
for i in 1 to 5
    out(i)
```

## Array
```
lt fruits = ["Apple", "Banana", "Orange"]
for f in fruits
    out(f)
```

## class
```
class P
    lt n: String
    lt a: Int

    fn __init__(n: String, a: Int) -> Void
        this.n = n
        this.a = a

    fn intro() -> String
        return "I'm ${n}、${a} years old."

let p = P("Mocha", 30)
out(p.intro())

```
