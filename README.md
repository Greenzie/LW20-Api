# LW20/SF20 API

## About

Visit http://www.lightware.co.za for more information about the products we provide.

## Supported Products

LW20/SF20

* Model: LW20
* Firmware: 1.0
* Software: 1.0

## Supported Platforms

Platform usage code implements communication layer, usses callback methods.

* Linux (32bit & 64bit), including Raspberry Pi.
* Windows (32bit & 64bit)
* Arduino
* ROS

## Overview

The layered structure of the API opens a variety of options for integration within your own application framework.
You can select a single layer to work with, or use components from each that accomplish your goals. Note: Not all
components can be mixed.

layers

* packet resolver
* packet builder
* event pump
* simple layer with callbacks
* transport layer

The event system requires continuous pumping and integrates into various architectural situations.
// Every command requires an event pump cycle to be managed to completion.
// If you have streaming commands, they can also be sent through. Otherwise they are ignored.
// You should hit the pump until you get COMPLETED.

By passing callbacks to your IO functions this layer will automatically manage the event loops.

This layer will handle all aspects of communication over various protocols & interfaces.
Usually for rapid prototyping. Most applications already have some internal communication structure in
place that they wish to use. Threading to allow for stream data capturing?

// If you don't have the memory to store a command buffer there is no harm in executing commands individually.
// Command buffers purely act as a convenience to manage a single pump cycle for sending multiple commands. 
// This is exactly what the config blocks use internally.

Sample Code
```c++
int main() {
}
```

This is a [Link](https://github.com) thing.

## Protocol

After issuing a request you must wait for a response before issuing the next request.


## License
**Unlicense (http://unlicense.org) **

This is free and unencumbered software released into the public domain.

Anyone is free to copy, modify, publish, use, compile, sell, or
distribute this software, either in source code form or as a compiled
binary, for any purpose, commercial or non-commercial, and by any
means.

In jurisdictions that recognize copyright laws, the author or authors
of this software dedicate any and all copyright interest in the
software to the public domain. We make this dedication for the benefit
of the public at large and to the detriment of our heirs and
successors. We intend this dedication to be an overt act of
relinquishment in perpetuity of all present and future rights to this
software under copyright law.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS BE LIABLE FOR ANY CLAIM, DAMAGES OR
OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,
ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.

For more information, please refer to <http://unlicense.org>