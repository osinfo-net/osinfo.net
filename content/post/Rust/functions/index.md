+++
author =  "Héctor Ruiz"
title =  "Functions"
date = "2022-09-18"
description = "In this article we will cover basic functions in Rust"
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
## Simple functions

In Rust we can create multiple functions apart from the main one. Here is a little example of how to do it:

```rust
fn main() {
	printn!("Hey, how are you doing!")

	hello_friend(); // We are calling a function called hello_there
}

fn hello_there() {  // We've created a new function called hello_there
	println!("Hello my friend!");
}
```
> Rust code uses snake case as the conventional style. This means all lowercase and underscore separated words.

## Parameterized functions
Functions can have parameters. Parameters or arguments are variables that are only in the scope of the function code. This means it cannot be accessed anywhere outside the function block. The arguments values are provided by the script.
```rust
fn main() {
	println!("Let's do some functions");
	addition(5);
}

fn addition (x: u32) {
	println!("The values is: {}", x);
}

```
> When we use arguments, we must specify the argument data type.
