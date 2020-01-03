vpath %.h inc
vpath %.c src
 
 
 
hello : hello.o
	gcc -o $@ $^
 
.PHONY : clean
 
clean:
	rm *.o hello