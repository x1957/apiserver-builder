load("@io_bazel_rules_go//proto:def.bzl", "go_proto_library")
load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = ["kv.pb.go"],
    importpath = "github.com/coreos/etcd/mvcc/mvccpb",
    visibility = ["//visibility:public"],
    deps = ["//vendor/github.com/golang/protobuf/proto:go_default_library"],
)

proto_library(
    name = "mvccpb_proto",
    srcs = ["kv.proto"],
    visibility = ["//visibility:public"],
    deps = ["//gogoproto:gogoproto_proto"],
)

go_proto_library(
    name = "mvccpb_go_proto",
    importpath = "github.com/coreos/etcd/mvcc/mvccpb",
    proto = ":mvccpb_proto",
    visibility = ["//visibility:public"],
    deps = ["//gogoproto:go_default_library"],
)
