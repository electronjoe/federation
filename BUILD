# Copyright (c) Outernet Council and Contributors.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

load("@rules_go//proto:def.bzl", "go_proto_library")
load("@protobuf//bazel:proto_library.bzl", "proto_library")

proto_library(
    name = "federation_proto",
    srcs = ["federation.proto"],
    visibility = ["//visibility:public"],
    deps = [
        "@org_outernetcouncil_nmts//proto/types/geophys:motion_proto",
        "@org_outernetcouncil_nmts//proto/types/ietf:inet_proto",
        "@org_outernetcouncil_nmts//proto:nmts_proto",
        "@googleapis//google/type:interval_proto",
        "@protobuf//:duration_proto",
    ],
)

go_proto_library(
    name = "federation_go_proto",
    importpath = "oc.com/smo/api/fed/v1alpha",
    protos = [":federation_proto"],
    visibility = ["//visibility:public"],
    deps = [
        "@org_outernetcouncil_nmts//proto/types/geophys:geophys_go_proto",
        "@org_outernetcouncil_nmts//proto/types/ietf:ietf_go_proto",
        "@org_outernetcouncil_nmts//proto:nmts_go_proto",
        "@org_golang_google_genproto//googleapis/type/interval",
    ],
)
