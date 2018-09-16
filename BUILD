cc_library(
    name = "core",
    srcs = glob(["lib/*.so*"]) + glob(["lib64/*.so*"]),
    hdrs = glob(["include/**/*.hpp"]) + glob(["include/**/*.h"]),
    includes = ["include"],
    visibility = ["//visibility:public"], 
    linkstatic = 1,
)
