#create a makefile file
TARGET=main
INC = 	-I../add	\
		-I../sub	\
		-I../mux
SRC = 	../main.c		\
		../sub/sub.c	\
		../mux/mux.c	\
		../add/add.c
OBJ_DIR = $(shell pwd)
OBJ = $(SRC:.c=.o)
CFLAGS = -g -Wall
CC = gcc
$(TARGET):$(OBJ)
	$(CC) -o $@ $^
.PHONY:clean
clean:
	rm -rf $(TARGET) $(OBJ)

#缺省规则
# %.o:%.c
# .c.o
.c.o:
	$(CC) $(CFLAGS) $(INC) -o $@ -c $< 

