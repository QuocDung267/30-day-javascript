
[<< Day 1](../readMe.md) | [Day 3 >>](../03_Day_Booleans_operators_date/03_booleans_operators_date.md)

![Thirty Days Of JavaScript](../images/banners/day_1_2.png)

- [📔 Day 2](#-day-2)
	- [Data Types](#data-types)
		- [Primitive Data Types(Nguyên thủy)](#primitive-data-types)
		- [Non-Primitive Data Types(không nguyên thủy)](#non-primitive-data-types)
	- [Numbers](#numbers)
		- [Declaring Number Data Types](#declaring-number-data-types)
		- [Math Object](#math-object)
			- [Random Number Generator](#random-number-generator)
	- [Strings](#strings)
		- [String Concatenation](#string-concatenation)
			- [Concatenating Using Addition Operator](#concatenating-using-addition-operator)
			- [Long Literal Strings](#long-literal-strings)
			- [Escape Sequences in Strings](#escape-sequences-in-strings)
			- [Template Literals (Template Strings)](#template-literals-template-strings)
		- [String Methods](#string-methods)
	- [Checking Data Types and Casting](#checking-data-types-and-casting)
		- [Checking Data Types](#checking-data-types)
		- [Changing Data Type (Casting)](#changing-data-type-casting)
			- [String to Int](#string-to-int)
			- [String to Float](#string-to-float)
			- [Float to Int](#float-to-int)
	- [💻 Day 2: Exercises](#-day-2-exercises)
		- [Exercise: Level 1](#exercise-level-1)
		- [Exercise: Level 2](#exercise-level-2)
		- [Exercises: Level 3](#exercises-level-3)
# 📔 Day 2
## Loại dữ liệu
Dữ liệu được chia thành 2 loại:
1. Primitive data types (kiểu nguyên thủy)
2. Non-primitive data types(Object References - không nguyên thủy)

### Primitive data types (kiểu nguyên thủy)

Loại dữ liệu nguyên thủy trong Javascript bao gồm:

1. Number: Integers, floats
2. Strings: Chuỗi
3. Booleans: Giá trị true hoặc False
4. Null: Dữ liệu rỗng, không có giá trị
5. Undefined: Biến được khai báo không có giá trị
6. Symbol: Một giá trị duy nhật được tạo bởi symbol

### Non-primitive data types(Object References - không nguyên thủy)

Non-primitive data types bao gồm:

1. Object
2. Array

Các kiểu dữ liệu nguyên thủy là các kiểu dữ liệu bất biến (không thể sửa đổi). Khi chúng được khởi tạo và không được sửa đổi nó

**Ví dụ:**
```js
let word = 'JavaScript'
```
### Non-Primitive Data Types - kiểu dữ liệu không nguyên thủy

- Các kiểu dữ liệu không nguyên thủy có thể sửa đổi hoặc thay đổi 

**Ví dụ:**

```js
let nums = [1, 2, 3]
nums[0] = 10

console.log(nums)  // [10, 2, 3]
```
Như vậy cho thấy *Mảng* là kiểu dữ liệu không nguyên thủy có thể thay đổi được. Các loại dữ liệu không nguyên thủy không thể so sánh theo giá trị được. Ngay khi cả hai đều có chung thuộc tính và giá trị, chúng không hoàn toàn bằng nhau

```js
let nums = [1, 2, 3]
let numbers = [1, 2, 3]

console.log(nums == numbers)  // false

let userOne = {
name:'Jasson',
role:'Student',
country:'Viet Nam'
}

let userTwo = {
name:'Jasson',
role:'Student',
country:'Viet Nam'
}

console.log(userOne == userTwo) // false
```

