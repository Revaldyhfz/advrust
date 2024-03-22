# Rust Webserver

## Module 6

### Commit 1

The handle_connection method reads lines from a `TcpStream` using a `BufReader`, which helps in efficient reading by buffering the input. It collects the lines until it encounters an empty line, indicating the end of the HTTP headers. The collected HTTP request is then printed to the console.

This method also handles potential errors that may occur during reading from the stream or unwrapping lines. It's typically used in the context of building an HTTP server to handle incoming connections and process HTTP requests efficiently.

### Commit 2

![Commit 2](/assets/images/commit2.png)

### Commit 3

Refactoring is crucial to streamline code and enhance readability. In this case, the refactoring aims to eliminate repetition by consolidating the differences into distinct if and else blocks. These blocks handle similar tasks of reading files and writing their contents to the stream. By isolating the discrepancies in status line and filename, the code becomes more concise and easier to maintain. This approach adheres to the principle of DRY (Don't Repeat Yourself), fostering modular and error-resistant code.

![Commit 3](/assets/images/commit3.png)