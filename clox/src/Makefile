
CC = gcc
CFLAGS=-I.

main.o: chunk.o value.o memory.o debug.o vm.o compiler.o scanner.o main.c
	$(CC) -o main.o  chunk.o value.o memory.o debug.o vm.o compiler.o scanner.o main.c $(CFLAGS)
vm.o: compiler.o scanner.o debug.o chunk.o value.o memory.o chunk.o value.o vm.c
	$(CC) -c -o vm.o  compiler.o scanner.o debug.o chunk.o value.o memory.o chunk.o value.o vm.c $(CFLAGS)
compiler.o: scanner.o compiler.c
	$(CC) -c -o compiler.o  scanner.o compiler.c $(CFLAGS)
scanner.o: scanner.c
	$(CC) -c -o scanner.o  scanner.c $(CFLAGS)
debug.o: chunk.o value.o memory.o value.o debug.c
	$(CC) -c -o debug.o  chunk.o value.o memory.o value.o debug.c $(CFLAGS)
chunk.o: value.o memory.o memory.o chunk.c
	$(CC) -c -o chunk.o  value.o memory.o memory.o chunk.c $(CFLAGS)
value.o: memory.o value.c
	$(CC) -c -o value.o  memory.o value.c $(CFLAGS)
memory.o: memory.c
	$(CC) -c -o memory.o  memory.c $(CFLAGS)
clean:
	rm main.o vm.o compiler.o scanner.o debug.o chunk.o value.o memory.o  2>/dev/null
