load("@npm_angular_bazel//:index.bzl", "ng_module")
load("@io_bazel_rules_sass//:defs.bzl", "sass_binary")

package(default_visibility = ["//frontend:__subpackages__"])

ng_module(
    name = "memory_viewer",
    srcs = [
        "memory_viewer.ts",
        "memory_viewer_module.ts",
    ],
    assets = [
        ":memory_viewer_css",
        "memory_viewer.ng.html",
    ],
    deps = [
        "@npm//@angular/core",
        "@org_xprof//frontend/app/common/angular:angular_material_divider",
        "@npm//@angular/router",
        "@npm//@ngrx/store",
        "@org_xprof//frontend/app/common/interfaces",
        "@org_xprof//frontend/app/common/utils",
        "@org_xprof//frontend/app/components/memory_viewer/max_heap_chart",
        "@org_xprof//frontend/app/components/memory_viewer/memory_usage",
        "@org_xprof//frontend/app/components/memory_viewer/program_order_chart",
        "@org_xprof//frontend/app/services/data_service",
        "@org_xprof//frontend/app/store",
    ],
)



sass_binary(
    name = "memory_viewer_css",
    src = "memory_viewer.scss",
    sourcemap = False,
    deps = [
        "@org_xprof//frontend/app/styles:common",
    ],
)
