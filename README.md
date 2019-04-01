# Data Types

## Learning Goals

* Define reserved word
* Define data versus other words in a Ruby file
* Describe what a data type is
* Identify an `Integer`
* Identify a `Float`
* Identify Boolean Values
* Identify `String` Values
* Identify `Symbol` Values
* Name the Scalar Data Types in Ruby
* Ask IRB for the Data Type of a Value

## Introduction

Thus far in all the _expression_ we've learned, we've only used one type of
_constant_: numbers. To be more specific, we've only used _whole_ numbers, or
"Integers." But the world is not simply Integers, there are other things in the
world: text, truth and falsity, and numbers that lie between the whole numbers
(fractions and decimals). Let's learn about them so that we can make our
_expressions_ more exciting!

## Define Reserved Word

We haven't seen any reserved words _yet_ in Ruby, but they're the words that
make Ruby do something else besides _evaluate_ an _expession_. They look like
`def` or `if`.

## Define Data

The _constants_ or _values_ are also called _data_. When Ruby looks at your
expressions, if it's not a bare word (made by us!) or a reserved word for Ruby
it's _data_.

## Programming as Conversation: Classification to Data Types

A baby spends the fist 3-5 years of their life running _assignment expressions_
learning about "dogs," "boats," and "trains." They're adding "bare words" to
their vocabulary that point to things.

Eventually, after they age a bit, the children start learning more advanced
concepts like "similar" or "dissimilar" or "belonging to a group." "Sesame
Street" says it like so:

<iframe width="560" height="315" src="https://www.youtube.com/embed/rsRjQDrDnY8" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

We call the classifications that data can be sorted into "data types."

## Name the Scalar Data Types in Ruby

The five _scalar_ data types are:

* `Integer`
* `Float`
* `Boolean`
* `String`
* `Symbol`

What does "_scalar_" mean? It means, things that could be put on a _scale_. All
of the following are _scalar_ values.

## Identify an `Integer`

There's a number _scale_ for whole numbers, or `Integer`s (-1, 0, 1, ...).
You've created several `Integer` constants in this module.

## Identify a `Float`

There's a number _scale_ for `Float`ing point numbers
(-0.0001...0....1,000,000).  Create `Float`s the same way you create
`Integer`s: simply type them in.

## Identify Boolean Values

The mathematics of _expressions_ made up only of `true` and `false` was
established by George Boole, an English mathematician. In his honor, the
_scale_ of values between `true` and `false` are called "Boolean." To use these
in Ruby expressions, you just type in `true` or `false`

## Identify `String` Values

You create `String`s by surrounding text in `""` or `''`. We'll only use `""`
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

The last data type we'll discuss is a `Symbol`. It's like a plain old bare
word, but with a `:` in front. It looks like `:i_am_a_symbol`. It's a _scalar_
because of the same logic as behind a `String`. We don't use them much until we
start using (suspense!) non-scalar data types in Ruby (which we'll learn
later!)

So now you can go back to any _assignment expression_ and change the RHS to be
one of these new values! Try it out in IRB!

```ruby
beauty = true  # Profound! Is beauty `true`?
```

## Ask IRB for the Data Type of a Value

Amazingly, Ruby will tell us what kind of type a given piece of data is:

```ruby
10.class #=> Fixnum
10.0.class #=> Float
true.class #=> TrueClass
false.class #=> FalseClass
"A fellow of infinite jest".class #=> String
:byron_the_poodle.class #=> Symbol
```

Ruby says that `10` is a `Fixnum`. A `Fixnum` is a number without a decimal, an
Integer. Adding `.class` to the end of a _scalar value_ invokes the `class`
_method_ on the variable. We'll learn more about methods when we get to
Object-Oriented Ruby, but for now it's enough to know that you can ask data
about itself in Ruby (pretty amazing). The `class` method asks a piece of data
what data type it has.

> **WEIRDNESS**: You might also note that instead of `Boolean`, Ruby returns
`TrueClass` and `FalseClass`. There is a subtlety about how Ruby works, but all
programmers know that `true` and `false` are of data type `Boolean`. Knowing
that Ruby returns `TrueClass` to `true.class` probably would help you in a Ruby
trivia competition, but Rubyists often talk about "Boolean" values despite the
fact that Ruby doesn't _actually_ have a Boolean type.

## Conclusion

OK! So you've now discovered the "types" of data in Ruby. You should now use
IRB to try the _essential three_ expressions with these new types of data. Look
at a _constant expression_ with `String`; write an _assignment expression_ with
a variable and a `String`; lookup the content of the variable and make sure you
get your `String` back out.

Remember conversation: if you've ever known a 3-5 year old, the process we just
described is ***what they're doing all the time***. They're using the
_essential three_ expressions to expand, communicate about, and re-expand their
world!
