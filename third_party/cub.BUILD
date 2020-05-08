# Description: CUB library which is a set of primitives for GPU programming.

load("@rules_cc//cc:defs.bzl", "cc_library")
load("@local_config_cuda//cuda:build_defs.bzl", "if_cuda")

package(
    default_visibility = ["//visibility:public"],
)

licenses(["notice"])  # BSD

exports_files(["LICENSE.TXT"])

filegroup(
    name = "cub_header_files",
    srcs = glob([
        "cub/**",
    ]),
)

cc_library(
    name = "cub",
    hdrs = if_cuda([":cub_header_files"]),
    include_prefix = "third_party",
    deps = [
        "@local_config_cuda//cuda:cuda_headers",
    ],
)
