# tokio_scgi

This is a Rust library which implements support for building [SCGI](https://python.ca/scgi/) servers and clients. It comes in the form of a Tokio Codec which can be used in asynchronous code, but it can also be invoked directly in synchronous or non-Tokio code.

SCGI is a [simple and efficient](http://python.ca/scgi/protocol.txt) protocol for communicating between frontend web servers and backend applications over a TCP or local Unix socket. It compares (favorably) to [FastCGI](https://en.wikipedia.org/wiki/FastCGI), another protocol with a similar purpose. This library provides support for writing both SCGI servers and clients in Rust, with support for both TCP and Unix sockets.

For usage information and working client/server examples, see [the project README and repo](https://github.com/nickbp/tokio-scgi).

## async/await

The tokio-scgi 0.2.0 release switches the client/server examples to using async/await. There have been no changes to the SCGI codecs themselves, and they do not require async/await.

Building the examples provided with tokio-scgi 0.2.0 therefore requires Rust 1.39.0 or newer, while the codecs themselves do not. If you regardless want to compile the examples with an older version of Rust, then you can use tokio-scgi 0.1.0, and the codecs themselves will be the same. However any future changes to the codecs will be against the 0.2.0 tree.
