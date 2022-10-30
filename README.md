# cutest
C single header file testing framework.


## Usage

```C
#include "cutest.h"


void
test_demo() {
    /* Integer */
    eqint(7, 7);
    
    /* Bool */
    eqbool(true, true);
    istrue(true);
    isfalse(false);
  
    /* Character */
    eqchr('a', 'a');
    eqstr("foo", "foo");
    eqnstr("foo", "foo", 3);
  
    /* Binary */
    eqbin("foo\0bar", "foo\0bar");
}


int main() {
    test_demo();
    return EXIT_SUCCESS;
}
```

## Build & Install

```bash
mkdir build
cd build
cmake ..
make
```

### Install with makefile

```bash
cd build
make install
```


### Create debian package

```bash
cd build
cpack
```

After that, `libcutest-*.deb` will be generated insode the `build` directory.

#### Install using debian package

```bash
cd build
sudo dpkg -i libcutest-*.deb
```

##### Uninstall

```bash
sudo dpkg -P libcutest
```

Or

```bash
sudo apt remove libcutest
```
