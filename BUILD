load("@bazel_gazelle//:def.bzl", "gazelle")

# gazelle:prefix github.com/jarreds/toomanyfiles
gazelle(name = "gazelle")

load("@io_bazel_rules_go//go:def.bzl", "go_binary", "go_library")

go_library(
    name = "go_default_library",
    srcs = ["main.go"],
    importpath = "github.com/jarreds/toomanyfiles",
    visibility = ["//visibility:private"],
    deps = ["@com_github_awslabs_goformation//cloudformation/resources:go_default_library"],
)

go_binary(
    name = "toomanyfiles",
    embed = [":go_default_library"],
    visibility = ["//visibility:public"],
)
