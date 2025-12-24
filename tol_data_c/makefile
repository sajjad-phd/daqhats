NAME = channel4_ringbuffer_logger
OBJ = $(NAME).o
LIBS = -ldaqhats -lpthread
CFLAGS = -Wall -I/usr/local/include -g -std=c99 -D_POSIX_C_SOURCE=200809L
CC = gcc
EXTENSION = .c

all: $(NAME)

%.o: %$(EXTENSION) $(DEPS)
	$(CC) -c -o $@ $< $(CFLAGS)

$(NAME): $(OBJ)
	$(CC) -o $@ $^ $(CFLAGS) $(LIBS)

.PHONY: clean

clean:
	@rm -f *.o *~ core $(NAME)
