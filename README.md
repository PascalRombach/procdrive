# procdrive
Procdrive is a procedural wrapper around 
[`py-easydrive`](https://github.com/PascalRombach/py-easydrive)
which is itself a wrapper around [`py-drivesdk`](https://github.com/HHG-TecLap/py-drivesdk).

This library was developed to provide a practical environment for learning Python.
Procdrive aims to be simple and intuitive and a transition into more complicated language constructs
such as object orientation and exception handling.

## Limitations
Since Procdrive is not object-oriented, it does not provide support 
for controlling multiple vehicles at the same time.
If you require this functionality you should check out the other libraries mentioned above.

## Installation
### Linux
```sh
python3 -m pip install procdrive
```
### Windows
```sh
py -m pip install procdrive
```

## Code Example
Coding in procdrive is very simple. 
The following code scans the current map in and then reports the track pieces in order.
```py
from procdrive import *

connect()
scan()

set_speed(300)
while True:
    print(wait_for_track_change())
```