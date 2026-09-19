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

load("//TODO/bazel_rules/rules_cc/cc:cc_library.bzl", "cc_library")
load("//TODO/bazel_rules/rules_rust/rust:defs.bzl", "rust_library")
load("//TODO/bazel_skylib/rules:build_test.bzl", "build_test")
load("//TODO/llvm/llvm-project/llvm:targets.bzl", "llvm_targets")

filtered_llvm_targets = llvm_targets

package(default_applicable_licenses = ["//TODO/rust_toolchain:license"])

exports_files([
    "BUILD",
])

rust_library(
    name = "rustc_llvm",
    srcs = glob(
        include = ["**/*.rs"],
    ),
    edition = "2021",
    rustc_flags = [
        "--cap-lints=allow",
        "-Zallow-features=unsafe_attributes,unsafe_extern_blocks,rustdoc_internals,extern_types",
    ] + [
        "--cfg=llvm_component=\"%s\"" % target.lower()
        for target in filtered_llvm_targets
    ],
    visibility = ["TODO/rust_toolchain:rustc_visibility"],
    deps = ["TODO/rust/libc/v0_2:libc"],
)
