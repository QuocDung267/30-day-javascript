
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
country:'VietNam'
}

let userTwo = {
name:'Jasson',
role:'Student',
country:'VietNam'
}

console.log(userOne == userTwo) // false
```
Không so sánh được các loại dữ liệu không nguyên thủy, không được phép so sánh mảng, hàm và các đối tượng với nhau. Các giá trị không nguyên thủy được gọi là các loại tham chiếu, vì chúng được so sánh theo tham chiếu thay vì giá trị, Hai đối tượng chỉ hoàn toàn bằng nhau nếu chúng đề cập đến cùng một đối tượng cơ bản.

```js
let nums = [1, 2, 3]
let numbers = [1, 2, 3]

console.log(nums == numbers)  // false

let userOne = {
name:'Jasson',
role:'Student',
country:'Finland'
}

let userTwo = {
name:'Jasson',
role:'Student',
country:'VietNam'
}

console.log(userOne == userTwo) // false
```
## Number

Số là số nguyên và giá trị thập phân có thể thực hiện tất cả các phép toán số học.

```js
let age = 35
const gravity = 9.81  // we use const for non-changing values, gravitational constant in  m/s2
let mass = 72         // mass in Kilogram
const PI = 3.14       // pi a geometrical constant

// More Examples
const boilingPoint = 100 // temperature in oC, boiling point of water which is a constant
const bodyTemp = 37      // oC average human body temperature, which is a constant

console.log(age, gravity, mass, PI, boilingPoint, bodyTemp)
```
## Math object

Math Object cung cấp rất nhiều phương thức để làm việc với các con số.

```js
const PI = Math.PI

console.log(PI)                            // 3.141592653589793

// Rounding to the closest number
// if above .5 up if less 0.5 down rounding

console.log(Math.round(PI))                // 3 to round values to the nearest number

console.log(Math.round(9.81))              // 10

console.log(Math.floor(PI))                // 3 rounding down

console.log(Math.ceil(PI))                 // 4 rounding up

console.log(Math.min(-5, 3, 20, 4, 5, 10)) // -5, returns the minimum value

console.log(Math.max(-5, 3, 20, 4, 5, 10)) // 20, returns the maximum value

const randNum = Math.random() // creates random number between 0 to 0.999999
console.log(randNum)

// Let us  create random number between 0 to 10

const num = Math.floor(Math.random () * 11) // creates random number between 0 and 10
console.log(num)

//Absolute value
console.log(Math.abs(-10))      // 10

//Square root
console.log(Math.sqrt(100))     // 10

console.log(Math.sqrt(2))       // 1.4142135623730951

// Power
console.log(Math.pow(3, 2))     // 9

console.log(Math.E)             // 2.718

// Logarithm
// Returns the natural logarithm with base E of x, Math.log(x)
console.log(Math.log(2))        // 0.6931471805599453
console.log(Math.log(10))       // 2.302585092994046

// Returns the natural logarithm of 2 and 10 respectively
console.log(Math.LN2)           // 0.6931471805599453
console.log(Math.LN10)          // 2.302585092994046

// Trigonometry
Math.sin(0)
Math.sin(60)

Math.cos(0)
Math.cos(60)
```
## String

Các chuỗi là các văn bản, nằm dưới trích dẫn dấu ngoặc , kép , đánh dấu ngược `` . Để khai báo một chuỗi, chúng ta cần một tên biến, toán tử gán, một giá trị trong dấu nháy đơn, nháy kép hoặc nháy ngược. Hãy xem một số ví dụ về chuỗi:

```js
let space = ' '           // an empty space string
let firstName = 'Jasson'
let lastName = 'Yetayeh'
let country = 'Finland'
let city = 'Helsinki'
let language = 'JavaScript'
let job = 'teacher'
let quote = "The saying,'Seeing is Believing' is not correct in 2020."
let quotWithBackTick = `The saying,'Seeing is Believing' is not correct in 2020.`
```
### Nối chuỗi

Kết nối hai hoặc nhiều chuỗi với nhau được gọi là nối. Sử dụng các chuỗi đã khai báo trong phần Chuỗi trước đó:

```js
let fullName = firstName + space + lastName; // concatenation, merging two string together.
console.log(fullName); // Jasson V
```

#### Chuỗi ký tự dài

Một chuỗi có thể là một ký tự hoặc một đoạn hoặc một trang. Nếu chiều dài chuỗi quá lớn, nó không vừa với một dòng. Chúng ta có thể sử dụng ký tự gạch chéo ngược (\) ở cuối mỗi dòng để chỉ ra rằng chuỗi sẽ tiếp tục ở dòng tiếp theo. Ví dụ:

```js
const paragraph = "My name is Asabeneh Yetayeh. I live in Finland, Helsinki.\
I am a teacher and I love teaching. I teach HTML, CSS, JavaScript, React, Redux, \
Node.js, Python, Data Analysis and D3.js for anyone who is interested to learn. \
In the end of 2019, I was thinking to expand my teaching and to reach \
to global audience and I started a Python challenge from November 20 - December 19.\
It was one of the most rewarding and inspiring experience.\
Now, we are in 2020. I am enjoying preparing the 30DaysOfJavaScript challenge and \
I hope you are enjoying too."

console.log(paragraph)
```

#### Trình tự thoát trong chuỗi

Trong JavaScript và các ngôn ngữ lập trình khác \ theo sau bởi một số ký tự là một chuỗi thoát. Hãy xem các ký tự thoát phổ biến nhất:

- \n: dòng mới
- \t: Tab, có nghĩa là 8 dấu cách
- \\\\: Dấu gạch chéo ngược
- \\': Dấu nháy đơn (')
- \\": Trích dẫn kép (") 