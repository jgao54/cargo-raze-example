workspace(name = "cargo-raze-example")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "rules_rust",
    sha256 = "531bdd470728b61ce41cf7604dc4f9a115983e455d46ac1d0c1632f613ab9fc3",
    strip_prefix = "rules_rust-d8238877c0e552639d3e057aadd6bfcf37592408",
    urls = ["https://github.com/bazelbuild/rules_rust/archive/d8238877c0e552639d3e057aadd6bfcf37592408.tar.gz"],
)

load("@rules_rust//rust:repositories.bzl", "rust_repositories")

rust_repositories(
    edition = "2018",
    version = "1.58.1",
)

load("//cargo:crates.bzl", "raze_fetch_remote_crates")

raze_fetch_remote_crates()
