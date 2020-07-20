package(default_visibility = ["//visibility:public"])

filegroup(
    name = "linux-x86",
    srcs = glob(["**"]),
)

filegroup(
    name = "linux-x86-bundle",
    srcs = glob(
        include = ["lib/python2.7/**"],
        exclude = [
            "lib/python2.7/test/**",
            "lib/python2.7/unittest/**",
            "lib/python2.7/config/**",
            "lib/python2.7/distutils/**",
            "lib/python2.7/idlelib/**",
            "lib/python2.7/lib2to3/**",
            "lib/python2.7/plat-linux2/**",
            "lib/python2.7/bsddb/test/**",
            "lib/python2.7/ctypes/test/**",
            "lib/python2.7/email/test/**",
            "lib/python2.7/lib-tk/test/**",
            "lib/python2.7/sqlite3/test/**",
        ],
    ),
)
