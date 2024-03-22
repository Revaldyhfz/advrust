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

### Commit 4

The purpose of the test is to illustrate the impact of a long-running operation (sleeping for 5 seconds in this case) on the server's responsiveness to other requests. When accessing the `/sleep` endpoint, the server intentionally delays the response by sleeping for 5 seconds. Subsequently, if a request is made to the `/` endpoint while the `/sleep` request is still processing, the `/` request will be queued and delayed until the `/sleep` request completes.

### Commit 5


In a multithreaded server utilizing a ThreadPool, the ThreadPool oversees a set number of worker threads, each persistently awaiting tasks. Upon receiving a job, a worker thread within the ThreadPool picks up the task, executes it, and then promptly becomes ready to process additional tasks. This framework optimizes the handling of concurrent operations by avoiding the need to spawn a new thread for every task, a process that can strain system resources. Instead, the ThreadPool efficiently manages worker threads, ensuring the server can handle multiple tasks simultaneously while maintaining resource efficiency.

### Bonus

The build function replaces the new function in initializing ThreadPool instances. It encapsulates the initialization logic, enhancing code organization and clarity while maintaining the same functionality as new.