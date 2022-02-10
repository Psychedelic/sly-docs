---
date: "1"
---
# SLY - Installing SLY

## SLY - Installing SLY


## Manual Installation

To install SLY manually, you can clone the repository:

```
git clone git@github.com:Psychedelic/sly.git
```

Then build it locally

```
cargo build
```

And then the target binary will be available in the following route (from the project's root)

```
target/debug/sly
```

## Installing from Cargo

Currently, SLY is in alpha version, and you need to install it from source code, but because Rust is awesome, you can do that by simply running cargo:

```
cargo install sly-cli
```

> We will release binary releases as soon as SLY is out of alpha.
