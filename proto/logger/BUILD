package(default_visibility = ["//visibility:public"])

load("@io_grpc_grpc_java//:java_grpc_library.bzl", "java_grpc_library")
load("@io_bazel_rules_go//proto:def.bzl", "go_proto_library")

proto_library(
	name = "logger_proto",
	srcs = ["logger.proto"],
	# visibility = ["//visibility:public"], # default visibility rule above
)

java_proto_library (
	name = "logger_java_proto_library",
  deps = [":logger_proto"],
)

java_grpc_library(
	name = "logger_java_grpc_library",
	srcs = [":logger_proto"],
  deps = [":logger_java_proto_library"],
)

go_proto_library(
	name = "logger_go_proto_library",
	importpath = "bootcamp/proto/logger", # generated code path referenced in the `server.go`
	proto = ":logger_proto",
	compilers = ["@io_bazel_rules_go//proto:go_grpc"],
	# visibility = ["//visibility:public"], # default visibility rule above
)
