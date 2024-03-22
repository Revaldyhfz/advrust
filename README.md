# Rust Webserver

## Module 6

### Commit 1

The handle_connection method reads lines from a `TcpStream` using a `BufReader`, which helps in efficient reading by buffering the input. It collects the lines until it encounters an empty line, indicating the end of the HTTP headers. The collected HTTP request is then printed to the console.

This method also handles potential errors that may occur during reading from the stream or unwrapping lines. It's typically used in the context of building an HTTP server to handle incoming connections and process HTTP requests efficiently.

### Commit 2

![Commit 2](/assets/images/commit2.png)