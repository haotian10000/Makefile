
CC:=gcc


vpath %.h inc
vpath %.c src
vpath %.o obj

SRC = 	./src/main.c		\
		./src/sub.c	\
		./src/add.c
OBJ_DIR = $(shell pwd)
OBJS = $(SRC:.c=.o)
OBJSD = $(SRC:.c=.d)
OJ = main.o sub.o add.o 
INCLUDE_DIR = -I./inc


main : $(OBJSD)
	#$(CC) -o $@ $^
%.d: %.c
	@set -e; rm -f $@; \
	$(CC) $(INCLUDE_DIR) -MM  $< > $@.$$$$; \
	sed 's,\($*\)\.o[ :]*,\1.o $@ : ,g' < $@.$$$$ > $@; \
	rm -f $@.$$$$
%.o:%.c
	$(CC) $(INCLUDE_DIR) -c $<  -o $@
 
.PHONY : clean
 
clean:
	rm -rf main ./src/*.o *.o ./obj/*.o ./src/*.d