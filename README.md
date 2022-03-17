### Example of an edge case not currently handled by cargo-raze

The repo contains a simple example where package A has a dependency on package B and both packages depends on different versions of `clap`. One of the `clap` is renamed to `clap3` in package B's Cargo.toml, however in the generated Bazel aliases, both packages show up as `clap`.

To trigger the build error, run `bazel build //packageA`.
