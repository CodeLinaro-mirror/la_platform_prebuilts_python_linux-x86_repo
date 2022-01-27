package(default_visibility = ["//visibility:public"])

filegroup(
    name = "linux-x86",
    srcs = glob(["**"]),
)

filegroup(
    name = "linux-x86-bundle",
    srcs = glob(
        include = ["lib/python3.9/**"],
        exclude = [
            "lib/python3.9/test/**",
            "lib/python3.9/unittest/**",
            "lib/python3.9/config/**",
            "lib/python3.9/distutils/**",
            "lib/python3.9/idlelib/**",
            "lib/python3.9/lib2to3/**",
            "lib/python3.9/plat-linux2/**",
            "lib/python3.9/bsddb/test/**",
            "lib/python3.9/ctypes/test/**",
            "lib/python3.9/email/test/**",
            "lib/python3.9/lib-tk/test/**",
            "lib/python3.9/sqlite3/test/**",
            "lib/python3.9/site-packages/setuptools/gui-64.exe",
            "lib/python3.9/site-packages/setuptools/gui.exe",
            "lib/python3.9/site-packages/setuptools/cli.exe",
            "lib/python3.9/site-packages/setuptools/cli-64.exe",
            "lib/python3.9/site-packages/setuptools/cli-32.exe",
            "lib/python3.9/site-packages/setuptools/gui-32.exe",
            "lib/python3.9/site-packages/pip/_vendor/distlib/w64.exe",
            "lib/python3.9/site-packages/pip/_vendor/distlib/t64.exe",
            "lib/python3.9/site-packages/pip/_vendor/distlib/t32.exe",
            "lib/python3.9/site-packages/pip/_vendor/distlib/w32.exe",
        ],
    ),
)
