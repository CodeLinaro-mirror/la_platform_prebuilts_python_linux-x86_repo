package(default_visibility = ["//visibility:public"])

filegroup(
    name = "linux-x86",
    srcs = glob(["**"]),
)

filegroup(
    name = "linux-x86-bundle",
    srcs = glob(
        include = ["lib/python3.8/**"],
        exclude = [
            "lib/python3.8/test/**",
            "lib/python3.8/unittest/**",
            "lib/python3.8/config/**",
            "lib/python3.8/distutils/**",
            "lib/python3.8/idlelib/**",
            "lib/python3.8/lib2to3/**",
            "lib/python3.8/plat-linux2/**",
            "lib/python3.8/bsddb/test/**",
            "lib/python3.8/ctypes/test/**",
            "lib/python3.8/email/test/**",
            "lib/python3.8/lib-tk/test/**",
            "lib/python3.8/sqlite3/test/**",
        ],
    ),
)
