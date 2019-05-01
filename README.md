# Reviewing Data Types

## Learning Goals

- Define bare word
- Define reserved word
- Define data versus other words in a Ruby file
- Describe what a data type is
- Identify an `Integer`
- Identify a `Float`
- Identify Boolean Values
- Identify `String` Values
- Identify `Symbol` Values
- Name the Scalar Data Types in Ruby
- Ask IRB for the Data Type of a Value

## Introduction

Now that we've covered the basics of expressions and statements, we will review
the most common data types in Ruby. First, though, we will need to clarify a
few terms.

## Define Bare Word

In Ruby, we can add our own words to the code, known as bare words. We can store
values with bare words, as we saw in the previous lesson.

```ruby
greeting = "Hello, do you like my hat?"

greeting
#=> "Hello, do you like my hat?"
```

Ruby doesn't know these words until we have defined them. If the code above was
flipped:

```ruby
greeting
greeting = "Hello, do you like my hat?"
```

And this code was run in IRB, we would get an error. Ruby needs to know the
definition of `greeting` before it can look it up and return it.

> **ASIDE**: Bare words are also often referred to as _variables_. Ruby actually
> has multiple ways to declare variables and constants, but we will primarily use
> bare words until we get to Object-Oriented Ruby.

## Define Reserved Word

We have seen a few examples of reserved words already. `if`, `do`, `end` and
`while` are all reserved words. These are a part of the Ruby language.

## Define Data

_Constants_ (like `5` and `10`) and _values_ are also called _data_. When Ruby
looks at your expressions, if it's not a bare word or a reserved word for Ruby
it's _data_.

## Classification to Data Types

A baby spends the first 3-5 years of their life running _assignment expressions_
learning about "dogs," "boats," and "trains." They're adding "bare words" to
their vocabulary that point to things.

Eventually, after they age a bit, the children start learning more advanced
concepts like "similar" or "dissimilar" or "belonging to a group." "Sesame
Street" says it like so:

<iframe width="560" height="315" src="https://www.youtube.com/embed/rsRjQDrDnY8" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

We call the classifications that data can be sorted into "data types."

## Name the Scalar Data Types in Ruby

The five _scalar_ data types are:

- [`Integer`][integer]
- [`Float`][float]
- [`Boolean`][boolean]
- [`String`][string]
- [`Symbol`][symbol]

What does "_scalar_" mean? It means things that could be put on a _scale_. All
of the following are _scalar_ values.

## Identify an `Integer`

There's a number _scale_ for whole numbers, or [`Integer`s][integer] (-1, 0, 1, ...).
You've created several `Integer` constants in this module.

## Identify a `Float`

There's a number _scale_ for `Float`ing point numbers
(-0.0001...0....1,000,000). Create [`Float`s][float] the same way you create
`Integer`s: simply type them in.

## Identify Boolean Values

The mathematics of _expressions_ made up only of `true` and `false` was
established by George Boole, an English mathematician. In his honor, the
_scale_ of values between `true` and `false` are called "Boolean." To use
[`Boolean`s][boolean] in Ruby expressions, you just type in `true` or `false`.

If you remember from the previous lesson, we used a boolean when assigning
the `raining` bare word and then used this word in an `if..else..end` statement.

```ruby
raining = true

if raining
  puts "Bring an umbrella!"
else
  puts "Have a nice day!"
end
```

## Identify `String` Values

You create [`String`s][string] by surrounding text in `""` or `''`. We'll only use `""`
for the time being, though.

Some programming languages make a difference between a single `String` element
(called a **char** for character) and a collection of **chars** called a
`String`. Ruby does not. A `String` of one character is a `String` just like a
`String` with the US Constitution in it.

You might be OK with considering `true` and `false` as being on a scale, and
thus _scalar_; and you're probably OK with numbers like `Float`s and `Integer`s
being on a scale, and thus _scalar_; but the following might sound strange:
`String`s are also considered scalar.

Consider that each letter in a `String` is on the following _scale_:

```
["A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "O",
"P", "Q", "R", "S", "T", "U", "V", "W", "X", "Y", "Z", "a", "b", "c", "d",
"e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s",
"t", "u", "v", "w", "x", "y", "z"]
```

To "go up one" from `"aaa"` we go to `"aab"`, and then `"aac"` and so on. But
what would happen if we wanted to go "up one" from `aaz`? Well, you'd "carry"
the `z+1`, just like arithmetic, and wind up with "abA." So, in this view,
`String`s are _scalar_.

## Identify `Symbol` Values

The last data type we'll discuss is a [`Symbol`][symbol]. It's like a plain old
bare word, but with a `:` in front. It looks like `:i_am_a_symbol`. It's a
_scalar_ because of the same logic as behind a `String`.

`Symbol`s and `String`s are indeed similar, save for a critical difference:
every time you type the same symbol,

```ruby
:hi
:hi
:hi
```

...you refer to the _same_ symbol. Every time
you type the same string,

```ruby
"hi"
"hi"
"hi"
```

Ruby considers each a different string! This is subtle, and we'll revisit this
when we talk about hashes.

## Ask IRB for the Data Type of a Value

Amazingly, Ruby will tell us what kind of type a given piece of data is:

```ruby
10.class #=> Integer
10.0.class #=> Float
true.class #=> TrueClass
false.class #=> FalseClass
"A fellow of infinite jest".class #=> String
:byron_the_poodle.class #=> Symbol
```

Ruby says that `10` is an `Integer`. An `Integer` is a number without a decimal, an
Integer. Adding `.class` to the end of a _scalar value_ invokes the `class`
_method_ on the variable. We'll learn more about methods when we get to
Object-Oriented Ruby, but for now it's enough to know that you can ask data
about itself in Ruby (pretty amazing). The `class` method asks a piece of data
about what data type it has.

> **WEIRDNESS**: You might also note that instead of `Boolean`, Ruby returns
> `TrueClass` and `FalseClass`. There is a subtlety about how Ruby works, but all
> programmers know that `true` and `false` are of data type `Boolean`. Knowing
> that Ruby returns `TrueClass` to `true.class` probably would help you in a Ruby
> trivia competition, but Rubyists often talk about "Boolean" values despite the
> fact that Ruby doesn't _actually_ have a Boolean type.

## Conclusion

OK! So we've now reviewed the "types" of data in Ruby. Data is any sort of value
or constant that isn't a bare word or reserved word. We use data in our programs
to perform calculations in the case of `Integer`s and `Float`s. We've seen that
`Boolean`s are a part of `if` statements. Very frequently, we simply want to
personalize our programs and have them print human-readable sentences. For this
sort of data, we have `String`s. `Symbol`s are very similar to `String`s, with

Every piece of data has a type and we can find
out what this type is by adding `.class` to the end of the piece of data.

## Resources

- [`Integer`][integer]
- [`Float`][float]
- [`Boolean`][boolean]
- [`String`][string]
- [`Symbol`][symbol]

[integer]: https://ruby-doc.org/core-2.5.0/Integer.html
[float]: https://ruby-doc.org/core-2.5.0/Float.html
[boolean]: https://ruby-doc.org/core-2.5.0/Boolean.html
[string]: https://ruby-doc.org/core-2.5.0/String.html
[symbol]: https://ruby-doc.org/core-2.5.0/Symbol.html
