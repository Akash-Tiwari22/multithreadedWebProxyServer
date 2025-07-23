# Multithreaded Web Proxy Server in C

A high-performance multithreaded HTTP proxy server implemented in C using POSIX threads, semaphores, and socket programming. It handles multiple client requests concurrently and caches web responses using an LRU (Least Recently Used) strategy to optimize performance and reduce network traffic.

---

## 🔧 Features

- Handles multiple concurrent HTTP GET requests using POSIX threads.
- Uses semaphores for safe thread synchronization.
- Implements an LRU cache to store and serve repeated web responses.
- Parses and forwards HTTP requests to the target server.
- Logs client-server interactions for debugging and analysis.
- Basic website filtering and IP masking functionality.

---

## 🧠 Concepts Covered

- Multithreading with `pthread_create`, `pthread_join`, and `pthread_exit`
- Thread synchronization using `semaphore.h`
- Socket programming with `bind`, `listen`, `accept`, and `connect`
- Memory-safe buffer handling and linked list cache management
- Operating System fundamentals: concurrency, locking, IPC

---

## 🚀 How It Works

1. The server listens on a specified port for incoming client connections.
2. For every new client, a new thread is spawned to handle its request.
3. Requests are parsed and forwarded to the destination web server.
4. Responses are cached using an LRU algorithm.
5. Cached responses are served directly to reduce latency and bandwidth.

---

📉 Limitations
Only supports HTTP GET requests (not POST or HTTPS).

Fixed cache size and memory limit.

Some dynamic websites may not render completely from cache.

 Future Improvements
Add HTTPS support with TLS/SSL.

Implement support for POST and other HTTP methods.

Add configurable domain filtering and request logging.

Use multiprocessing with shared memory for better scalability.


🙌 Acknowledgments
This project was inspired by coursework in Operating Systems and Networking(Applied OS by Lovepreet ), and serves as a practical exercise in understanding real-world concurrency, thread safety, and caching systems.

