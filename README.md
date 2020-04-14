Minimalistic kernel built in rust following [Phil Opp blogs](https://os.phil-opp.com/freestanding-rust-binary/)


Utility commands

`rustup target add thumbv7em-none-eabihf`

// Nightly rust toolchain

`rustup override add nightly`

// Build for out carge

`cargo build --target x86_64-rust_os.json`

// Install cargo xbuild to cross compile

cargo install cargo-xbuild

// If you don't have src (used by the cargo xbuild)

rustup component add rust-src

// build with xcargo

cargo xbuild --target x86_64-rust_os.json

// with the .cargo/config

cargo xbuild

// From the root dir run 

qemu-system-x86_64 -drive format=raw,file=target/x86_64-rust_os/debug/bootimage-rust_os.bin

//with the .cargo/config

cargo xrun
