# CURL Wrapper (Requests.hpp)

### About

This is a a C++ wrapper for libcurl that provides a cleaner scripting interface and support for asynchronous requests.

It works on a RAII basis and hides any raw pointers exposed by the CURL library through the use of encapsulation. It also provides several utility functions such as checking the status of a request.

If you find a bug or have a feature-request, please raise an issue.

### Example

```cpp
(On program start ...)
Networking::Requests::Init();

(Runtime...)
auto message = Networking::Requests::Client(query);
message.Set(CURLOPT_TIMEOUT, 20);

auto response = message.Send();

(Finalisation...)
Networking::Requests::Dispose();
```

### Dependencies

#### [libcurl](https://curl.se/libcurl/)

### Instructions

The implementation is header-only and written in templated C++17. You should need not need to make any adjustments to your project settings or compiler flags. 

Simply include the header and dependencies in your project and you are ready to start!