INCLUDE_DIRS = 
LIB_DIRS = 
CC=gcc

CDEFS=
CFLAGS= -O3 $(INCLUDE_DIRS) $(CDEFS)
LIBS= 

HFILES= 
CFILES= sumnums.c edited-sumnums.c edited-openmp-sumnums.c

SRCS= ${HFILES} ${CFILES}
OBJS= ${CFILES:.c=.o}

all:	edited-openmp-sumnums edited-sumnums sumnums

clean:
	-rm -f *.o *.d
	-rm -f sumnums
	-rm -f edited-sumnums
	-rm -f edited-openmp-sumnums

distclean:
	-rm -f *.o *.d
	-rm -f sumnums
	-rm -f edited-sumnums
	-rm -f edited-openmp-sumnums

sumnums: sumnums.o
	$(CC) $(CFLAGS) -o $@ $@.o -lpthread

edited-sumnums: edited-sumnums.o
	$(CC) $(CFLAGS) -o $@ $@.o -lpthread

edited-openmp-sumnums: edited-openmp-sumnums.o
	$(CC) $(CFLAGS) -fopenmp -o $@ $@.o -fopenmp

depend:

.c.o:
	$(CC) $(CFLAGS) -c $<
