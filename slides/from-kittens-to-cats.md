## From Kittens<br>To Cats 😸

The theory behind `cats`

---

# Functor

----

# Monad

----

# Monoid

----

# Category theory

----

# Cats

---

# Visual tour

----

![](diagrams/010-scala.png)

----

![](diagrams/015-multi-paradigm.png)

Scala is a multi-paradigm language.

----

![](diagrams/020-scala-with-cats.png)

`cats` is a library

----

![](diagrams/030-scala-with-cats-effect.png)

`cats-effect` is another library

----

![](diagrams/025-cats-for-fp.png)

`cats` enables a more consistent experience with functional programming

----

![](diagrams/040-new-ideas.png)

`cats` introduces new concepts to Scala

----

![](diagrams/050-other-languages.png)

Category theory is not unique to Scala

----

![](diagrams/060-not-every-language.png)

Not every language can support these new ideas

---

# Math review

----

## Natural numbers
# `1 + 2 = 3`

----

## Natural numbers
- Given a `natural number`
- And given another `natural number`
- And the `addition` operation
- We can get another `natural number`

----

## Rational numbers
## `1.2 + 8.3 = 9.5`

----

## Rational numbers
- Given a `rational number`
- And given another `rational number`
- And the `addition` operation
- We can get another `rational number`

----

## Strings

```
"foo" + "bar" == "foobar"
```

----

## Strings
- Given a `String`
- And given another `String`
- And the `concatenate` operation
- We can get another `String`

----

### Natural numbers, rational numbers, and `String`s are **structured similarly**.

----

### 🤔 Can the **common structure** be factored out?

----

### **Category theory** is the study of similarly structured things.

Where things include numbers.

----

### `cats` is the application of **cat**egory theory to types in Scala

----

### `cats` provides a **consistent interface** to different types in Scala **if** they are structured similarly

Interface as in "coding experience", not literally a Java `interface`

---

## The structure

----

### Built-in types

```scala
1 + 2 == 3
"foo" + "bar" == "foobar"
```

----

### 🤔 What about a new type?

```scala
case class Frac(numerator: Int, denominator: Int)

// built-in + not defined for Frac
Frac(1, 2) + Frac(3, 4) == Frac(7, 8)
```

----

### `+` could be a normal method off of `Frac`...

```scala
case class Frac(numerator: Int, denominator: Int) {
  def `+`: Frac =
    ???
}
```

----

### But what about structural sharing with `Int` and `String`?

---

---

# Scala review

---

# The structure

---

# Recap

----

`cats` is a Scala library that enhances the **functional programming** experience by providing **consistent interfaces** to types that share similar properties by using **type classes** and **evidence**.
