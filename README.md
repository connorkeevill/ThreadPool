ThreadPool
==========

A simple C++17 Thread Pool implementation.

Basic usage:
```c++
// create thread pool with 4 worker threads
ThreadPool pool(4);

// enqueue and store future
auto result = pool.enqueue([](int answer) { return answer; }, 42);

// get result from future
std::cout << result.get() << std::endl;

```

**Note:** this repo is essentially as the [original forked repo](https://github.com/progschj/ThreadPool), 
but has been updated to remove the deprecated std::result_of method and replace it with the (now recommended)
std::invoke_result method.
