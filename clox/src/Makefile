
CC = gcc
CFLAGS=-I. -g

main.o:
	$(CC) -o main.o object.c main.c debug.c value.c scanner.c vm.c compiler.c memory.c chunk.c table.c $(CFLAGS)
clean:
	rm main.o  2>/dev/null
