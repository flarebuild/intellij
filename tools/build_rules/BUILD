alias(
    name = "remote_jdk8",
    actual = select(
        {
            "@bazel_tools//src/conditions:darwin": "@remotejdk8_macos//:jdk",
            "@bazel_tools//src/conditions:darwin_x86_64": "@remotejdk8_macos//:jdk",
            "@bazel_tools//src/conditions:linux_x86_64": "@remotejdk8_linux//:jdk",
        },
        no_match_error = "Could not find a JDK for host execution environment, please explicitly" +
                         " provide one using `--host_javabase.`",
    ),
    visibility = ["//visibility:public"],
)
