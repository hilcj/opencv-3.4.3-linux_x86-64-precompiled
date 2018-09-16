# Precompiled opencv for Bazel

This is a precompiled version of OpenCV-3.4.3 for Bazel build with C++ language.

Binaries files included, use at your own risk!

Refer to Bazel @ https://bazel.build/

Add below paragraph to your WORKSPACE:

```
...

git_repository(
    name = "opencv_3_4_3_linux_x86_64_precompiled",
    commit = "79873865dc471da6548c692f8fff665339121ca9",
    remote = "https://github.com/hilcj/opencv-3.4.3-linux_x86-64-precompiled.git",
)

...
```

Running example:

MyFile.h

```
...
#include "opencv2/opencv.hpp"
...
```

BUILD

```
...
deps = ["@opencv_3_4_3_linux_x86_64_precompiled//:core"]
...
```


## Note
Known conflict with Google ProtoBuf. To solve the conflict, you may use some C++ #define macros to do the trick.

```
...
#define int64 int64_opencv
#define uint64 uint64_opencv
#include "opencv2/opencv.hpp"
#undef int64
#undef uint64
...
```
