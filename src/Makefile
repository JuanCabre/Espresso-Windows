# This is the Makefile for the espresso project. It is used to compile the source code into an executable file.

# The following variable defines the compiler. It uses mingw-w64 to compile the source code into a Windows executable file.
# Make sure to install mingw-w64 before using this Makefile. You can install it using the following command:
# sudo apt-get install mingw-w64
CC = x86_64-w64-mingw32-gcc

SRC := $(wildcard *.c)

OBJ := ${SRC:.c=.o}

TARGETDIR := ../bin
TARGET := $(TARGETDIR)/espresso.exe

all: prepare $(TARGET)

prepare:
	mkdir -p $(TARGETDIR)

$(TARGET): $(OBJ)
	$(LINK.c) $(OBJ) -o $(TARGET)

clean:
	@- $(RM) -r $(TARGETDIR)
	@- $(RM) $(OBJ)

