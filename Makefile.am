AUTOMAKE_OPTIONS = foreign

#CC      ?= gcc
CFLAGS  ?= -O0 -ggdb -pedantic -Wall -I /usr/include/libdrm
LDFLAGS ?= -ldrm

include_HEADERS = framebuffer.h config.h

bin_PROGRAMS = drm-framebuffer
drm-framebuffer_SOURCES = main.c framebuffer.c

OBJ = main.o framebuffer.o
PROGNAME = drm-framebuffer

%.o: %.c $(DEPS)
	$(CC) -c -o $@ $< $(CFLAGS)

all: $(OBJ)
	$(CC) $(CFLAGS) -o $(PROGNAME) $(OBJ) $(LDFLAGS)
