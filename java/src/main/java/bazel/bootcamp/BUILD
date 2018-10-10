# deps you may need for various targets
#    "@io_grpc_grpc_java//core",
#    "@io_grpc_grpc_java//netty",
#    "@junit_junit//jar",

java_binary(
    name = "HelloBazelBootcamp",
    srcs = ["HelloBazelBootcamp.java"], # relative path file reference
)

java_binary(
	name = "java-logging-client",
	srcs = [
		"JavaLoggingClient.java",
		"JavaLoggingClientLibrary.java",
	],
	main_class = "bazel.bootcamp.JavaLoggingClient",
	deps = [
		"//proto/logger:logger_java_proto_library",
		"//proto/logger:logger_java_grpc_library",
		"@io_grpc_grpc_java//core",
		"@io_grpc_grpc_java//netty",
		"@junit_junit//jar",
	]
)
