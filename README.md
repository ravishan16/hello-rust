
# [Getting Started with Rust](https://www.rust-lang.org/learn/get-started)

```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
# VSCode Rust Extensions

- [Trusty](https://marketplace.visualstudio.com/items?itemName=polypus74.trusty-rusty-snippets)
- [Rust Lang](https://marketplace.visualstudio.com/items?itemName=rust-lang.rust)

#Create Project
```
mkdir hello-rust
cd hello-rust
cargo init hello-rust
```

# Run Project
```
cargo run
```


# Adding Dependency

[Cargo.toml](Cargo.toml) - Add Dependecies
----------
```
[dependencies]
ferris-says = "0.1"
```

# Using ferries_says

[main.rs](src\main.rs) - Add Dependecies

```
extern crate ferris_says;

use ferris_says::say;
use std::io::{ stdout, BufWriter };

fn main() {
    let stdout = stdout();
    let out = b"Hello fellow Rustaceans!";
    let width = 24;

    let mut writer = BufWriter::new(stdout.lock());
    say(out, width, &mut writer).unwrap();
}
```

# Output

```
R🤡V @👽:~/c/g/hello-rust$ cargo run                                 
    Finished dev [unoptimized + debuginfo] target(s) in 0.02s
     Running `target/debug/hello-rust`
----------------------------
| Hello fellow Rustaceans! |
----------------------------
              \
               \
                  _~^~^~_
              \) /  o o  \ (/
                '_   -   _'
                / '-----' \
```