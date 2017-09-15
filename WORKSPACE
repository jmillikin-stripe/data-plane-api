workspace(name = "envoy_api")

load("//bazel:repositories.bzl", "api_dependencies")

api_dependencies()

git_repository(
    name = "com_google_protobuf",
    # v3.4.0
    commit = "80a37e0782d2d702d52234b62dd4b9ec74fd2c95",
    remote = "https://github.com/google/protobuf.git",
)

bind(
    name = "protobuf",
    actual = "@com_google_protobuf//:protobuf",
)

bind(
    name = "protobuf_python",
    actual = "@com_google_protobuf//:protobuf_python",
)

bind(
    name = "protobuf_python_genproto",
    actual = "@com_google_protobuf//:protobuf_python_genproto",
)

bind(
    name = "protoc",
    actual = "@com_google_protobuf//:protoc",
)

new_http_archive(
    name = "six_archive",
    build_file = "@com_google_protobuf//:six.BUILD",
    sha256 = "105f8d68616f8248e24bf0e9372ef04d3cc10104f1980f54d57b2ce73a5ad56a",
    url = "https://pypi.python.org/packages/source/s/six/six-1.10.0.tar.gz#md5=34eed507548117b2ab523ab14b2f8b55",
)

bind(
    name = "six",
    actual = "@six_archive//:six",
)
