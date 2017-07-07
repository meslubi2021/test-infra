package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_test(
    name = "go_default_test",
    srcs = [
        "hook_test.go",
        "server_test.go",
    ],
    library = ":go_default_library",
    tags = ["automanaged"],
    deps = [
        "//prow/config:go_default_library",
        "//prow/github:go_default_library",
        "//prow/phony:go_default_library",
        "//prow/plugins:go_default_library",
    ],
)

go_library(
    name = "go_default_library",
    srcs = [
        "events.go",
        "server.go",
    ],
    tags = ["automanaged"],
    deps = [
        "//prow/config:go_default_library",
        "//prow/github:go_default_library",
        "//prow/plugins:go_default_library",
        "//vendor:github.com/Sirupsen/logrus",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
)