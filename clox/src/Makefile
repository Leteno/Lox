
CC = gcc
CFLAGS=-I.

main.o: chunk.o value.o memory.o debug.o vm.o main.c
	$(CC) -o main.o  chunk.o value.o memory.o debug.o vm.o main.c $(CFLAGS)
vm.o: debug.o chunk.o value.o memory.o chunk.o value.o vm.c
	$(CC) -c -o vm.o  debug.o chunk.o value.o memory.o chunk.o value.o vm.c $(CFLAGS)
debug.o: chunk.o value.o memory.o value.o debug.c
	$(CC) -c -o debug.o  chunk.o value.o memory.o value.o debug.c $(CFLAGS)
chunk.o: value.o memory.o memory.o chunk.c
	$(CC) -c -o chunk.o  value.o memory.o memory.o chunk.c $(CFLAGS)
value.o: memory.o value.c
	$(CC) -c -o value.o  memory.o value.c $(CFLAGS)
memory.o: memory.c
	$(CC) -c -o memory.o  memory.c $(CFLAGS)
clean:
	rm main.o vm.o debug.o chunk.o value.o memory.o  2>/dev/null
