workspace(name = "rules_bloop")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

## bazelbuild/rules_scala

rules_scala_version="69d3c5b5d9b51537231746e93b4383384c9ebcf4" # update this as needed

http_archive(
    name = "io_bazel_rules_scala",
    strip_prefix = "rules_scala-%s" % rules_scala_version,
    type = "zip",
    url = "https://github.com/bazelbuild/rules_scala/archive/%s.zip" % rules_scala_version,
)

load("@io_bazel_rules_scala//scala:toolchains.bzl", "scala_register_toolchains")
scala_register_toolchains()

load("@io_bazel_rules_scala//scala:scala.bzl", "scala_repositories")
scala_repositories()

protobuf_version="66dc42d891a4fc8e9190c524fd67961688a37bbe"
protobuf_version_sha256="983975ab66113cbaabea4b8ec9f3a73406d89ed74db9ae75c74888e685f956f8"

http_archive(
    name = "com_google_protobuf",
    url = "https://github.com/protocolbuffers/protobuf/archive/%s.tar.gz" % protobuf_version,
    strip_prefix = "protobuf-%s" % protobuf_version,
    sha256 = protobuf_version_sha256,
)



