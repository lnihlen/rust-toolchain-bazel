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

load("//TODO/bazel_rules/rules_rust/rust:defs.bzl", "rust_library")
load("//TODO/rust_toolchain:defs.bzl", "cfg_environ")

package(
    default_applicable_licenses = [
        "//TODO/rust_toolchain:license",
    ],
)

exports_files([
    "BUILD",
])

rust_library(
    name = "rustc_proc_macro",
    srcs = ["//TODO/rust_toolchain/library:proc_macro_srcs"],
    crate_features = ["rustc_internal"],
    edition = "2024",
    require_explicit_unstable_features = 0,
    rustc_env = cfg_environ(
        CARGO_PKG_NAME = "rustc_proc_macro",
        CFG_COMPILER_HOST_TRIPLE = "x86_64-unknown-linux-gnu",
    ),
    rustc_flags = [
        "--cap-lints=allow",
    ],
    version = "0.0.0",
    visibility = [
        "private",
    ],
    deps = [
        "//TODO/rust/rustc_literal_escaper/v0_0_8:rustc_literal_escaper",
    ],
)
