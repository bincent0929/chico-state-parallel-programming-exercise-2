INCLUDE_DIRS = 
LIB_DIRS = 
CC=gcc

CDEFS=
CFLAGS= -O3 $(INCLUDE_DIRS) $(CDEFS)
LIBS= 

HFILES= 
CFILES= sumnums.c edited-sumnums.c

SRCS= ${HFILES} ${CFILES}
OBJS= ${CFILES:.c=.o}

all:	edited-sumnums sumnums

clean:
	-rm -f *.o *.d
	-rm -f sumnums
	-rm -f edited-sumnums

distclean:
	-rm -f *.o *.d
	-rm -f sumnums
	-rm -f edited-sumnums

sumnums: sumnums.o
	$(CC) $(LDFLAGS) $(CFLAGS) -o $@ $@.o -lpthread

edited-sumnums: edited-sumnums.o
	$(CC) $(LDFLAGS) $(CFLAGS) -o $@ $@.o -lpthread

depend:

.c.o:
	$(CC) $(CFLAGS) -c $<
