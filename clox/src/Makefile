
CC = gcc
CFLAGS=-I.

main.o: chunk.o memory.o debug.o
	$(CC) -o main.o  chunk.o memory.o debug.o main.c $(CFLAGS)
debug.o: chunk.o memory.o
	$(CC) -c -o debug.o  chunk.o memory.o debug.c $(CFLAGS)
chunk.o: memory.o
	$(CC) -c -o chunk.o  memory.o chunk.c $(CFLAGS)
memory.o:
	$(CC) -c -o memory.o  memory.c $(CFLAGS)
clean:
	rm main.o debug.o chunk.o memory.o  2>/dev/null
