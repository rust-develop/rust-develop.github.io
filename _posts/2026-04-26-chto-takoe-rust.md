---
layout: post
title: "What is Rust and Why Should You Learn It?"
date: 2026-04-26 12:00:00 +0300
categories: [rust, introduction]
tags: [rust, programming, introduction, beginner]
---

Rust is a systems programming language created at Mozilla Research and released in 2015. It is designed around three core principles: **safety**, **speed**, and **concurrency**.

## Why Rust?

Most systems languages like C and C++ give developers full control over memory, but with that comes full responsibility for bugs — memory leaks, use-after-free errors, data races. Rust solves these problems at the compiler level, without a garbage collector.

> "Rust is the most loved programming language" — Stack Overflow Developer Survey, 6 years in a row.

## Key Features

### 1. Ownership System

Every value in Rust has a single owner. When the owner goes out of scope, the memory is automatically freed:

```rust
fn main() {
    let s = String::from("Hello, Rust!");
    println!("{}", s);
} // s goes out of scope — memory is freed automatically
```

### 2. Borrowing

Instead of copying data, you can borrow a reference:

```rust
fn print_string(s: &String) {
    println!("{}", s);
}

fn main() {
    let s = String::from("Rust");
    print_string(&s); // pass a reference, not ownership
    println!("{}", s); // s is still available here
}
```

### 3. Speed like C/C++

Rust compiles to machine code with no garbage collector — performance matches C and C++.

### 4. Zero-cost Abstractions

High-level code compiles to the same machine code as hand-written low-level code.

## Where Is Rust Used?

- **System software** — operating systems, drivers, embedded firmware
- **WebAssembly** — fast code running in the browser
- **Networking** — high-performance servers and proxies
- **CLI tools** — fast command-line utilities
- **Game engines** — safe and performant game logic

## Who Uses Rust?

- **Linux kernel** — officially accepted as the second language for kernel development
- **Mozilla** — parts of the Firefox Gecko engine
- **Microsoft** — Windows components rewritten in Rust
- **Google** — Android, ChromeOS
- **Amazon** — AWS Firecracker hypervisor for Lambda

## Getting Started

Install Rust with one command:

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

Verify the installation:

```bash
rustc --version
cargo --version
```

Create your first project:

```bash
cargo new hello_rust
cd hello_rust
cargo run
```

This generates a `main.rs` file:

```rust
fn main() {
    println!("Hello, world!");
}
```

## Summary

Rust lets you write reliable, fast code without fear of memory bugs. If you want to explore systems programming or just try something new and powerful — Rust is an excellent choice.

In upcoming posts, we will dive deeper into the ownership system. Stay tuned!
