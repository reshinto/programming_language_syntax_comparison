# PROGRAMMING LANGUAGE SYNTAX COMPARISON
> A syntax summary, which also compares the differences between each programming language.
* List of languages
  * Python, Javascript, Ruby, Java, C++
## Table of Contents
- [Interpreted Language](#interpreted-language)
- [Compiled Language](#compiled-language)
- [Hello World](#hello-world)
- [Comments](#comments)
- [Variable declaration int](#variable-declaration-int)
- [Variable declaration float](#variable-declaration-float)
- [Variable declaration None](#variable-declaration-none)
- [Strings](#strings)
- [Boolean](#boolean)
- [Arithmetic Operators](#arithmetic-operators)
- [Comparison Operators](#comparison-operators)
- [Logical Operators](#logical-operators)
- [Getting Input](#getting-input)
- [Bitwise Operators](#bitwise-operators)
- [Increment](#increment)
- [Arrays and Lists](#arrays-and-lists)
- [Conditional Statement](#conditional-statement)
- [Loops](#loops)
- [Instantiation](#instantiation)
- [Functions](#functions)
- [Higher order functions](#higher-order-functions)
- [Hash Tables](#hash-tables)
- [Destructuring](#destructuring)
- [Spread Operator](#spread-operator)
- [Rest parameters](#rest-parameters)
- [Class](#class)
- [Importing Libraries](#importing-libraries)
- [Type Conversions](#type-conversions)
- [Find Data Type](#find-data-type)
- [String Concatenation](#string-concatenation)
- [JSON](#json)
- [Program Entry Point](#program-entry-point)
- [Swapping values](#swapping-values)
- [Error Handling](#error-handling)
- [Custom Error](#custom-error)
- [Asynchronous](#asynchronous)

## Interpreted Language
* python, javascript, ruby
## Compiled Language
* java, c++
## Hello World
### python 2
```python
print "Hello World"
```
### python 3
```python
print("Hello World")
```
### javascript
```javascript
console.log("Hello World");
```
### ruby
```ruby
print "Hello World"  # takes whatever you give it and prints it to the screen
puts "Hello World"  # adds a new (blank) line after the thing you want it to print
```
### java
```java
public class HelloWorld {
    public static void main(String args[]) {
        System.out.println("Hello World");
    }
}
```
### c++
```c++
#include <iostream>

int main() 
{
    std::cout << "Hello, World!";
    return 0;
}
```
## Comments
### python 2 & 3
```python
# Single line comment
    
"""
multi-line comments
"""
```
### javascript
```javascript
// Single line comment

/*
multi-line comments
*/
```
### ruby
```ruby
# Single line comment
    
=begin
multi-line comments
=end
```
### java
```java
// Single line comment

/*
multi-line comments
*/
```
### c++
```c++
// Single line comment

/*
multi-line comments
*/
```
## Variable declaration int
* integer ...-2, -1, 0, 1, 2...
### python 2 
```python
# int: -2147483648 ~ 2147483647
integer_name = 123
# long: -9223372036854775808L ~ 9223372036854775807L
long_name = 123L  # int beyond int size will automatically be converted to long
```
### python 3
```python
# python 3: int and long are combined into int
integer_name = 123
```
### javascript ES5
```javascript
// method 1
var integer_name;
integer_name = 123;  // accessible within the function

// method 2
var integer_name = 123;
```
### javascript ES6
```javascript
// method 1
let integer_name;
integer_name = 123;  // accessible only within the block {}

// method 2
let integer_name = 123;

// method 3
const integer_name = 123;  // variable value cannot be reassigned
```
### ruby
```ruby
integer_name = 123
```
### java
```java
// public/private/protected static final byte/short/int/long integer_name = 123;
/* 
public: visible to all classes
protected: visible to class they belong and any subclasses
private (most restricted): visible only to class they belong
static: can be accessed without creating a class instance
final: constant value, value cannot be changed
*/

// byte: -128 ~ 127, 8 bits
byte byte_name = 123;

// short: -32768 ~ 32767, 16 bits
short short_name = 123;

// int: -2147483648 ~ 2147483647, -2_147_483_648 ~ 2_147_483_647, 32 bits
int integer_name; integer_name = 123;
int integer_name = 123;  // default is visible within the same package

// long: -9223372036854775808L ~ 9223372036854775807L, can use _ same as int, 64 bits
long long_name = 123l;
long long_name = 123L;
```
### c++
```c++
// const unsigned char/short/int/long/long long integer_name = 123;
/* 
const: constant value, value cannot be changed
integer are signed by default: can assign both positive & negative values
unsigned integer (use when dealing with bit values): 0 ~ ...
  e.g. char: -128 ~ 127
  e.g. unsigned char: 0 ~ 255  // 128 + 127 = 255
*/

// char: 1 byte, -128 ~ 127, use C code to print "#include＜stdio.h＞ printf("%d", char_name);"
// 1 char has 8 bits
char char_name;
char_name = 123;

// similar to the rest of int variable declaration

// short/short int: 16 bits, 2 bytes, -32768 ~ 32767
short short_name;
short_name = 123;

short int short_name; short_name = 123;

// similar to the rest of int variable declaration

// int: 16 bits, 4 bytes, -2147483648 ~ 2147483647
int integer_name;
integer_name = 123;  // uninitialized

int integer_name = 123;  // C-like initialization

int integer_name (123);  // Constructor initialization

int age {123};  // C++11 list initialization syntax

// long/long int: 32 bits, 4 bytes, -2147483648 ~ 2147483647 bytes
long long_name;
long_name = 123;

long int long_name;
long_name = 123;

// similar to the rest of int variable declaration

// long long/long long int: 64 bits, 8 bytes, -9223372036854775808 ~ 9223372036854775807
long long long_name;
long_name = 123;

long long int long_name; long_name = 123;

// similar to the rest of int variable declaration
```
## Variable declaration float
* float, double
### python 2 & 3
```python
float_name = 1.123
float_name = 0.1123e1  # equals to 1.123
float_name = 0.1123E1  # equals to 1.123
float_name = 1123e-3  # equals to 1.123
float_name = 1123E-3  # equals to 1.123
```
### javascript ES5
```javascript
var float_name = 1.123;
```
### javascript ES6
```javascript
let float_name = 1.123;
const float_name = 1.123;
```
### ruby
### java:
```java
// float: 32 bits, 4 bytes
float float_name = 1.123f;  // have 7 decimal digits
float float_name = (float) 1.123;

// double: 64 bits, 8 bytes
double double_name = 1.123d;  // have 16 decimal digits
double double_name = 1.123;
```
### c++
```c++
// float: 4 bytes
float float_name;
float_name = 1.123;  // have 7 decimal digits

// similar to the rest of int variable declaration

// double: 8 bytes
double double_name;
double_name = 1.123;  // have 15 decimal digits

// similar to the rest of int variable declaration

// long double: 12 bytes
long double double_name;
double_name = 1.123;  // have 19 decimal digits

// similar to the rest of int variable declaration
```
## Variable declaration None
### python 2 & 3
```pythong
variable_name = None
```
### javascript
```javascript
// undefined is reserved for variables whose values have not yet been set.
let variable_name; // undefined

//null is reserved for variables whose values are explicitly nothing — instead of just “not yet defined.”
let variable_name2 = null;

// NaN is a special numeric value meaning “Not a Number”
let variable_name3 = NaN;
```
### ruby
```ruby
variable_name = nil  # nil is returned when no values are assigned, but nothing is displayed on screen
```
### java
### c++
## Strings
### python 2 & 3
```python
string_name = "string"
string_name = 'string'
# back slash not required, but will produce a new line if not given
string_name = """multi-line \
string\
"""

len(string_name)  # 6

# Character unicode point
# only accepts 1 character
ord("b")  # 98

# reverse string
string_name = string_name[::-1]  # "gnirts"

string_name = string_name.upper()  # "GNIRTS"
string_name = string_name.lower()  # "gnirts"

# capitalize string
string_name = string_name.title()  # "Gnirts"

# Replace string in string, string_name.replace(old, new, max)
string_name = string_name.replace("G", "xxx")  # "xxxnirts"
string_name = string_name.replace("x", "g", 1)  # "gxxnirts"

# string slicing
# extract characters from a string, from start position to but not including end position
new_string_name = string_name[1:4]  # "xxn"

# Split strings, string_name.split(separator, max)
string_name = string_name.split()  # ["gxxnirts"]  only works for string without spaces
string_name = "test string"
string_name1 = string_name.split()  # ["test", "string"]
string_name2 = string_name.split("s")  # ["te", "t ", "tring"]
string_name3 = string_name.split("s", 1)  # ["te", "t string"]

# Split string into an array of letters
string_name4 = list(string_name)  # ['t', 'e', 's', 't', ' ', 's', 't', 'r', 'i', 'n', 'g']
```
### javascript ES5
```javascript
var stringName = "string";
var stringName = 'string';
// back slash required
var stringName = "multi-line \
string";

stringName.length;  // 6

// Character unicode point
string.charCodeAt(stringIndex)
"abc".charCodeAt(1)  // 98

// reverse string
stringName.split("").reverse().join("");  // "gnirts"

stringName = stringName.toUpperCase();  // "GNIRTS"
stringName = stringName.toLowerCase();  // "gnirts"

// capitalize string
stringName = stringName.charAt(0).toUpperCase() + stringName.slice(1);  // "Gnirts"

// replace string with string, stringName.replace(old, new)
stringName = stringName.replace("G", "xxx");  // "xxxnirts"

// extract characters from a string, from start position to but not including end position
newStringName = stringName.substring(1, 4); // "xxn"
    
// Split string into arrays
stringName = "test string"
stringName1 = stringName.split()  // ["test string"]
stringName2 = stringName.split("")  // ['t', 'e', 's', 't', ' ', 's', 't', 'r', 'i', 'n', 'g']
stringName3 = stringName.split("s")  // ["te", "t ", "tring"]
```
### javascript ES6  // Almost all of ES5 are included in ES6
```javascript
// back slash not required, but will produce a new line if not given
var stringName = `multi-line \
string`;
let stringName = "string";
const stringName = "string";
```
### ruby
```ruby
string_name = "string"
    
string_name.length  # 6
    
string_name = string_name.reverse  # "gnirts"
    
string_name = string_name.upcase  # "GNIRTS"
string_name = string_name.downcase  # "gnirts"
    
string_name = string_name.capitalize  # "Gnirts"
    
# replace string in string, string_name.gsub!(/old/, new)
string_name = string_name.gsub!(/G/, "xxx")  # "xxxnirts"
    
# Split strings into an array
string_name = string_name.split("i")  # ["xxxn", "rts"]
string_name = "string"
string_name = string_name.split("")  # ["s", "t", "r", "i", "n", "g"]
    
    
# SYMBOLS: strings that are immutable, must use letters or underscores (_)
# used mainly for memory conservation or speed string comparison
# use a symbol if need a string to be immutable and not need to access string methods
# commonly used in hashed for keys
variable_name = :symbolStringWithoutQuotes
puts variable_name  # symbolStringWithoutQuotes

```
### java
```java
// character: 16 bits, 2 bytes, only 1 letter or symbol, must use single quotes ''
char charName = 'a';
char charName = '\u0061';  // unicode character for the letter a

// strings: must use double quotes ""
String stringName = "string";
String stringName = "multi-line " +
                     "string";
```
### c++
```c++
// character: only have 1 character, must use single quotes ''
char charName;
charName = 'a';

char charName = 'a';
char charName ('a');
char charName {'a'};

// strings
// C-style strings: an ARRAY of characters, must use double quotes ""
// THIS IS NOT A TRUE STRING, IT IS AN ARRAY OF CHARACTERS!!!!!!!
char * stringName = "string";
const char * stringName = "string";  // const is normally used
char stringName[] = "string";  // creates array of 7 chars, last char is null "\0"
char stringName[7] = "string";  // need give 7 slots for chars and null char
char stringName[7] = {'s', 't', 'r', 'i', 'n', 'g', 0};  // no 0 = error
char stringName[7] = {'s', 't', 'r', 'i', 'n', 'g', '\0'};  // no '\0' = error

//C++ strings: must add at the top "#include＜string＞", must use double quotes ""
#include＜string＞
std::string stringName;
stringName = "string";

// back slash not required, but can use if want to
std::string stringName = "multi-line"
                          "string";
std::string stringName ("string");
```
## Boolean
### python 2 & 3
* boolean_name = True
* boolean_name = False
* not True  # False
* not False  # True
### javascript ES5
* var boolean_name; boolean_name = true;
* var boolean_name = false;
* !true  // false
* !false  // true
* truthy: "xxx", 1, -1, 2.5, true
* falsey: false, 0, "", null, undefined, NaN
### javascript ES6
* let boolean_name; boolean_name = true;
* let boolean_name = false;
* const boolean_name = true;
### ruby
* boolean_name = true
* boolean_name = false
* truthy: true, 0, 1, -1, "", 
* falsey: false, nil
* Check if method exist
  * obj.respond_to?(:method)
    * example 1
      > [1, 2, 3].respond_to?(:push)  # true
    * example 2
      > 123.respond_to?(:next)  # true
    * example 3: false because array can't be turned into a symbol
      > [1, 2, 3].respond_to?(:to_sym) # false
### java
* boolean boolean_name = true;
* boolean boolean_name = false;
### c++: 8 bits
* bool boolean_name; boolean_name = true;  // produces a 1 output
* bool boolean_name = false;  // produces a 0 output
* bool boolean_name (true);
* bool boolean_name {false};
## Arithmetic Operators
### python 2
* addition: +
* subtraction: -
* multiplication: *
* division: 3.0/2  # output 1.5, 3/2 output 1
* modulus: %
* exponent: **
* floor division: 3//2  # output 1
### python 3
* division: 3/2  # output 1.5
* floor division: 3//2  # output 1
### javascript
* addition: +
* subtraction: -
* multiplication: *
* division: 3/2  // output 1.5
* modulus: %
* exponent: **
* floor division: Math.floor(3/2)  // output 1
### ruby
* addition: +
* subtraction: -
* multiplication: *
* division: 3.0/2  # output 1.5, 3/2 output 1
* modulus: %
* exponent: **
### java
* addition: +
* subtraction: -
* multiplication: *
* division: double double_name = 3.0/2;  // output 1.5, 3/2 output 1
* modulus: %
* exponent: Math.pow(3, 2);  // output 9
* floor division: int integer_name = 3/2;  // output 1
### c++
* addition: +
* subtraction: -
* multiplication: *
* division: double double_name = 3.0/2  // output 1.5, 3/2 output 1
* modulus: %
* exponent:
    * must add this to the top "#include＜cmath＞"
    * int integer_name = pow(3, 2);  // output 9
* floor division: 3/2  // output 1
## Comparison Operators
### python 2 & 3
* ==  # condition is True if both operand have equal contents
* is  # condition is True if both operand points to the same identical object
* !=  # condition is True if both operand do not have equal contents
* is not  # condition is True if both operand do not points to the same identical object
* ＜＞ # py2 only, condition is True if both operands do not equal contents
* ＞  # condition is True if right operand is less than left operand
* ＜  # condition is True if left operand is less than right operand
* ＞=  # condition is True if right operand is less than or equal to left operand
* ＜=  # condition is True is left operand is less than or equal to right operand
### javascript
* ==  // string or int will be automatically converted before comparison, only checks the value
    * var x = 5;
        * x == 5;  // is true
        * x == "5"  // is also true
* ===  // string or int will NOT be converted before comparison, checks both the value and type
    * var x = 5;
        * x === 5;  // is true
        * x === "5"  // is false
* !=
* !==
* ＞
* ＜
* ＞=
* ＜=
### ruby
* ==
* !=
* ＞
* ＜
* ＞=
* ＜=
* ＜=＞  # Combined Comparison Operator
```ruby
num1 = 2
num2 = 5
puts num1 <=> num2  # -1
puts num2 <=> num1  # 1
num1 = 3
num2 = 3
puts num1 <=> num2 # 0
    
string1 = "b"  # looks at only the 1st letter, "bz" will not change the outcome, unless both strings start with the same 1st letter
string2 = "e"
puts string1 <=> string2  # -1
puts string2 <=> string1  # 1
string1 = "c"
string2 = "c"
puts string1 <=> string2  # 0
```
### java
* ==
* !=
* ＞
* ＜
* ＞=
* ＜=
### c++
* ==
* !=
* ＞
* ＜
* ＞=
* ＜=
## Logical Operators
### python 2 & 3
* and
* or
* not
### javascript
* &&  // and
* ||  // or
* !  // not
* truthy and falsey examples
    * truthy1 && truthy2  // truthy2
    * falsey && truthy  // falsey
    * truthy && falsey  // falsey
    * falsey1 && falsey2  // falsey1
    * truthy1 || truthy2  // truthy1
    * truthy || falsey  // truthy
    * falsey1 || falsey2  // falsey2
### ruby
* &&  # and
* ||  # or
* !  # not
### java
### c++
## Getting Input
### python 2
```python
raw_input("What's your name?")

# input must be the same data type as xxx else return an error
input(xxx)
```
### python 3
```python
input("What's your name?")
```
### javascript
```javascript
// install readline-sync package locally via npm i readline-sync
var readlineSync = require('readline-sync'); // import package
var getInput = readlineSync.question("What's your name?");
```
### ruby
```ruby
# print question
print "What's your name?"
# get input
name = gets.chomp
```
### java
### c++
## Bitwise Operators
### python 2 & 3
```python
# Each digit is 1 bit, all bitwise operators converts to signed 32-bit integers, except for zero-fill right shift which results to unsigned 32 bit integer
a = 60  # 60 = ...0011 1100
b = 13  # 13 = ...0000 1101
c = 9  # 9 = ...0000 1001
# & is binary AND, return 1 if both a and b are 1
a & b  # 12 = ...0000 1100

# | is binary OR, return 1 if either a and or b HAVE a 1
a | b  # 61 = ...0011 1101

# ^ is binary XOR, return 1 if both a and b are not 1 or 0
a ^ b  # 49 = ...0011 0001

# ~ is binary ones complement, invert everything, 1 change to 0 and vice versa
~a  # -61 = ...1100 0011

# << is binary left shift, shift everything to the left by n digit(s)
a << 2  # 240 = ...1111 0000

# >> is binary right shift, shift everything to the right by n digit(s)
a >> 2  # 15 = ...0000 1111
c >> 2  # 3 = ...0000 0010, count the 1s
c = -9  # -9 = ...1111 0111
c >> 2  # -3 = ...1111 1101, count the 0s

# Zero fill right shift, shift everything to the right by n digits(s), leftmost will add n 0s
def zero_fill_right_shift(val, n):
    return (val >> n) if val >= 0 else ((val + 0x100000000) >> n)
zero_fill_right_shift(9, 2)  # 2 = ...0000 0010, count the 1s
c = -9  # -9 = ...1111 0111
zero_fill_right_shift(-9, 2)  # 1073741821 = 0011...1111 1101, count the 0s
```
### javascript
```javascript
// Each digit is 1 bit, all bitwise operators converts to signed 32-bit integers, except for zero-fill right shift which results to unsigned 32 bit integer
let a = 60  // 60 = ...0011 1100
let b = 13  // 13 = ...0000 1101
let c = 9  // 9 = ...0000 1001
// & is binary AND, return 1 if both a and b are 1, count the 1s
a & b  // 12 = ...0000 1100
    
// | is binary OR, return 1 if either a and or b HAVE a 1
a | b  // 61 = ...0011 1101
    
// ^ is binary XOR, return 1 if both a and b are not 1 or 0
a ^ b  // 49 = ...0011 0001
    
// ~ is binary ones complement, invert everything, 1 change to 0 and vice versa, count the 0s
~a  // -61 = ...1100 0011
    
// << is binary left shift, shift everything to the left by n digit(s)
a << 2  // 240 = ...1111 0000
    
// >> is Sign-propagating right shift, a binary right shift, shift everything to the right by n digit(s)
a >> 2  // 15 = ...0000 1111
c >> 2  // 3 = ...0000 0010, count the 1s
c = -9  // -9 = ...1111 0111
c >> 2  // -3 = ...1111 1101, count the 0s
    
// >>> is Zero fill right shift, shift everything to the right by n digits(s), leftmost will add n 0s
c >>> 2  // 2 = ...0000 0010, count the 1s
c = -9  // -9 = ...1111 0111
c >>> 2  // 1073741821 = 0011...1111 1101, count the 0s
```
### ruby
### java
### c++
## Increment
### python 2 & 3
* x = x + 1  # increment
* x += 1
### javascript
* x = x + 1;  // add 1 now
* x += 1;  // add 1 now
* ++x;  // preincrement, add 1 now
* x++;  // postincrement, display without addition now then add 1 later when called again
### ruby
* x = x + 1  # increment
* x += 1
### java
* x = x + 1;
* x += 1;
* ++x;  // preincrement, add 1 now
* x++;  // postincrement, display without addition now then add 1 later when called again
### c++
* x = x + 1;
* x += 1;
* ++x;  // preincrement, add 1 now
* x++;  // postincrement, display without addition now then add 1 later when called again
## Arrays and Lists
### python 2 & 3
```python
# Empty list
list_name = []
# List with elements
list_name = [1, "one", True]
# Nested lists
list_name = [1, ["two", 3]]

# Add element to list (left to right)
list_name.append(element)

# Modify an element
list_name[index] = element

# Access an element
list_name[index]

# Remove element from list (right to left)
list_name.pop()

# Add element to list at index
list_name.insert(index, element)

# Remove element from list at index
list_name.pop(index)

# Find list size
len(list_name)

# Method 1: remove all elements
del list_name[:]
# Method 2: remove all elements
list_name = []
# Method 3: remove all elements, only in python 3
list_name.clear()

# Get index of element, return ValueError if element does not exist
list_name.index(element)

Slice notation
# items start through stop-1
list_name[start:stop]
# items start through the rest of the array
list_name[start:]
# items from the beginning through stop-1
list_name[:stop]
# a copy of the whole array
list_name[:]
# start through not past stop, by step
list_name[start:stop:step]
list_name = [1, 2, 3, 4, 5]
list_name[::2]  # [1, 3, 5]
# last item in the array
list_name[-1]
# last two items in the array
list_name[-2:]
# everything except the last two items
list_name[:-2]
# all items in the array, reversed
list_name[::-1]
# the first two items, reversed
list_name[1::-1]
# the last two items, reversed
list_name[:-3:-1]
# everything except the last two items, reversed
list_name[-3::-1] 

# Merge 2 or more arrays together
new_list = list_name + list_name2

# Sort an array in ascending order
list_name = [2, 3, 1, 4]
# method 1
list_name2 = sorted(list_name)  # [1, 2, 3, 4]
# method 2
list_name.sort()  # [1, 2, 3, 4]

# Reverse sort an array
list_name.reverse()  # [4, 3, 2, 1]
```
### javascript
```javascript
// Method 1: empty list
var list_name = [];
// Method 2: empty list
var list_name = new Array();
// List with elements
var list_name = [1, "one", true];
// Nested lists
var list_name = [1, ["two", 3]];
    
    
// Modify an element
list_name[index] = element;
    
// Access an element
list_name[index];
    
    
// Remove element from list (right to left)
list_name.pop();
// Remove element from list (left to right)
list_name.shift();
// Remove number of elements (left to right) from index and insert new elements (left to right)
list_name.splice(index, number_of_element);

    
// Add element to list (left to right)
list_name.push(element);
// Add element to list (right to left)
list_name.unshift(element);
// Add element to list at index (left to right)
list_name.splice(index, 0, new_element1, new_element2...);
// Add & Remove elements to & from list at index (left to right)
list_name.splice(index, number_of_element, new_element1, new_element2...);
    
    
// Return the selected elements in an array, as a new array object
list.name.slice();
// Return the elements starting at the given 1st argument,
// and ends at, but does not include, the given 2nd argument
list_name.slice(1, 3);
list_name.slice(1);  // if 1 argument is given, return all elements from array from the 1st argument index
    
    
// Find list size
list_name.length;
// Remove all elements
list_name = [];
    
    
// Merge 2 or more arrays together
list_name1 = [1, 2, 3];
list_name2 = [4, 5, 6];
new_list = list_name1.concat(list_name2);
    
    
// Get index of element, return -1 if not present
list_name = ["element1", "element2", "element1"]
list_name.indexOf("element1")  // returns index of 0
list_name.indexOf("element1", 1);  // returns index of 2
list_name.indexOf("element1", 2);  // also returns index of 2
list_name.indexOf("element1", 0);  // returns index of 0
    
    
// Sort array in ascending order
list_name = [2, 3, 1, 4];
list_name.sort();  // [1, 2, 3, 4]
    
// Sort array in descending order
list_name.sort((a, b) => (b - a));  // [4, 3, 2, 1]
    
    
// Determine whether an array contains a specified element
list_name = ["a", "b", "c", "a"]
console.log(list_name.includes("b"))  // true
    
// Determine whether an array contains a specified element from starting index
console.log(list_name.includes("b", 2)  // false
console.log(list_name.includes("a", 2)  // true
```
### ruby
```ruby
# Empty list
list_name = []
# List with elements
list_name = [1, "one", True]
# Nested lists
list_name = [1, ["two", 3]]
    
# Add element to list (left to right)
# method 1
list_name.push(element);
# method 2
list_name << element;
    
# Add 0 to 10 to an array
(0..10).to_a  # [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
# Add 0 to 10 excluding 10 to an array
(0...10).to_a  # [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
    
# Access an elment
list_name[index]
    
# Sort an array in ascending
list_name = [3, 4, 1, 2]
# method 1
list_name1 = list_name.sort  # [1, 2, 3, 4]
# method 2
list_name.sort!  # [1, 2, 3, 4]
# Reverse sort an array, only works on already sorted array
# arrays that are not sorted will be reversed without sorting
# method 1
list_name1 = list_name.reverse  # [4, 3, 2, 1]
# method 2
list_name.reverse!
```
### java
```java
// Arrays: can only have 1 data type: string, int, etc.
// Empty string array of desired array size
String[] string_array = new String[length_of_desired_array];
// New string array with elements inside
String [] string_array = new String [] {string1, string2,...};  // Method 1
String[] string_array = {string1, string2,...};  // Method 2

// Add string array element, limited to array size
// Modify string array element value
string_array[index] = element;

// Access an element
string_array[index];

// Find array size
string_array.length;


// Arraylists: can only have 1 data type: string, int, etc.
import java.util.ArrayList;  // Must import to use

// Empty string arrayList
ArrayList<String> string_arrayList = new ArrayList<String>();

// Add string element to string arrayList (left to right)
string_arrayList.add(element);

// Modify an element at index
string_arrayList.set(index, element);

// Access an element
string_arrayList.get(index);

// Remove element from arrayList at index
string_arrayList.remove(index);

// Find arrayList size
string_arrayList.size();

// Remove all elements
string_arrayList.clear();
```
### c++
```c++
// Arrays
// Empty int array of desired array size
int int_array[length_of_desired_array];
// New int array with elements inside
int int_array [length_of_desired_array] {element1, element2,...};  // size declared
int int_array[] = {element1, element2,...};  // size automatically calculated

// Assign int element, limited to array size
// Modify int element value
int_array[index] = element;

// Access an element
int_array[index];

// Find array size: size of array (bytes) / size of an element of an array (bytes)
sizeof(int_array) / sizeof(int_array[0]);


// Vectors: a type of dynamic array
#include <vector>  // Must import to use

// Empty int vector of desired vector size, each element of 0 value will automatically be included
std::vector <int> int_vector (length_of_desired_array);
// New int vector with elements inside
std::vector <int> int_vector {element1, element2,...};
// New int vector with length of desired array and all value in parameter
// Method 1
std::vector <int> int_vector (length_of_desired_array, constant_value_for_all_elements);
// Method 2
std::vector <int> int_vector;
int_vector.assign(length_of_desired_array, constant_value_for_all_elements);

// Assign int element
int_vector[index] = element;

// Access an element
int_vector[index];
int_vector.at(index);

// Add element to vector (left to right), vector size will automatically increase
int_vector.push_back(element);
// Add element to vector at index
std::vector<int>::iterator it;  // Must create iterator for inserting or emplacing to work
it = int_vector.begin()  // Set it at index 0
// insert method: copies or moves the elements into the container by calling copy constructor or move constructor
int_vector.insert(it + index, element);  // Add element at index
// emplace method: elements are constructed in place, no copy or move operations are performed (better performance)
int_vector.emplace(it + index, element);  // Add element at index

// Remove element from vector at index
std::vector<int>::iterator it;  // Must create iterator for erase to work
it = int_vector.begin()  // Set it at index 0
int_vector.erase(it + index)  // Remove element at index
int_vector.erase(it + index, it + index)  // Remove a range of elements in the vector
// Remove element from vector (right to left)
int_vector.pop_back();  // does not return value

// Find vector size
int_vector.size();

// Resize vector
int_vector.resize(length_of_desired_array);

// Remove all elements
int_vector.clear();
```
## Conditional Statement
### python 2 & 3
```python
# If else statement
if condition_a:
    do_A
elif condition_b:
    do_B
else:
    do_something_else


# Ternary operator
do_A if condition_a else do_B


# Switch Statement is not available in python, but can create similar function
def switch(choice):
    case = {
        1: do_A,
        2: do_B,
    }
    case.get(choice, do_something_else)
```
### javascript
```javascript
// If else statement
if (condition_a) {
    do_A;
} else if (condition_b) {
    do_B;
} else {
    do_something_else;
}


// Ternary operator
condition_a ? do_A : do_B;


// Switch statement
switch(choice) {
    case choice_A:
        do_A;
        break;
    case choice_B:
        do_B;
        break;
    default:
        do_something_else;
}
```
### ruby
```ruby
# If else statement
if condition_a
    do_A
elsif condition_b
    do_B
else
    do_something_else
end


# Unless statement
condition_variable = boolValue
do_A unless condition_variable

# Unless else statement
# Check if something is false
unless condition_a
    do_A
else
    do_something_else
end


# check if a string exist in a string
if word.include? alphabet
    do_something
end


# check if value is nil, if not nil return false
object.nil?  # if object != nil returns false, else returns true

# check if array, hash, set, string is empty, return true if empty else false
object.empty?  # if object == [] or {} or "" or Set.new, return true


# Ternary operator
condition_a ? (do_A) : (do_B);
# example 1
puts true ? "yes" : "no"
# example 2
true ? (puts "yes") : (puts "no")

# Simpler if
do_A if condition_a

# One line Unless
do_A unless condition_a  # do_A if condition_a is false


# Case expression (similar to switch statement)
case choice
when choice_A:
    do_A;
when choice_B:
    do_B;
else
    do_something_else
end


# Conditional Assignment: assign only if variable is nil
favorite_book = nil
favorite_book ||= "book 1"
puts favorite_book # "book 1"
favorite_book ||= "book 2"
puts favorite_book # "book 1"
```
### java
```java
// If else statement
if (condition_a) {
    do_A;
} else if (condition_b) {
    do_B;
} else {
    do_something_else;
}


// {} not required if statement is a single line
if (condition_a)
    do_A;  // Single line statement
else if (condition_b)
    do_B;  // Single line statement
else
    do_something_else;  // Single line statement


// Ternary operator
condition_a ? do_A : do_B;


// Switch statement
switch(choice) {
    case choice_A:
        do_A;
        break;
    case choice_B:
        do_B;
        break;
    default:
        do_something_else;
        break;  // not required, but good to have in Java
}
```
### c++
```c++
// If else statement
if (condition_a) {
    do_A;
} else if (condition_b) {
    do_B;
} else {
    do_something_else;
}


// {} not required if statement is a single line
if (condition_a)
    do_A;  // Single line statement
else if (condition_b)
    do_B;  // Single line statement
else
    do_something_else;  // Single line statement


// Ternary operator
condition_a ? do_A : do_B;


// Switch statement
switch(choice) {
    case choice_A:
        do_A;
        break;
    case choice_B:
        do_B;
        break;
    default:
        do_something_else;
}
```
## Loops
### python 2
```python
# While loop
# declare_initial_conditional_value
i = 0
# Set condition
while i<5:  # Start from 0 to 4
    do_this
    # Include condition_increment_or_decrement
    i += 1
    # Can use break, continue, and pass statements to add additional functionality, or not use any
    break  # Breaks out of the current closest enclosing loop
    continue  # Goes to the top of the closest enclosing loop
    pass  # Does nothing at all


# For loop
# range() creates a list in python 2
# Looping with xrange()
for i in xrange(5):  # Starts from 0 to 4 (5 - 1)
    do_this
    # Can use break, continue, and pass statements to add additional functionality, or not use any
    break  # Breaks out of the current closest enclosing loop
    continue  # Goes to the top of the closest enclosing loop
    pass  # Does nothing at all
    
# Looping with xrange() and multiple parameters
for i in xrange(0, 5, 2):  # Start from 0 to 4 at every 2 steps (0,2,4)
    do_this
    
# Reverse loop
for i in xrange(4, -1, -1):  # Start from 4 to 0 at every -1 steps
    do_this


# Looping and getting each value
for value in list_name:  # [i1_value, i2_value, i3_value,...]
    print value


# Looping and getting index and value
for index, value in enumerate(list_name):
    print index, value  # output index, value
```
### python 3
```python
# For loop
# Looping with range()
for i in range(5):  # Starts from 0 to (5 - 1)
    do_this
    # Can use break, continue, and pass statements to add additional functionality, or not use any
    break  # Breaks out of the current closest enclosing loop
    continue  # Goes to the top of the closest enclosing loop
    pass  # Does nothing at all
    
# Looping with range() and multiple parameters
for i in range(0, 5, 2):  # Start from 0 to 4 at every 2 steps (0,2,4)
    do_this
    
# Reverse loop
for i in range(4, -1, -1):  # Start from 4 to 0 at every -1 steps
    do_this


# Looping and getting each value
for value in list_name:  # [value1, value2, value3,...]
    print(value)


# Looping and getting index and value
for index, value in enumerate(list_name):
    print(index, value)  # output index, value
```
### javascript ES5
```javascript
// While loop
// declare_initial_conditional_value
var i = 0;
// Set condition
while (i<5) {  // Start from 0 to 4
    do_this;
    // Include condition_increment_or_decrement;
    i++;
    // Can use break or continue to add additional functionality, or not use any
    break;  // Breaks out of the current closest enclosing loop
    continue;  // Goes to the top of the closest enclosing loop
}


// For loop
for (var i=0; i<5; i++) {  // Start from 0 to 4
    do_this;
    // Can use break or continue to add additional functionality, or not use any
    break;  // Breaks out of the current closest enclosing loop
    continue;  // Goes to the top of the closest enclosing loop
}

// Reverse loop
for (var i=4; i>=0; i--) {  // Start from 4 to 0
    do_this;
}

// forEach loop
// Looping through a list while calling a function
list_name.forEach(function(value, index, list){  // do not need to include all 3 parameters, but must be in order
    console.log(index, value, list);  // outputs index value list
});
```
### javascript ES6: Use let in loops when declaring
```javascript
// For of loop
// Looping and getting each value
for (let value of list_name) {  // [value1, value2, value3,...]
    console.log(value);  // output value
}
// Looping and getting index and value
for (let index_and_value of list_name.entries()) {
    console.log(index_and_value);  // output a list [index, value]
}

// For in loop
for (let index in list_name) {
    console.log(list_name[index]);
}
// For in loop normally used to get values from objects (hash table, dictionaries) than to arrays
// object = {key1:value1, key2:value2,...}
for (let index in object) {
    console.log(object[index]);  // outputs value, normally calling this way will not output value from objects
}
```
### ruby
```ruby
# While loop
# declare_initial_conditional_value
i = 0
# Set condition
while i<5 do  # Start from 0 to 4, do keyword is not mandatory
    do_this
    # Include condition_increment_or_decrement
    i += 1
end

# Until loop, backward while loop
i = 0
until i == 4  # Start from 0 to 4
    i += 1
end

# For loop, with ... (3 dots)
for i in numStart...numEnd  # for i in the range numStart up to but don't include numEnd
    do_this
end

# For loop, with .. (2 dots)
for i in numStart..numEnd  ## for i in the range numStart up to and include numEnd
    dot_this
end

# Loop method, an infinite loop, requireds break to stop loop
i = 4
loop do
    i -= 1
    break if i ==0  # Breaks out of the current closest enclosing loop
end

# Next keyword: used to skip over certain steps in loop
for i in 0...5
    next if i % 2 == 0   # do not do anything if i is an even number
    do_this
end

# Each Iterator
array = [1, 2, 3, 4, 5]
array2 = []
array.each { |value|  # Method 1: using {}
    value += 10
    array2.push(value)
}
puts array2  # [11, 12, 13, 14, 15]

array3 = []
array2.each do |value|  # Method 2: using do keyword
    value -= 10
    array3.push(value)
end
puts array3  # [1, 2, 3, 4, 5]

# Iterating over Multidimensional Arrays with Each Iterator
multiArray = [[1, 2], [3, 4], [5, 6]]
multiArray.each { 
    |sub_array| sub_array.each { 
        |value| do_something
    }
}

# Times Iterator
n.times { do_this }  # do_this will repeat n times

# Upto Iterator
# method 1: number
0.upto(5) { |num| print num, " " }  # 0 1 2 3 4 5
# method 2: alphabet
"A".upto("D") { |letter| prints letter, " " }  # A B C D

# Downto Iterator, "string" don't work
100.downto(95) { |num| print num, " " }  # 100 99 98 97 96 95
```
### java
```java
// While loop
// declare_initial_conditional_value
int i = 0;
// Set condition
while (i<5) {  // Start from 0 to 4
    do_this;
    // Include condition_increment_or_decrement;
    i++;
    // Can use break or continue to add additional functionality, or not use any
    break;  // Breaks out of the current closest enclosing loop
    continue;  // Goes to the top of the closest enclosing loop
}

// Do while loop: execute first before setting conditions
// declare_initial_conditional_value
int i = 0;
do {  // Start from 0 to 4
    do_this;
    // Include condition_increment_or_decrement;
    i++;
// Set condition
} while (i<5);

// For loop
for (int i=0; i<5; i++) {  // Start from 0 to 4
    do_this;
    // Can use break or continue to add additional functionality, or not use any
    break;  // Breaks out of the current closest enclosing loop
    continue;  // Goes to the top of the closest enclosing loop
}
// Reverse loop
for (int i=4; i>=0; i--) {  // Start from 4 to 0
    do_this;
}
```
### c++
```c++
// While loop
// declare_initial_conditional_value
int i = 0;
// Set condition
while (i<5) {  // Start from 0 to 4
    do_this;
    // Include condition_increment_or_decrement;
    i++;
    // Can use break or continue to add additional functionality, or not use any
    break;  // Breaks out of the current closest enclosing loop
    continue;  // Goes to the top of the closest enclosing loop
}

// Do while loop: execute first before setting conditions
// declare_initial_conditional_value
int i = 0;
do {  // Start from 0 to 4
    do_this;
    // Include condition_increment_or_decrement;
    i++;
// Set condition
} while (i<5);

// For loop
for (int i=0; i<5; i++) {  // Start from 0 to 4
    do_this;
    // Can use break or continue to add additional functionality, or not use any
    break;  // Breaks out of the current closest enclosing loop
    continue;  // Goes to the top of the closest enclosing loop
}
// Reverse loop
for (int i=4; i>=0; i--) {  // Start from 4 to 0
    do_this;
}

// Range-based for loop
// Looping and getting each value
for (int value : int_array) {
    cout << value << endl;  // output value per line
}
// Use auto to automatically detect array data type
for (auto value : array_name) {
    cout  << value << endl;
}

// Infinite for loops
for (;;)
    cout << "This will print forever" << endl;
```
## Instantiation
### python 2 & 3
```python
t = Thing()  # everything
```
### javascript
```javascript
v = getValue();  // plain function
t = new Thing();  // instantiation
```
### ruby
```ruby
t = thing  # instantiation
t = thing(argument)  # instantiation with arguments
```
### java
```java
v = getValue();  // plain function
t = new Thing();  // instantiation
```
### c++
```c++
v = getValue();  // plain function
t = new Thing();  // instantiation
```
## Functions
### python 2 & 3
* Function returns None by default if return statement is not declared
```python
# Normal function, use return to return values
def myFunction():
    do_something

# Normal function with parameters
def myFunction(a):
    do_something_with_a
    
# Default parameters
def myFunction(a=value):
    do_something_with_a
    
# Lambda function: a small anonymous function
# can take any number of arguments, but can only have 1 expression
myFunction = lambda a : do_something_with_a
myFunction = lambda a, b : do_something_with_a_and_b
```
### javascript ES5
* Function returns undefined by default if return statement is not declared
```javascript
// Normal function, use return to return values
function myFunction() {
    do_something;
}
// Normal function with parameters
function myFunction(a) {
    do_something_with_a;
}

// Function expression
let myFunction = function() {
    do_something;
}
// Function expression with parameters
let myFunction = function(a) {
    do_something_with_a;
}

// Arrow function: do not have their own "this" keyword
// 1 line arrow function
let myFunction = () => do_something;  // () at (do_something) not necessary if on single line
// 1 line arrow function with arguments
let myFunction = (a) => (
    do_something_with_a
);
// arrow function, must use return keyword
let myFunction = () => {
    return do_something
};
// arrow function with arguments
let myFunction = (a) => {
    return do_something_with_a
};

// Immediately Invoked Function Expressions (IIFE)
// method 1
(function() {
    do_something;
})();
// method 2
(function() {
    do_something;
}());
// method 3: no returning of value
!function() {
    do_something;
}();
```
### javascript ES6
```javascript
// Default parameters
function myFunction(a=value) {
    do_something_with_a;
}
```
### ruby
* Function returns result regardless of whether return statement is declared or not
  * Reason: ruby applies Implicit Return feature
```ruby
# Normal function, use return to return values
def myFunction
    do_something
end

# Normal function with parameters
def myFunction(parameter)
    do_something
end

# Default parameters
def myFunction(a=value)
    do_something_with_a
end

# Blocks: nameless methods, similar to anonymous functions in JavaScript or lambdas in Python
# can replace "do" and "end" with {}
# 1st type
# original way
arrayName.each do |num|
    do_something_with_num
end
# blocks way
arrayName.each { |num| do_something_with_num }

# 2nd type: Yield
def myFunction
    yield  # can have multpile yield
    yield
end
myFunction { print "test" }  # "testtest"

def myFunction
    yield 1  # can pass any number of arguments to yield
    yield 2
end
myFunction { |num| print num * 10 }  # 1020

# Explicit Blocks
def myFunction(&blockName)  # & is used to define the block's name
    blockName.call
end
myFunction { print "test" }  # "test"

# Lambda
myFunction = -> { puts "test" }
myFunction.call  # "test", call is required to call the lambda function
```
### java
### c++
## Higher order functions
### python 2
```python
# Map: applies a given function to each item of an iterable (list, tuple etc.) and returns a list of the results
# map(function, iterable, ...)
arr = [1, 2, 3]
def add(n):
    return n + n
map(add, arr)  # return <map object at 0x10473e518>
list(map(add, arr))  # return [2, 4, 6]


# Filter: filter and return a new array based on the conditions
# filter(function, iterable)
arr = [1, 2, 3]
def condition(n):
    if n < 3:
        return n
filter(condition, arr)  # return <filter object at 0x10473e550>
list(filter(condition, arr))  # return [1, 2]


# Reduce: executes a function on each element, resulting in a single output value
arr = [1, 2, 3]
def compute(n, m):
    return n * m
reduce(compute, arr)  # return 6

# Zip: combines 2 arrays or tuples into an array of tuples
arr1 = [1, 2, 3]
arr2 = ["1", "2", "3"]
zpp(arr1, arr2)  # [(1, '1'), (2, '2'), (3, '3')]
```
### python 3
```python
# Reduce: executes a function on each element, resulting in a single output value
arr = [1, 2, 3]
def compute(n, m):
    return n * m
from functools import reduce  # requires import in python 3
reduce(compute, arr)  # return 6

# Zip: must call a list() or tuple() on the zip method
list(zip(s, t))  # [(1, '1'), (2, '2'), (3, '3')]
tuple(zip(s, t)) # ((1, '1'), (2, '2'), (3, '3'))
```
### javascript
```javascript
// Map: create a new array from a current array
// array.map(element, currentIndex, originalArray)
const companies = [
    {name: "company1", category: "industry1"},
    {name: "company2", category: "industry2"}
];
// callback method
const companyNames = companies.map(function(company) {
    return company.name;
}
// arrow function method
const companynames = companies.map((company) => company.name);


// Filter: creates a new array with all elements that pass the condition implemented by the provided function
// array.filter(element, currentIndex, originalArray)
const ages = [age1, age2, age3];
// callback method
const canDrink = ages.filter(function(age) {
    if (condition) {
        return true;
    }
}
// arrow function method
const canDrink = ages.filter(age => condition);


// Reduce: executes a function on each element of the array, resulting in a single output value
// array.reduce(function(accumulator, currentValue){ do_something }, initialValue)
let arr = [1, 2, 3];
// no initial value
arr.reduce(function(accumulator, currentValue) {
    return accumulator + currentValue;
});  // returns a value of 6
/*
accumulator | currentValue | returned value
    1       |       2      |        3
    3       |       3      |        6
*/

// initial value included
arr.reduce(function(accumulator, currentValue) {
    return accumulator + currentValue;
}, 10);  // returns a value of 16
/*
accumulator | currentValue | returned value
    10      |       1      |        11
    11      |       2      |        13
    13      |       3      |        16
*/


// Sort: sorts the elements of an array in place and returns the sorted array
// array.sort(compareFunction)
// if compareFunction is not used, all sorted elements will be sorted based on it's string value
let array = ["1", 30, 4, 21, 100000];
array.sort();  // returns ["1", 100000, 21, 30, 4]

// sort in ascending order
array.sort((a, b) => a - b);  // returns ["1", 4, 21, 30, 100000]

// sort in descending order
array.sort((a, b) => b - a);  // returns [100000, 30, 21, 4, "1"]

// Zip is not available is Javascript, use Maps instead
const arr1 = [1, 2, 3];
const arr2 = ["1", "2", "3"];
function zip(arrays) {
    return arrays[0].map(function(_,i){
        return arrays.map(function(array){return array[i]})
    });
}
zip([arr1, arr2]);  // [[1, '1'], [2, '2'], [3, '3']]
```
### ruby
```ruby
# Zip: combine 2 arrays
arr1 = [1, 2, 3]
arr2 = ["1", "2", "3"]
puts arr1.zip(arr2)  # [[1, '1'], [2, '2'], [3, '3']]
```
### java
### c++
## Hash Tables 
* Hash Tables, Dictionaries, Objects
### python 2 & 3
```python
# Create dictionary
newDict = {}

# Create dictionary and assign key value pairs
# method 1
newDict = {
    "key1": "value1",
    "key2": 123,
    "key3": True,
    "key4": myFunction
}
# method 2
newDict = dict(key1="value1", key2="value2")

# Add or reassign key value pair
newDict["Key"] = "Value"  # method 1
newDict.update({"key": "value"})

# Set multiple keys with a similar value
newKeys = ("key1", "key2", "key3")
newValue = value
newDict = dict.fromkeys(newKeys, newValue)

# Return value of the item with the specified key
# If the key does not exist, insert the key, with the specified value
newVariable = newDict.setdefault("key", "newValue")

# Get value
newDict["key"]  # method 1
newDict.get("key")  # method 2

# Loop through Dictionary and get each key
# method 1
for key in newDict:
    print(key)
# method 2
for key in newDict.keys():
    print(key)
    
# Loop through Dictionary and get each value
# method 1
for key in newDict:
    print(newDict[key])
# method 2
for value in newDict.values():
    print(value)
    
# Loop through both keys and values
for key, value in newDict.items():
    print(key, value)
    
# Check if key exists
if "key" in newDict:
    return True
    
# Get dictionary length
len(newDict)

# Copy dictionary
# cannot copy just from dict2 = dict1 as it is just referencing to dict1
# method 1
newDict2 = newDict.copy()
# method 2
newDict2 = dict(newDict)

# Remove items
newDict.pop("key")  # method 1
del newDict["key1"]  # method 2

# Remove last inserted item
newDict.popitem()

# Delete entire dictionary
del newDict  # method 1
newDict.clear()  # method 2
```
### javascript ES5
```javascript
// Objects
// Create object
let newObj = new Object();  // method 1
let newObj = {};  // method 2, literal notation

// Create object and assign values
// keys can only be strings without quotes
let newObj = {
    key1: "stringValue",
    key2: 123,
    key3: true,
    key4: ["array", "array2"],
    key5: {anotherKey: anotherValue},
    key6: function(arg){return do_something_with_arg}
};

// Creates a new object, using an existing object as the prototype of the newly created object
let newObj2 = Object.create(newObj);  // method 1
let newObj2 = Object.assign({}, newObj);  // method 2

// Assign and Reassign values
newObj["key1"] = "newString";  // method 1, bracket notation
newObj.key1 = "newString2";  // method 2, dot notation

// Copy the values of all enumerable own properties from one or more source objects to a target object
// return the target object
const target = { a: 1, b: 2 };
const source = { b: 4, c: 5 };
const newObj = Object.assign(target, source);  // newObj, target = { a: 1, b: 4, c: 5 }

// Get value
newObj["key1"];  // method 1
newObj.key1;  // method 2

// Get an array of keys
Object.keys(newObj);

// Get an array of values
Object.values(newObj);

// Loop through all key value pairs
// must be (key, value)
for (let [key, value] of Object.entries(newObj)) {console.log(`Key: ${key}, Value: ${value}`);}

// Defines a new property directly on an object, or modifies an existing property on an object, and returns the object
// Object.defineProperty(obj, propertyName, descriptor)
Object.defineProperty(newObj, property1, {value: "123", writable: true});  // newObj.property1 = 123

// Seals an object
// prevent addition of properties, however defined properties still can be changed
Object.seal(newObj);

// Freeze an object
// makes the object immutable, meaning no change to defined property allowed, unless they are objects.
Object.freeze(newObj);
```
### javascript ES6
```javascript
// Maps or Hash tables
// Create new Map or hash table
const newDict = new Map();

// Add key value pair data
// keys does not need to be strings, can be numbers, booleans, etc.
newDict.set(key1, value1);
newDict.set(key2, value2);

// Get all keys
newDict.keys();

// Get all values
newDict.values();

// Iterate over Maps to get each key
for (let key of newDict.keys()) {
    console.log(key);
}

// Iterate over Maps to get each value
for (let value of newDict.values()) {
    console.log(value);
}

// Get value
newDict.get(key);

// Get hash table size
newDict.size;

// Check if key value pair exist with key input
newDict.has(key);

// Loop through all key value pairs
// method 1, must be (value, key)
newDict.forEach((value, key) => console.log(`Key: ${key}, Value: ${value}`));
// method 2, must be (key, value)
for (let [key, value] of newDict.entries()) {console.log(`Key: ${key}, Value: ${value}`);}

// Delete key value pair
newDict.delete(key);
// Delete all key value pairs
newDict.clear()


// WeakMap: similar to Map, but all keys must be objects
// Create new weak map
const newDict = new WeakMap();

// Add key value pair data
// key MUST be and Object
newDict.set(obj1, value1);
newDict.set(obj2, value2);

// Get value
newDict.get(obj);

// Delete key value pair
newDict.delete(obj);

// Check if key value pair exist with key input
newDict.has(obj);
```
### ruby
```ruby
# Hash literal notation, OLD SYNTAX
hash_name = {
    key1 => value1,
    "name" => "myName",
    "age" => 123,
    "hungry?" => true,
    111 => "one one one",
    false => "weird"
}

# NEW SYNTAX
# keys are symbols in this case
hash_name = {
    key1: value1,
    name: "myName",
    age: 123,
    hungry: true,
}

# Hash constructor notation
# Create a new empty hash
hash_name = Hash.new


# Adding to a Hash
hash_name["newKey"] = "new value"


# Accessing hash value
hash_name["hungry"]  # true


# Delete a key value pair
hash_name.delete(key)


# Iterating over Hashes
hash_name.each do [keyName, valueName|
    do_something_with_keyName_and_valueName
end


# sort_by: Maps Hash into an array and then sort them via values in ascending order
colors = {
    "blue" => 3,
    "green" => 1,
    "red" => 2
}
colors = colors.sort_by do |color, count|
    count
end
puts colors  # [["green", 1], ["red", 2], ["blue", 3]]


# nil does not display anything
myHash = Hash.new()
puts myHash  # {}
puts myHash["nonexistent key"] # display nothing
# Replace nil and Set default value when key does not exist
myHash = Hash.new("no such key")
puts myHash  # {}
puts myHash["nonexistent key"]  # "no such key"


# Symbols used in Hashes
myHash = {
    :cat => "meow",
    :number => 123
}


# Select method: Grab specific value(s) from a hash with key or value
grades = {
    alice: 100,
    bob: 92,
    chris: 95,
    dave: 97
}
newHash = grades.select { |nameKey, gradeValue| gradeValue < 97 }  # Grab values with value
puts newHash  # { :bob => 92, :chris => 95 }

newHash = grades.select { |nameKey, gradeValue| nameKey == :alice }  # Grab values with key
puts newHash  # { :alice => 100 }


# Loop all keys
grades.each_key { |key| print key, " " }  # alice bob chris dave

# Loop all values
grades.each_value { |value| print value, " " }  # 100 92 95 97
```
### java
### c++
## Destructuring
### python 2 & 3
```python
# Tuples
xVariable, yVariable = (xValue, yValue)

# Arrays
xVariable, yVariable = [xValue, yValue]

# String
xVariable, yVariable = "xy"

# Dictionaries
xKey, yKey = {"xKey": xValue, "yKey": yValue}
```
### javascript ES6
```javascript
// Arrays
const [xVariable, yVariable] = [xValue, yValue];

// Objects
const obj = {
    xKey: xValue,
    yKey: yValue
}
// declaring variables
const {xKey, yKey} = obj;  // variable names must be the same as object key names

// assigning different variable names
const {xKey: xNewKey, yKey: yNewKey} = obj;
```
### ruby
### java
### c++
## Spread Operator
### python 2 & 3
```python
# *args (splat)
# Takes an array and transform (unpacks) it into single values
# Must utitlize all of the element of the array to work
myFunction(a, b, c)  # normal method
myFunction(*Tuple)  # (a, b, c)
myFunction(*List)  # [a, b, c]
myFunction(*String)  # "abc"
myFunction(*Dict)  # {"a": value1, "b": value2}  only utilize the keys

# **kwargs
myFunction(**Dict) # {"a": value1, "b": value2}  utilize both keys and values
```
### javascript ES6
```javascript
// Takes an array and transform (unpacks) it into single values
// Must utitlize all of the element of the array to work
let arr = [a, b, c];
myFunction(a, b, c);  // normal method
myFunction.apply(null, arr)  // using the apply() method
myFunction(...arr);  // spread method

// join multiple arrays together
let arr1 = [a, b, c];
let arr2 = [d, e, f];
let totalArr = arr1.concat(arr2);  // concat method
let totalArr = [...arr1, ...arr2];
```
### ruby
### java
### c++
## Rest parameters
### python 2 & 3
```python
# *args
# Receive a couple of single values and transform them into an array
def myFunction(*args):
    newArr = args  # args is an array of arugments

# **kwargs
# Receive a couple of keys and values and transform them into a dictionary
def myFunction(**kwargs):
    newDict = kwargs  # kwargs is a dictionary of keys and values
# calling example
myFunction(var1=value1, var2=value2)
```
### javascript ES6
```javascript
// Receive a couple of single values and transform them into an array
function myFunction(...args) {
    let argsArr = args;  // args is an array of arguments
}
```
### ruby
```ruby
# *parameter
# Receive a couple of single values and transform them into an array
def myFunction(*parameter):
    newArr = args  # args is an array of arugments
end
```
### java
### c++
## Class
### python 2
``` python
class MathClass:
    def __init__(self, arg1, arg2):
        self.arg1 = arg1
        self.arg2 = arg2
        self.total = self.outterAdd(arg1, arg2)
        
    def innerAdd(self, arg3):
        return self.arg1 + self.arg2 + arg3
        
    # Static method knows nothing about the class and just deals with the parameters
    def outterAdd(number1, number2):
        return number1 + number2
    outterAdd = staticmethod(outterAdd)
    
    
test = MathClass(2, 4)
print (test.total)  # 6
print (test.innerAdd(2))  # 8
print (test.outterAdd(3, 7))  # 10
print (MathClass.outterAdd(4, 5)  # 9
```
### python 3
```python
class MathClass:
    def __init__(self, arg1, arg2):
        self.arg1 = arg1
        self.arg2 = arg2
        self.total = self.outterAdd(arg1, arg2)
        
    def innerAdd(self, arg3):
        return self.arg1 + self.arg2 + arg3
        
    # Static method knows nothing about the class and just deals with the parameters
    @staticmethod
    def outterAdd(number1, number2):
        return number1 + number2
    
    
test = MathClass(2, 4)
print(test.total)  # 6
print(test.innerAdd(2))  # 8
print(test.outterAdd(3, 7))  # 10
print(MathClass.outterAdd(4, 5))  # 9


# Using classmethod: method 1
class Person:
    name = "Default name"
    
    @classmethod
    def change_name(clas, new_name):
        cls.name = new_name
        
        
person1 = Person()
print(person1.name)  # Default name
person1.change_name("New name")
print(person1.name)  # New name


# Using classmethod: method 2
class Person2:
    def __init__(self, name):
        self.name = name
    
    @classmethod
    def use_default_name(cls):
        return cls("Default name")
        
     
person2 = Person2("My name")
print(person2.name)  # My name
person3 = Person2.use_default_name()
print(person3.name)  # Default name
```
### javascript ES5
```javascript
// Constructor
var MathClass = function(arg1, arg2) {
  this.arg1 = arg1;
  this.arg2 = arg2;
}

// Instantiation
var test = new MathClass(2, 4);

// Add method
MathClass.prototype.innerAdd = function(arg3) {
  return this.arg1 + this.arg2 + arg3;
}

test.innerAdd(2);  // 8
```
### javascript ES6
```javascript
// Case 1: normal javascript way
class MathClass {
  constructor(arg1, arg2) {
    this.arg1 = arg1;
    this.arg2 = arg2;
    this.total = this.constructor.outterAdd(arg1, arg2);
  }
  
  innerAdd(arg3) {
    return this.arg1 + this.arg2 + arg3;
  }
  
  // Static method knows nothing about the class and just deals with the parameters
  static outterAdd(number1, number2) {
    return number1 + number2;
  }
}
const test = new MathClass(2, 4);
console.log(test.total);  // 6
console.log(test.innerAdd(2));  // 8
console.log(test.constructor.outterAdd(3, 7));  // 10
console.log(MathClass.outterAdd(4, 5));  // 9

// Case 2: event handlers in React
class MathClass {
  constructor(arg1, arg2) {
    this.arg1 = arg1;
    this.arg2 = arg2;
    this.innerAdd = this.innerAdd.bind(this);  // this is required to prevent TypeError
  }
  
  innerAdd(arg3) {
    return this.arg1 + this.arg2 + arg3;
  }
  const test = new MathClass(2, 4);
  console.log(test.innerAdd(2));  // 6
  // event handlers in React does this (not React fault, caused by "this" binding in javascript)
  const showResults = test.innerAdd;
  console.log(showResults(2));  // return a TypeError due to wrong "this" reference, bind is required
```
### ruby
### java
### c++
## Importing Libraries
### python 2 & 3
```python
# import module from libraries
import module_name  # must call module_name to use

# Using alias
import module_name as mn  # must call mn to use

# import class or function from a module
from module_name import function_name


# Absoute imports within the same project (file extensions not required)
from folder1 import module1  # example 1
from folder1.module2 import function1  # example 2
from folder2 import class1  # example 3
from folder2.subfolder1.module5 import function2  # example 4


# Relative imports (dot feature is similar to terminal)
from .module1 import class1  # example 1
from ..folder2 import function1 # example 2
from . import class2 # example 3
```
### javascript ES5
```javascript
// Before a module can be imported, it has to be exported first
var objectName.functionName = function();
module.exports = objectName;  // can be an object of functions
// alternative exports, import rules also change
exports.moduleName = objectName;  // preset a name to the module

// importing a module
// moduleName can be path too
var mn = require("moduleName");  // must call mn to use
var {function1, function2} = require("moduleName");  // importing multiple functions from a module
// import for alternative export
var mn = require("moduleName").moduleName;
```
### javascript ES6
```javascript
// Before a module can be imported, it has to be exported first
export default objectName;  // exporting a single or nested functions or class

// {} must be used when importing
// method 1
export {functionName};  // export only 1 class or function (can be used for importing multiple functions or classes
// method 2, can be function, class, objects, etc.
export const functionName = () => {do_something}


// import class or function from module
import "moduleName";  // import module
import name from "moduleName";  // name can be anything if only have 1 export
import * as name from "moduleName";  // import multiple exports as name
import {function1} from "moduleName";  // import a function from a module of multiple exports
import {function1 as f1} from "moduleName";  // import a function with alias
import {function1, function2} from "moduleName";  // import multiple functions
import name, {function1} from "/modules/path/moduleName"; // function1 can be used directly or via name.function1
```
### ruby
### java
### c++
## Type Conversions
### python 2 & 3
```python
# Convert to Integer, floats will round down
int(type_to_convert)

# Convert to floats
float(type_to_convert)

# Convert to strings
str(type_to_convert)

# Convert to arrays
list(type_to_convert)  # cannot be a number

# Convert to tuples
tuple(type_to_convert)  # cannot be a number

# Convert to sets
set(type_to_convert)  # cannot be a number
```
### javascript
### ruby
```ruby
# String to symbol
# method 1
"string".to_sym  # :string
# method 2
"string".intern  # :string

# Object to string
:string.to_s  # "string"
123.to_s  # "123"

# String to integer
"123".to_i  # 123
```
### java
### c++
## Find Data Type
### python 2 & 3
```python
# Get data type
num = 123
type(num)  # int

# Get boolean value
isinstance(num, int)  # True
isinstance(num, str)  # False
```
### javascript
```javascript
# Get data type: "number", "string", "boolean", "object", "undefined", "function"
# null and arrays are classified as object
# classes and methods are classfied as function
let num = 123;
typeof num;  // "number"

let array = [1, 2, 3];
typeof array;  // "object"
```
### ruby
```ruby
# Get data type, function won't provide a specify class type
puts "test".class  # String
puts :stringSym.class  # Symbol
puts 123.class  # Fixnum
puts 1.23.class  # Float
puts true.class  # TrueClass
puts false.class  # FalseClass
puts nil.class  # NilClass
hashName = Hash.new()
puts hashName.class  # Hash
class Myclass
    def myFunc
        do_something
    end
end
puts Myclass.class  # Class

# Get id of object
puts "string".object_id  # 2343215, some random number where object is stored in memory
```
### java
### c++
## String Concatenation
### python 2
```python
string_name = "string1" + "string2"  # "string1string2"

# String formatting
# % string operator: old style, soon to be deprecated
string_name = "%s %s" % ("string1", "string2")  # "string1 string2"

# {} operator: python 2.6 and above
# method 1
string_name = "{} {}".format("string1", "string2")  # "string1 string2"
# method 2
string_name = "{0} {1}".format("string1", "string2")  # "string1 string2"
```
### python 3
```python
# f string: python 3.6 and above
string1 = "string1"
string2 = "string2"
string_name = f"{string1} {string2}"  # "string1 string2"
```
### javascript ES5
```javascript
// javascript allows data type mashups, numbers will be converted to strings when concatenated with a string.
let stringName = "string1" + "string2" + 123;  // "string1string2123"
```
### javascript ES6
```javascript
let string1 = "string 1 value";
let string2 = "string 2 value";
let stringName = `${string1} ${string2} 123`;  // "string 1 value string 2 value 123"
```
### ruby
```ruby
string1 = "string1"
string2 = "string2"
string_name = "#{string1} #{string2}"  # "string1 string2"

string_name << "string 3"  # "string1 string2string3"

# to_s: numbers need to be converted to a string to be concatenated
puts "one" + 1.to_s  # "one1"
```
### java
### c++
## JSON
### python 2 & 3
```python
import json  # must import to use

# python objects that can be converted: dict, list, tuple, string, int, float, True, False, None
# Convert JSON to python
json.loads(json_object)

# Convert python to JSON
json.dumps(python_object)
```
### javascript
```javascript
// JSON (JavaScript Object Notation): a lightweight, text-based data format that's based on JavaScript.
// convert js to JSON
let objName = {title: 'Black Panther'};
objName = JSON.stringify(objName);

// convert JSON to js
let objName = {"title": "Black Panther"};
objName = JSON.parse(objName);
```
### ruby
### java
### c++
## Program Entry Point
### python 2 & 3
```python
if __name__ === "__main__":
    # do something
```
### javascript
```javascript
// only works in node js
if (require.main === module) {
  // do something
}
```
### ruby
### java
### c++
## Swapping values
### python 2 & 3
```python
a, b = 1, 2
# method 1
temp = a
a = b
b = temp

# method 2
a, b = b, a
```
### javascript ES5
```javascript
let a = 1;
let b = 2;
const temp = a;
a = b;
b = temp;
```
### javascript ES6
```javascript
[a, b] = [b, a];
```
### ruby
### java
### c++
## Error Handling
### python 2 & 3
* try: lets you test a block of code for errors
* except: except block lets you handle the error
  * covers all error types
    > except:
  * define exception type (can write multiple except statements)
    > except NameError:
  * save error to variable e
    > except ValueError as e:
  * list of important error types
    * AssertionError, AttributeError, EOFError, FloatingPointError, GeneratorExit, ImportError, IndexError, KeyError
    * KeyboardInterrupt, MemoryError, NameError, NotImplementedError, OSError, OverflowError, ReferenceError, RuntimeError
    * StopIteration, SyntaxError, IndentationError, TabError, SystemError, TypeError, UnboundLocalError, UnicodeError
    * UnicodeEncodeError, UnicodeDecodeError, UnicodeTranslateError, ValueError, ZeroDivisionError
* else: code to be executed if no errors were raised
* finally: if specified, will be executed regardless if the try block raises an error or not
  * useful to close objects and clean up resources
```python
# similar to if else
try:  # must start with try
    do_something
except:  # must have to handle errors
    do_something_if_error_occurs
else:  # not required
    do_something_if_no_error
finally:  # not required
    do_something_when_try_&_except_or_else_is_completed
```
### javascript
* try: lets you test a block of code for errors
* catch: lets you handle the error
* finally: lets you execute code, after try and catch, regardless of the result
```javascript
try {
  doSomething;
} catch(error) {
  doSomethingIfErrorOccurs;
} finally {
  doSomethingWhenTryAndCatchIsCompleted;
}
```
### ruby
### java
### c++
## Custom Error
### python 2 & 3
```python
# raise generic exception
raise Exception("custom message")

# raise specific exception
raise ValueError("custom message")
```
### javascript
```javascript
throw "custom message"; // throw a text

throw 123; // throw a number
```
### ruby
### java
### c++
## Asynchronous
### python
### javascript ES5
```javascript
// callback example
function sendMessage(message, callback) {
  return callback(message);
}
sendMessage("Message for console", console.log); // "Message for console"

// callback with anonymous functions
function greet(name, formatName) {
  return `Hello ${formatName(name)}`;
}
console.log(greet("tim", function(name){
  return name.toUpperCase();
}); // "TIM"
```
### javascript ES6
### ruby
### java
### c++
