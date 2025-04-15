CFLAGS=-ggdb -Wall -Wextra

all: hello hello.i hello.s

hello.o: hello.c
	gcc $(CFLAGS) -Wa,-a=hello.lst -c hello.c
hello: hello.o
	gcc $(CFLAGS) -static -Wl,-Map=hello.map hello hello.o
hello.i: hello.c
	gcc -E hello.c  >hello.i
hello.s: hello.c
	gcc -S hello.c
# Type "make verbose" to see whole command line

verbose:
	gcc -v $(CFLAGS) -Wextra -c hello.c
clean:
	rm -f hello hello.o hello.i hello.s
