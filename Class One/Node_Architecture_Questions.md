# Architecture Questions
**1. How does Node.js handle multiple concurrent connections despite being single-threaded?**
Node.js handles multiple concurrent connections via its event loop and non-blocking I/O.

> Despite being single-threaded, it doesn't wait for I/O operations (like database queries or file reads) to complete. Instead, when an I/O request is made, it's offloaded to the operating system. Node.js's event loop then continues processing other tasks. Once the I/O operation finishes, it triggers a "callback" function, which is then executed by the event loop. This allows it to manage thousands of simultaneous connections efficiently without blocking the main thread.
>

**2. Explain the concept of non-blocking I/O in Node.js and provide an example of when it's beneficial.**

- Non-blocking I/O in Node.js means operations (like reading files, network requests) don't stop the main program execution to wait for completion. Instead, Node.js initiates the operation and immediately moves on to other tasks. Once the I/O is done, it triggers a callback function.

- Benefit Example: Imagine a web server handling many user requests for data from a slow database. With non-blocking I/O, the server can request data for User A, immediately start processing User B's request, and then efficiently handle User A's data when it finally arrives, without any user experiencing delays due to others. This prevents the server from freezing.

**3. What is the event-driven architecture in Node.js and how does it contribute to its efficiency?**

- The event-driven architecture in Node.js means it reacts to "events" rather than following a linear flow. When an asynchronous operation (like a file read or network request) finishes, it emits an "event." Node.js then executes a corresponding "callback function" that was set up to listen for that event.


- This contributes to efficiency because the single main thread (the event loop) never idles waiting. It constantly processes events from a queue. This non-blocking nature allows Node.js to handle many concurrent operations with minimal overhead, making it highly efficient for I/O-bound tasks.