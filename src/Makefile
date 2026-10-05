CC = gcc
CFLAGS = -g -Wall -Wextra
CPPFLAGS = -I./

OBJECTS = \
	./build/compiler.o \
	./build/cprocess.o \
	./build/helpers/vector.o \
	./build/helpers/buffer.o

.PHONY: all clean

all: main

main: main.c $(OBJECTS)
	$(CC) $(CFLAGS) $(CPPFLAGS) $^ -o $@

./build/%.o: %.c
	mkdir -p $(@D)
	$(CC) $(CFLAGS) $(CPPFLAGS) -c $< -o $@

clean:
	rm -f main $(OBJECTS)