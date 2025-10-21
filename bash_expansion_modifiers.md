---
title: Bash_Expansion_Modifiers
date: 2023-04-18 16:10
---
In Bash, there are several expansion modifiers that can be used to manipulate the value of a variable or parameter within shell scripts. These modifiers are applied using curly braces `{}` immediately following the variable or parameter name.

Here are some of the most commonly used expansion modifiers in Bash:

1. `${var:-value}`: If `var` is not set or is null, substitute the value `value`.
2. `${var:=value}`: If `var` is not set or is null, set it to the value `value` and return the value.
3. `${var:+value}`: If `var` is set and is not null, substitute the value `value`. Otherwise, return an empty string.
4. `${var:?message}`: If `var` is not set or is null, print the message `message` to standard error and exit the script with a non-zero status.
5. `${var#pattern}`: Remove the shortest match of `pattern` from the beginning of `var`.
6. `${var##pattern}`: Remove the longest match of `pattern` from the beginning of `var`.
7. `${var%pattern}`: Remove the shortest match of `pattern` from the end of `var`.
8. `${var%%pattern}`: Remove the longest match of `pattern` from the end of `var`.
9. `${var/pattern/replacement}`: Replace the first match of `pattern` with `replacement`.
10. `${var//pattern/replacement}`: Replace all matches of `pattern` with `replacement`.
11. `${#var}`: Return the length of `var`.

These expansion modifiers can be very useful in shell scripting to manipulate strings and variables in various ways.

name="John Doe"

echo "${name}"
John Doe

echo "${name:-Unknown}"
Unknown

echo "${name:=John Doe}"
John Doe

echo "${name?'Please enter your name: '}"
Please enter your name: John Doe

echo "${name:0:3}"
Joh

echo "${name:3:4}"
Doe

echo "${name/Doe/Smith}"
John Smith

echo "${name/D/d}"
John doe

echo "${name/D/d/i}"
John idoe

echo "${name%.txt}"
John Doe

echo "${name%%.txt}"
John

echo "${name/.txt/.html}"
John Doe.html

echo "${name,,}"
john doe

echo "${name^^}"
JOHN DOE

echo "${name,,,}"
johndoe

echo "${name^^,,}"
JOHNDOE
