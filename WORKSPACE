workspace(
    name = "kobo_tweaks",
)

## Versions

# https://github.com/pgaskin/NickelMenu/releases
NICKEL_MENU_VERSION = "0.4.0"

## End Versions

all_content = """filegroup(name = "all", srcs = glob(["**"]), visibility = ["//visibility:public"])"""

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive", "http_file")

http_archive(
    name = "rules_pkg",
    sha256 = "352c090cc3d3f9a6b4e676cf42a6047c16824959b438895a76c2989c6d7c246a",
    url = "https://github.com/bazelbuild/rules_pkg/releases/download/0.2.5/rules_pkg-0.2.5.tar.gz",
)

load("@rules_pkg//:deps.bzl", "rules_pkg_dependencies")

rules_pkg_dependencies()

http_file(
    name = "nickel_menu",
    downloaded_file_path = "nickel_menu_KoboRoot.tgz",
    urls = [
        "https://github.com/pgaskin/NickelMenu/releases/download/v{version}/KoboRoot.tgz".format(version = NICKEL_MENU_VERSION),
    ],
)

http_file(
    name = "config_guess",
    downloaded_file_path = "config.guess",
    urls = [
        "https://git.savannah.gnu.org/gitweb/?p=config.git;a=blob_plain;f=config.guess",
    ],
)
