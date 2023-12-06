nusb
----

A new pure-Rust library for cross-platform low-level access to USB devices.

[Documentation](https://docs.rs/nusb)

### Compared to [rusb](https://docs.rs/rusb/latest/rusb/) and [libusb](https://libusb.info/)

* Pure Rust, no dependency on libusb or any other C library.
* Async-first, while not requiring an async runtime like `tokio` or
  `async-std`. Still easily supports blocking with
  `futures_lite::block_on`.
* No context object. You just open a device. There is a global event loop thread
  that is started when opening the first device.
* Thinner layer over OS APIs, with less internal state.

### :construction: Current status

* Support for Linux, Windows, and macOS
* Control, bulk and interrupt transfers work
* Minimally tested: please test with your device and report issues

### License
MIT or Apache 2.0, at your option
