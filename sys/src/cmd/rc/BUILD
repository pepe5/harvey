load('//sys/src/harvey.BUILD', "harvey_binary")

harvey_binary(
	name="rc",
	includes=[
		"//sys/include",
		"//amd64/include",
		"//sys/src/cmd/rc"
	],
	deps=[
		":syn",
		"//sys/src/libip:libip",
		"//sys/src/libbio:libbio",
		"//sys/src/libauth:libauth",
		"//sys/src/libndb:libndb",
		"//sys/src/libString:libString",
		"//sys/src/lib9p:lib9p",
		"//sys/src/libc:libc",
	],
    srcs=[
		"code.c",
		"exec.c",
		"getflags.c",
		"glob.c",
		"havefork.c",
		"here.c",
		"io.c",
		"lex.c",
		"pcmd.c",
		"pfnc.c",
		"plan9.c",
		"simple.c",
		"subr.c",
		"trap.c",
		"tree.c",
		"var.c",
		"x.tab.c",
	],
)

yacc(
    name="syn",
    yaccopts=[
        "-d",
        "--file-prefix=x"
    ],
    srcs=[
        "syn.y"
    ],
    hdrs=[
        "x.tab.h"
    ],
    exports=[
        "x.tab.c"
    ]
)
