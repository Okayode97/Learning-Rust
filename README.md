# Learning Rust

This repo was made to detail my notes and example projects i made, while trying to learn Rust.


I found these resources to be very useful and my notes are largely based on them.
- [Learning-rust.github.io](https://learning-rust.github.io/docs/index.html)
- [The Rust Programming Languages](https://doc.rust-lang.org/book/title-page.html)
- [Rust Programming Course for Beginners: FreeCodeCamp.org](https://www.youtube.com/watch?v=MsocPEZBd-M)


<br>

## **Installing Rust**
- [Download rustup](https://www.rust-lang.org/tools/install)
- [Install visual studio C++ build tools](https://visualstudio.microsoft.com/visual-cpp-build-tools/)
  - Desktop development with C++
  - C++ Clang-cli for v142 build tools
  - C++ Clang compiler for windows.

Check rust installation by running 
```
rustc --version
```

<br>

## **Rust Overview**
Rust is a compiled programming langauage, meaning it features a compiler (rustc) which converts the source code into a machine code (a binary execuatable file). It support different programming paradigms (functional, object orientated, etc...)

<br>

Rust tooling ecosystem
- Rustc: Compiler which takes the Rust code and compiles it nto a binary executable file
- rustup: Comandline utility to install and update Rust
- cargo: Rust build system and package manager. I like to think of it as rust's version of pip.

Linters
- rustfmt & cargo-fmt: lints project againt rust style guidelines
- cargo-clippy: extra checks for mistakes and stylistic choice
  
Documenation
- rustdoc: Copy of Rust documentation

<br>

**Creating a new rust project using cargo**
```
cargo new PROJECT_NAME
```
This would create a new boiler plate rust project defined aa a git repository. The project directory contains the cargo.toml file which manages the project metadata and the src/main.rs file which would be the default entry point for the application.

<br>

**Running Rust Code**
```
cargo run
```
Within the main rust project directory, calling cargo run would compile the src/main.rs file, creating a binary executable file. The executable file is then ran.

Alternative
```
rustc src/main.rs
main.exe
```
using rustc the binary file is created by passing in the rust file to compile and then the executable file is then called by the user to run it.

<br>

**Defining Functions**
```rust
fn function_name(){

}
```
Functions are defined using the fn keyword and the naming convention follows the snake_case

<br>

**Mini introduction to macros and metaprogramming**
>macros are a way of writing code that writes other code

Macros in Rust are denoted with ! as seen with 
```rust
println!("Walloo)
vec!()
```
So... how are they different from functions aren't they just built in functions in Rust? Key differences
- Functions must have clearly defined arguments, while marcos can take in a number of arguments
- macros definitions are must more complex than function definitions
- macros must be defined before they are called, unlike functions which can be defined and called anywhere

<br>

**Comments**
```rust
//This is an example of a comment

/*
This is an example of a block comment
*/
```

**Printing Text and Formatting**

