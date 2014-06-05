CC=gcc
CFLAGS=-Wall
CLIBRT=-lrt
GPIOSRCS=para_morse.c para_gpio.c
GPIODEPS=makefile $(GPIOSRCS) para_morse.h para_gpio.h

all: pmorse gpiotest

pmorse: pmorse.c $(GPIODEPS)
	$(CC) -o pmorse pmorse.c $(GPIOSRCS) $(CFLAGS)

gpiotest: gpiotest.c $(GPIODEPS)
	$(CC) -o gpiotest gpiotest.c $(GPIOSRCS) $(CFLAGS) $(CLIBRT)

clean:
	rm -f pmorse gpiotest

.PHONY: all clean
