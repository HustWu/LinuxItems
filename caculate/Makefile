#generate cacu_makefile,":"right is target
cacu_makefile:main.o add_int.o add_float.o sub_int.o sub_float.o 
	gcc -o cacu_makefile ./add/add_int.o ./add/add_float.o \
		./sub/sub_int.o ./sub/sub_float.o main.o
add_int.o:./add/add_int.c ./add/add.h
	gcc -c -o ./add/add_int.o ./add/add_int.c 
add_float.o:./add/add_float.c ./add/add.h
	gcc -c -o ./add/add_float.o ./add/add_float.c 
sub_int.o:./sub/sub_int.c ./sub/sub.h
	gcc -c -o ./sub/sub_int.o ./sub/sub_int.c 
sub_float.o:./sub/sub_float.c ./sub/sub.h
	gcc -c -o ./sub/sub_float.o ./sub/sub_float.c 
main.o:main.c add/add.h sub/sub.h
	gcc -c -o ./main.o main.c -I ./add -I ./sub
clean:
	rm -f cacu_makefile add/add_int.o add/add_float.o sub/sub_int.o \
		sub/sub_float.o main.o
