
CC = gcc
CFLAGS=-I.

main.o: chunk.o value.o memory.o debug.o vm.o compiler.o scanner.o main.c
	$(CC) -o main.o  chunk.o value.o memory.o debug.o vm.o compiler.o scanner.o main.c $(CFLAGS)
scanner.o: scanner.c
	$(CC) -c -o scanner.o  scanner.c $(CFLAGS)
debug.h: chunk.o memory.o value.o debug.h
	$(CC) -c -o debug.h  chunk.o memory.o value.o debug.h $(CFLAGS)
memory.o: memory.c
	$(CC) -c -o memory.o  memory.c $(CFLAGS)
compiler.h: vm.o chunk.o value.o scanner.o debug.o memory.o compiler.h
	$(CC) -c -o compiler.h  vm.o chunk.o value.o scanner.o debug.o memory.o compiler.h $(CFLAGS)
chunk.h: value.o memory.o chunk.h
	$(CC) -c -o chunk.h  value.o memory.o chunk.h $(CFLAGS)
vm.o: compiler.o scanner.o memory.o debug.o chunk.o value.o vm.c
	$(CC) -c -o vm.o  compiler.o scanner.o memory.o debug.o chunk.o value.o vm.c $(CFLAGS)
value.h: memory.o value.h
	$(CC) -c -o value.h  memory.o value.h $(CFLAGS)
clean:
	rm main.o scanner.o memory.o vm.o  2>/dev/null
