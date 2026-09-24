load("@rules_python//python:py_runtime.bzl", "py_runtime")
load("@rules_python//python:py_runtime_pair.bzl", "py_runtime_pair")
load("@rules_python//python:py_exec_tools_toolchain.bzl", "py_exec_tools_toolchain")

package(default_visibility = ["//visibility:public"])

py_runtime(
    name = "prebuilt_python3",
    files = [":linux-x86"],
    interpreter = "bin/python3",
    python_version = "PY3",
)

py_exec_tools_toolchain(
    name = "exec_tools_toolchain_impl",
    exec_interpreter = "@rules_python//python:none",
)

py_runtime_pair(
    name = "prebuilt_python",
    py2_runtime = None,
    py3_runtime = ":prebuilt_python3",
)

toolchain(
    name = "python_toolchain",
    exec_compatible_with = [
        "@platforms//os:linux",
    ],
    toolchain = ":prebuilt_python",
    toolchain_type = "@bazel_tools//tools/python:toolchain_type",
)

toolchain(
    name = "exec_tools_toolchain",
    toolchain = ":exec_tools_toolchain_impl",
    toolchain_type = "@rules_python//python:exec_tools_toolchain_type",
    exec_compatible_with = ["@platforms//os:linux"],
)

filegroup(
    name = "linux-x86",
    srcs = glob(
        include = ["**"],
        exclude = [
            "**/*.pyc",
            "lib/python3.13/**/__pycache__/**",
        ],
    ),
)

filegroup(
    name = "linux-x86-bundle",
    srcs = glob(
        include = ["lib/python3.13/**"],
        exclude = [
            "lib/python3.13/**/__pycache__/**",
            "lib/python3.13/**/*.pyc",
            "lib/python3.13/test/**",
            "lib/python3.13/unittest/**",
            "lib/python3.13/config/**",
            "lib/python3.13/distutils/**",
            "lib/python3.13/idlelib/**",
            "lib/python3.13/lib2to3/**",
            "lib/python3.13/plat-linux2/**",
            "lib/python3.13/bsddb/test/**",
            "lib/python3.13/ctypes/test/**",
            "lib/python3.13/email/test/**",
            "lib/python3.13/lib-tk/test/**",
            "lib/python3.13/sqlite3/test/**",
            "lib/python3.13/site-packages/setuptools/gui-64.exe",
            "lib/python3.13/site-packages/setuptools/gui.exe",
            "lib/python3.13/site-packages/setuptools/cli.exe",
            "lib/python3.13/site-packages/setuptools/cli-64.exe",
            "lib/python3.13/site-packages/setuptools/cli-32.exe",
            "lib/python3.13/site-packages/setuptools/gui-32.exe",
            "lib/python3.13/site-packages/pip/_vendor/distlib/w64.exe",
            "lib/python3.13/site-packages/pip/_vendor/distlib/t64.exe",
            "lib/python3.13/site-packages/pip/_vendor/distlib/t32.exe",
            "lib/python3.13/site-packages/pip/_vendor/distlib/w32.exe",
        ],
    ),
)
