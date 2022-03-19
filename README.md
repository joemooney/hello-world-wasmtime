# Hello World in wasm Using wasmtime

`https://docs.wasmtime.dev/tutorial-create-hello-world.html`

* WebAssembly major goal: be close to native code in terms of performance


## Install

```
  rustup target add wasm32-wasi
  curl https://wasmtime.dev/install.sh -sSf | bash
  # these are added to your ~/.bashrc
  export WASMTIME_HOME="$HOME/.wasmtime"
  export PATH="$WASMTIME_HOME/bin:$PATH"
```

## Build

```
  cargo new hello-world-wasmtime
  cd hello-world-wasmtime/
  cargo build --target wasm32-wasi
```

## Run

```
  wasmtime target/wasm32-wasi/debug/hello-world-wasmtime.wasm 
```
