
CC = gcc
CFLAGS=-I.

main.o: chunk.o value.o memory.o debug.o
	$(CC) -o main.o  chunk.o value.o memory.o debug.o main.c $(CFLAGS)
debug.o: chunk.o value.o memory.o value.o
	$(CC) -c -o debug.o  chunk.o value.o memory.o value.o debug.c $(CFLAGS)
chunk.o: value.o memory.o memory.o
	$(CC) -c -o chunk.o  value.o memory.o memory.o chunk.c $(CFLAGS)
value.o: memory.o
	$(CC) -c -o value.o  memory.o value.c $(CFLAGS)
memory.o:
	$(CC) -c -o memory.o  memory.c $(CFLAGS)
clean:
	rm main.o debug.o chunk.o value.o memory.o  2>/dev/null
