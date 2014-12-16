CC = gcc
CFLAGS = -I ../include -c -Wall -g  
LDFLAGS= -fPIC -shared

OBJS= $(patsubst %.c, %.o, $(wildcard *.c))
LIB_NAME = ../../lib/libpower.so

all: $(OBJS) $(LIB_NAME)

%.o: %.c
	$(CC) $(CFLAGS) $^ -o $@

$(LIB_NAME): $(OBJS)
	$(CC) $(LDFLAGS) $^ -o $@
	@echo "@@ building .so completed"


clean:
	rm $(LIB_NAME) $(OBJS)


