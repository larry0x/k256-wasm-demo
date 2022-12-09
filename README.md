# k256-wasm-demo

Building this contract to `wasm32-unknown-unknown` target

```bash
cargo build --target wasm32-unknown-unknown
```

Should result in the following error:

```plain
   Compiling subtle v2.4.1
   Compiling cfg-if v1.0.0
   Compiling zeroize v1.5.7
   Compiling const-oid v0.9.1
   Compiling base64ct v1.5.3
   Compiling base16ct v0.1.1
   Compiling typenum v1.16.0
   Compiling serde v1.0.149
   Compiling crunchy v0.2.2
   Compiling serde_json v1.0.89
   Compiling itoa v1.0.4
   Compiling generic-array v0.14.6
   Compiling ryu v1.0.11
   Compiling thiserror v1.0.37
   Compiling schemars v0.8.11
   Compiling dyn-clone v1.0.9
   Compiling getrandom v0.2.8
   Compiling hex v0.4.3
error: the wasm32-unknown-unknown target is not supported by default, you may need to enable the "js" feature. For more information see: https://docs.rs/getrandom/#webassembly-support
   --> /Users/larry/.cargo/registry/src/github.com-1ecc6299db9ec823/getrandom-0.2.8/src/lib.rs:263:9
    |
263 | /         compile_error!("the wasm32-unknown-unknown target is not supported by \
264 | |                         default, you may need to enable the \"js\" feature. \
265 | |                         For more information see: \
266 | |                         https://docs.rs/getrandom/#webassembly-support");
    | |________________________________________________________________________^

   Compiling static_assertions v1.1.0
error[E0433]: failed to resolve: use of undeclared crate or module `imp`
   --> /Users/larry/.cargo/registry/src/github.com-1ecc6299db9ec823/getrandom-0.2.8/src/lib.rs:290:5
    |
290 |     imp::getrandom_inner(dest)
    |     ^^^ use of undeclared crate or module `imp`

   Compiling byteorder v1.4.3
For more information about this error, try `rustc --explain E0433`.
error: could not compile `getrandom` due to 2 previous errors
warning: build failed, waiting for other jobs to finish...
```
