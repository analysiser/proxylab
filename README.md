# ProxyLab #

For an assignment in a course at CMU (15-213 Introduction to Computer Systems) myself and one partner wrote a multi-threaded caching proxy server in C. The server used basic Unix socket functions to accept requests from clients, and for each request spawned a separate thread to handle that request. Requests to the third-party server were also made using basic socket functions rather than any library such as `cURL`. This involved a lot of string parsing and manual header management. Once completed, one could connect to the server and use it as an HTTP proxy to browse the web. The performance increase from the cache was quite noticable.

The server cached responses in a global in-memory cache. As the cache was global to all threads, this assignment involved a lot of creating thread-safe code and debugging difficult concurrency issues. Reader / writer locks on the cache were handled using the `pthreads` library.

Although I wish I could post the code here, the academic integry policy at CMU prevents me from doing so. However, if you are a potential employer or someone else with a valid reason to view my code for this assignment, please contact me personally and I'd be happy to provide it to you.
