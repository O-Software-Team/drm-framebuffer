AUTOMAKE_OPTIONS = foreign

CC      ?= gcc
CFLAGS  ?= -O0 -ggdb -pedantic -Wall -I /usr/include/libdrm
LDFLAGS ?= -ldrm
include_HEADERS = drm-framebuffer.h

bin_PROGRAMS = drm-framebuffer
drm-framebuffer_SOURCES = drm-framebuffer.c

OBJ = main.o framebuffer.o
PROGNAME = drm-framebuffer

all: $(OBJ)
	$(CC) $(CFLAGS) -o $(PROGNAME) $(OBJ) $(LDFLAGS)
