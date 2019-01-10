cc_library(
    name = "config_h",
    hdrs = glob(["stub-config/*.h"]),
    includes = ["stub-config"],
    visibility = ["//bin:__pkg__"],
)

cc_library(
    name = "m4_lib_hdrs",
    hdrs = glob(["lib/*.h"]),
    strip_include_prefix = "lib",
    visibility = ["//bin:__pkg__"],
)

cc_library(
    name = "m4_lib",
    srcs = glob([
        "lib/x*.c",
        "lib/gl_*.c",
        "src/*.c",
        "src/*.h",
    ]) + [
        "lib/basename-lgpl.c",
        "lib/c-ctype.c",
        "lib/c-stack.c",
        "lib/c-strcasecmp.c",
        "lib/clean-temp.c",
        "lib/cloexec.c",
        "lib/close-stream.c",
        "lib/closein.c",
        "lib/closeout.c",
        "lib/dup-safer.c",
        "lib/error.c",
        "lib/execute.c",
        "lib/exitfail.c",
        "lib/fatal-signal.c",
        "lib/fd-safer.c",
        "lib/filenamecat-lgpl.c",
        "lib/filenamecat.c",
        "lib/fpending.c",
        "lib/freadahead.c",
        "lib/localcharset.c",
        "lib/memchr2.c",
        "lib/mkstemp-safer.c",
        "lib/obstack.c",
        "lib/pipe-safer.c",
        "lib/progname.c",
        "lib/quotearg.c",
        "lib/regex.c",
        "lib/secure_getenv.c",
        "lib/sig-handler.c",
        "lib/spawn-pipe.c",
        "lib/tmpdir.c",
        "lib/verror.c",
        "lib/version-etc-fsf.c",
        "lib/version-etc.c",
        "lib/wait-process.c",
        "lib/vasprintf.c",
        "lib/vasnprintf.c",
        "lib/printf-parse.c",
        "lib/printf-args.c",
    ],
    copts = [
        "-UDEBUG",
        "-Wno-unused-function",
    ],
    textual_hdrs = [
        "lib/regex_internal.c",
        "lib/regcomp.c",
        "lib/regexec.c",
    ],
    visibility = ["//bin:__pkg__"],
    deps = [
        ":config_h",
        ":m4_lib_hdrs",
    ],
)
