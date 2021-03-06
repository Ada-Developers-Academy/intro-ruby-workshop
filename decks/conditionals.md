@snap[midpoint span-100]

# Conditionals

@snapend

---

## Agenda

@snap[west span-50]

9:00  - Intro

9:20  - Hello World

9:50  - **Break**

10:00 - Variables + Strings

11:00 - **Break**

@snapend

@snap[east span-50 text-left]

11:10 - Numbers + Math

11:50 - **Break**

<span style="color: #EF654A">12:00 - Conditionals</span>

12:30 - **Done!**

@snapend

---

## Learning Goals

By the end of this module, students will be able to...

- **Use** conditionals to allow programs to behave differently for different data
- **List** the different relational operators
- **Describe** debugging techniques for complex programs
- **Define** the following terms: conditional, inequality, Boolean, branch

---

## Conditionals

Sometimes we need our program to make a choice about what to do next

- Should I run these statements or not?

- Should I run these statements or those statements?

---

## Conditionals

```ruby zoom-15
puts "Enter username:"
username = gets.chomp

if username == "alovelace"
  puts "Welcome back Ada"
end

puts "Initializing user settings..."
```

**Predict and observe:**

- What if you type `alovelace`?
- What if you type `kjohnson`?

---

## Inequalities

```ruby zoom-15
spring_sales = 15 + 22 + 17

if spring_sales > 40
  puts "What a strong quarter!"
end
```

**Predict and observe**

---

## Comparing Variables

```ruby zoom-15
spring_sales = 15 + 22 + 17
summer_sales = 35 + 16 + 27

if spring_sales < summer_sales
  puts "Summer was stronger"
end
```

**Predict and observe**

---

## if - else

```ruby zoom-15
spring_sales = 15 + 22 + 17
summer_sales = 35 + 16 + 27

if spring_sales > summer_sales
  puts "Spring was stronger"
else
  puts "Summer was stronger"
end
```

**Predict and observe**

We call each path the code can take a **branch**, as in "the if branch" and "the else branch"

---

## Relational Operators

| op   | name             | 5 vs 10 | 8 vs 8 | 10 vs 5 |
| ---- | ---------------- | ------- | ------ | ------- |
| `==` | equal            | ❌      | ✅     | ❌      |
| `!=` | not equal        | ✅      | ❌     | ✅      |
| `<`  | less than        | ✅      | ❌     | ❌      |
| `<=` | less or equal    | ✅      | ✅     | ❌      |
| `>`  | greater than     | ❌      | ❌     | ✅      |
| `>=` | greater or equal | ❌      | ✅     | ✅      |

---

## Data Types

```ruby zoom-15
result = 2 + 3
```

What is the **value** of `result`?

What is the **data type** of `result`?

---

## Data Types

```ruby zoom-15
result = 2 < 3
```

What is the **value** of `result`?

What is the **data type** of `result`?

---

## Boolean Values

Ruby includes the values `true` and `false`

<p class="small">Called **Boolean** values, after George Boole</p>
<br>
Represents the results of a **comparison**

<p class="small">Like `spring_sales < 40`</p>
<br>
Can be stored in a variable like any other value

You don't see them typed out very often, but it's good to know they're there

---

## Conditional Debugging

What if we make a mistake writing our conditional and our code goes down the wrong path?

<p class="small">No error, but bad behavior</p>
<br>
How can we get more info about what went wrong?

---

## Conditional Debugging

```ruby zoom-15
spring_sales = # complex math
sales_target = # different complex math

if spring_sales > sales_target
  # we expected the program to take
  # this branch, but it didn't!
end
```

Could be the math was wrong, we've used the wrong operator, or something else

---

## Intermediate Variable

```ruby zoom-12
spring_sales = # complex math
sales_target = # different complex math

puts "spring_sales is #{spring_sales}"
puts "sales_target is #{sales_target}"

comparison = spring_sales > sales_target
puts "comparison result is #{comparison}"
if comparison
  # ...
end
```
<br>

**_"When in doubt, print it out"_**

---

## Common Mistake

```ruby zoom-15
puts "Enter username:"
username = gets.chomp

if username = "alovelace"
  puts "Welcome back Ada"
end

puts "Initializing user settings..."
```

This program always prints `Welcome back Ada`. Why?

---

## Conditional Syntax

@snap[west span-50]
```ruby zoom-12
if value relation value
  statement
  more statements

else # optional
  statement(s)
end
```
@snapend

@snap[east span-50 text-left]
```ruby zoom-12
if spring_sales > target
  puts "Met the target!"
  party_points += 1

else
  puts "Maybe next time"
end
```
@snapend

---

## Practice Tracker

```ruby zoom-12
week1_hours = 4
# ...

total = 0
total += week1_hours
# ...
puts "#{name} averages #{average} hours / week"
```

Modify the program to print a different message depending on if the last week's practice was greater than the average

---

## Practice Tracker

```ruby zoom-12
week1_hours = 4
# ...

puts "#{name} averages #{average} hours / week"
if week3_hours > average
  puts "Congrats! Last week they practiced more than average!"
else
  puts "Last week they practiced less than average."
end
```

---

## Vocab

Term | Definition
--- | ---
Conditional | A code structure that allows the program to behave differently with different data
Inequality | A comparison between two values, like `average < 7`
Boolean | Data type representing the value of an inequality: `true` or `false`
Branch | The code inside each side of an if/else conditional

---

## Review Questions

- What is the syntax of an if/else conditional?

- What are the two boolean values?

- How can you get more information about a program that is misbehaving?