CC = gcc
LINKER = gcc
SRC = ../src
CFLAGS = -c -I ../../src/service -Wall -g

# test.o
OBJ_DIR= ./
OBJS= $(patsubst %.c, %.o, $(wildcard *.c))  

# softbus.o, service.o
OTHER_OBJS= ../../build/*.o
EXES= $(patsubst %.c, %, $(wildcard *.c))

all: $(OBJS) $(EXES)

%.o: %.c
	$(CC) $(CFLAGS) $^ -o $@

$(EXES): $(OBJS) $(OTHER_OBJS)
	$(LINKER) -o $@ $^ 

clean:
	rm *.o


