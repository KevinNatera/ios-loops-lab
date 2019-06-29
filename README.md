# Loops Lab

## Instructions for lab submission

1. Fork the assignment repo
1. Clone your Fork to your machine
1. Complete the lab
1. Push your changes to your Fork
1. Submit a Pull Request back to the assignment repo
1. Paste a link to of your Fork on Canvas and submit


## Question 1

Write code that prints all the numbers from 1 to 150, **inclusive.**

let numbers = 1...150

for aNumber in numbers {
print(aNumber)
}

***
## Question 2

Write code that prints all the numbers from 142 to 159, **exclusive.**

let numbers = 142..<159

for aNumber in numbers where aNumber != 142 {
print(aNumber)
}

***
## Question 3

Write code that prints only the even numbers from 15 to 80, **inclusive.**

let numbers = 15...80

for aNumber in numbers where aNumber % 2 == 0 {
print(aNumber)
}

***
## Question 4

Write code that prints only the odd numbers from 19 to 51, **inclusive.**

let numbers = 19...51

for aNumber in numbers where aNumber % 2 != 0 {
print(aNumber)
}

***
## Question 5

Write code that prints all the numbers that end in a **5** from 1 to 100, **exclusive.**

let numbers = 1..<100

for aNumber in numbers where aNumber % 5 == 0 && aNumber % 10 != 0 {
print(aNumber)
}

***
## Question 6

Write code that prints all the numbers that end in a 7 from 1 to 40, **inclusive.**

let numbers = 1...40

for aNumber in numbers where aNumber % 10 == 0 {
print(aNumber - 3)
}

***
## Question 7

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 3`

let numbers = 20...150

for aNumber in numbers where aNumber % 3 == 0 {
print(aNumber)
}

***
## Question 8

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 2 and 3`

let numbers = 20...150

for aNumber in numbers where aNumber % 2 == 0 && aNumber % 3 == 0{
print(aNumber)
}

***
## Question 9

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that end with a 4`

let numbers = 20...150

for aNumber in numbers where aNumber % 10 == 0 && aNumber != 20 {
print(aNumber - 6)
}

***
## Question 10

Given a range of numbers from 20 to 150, print out all the numbers that follows these conditions:

`Print out numbers: 31, 35, 40 to 60.`

let numbers = 20...150

for aNumber in numbers where aNumber < 61 {
switch aNumber {
case 31: print(aNumber)
case 35: print(aNumber)
case 40...60: print(aNumber)
default: aNumber
}
}

***
## Question 11

Without using Xcode, how many times will the loop below run?  Explain why.

```swift
var i = 5

while (i > 3) {
    i += 1
}

The above code will loop infinitely because the loop adds 1 to i while it is greater than three, and there isn't a line of code that eventually makes this condition false.

```

***
## Question 12

Change the code below to make the loop stop executing when i reaches 9.

```swift
var i = 5

while (i > 3) {
    i += 1
}


var i = 5

while (i < 10) {
  i += 1
}

```

***
## Question 13

Change the code below to make the loop stop executing after it has run 1,000 times.

```swift
var i = 5

while (i > 3) {
    i += 1
}


var i = 5

while (i < 1005) {
i += 1
}

```

***
## Question 14

Change the code below to make the loop stop executing after it has run 1,000 times and also make it print out the current value of i **only if i is an even number.**

```swift
var i = 5

while (i > 3) {
    i += 1
}


var i = 5

while (i < 1005) {
  if i % 2 == 0 {
   print(i)
 }
  i += 1
}
```

***
## Question 15

What's the difference in syntax between the following two while loops?  Will their outputs be different?  Explain why or why not.

```swift
//loop one
var i = 1

while i <= 10 {
    print("i = \(i)")
    i += 1
}

//loop two
var i = 1

repeat {
    print("i = \(i)")
    i += 1
} while i <= 10


Loop one uses a traditional while loop, whereas loop two uses a repeat loop and while to set the condition. These two loops will have the same output because both their condition and the action they execute are the same.

```

***
## Question 16

What's the difference between `break` and `continue`?  Give an example that demonstrates their differences.

Break completely stops a loop, whereas continue repeats the loop for its next iteration

An example of a break is :

var i = 5

while (i < 999) {
print(i)
i += 1
break
}

An example of a continue is :

for i in 1...5 {
if i == 4 {
continue
}
print("i = \(i)")
}

***
## Question 17

Without using Xcode, what will the loop below print? Select all that apply.

```swift
for i in 1...10 {
    if (i >= 4 && i <= 7){
        continue
    }
    print(i)
}
```

[x]1
[x]2
[x]3
[]4
[]5
[]6
[]7
[x]8
[x]9
[x]10

***
## Question 18

Without using Xcode, what will the loop below print? Select all that apply.

```swift
for i in 1...10 {
    if (i >= 4 && i <= 7){
        break
    }
    print(i)
}
```

[x]1
[x]2
[x]3
[]4
[]5
[]6
[]7
[]8
[]9
[]10

***
## Question 19

Without using Xcode, what will the loop below print?  Explain below.

```swift
outerloop: for x in 1...3 {
    innerloop: for y in 1...3 {
        if y == 2{
            continue outerloop
        }
        print("x = \(x), y = \(y)")
    }
}

x = 1, y = 1
x = 2, y = 1
x = 3, y = 1

The loop will print this because the if statement "if y == 2 { continue outerloop }" prevents the value of y from reaching its next iteration. 

```

***
## Question 20

Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** x and y are both integers.

for x in 0...10 {
  for y in 0...10 {
    print("\(x),\(y)", separator: "",
    terminator: " ")
  }
 print("")
}

***
## Question 21

Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** the difference of x and y is at least 5, and x and y are both integers.

for x in 0...10 {
   for y in 0...10 {
     if x - y >= 5 || y - x >= 5 {
     print("\(x),\(y)", separator: "",
     terminator: " ")
    }
   }
  print("")
}

***
## Question 22

Print the first `N` square numbers. A **square number**, also called perfect square, is an integer that is obtained by squaring some other integer; in other words, it is the product of some integer with itself (ex. 1 = 1*1, 4 = 2 * 2, 9 = 3* 3 …).

Example:
Input: `var N = 5`

Output:
```swift
1
4
9
16
25

var N = 5

var i = 1

while i <= N {
print(i * i)
i += 1
}

```

***
## Question 23

Given an integer N draw a square of N x N asterisks. Look at the examples.

Example 1:
Input: `var N = 2`

Output:
```swift
**
**
```

Example 2:
Input: `var N = 3`

Output:
```swift
***
***
***
```

Hint 1
Try printing a single line of * first.

Hint 2
You can use print("") to print an empty line.


var N = 5
var space = ""
var i = 0

for _ in i..<N {
   for _ in i..<N {
  space += "*"
  i += 1
 } 
  print("\(space)")
}


***
