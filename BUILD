# load("@rules_cc//cc:cc_library.bzl", "cc_library")

cc_library(
    name = "a",
    srcs = ["a.cc"],
    hdrs = ["a.h"],
    defines = ["I_AM_A"],
    deps = [":b"],
)

cc_library(
    name = "b",
    hdrs = ["b.h"],
    deps = [":c"],
    defines = ["I_AM_B"],
)

cc_library(
    name = "c",
    hdrs = ["c.h"],
    defines = ["I_AM_C"],
)
