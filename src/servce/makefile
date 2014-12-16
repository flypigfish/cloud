CC = gcc
CFLAGS = -I ../include -c -Wall -g

OBJ_DIR=../../build
OBJS= $(patsubst %.c, $(OBJ_DIR)/%.o, $(wildcard *.c))

.PHONY: all

all: $(OBJS)

$(OBJ_DIR)/%.o: %.c
	$(CC) $(CFLAGS) $^ -o $@

clean:
	rm $(OBJS)


