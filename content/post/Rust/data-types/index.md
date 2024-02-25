+++
author =  "Héctor Ruiz"
title =  "Data types"
date = "2022-09-18"
description = "In this article we will Rust data types and how they behave"
tags = [ 
    "practitioner",
	"code"
]
categories = [
    "Rust"
]
series = ["Themes Guide"]
image = "rust.jpg"

[[links]]
title = "GitHubi OS Info"
description = "GitHub is the world's largest software development platform."
website = "https://github.com/osinfo-net"
image = "https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png"

[[links]]
title = "GitHub IT-Noobie"
description = "GitHub is the world's largest software development platform."
website = "https://github.com/IT-Noobie"
image = "it-noobie.png"
+++

## Data types subsets
Rust is statically typed language. This means that Rust must know the type of all variables at compile time. It's not always necessary to explictly mark the data type.
> Rust compiler can normally infer which type we want to use, **but it's a good practice to do it**.

Rust is composed from two subsets of data types:
* **Scalar**
* **Compound** 
---
### Scalar
Scalar subset could be simplified as **single values data types**. Scalar data types are the following:
* **Integer**
* **Float**
* **Boolean**
* **Char**

#### Integer
An integer is a number without fractional component. Inside integer there are two types:
* **Signed**: They are always positive.
* **Unsigned**: They can be positive or negative.

You can differenciate them in a very simple way. If you have to write this number on paper, **do you need to write the sign?** 

- If it's **yes**, well it's a **signed integer**. 

- If not, then it's a **unsigned integer**.
```rust
fn main() {
	let x: i32 = -5; // Needs a sign, then signed
	let y: u64 = 5;  // It doesn't need a sign, then unsigned
}
```

##### Types of Integer


   Length | Signed  | Unsigned
----------|---------|---------
  8-bit   | i8      | u8
 16-bit   | i16     | u16
 32-bit   | i32     | u32
 64-bit   | i64     | u64
   arch   | isize   | usize

#### Floating-Point
Floating point are numbers with decimal points.
```rust
fn main() {
	let x: f32 = 3.14;
}
```
##### Types of Floating-Point

  Length | Floating type      
---------|--------------
  32-bit | f32     
  64-bit | f64 

#### Boolean
Boolean it's a data type that can be either true or false.
```rust
fn main() {
	let check: bool = false;
}
```

#### Char
Char, which is different from strings, is the language's most primitive alphabetic type and it's specified with simple quotes.
```rust
fn main() {
	let char = 's';
	let emoji = '🐧';
}
```
> It can also represent Chinese, Japanese, Korean, emoji and zero-width spaces.
---
### Compound
Compound data types are those that can group multiple data types. Rust, with no crates, have two types:
* **Tuple**
* **Arrays**

#### Tuple
A tuple, also known as vector, is a general way to group values with different data types.
 ```rust
fn main() {
	let tup: (i32, u64, f32) = (-500, 4, 8.3);

	// Ways to access to tuple values
	let first  = tup.0;
	let second = tup.1;
	let (first, second, third) = tup; 
}
 ```

#### Arrays
The difference between arrays and tuples is that, in arrays, **data types must be the same**.
```rust
fn main () {
	let array: i64 = [1, 2, 3, 4];

	// Access array values
	let first  = array[0];
	let second = array[1];
}
```
