Intro to R - Module 3
========================================================

The simplest and most common data structure in R is the vector. 

---

Vectors come in two different flavors: atomic vectors and lists. An atomic vector contains exactly one data type, whereas a list may contain multiple data types. We'll explore atomic vectors further before we get to lists.

---

In the last lesson, we dealt entirely with numeric vectors, which are one type of atomic vector. Other types of atomic vectors include logical, character, integer, and complex.

---

Logical vectors can contain the values `TRUE`, `FALSE`, and `NA` (for "not available"). These values are generated as the result of "conditions". Let's experiment with some simple conditions.

---

First, create a numeric vector `num_vect` that contains the values 0.5, 55, -10, and 6.


```r
num_vect <- c(0.5, 55, -10, 6)
```


---

Now, create a variable called `tf` that gets the result of `num_vect < 1`, which is read as "num_vect is less than 1".


```r
tf <- num_vect < 1
```


---

What do you think `tf` will look like?

1. a vector of 4 logical values
2. a single logical value

---

Print the contents of `tf` now.


```r
tf
```

```
## [1]  TRUE FALSE  TRUE FALSE
```


---

The statement `num_vect < 1` is called a "condition" and `tf` tells us whether each corresponding element of our numeric vector `num_vect` satisfies this condition.

---

The first element of `num_vect` is 0.5, which is less than 1 and therefore the statement 0.5 < 1 is `TRUE`. The second element of `num_vect` is 55, which is greater than 1, so the statement 55 < 1 is `FALSE`. The same logic applies for the third and forth elements.

---

Let's try another. Type `num_vect >= 10` without assigning the result to a new variable.


```r
num_vect >= 6
```

```
## [1] FALSE  TRUE FALSE  TRUE
```


---

This time, we are asking whether each individual element of `num_vect` is greater than OR equal to 6. Since only 55 and 6 are greater than or equal to 6, the second and forth elements of the result are `TRUE` and the first and third elements are `FALSE`.

---

The `<` and `>=` symbols in these examples are called "logical operators". Other logical operators include `>`, `<=`, `==` for exact equality, and `!=` for inequality.

---

If we have two logical expressions, `A` and `B`, we can ask whether at least one is `TRUE` with `A | B` (logical "or" a.k.a. "union") or whether they are both `TRUE` with `A & B` (logical "and" a.k.a. "intersection"). Lastly, `!A` is the negation of `A` and is `TRUE` when `A` is `FALSE` and vice versa.

---

It's a good idea to spend some time playing around with various combinations of these logical operators until you get comfortable with their use. We'll do a few examples here to get you started.

---

Try your best to predict the result of each of the following statements. You can use pencil and paper to work them out if it's helpful. If you get stuck, just guess and you've got a 50% chance of getting the right answer!

---

`(3 > 5) & (4 == 4)`

1. `TRUE`
2. `FALSE`

---

`(TRUE == TRUE) | (TRUE == FALSE)`

1. `TRUE`
2. `FALSE`

---

`((111 >= 111) | !(TRUE)) & ((4 + 1) == 5)`

1. `TRUE`
2. `FALSE`

---

Don't worry if you found these to be tricky. They're supposed to be. Working with logical statements in R takes practice, but your efforts will be rewarded in future lessons (e.g. subsetting and control structures).

---
