IDIR = headings
CC=gcc
CFLAGS=-I$(IDIR)
ODIR=obj
#LIBS=-lm

_DEPS = dicto.h game.h
DEPS = $(patsubst %,$(IDIR)/%,$(_DEPS))

_OBJ = main.o game.o dictio.o
OBJ = $(patsubst %,$(ODIR)/%,$(_OBJ))

$(ODIR)/%.o: %.c $(DEPS)
	$(CC) -c -o $@ $< $(CFLAGS)

HangMan: $(OBJ)
	$(CC) -o $@ $^ $(CFLAGS) $(LIBS)

.PHONY: clean

clean:
	rm -f $(ODIR)/*.o *~ core $(INCDIR)/*~
