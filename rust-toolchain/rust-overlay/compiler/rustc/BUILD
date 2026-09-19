# Copyright 2026 Google LLC
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#    https://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

load("TODO/bazel_rules/rules_rust/rust:defs.bzl", "rust_binary")

package(default_applicable_licenses = ["//TODO/rust_toolchain:license"])

rust_binary(
    name = "bin/rustc_main",
    srcs = [
        "src/main.rs",
    ],
    edition = "2021",
    require_explicit_unstable_features = 0,
    rustc_flags = [
        "--cap-lints=allow",
    ],
    visibility = ["public"],
    deps = [
        "//TODO/rust_toolchain/compiler/rustc_codegen_ssa",
        "//TODO/rust_toolchain/compiler/rustc_driver",
    ],
)
