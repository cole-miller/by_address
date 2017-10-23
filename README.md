# by_address

Rust wrapper type that implements hashing and comparison based on address
rather than value.

* [API Documentation](https://docs.rs/by_address)
* [crates.io package](https://crates.io/crates/by_address)
* [Source code](https://github.com/mbrubeck/by_address)

# Overview

`ByAddress` can be used to wrap any pointer type (i.e. any type that implements the Deref
trait).  This includes references, raw pointers, smart pointers like `Rc<T>`
and `Box<T>`, and specialized pointer-like type like `Vec<T>` and `String`.

The wrapped pointer implements the following traits based on the address of
its contents, rather than their value:

* Hash
* Eq, PartialEq
* Ord, PartialOrd

## no_std

This crate does not depend on libstd, so it can be used in [`no_std`][3]
projects.

[`no_std`]: https://doc.rust-lang.org/book/no-stdlib.html

## License

Licensed under the Apache License, Version 2.0 or the MIT license, at your
option.  See the license files in this directory for details.
