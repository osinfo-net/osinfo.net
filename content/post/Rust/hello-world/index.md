+++
author =  "Héctor Ruiz"
title =  "Hello Rust!"
date = "2022-09-15"
description = "Hello world on Rust"
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

Welcome beginner to this bravefull journey. You've started learning Rust and as any other programming language you have to start with hello world!

## Simple way
You'll have to create a file. We will called it `hello_world.rs`:
```bash
touch hello_world.rs
```

Next we will write our first Rust script. To run a Rust script, everything must be inside the main function:

```rust
fn main() {
    println!("Hello world");
}
```
And that's it, we've created our first Rust script. To run it we will have to compile it first and then execute it. To do so, run:
```bash
rustc hello_world.rs \ # This will generate a binary called hello_world
./hello_world             # This will run the binary
```

## The right way
We, rustians, create packages with cargo. Cargo is a powerful tool you'll use compile, build, check and more stuff that will make your life easier.
First, we create a new Rust project:
```bash
cargo new hello_cargo --bin
```
This will create a new folder called hello_cargo. Inside we will found several files and folder, but we will just ignore it this time.
Next we will go to `src/` directory. There we should see a script called `main.rs`. You should see that this script already has a hello world script:
```rust
fn main() {
    println!("Hello, world!");
}
```
We will run the following command to build and run our code:
```bash
cargo run
    Finished dev [unoptimized + debuginfo] target(s) in 0.00s
     Running `debug/hello_cargo`

