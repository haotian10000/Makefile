vpath %.h inc
vpath %.c src
 
 
 
edit : main.o kbd.o
	gcc -o $@ main.o kbd.o
main.o :  main.c kbd.h
	gcc -c $< -Iinc
kbd.o : kbd.c kbd.h 
	gcc  -c $< -Iinc
 
.PHONY : clean
 
clean:
	rm *.o edit