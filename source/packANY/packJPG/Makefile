# Project: packJPG
# Makefile created by Matthias Stirner 01/30/2012
# Working with GCC 4.6.0

CC      = gcc
CPP     = g++
RC      = windres -O coff
RM      = del
CFLAGS  = -I. -DDEV_BUILD -O3 -Wall -pedantic -funroll-loops -ffast-math -fsched-spec-load -fomit-frame-pointer
LDFLAGS = -s -static-libgcc -static-libstdc++
DEPS    = bitops.h aricoder.h pjpgtbl.h dct8x8.h Makefile
OBJ     = bitops.o aricoder.o packjpg.o
RES     = icons.res
BIN     = packJPG

%.o: %.cpp $(DEPS)
	$(CPP) -c -o $@ $< $(CFLAGS)
	
%.res: %.rc
	$(RC) $< $@

$(BIN): $(OBJ) $(RES)
	$(CPP) -o $@ $^ $(LDFLAGS)

clean:
	$(RM) *.o
