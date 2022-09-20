# UART C++ Class Component for ESP-IDF

## Requirements
ESP-IDF 4.4 and higher.

[pl_common](https://github.com/plasmapper/common-esp-cpp) component.

## Installation
Add this to `main/idf_component.yml`:
```yaml
dependencies:
  pl_uart:
    path: component
    git: https://github.com/plasmapper/uart-esp-cpp.git
```
Add this to the source code:
```C++
#include "pl_uart.h"
```
Add `extern "C"` to `app_main` in `main.cpp`:
```C++
extern "C" void app_main(void) {...}
```

## Features
1. UART port class.
2. UART server class. 

## Examples
[UART port](examples/port)  
[UART echo server](examples/echo_server)

## Documentation
[Documentation](https://plasmapper.github.io/esp-cpp/uart)