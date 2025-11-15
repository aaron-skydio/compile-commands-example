load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "wolfd_bazel_compile_commands",
    sha256 = "2505ca4a14aa6a9a6da08e4e0ec2409d00a2f57dc79086b3fe1d4ba0b136afd5",
    strip_prefix = "bazel-compile-commands-67fb28bbca6b7caf99e3d0d4844dd5ddf269c047",
    urls = ["https://github.com/danny-skydio/bazel-compile-commands/archive/67fb28bbca6b7caf99e3d0d4844dd5ddf269c047.tar.gz"],
)

load("@wolfd_bazel_compile_commands//:deps.bzl", "bazel_compile_commands_dependencies")

# We need rules_python and com_google_protobuf, if you have other versions it should be okay.
# If you want other versions, load them before calling bazel_compile_commands_dependencies!
bazel_compile_commands_dependencies()

load("@rules_python//python:repositories.bzl", "python_register_toolchains")

# Python 3.8+ should work.
python_register_toolchains(
    name = "python_3_11",
    python_version = "3.11",
)

load("@rules_proto//proto:repositories.bzl", "rules_proto_dependencies", "rules_proto_toolchains")

rules_proto_dependencies()

rules_proto_toolchains()
