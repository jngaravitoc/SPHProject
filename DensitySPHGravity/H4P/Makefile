# Makefile for halogen4muse

# Executable

BASE    = halogen4muse
EXT     = 
EXE     = $(BASE)$(EXT)

# Compiler stuff

CC	= gcc
CFLAGS	= -O3 -Wall
LIBS	= -lm

# Object definition

OBJ	= $(BASE).o functions.o routines.o

# Rules

$(EXE):	$(OBJ) Makefile
	$(CC) $(CFLAGS) $(OBJ) -o $(EXE) $(LIBS)

clean:
	-rm -f *.o *~ $(EXE)

tar:
	cd ..; tar cvf - $(BASE)/*.c $(BASE)/*.h $(BASE)/Makefile > $(BASE).tar

# Dependencies

halogen4muse.o: definitions.h functions.h routines.h
functions.o: definitions.h functions.h routines.h
routines.o: definitions.h functions.h routines.h

