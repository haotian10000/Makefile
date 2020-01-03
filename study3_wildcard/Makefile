
CC:=gcc
object:= $(patsubst %.c,%.o,$(wildcard *.c))

main:$(object)
	$(CC) -o $@ $^
.c.o:
	$(CC) -c $< -o $@

.PHONY:clean
clean:
	rm -rf *.o main
