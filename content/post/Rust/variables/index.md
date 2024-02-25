+++
author =  "Héctor Ruiz"
title =  "Variables, constants and shadowing"
date = "2022-09-18"
description = "In this article we will cover variables, constants and a rust concept called shadowing"
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
title = "GitHub OS Info"
description = "OS Info github account."
website = "https://github.com/osinfo-net"
image = "https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png"

[[links]]
title = "GitHub IT-Noobie"
description = "Main contributor of Rust pages."
website = "https://github.com/IT-Noobie"
image = "it-noobie.png"

+++

## Variables
Variales are names given to computer memory location where your store data in a program. In Rust, we define variables with `let`:
```rust
fn main() {
	let name = "osinfo";
	let number: u32 = 1;
	let array = [1,2,3,4];
}
```
In Rust we have two types of variables which are:
* **Immutable variables**: Default behaviour, you can't modify its value.
* **Mutable variables**: You can modify the value of the variable.
```rust
fn main () {
	let a: i32 = -5;     // Immutable variable
	let mut b: u32 = 9;  // Mutable variable
}
```
> You have to specify `mut` to make variables mutable.
---

## Constants
Constants are variables that can't be converted to mutable by design and have an explicit data type.
```rust
fn main () {
	const MAX_POINT: i32 = -5;    
}
```
> Constants must be written in uppercase by convention.
---
## Shadowing
Shadowing is a Rust concept of assigning a new value to an immutable variable. With an example is easier to understand:

```rust
fn main () {
	let x: u32 = 4;
	let x: u32 = x +1
	
	println!("The value of x is: {}", x);
}
```
Rust programmers say that the first variable declaration is being shadowed by the second. 

###  Shadowing vs Mutable variables
* Without using `let`, script will fail.
* You can only do certain transformations:
	* Change data type.
	* Change value adressing the previous value.
	* ...
* After a modification has been made, the variable will remain immutable.

