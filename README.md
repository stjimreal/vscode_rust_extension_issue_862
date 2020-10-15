<!--
 * @Date: 2020-10-15 22:07:20
 * @LastEditors: LIULIJING
 * @LastEditTime: 2020-10-15 22:27:43
-->

# The VS Code Rust extension is parsing infinitely when using Cargo's workspace traits

## How to start the infinite loop?

Several Needs:

- Make sure your Rust project is running on `VS Code`.
- The `VS Code Extension` is `Rust 0.7.8` and make sure it is running stably.

In `cycle-tree/Cargo.toml`:

```Rust
[dependencies]
weak-ref = {path = "../weak-ref"}
```

`Comment` the last line by adding `#` at the beggining like this:

```Rust
[dependencies]
#weak-ref = {path = "../weak-ref"}
```

> Now your latest version Rust Extension is running infinitely.

## How to stop it?

`Uncomment` the last line.

> You can try the issue in any `Crates` or  as you like.