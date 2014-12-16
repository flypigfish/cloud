CC = gcc
CFLAGS = -I ../include -c -Wall -g

OBJ_DIR= ./
OBJS= $(patsubst %.c, $(OBJ_DIR)/%.o, $(wildcard *.c))

all: $(OBJS)

%.o: %.c
	$(CC) $(CFLAGS) $^ -o $@

clean:
	rm $(OBJS)


