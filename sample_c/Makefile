#
# mruby/c  sample_c/Makefile
#
# Copyright (C) 2015,2016 Kyushu Institute of Technology.
# Copyright (C) 2015,2016 Shimane IT Open-Innovation Center.
#
#  This file is distributed under BSD 3-Clause License.
#

TARGETS = mrubyc mrubyc_sample mrubyc_concurrent
CFLAGS = -g -I ../src -Wall -Wpointer-arith
LDFLAGS = -L ../src
LIBMRUBYC = ../src/libmrubyc.a

all: $(TARGETS)

mrubyc: main.c $(LIBMRUBYC)
	$(CC) $(CFLAGS) $(LDFLAGS) -o $@ main.c $(LIBMRUBYC)

mrubyc_sample: main_sample.c $(LIBMRUBYC)
	$(CC) $(CFLAGS) $(LDFLAGS) -o $@ main_sample.c $(LIBMRUBYC)

mrubyc_concurrent: main_concurrent.c $(LIBMRUBYC)
	$(CC) $(CFLAGS) $(LDFLAGS) -o $@ main_concurrent.c $(LIBMRUBYC)

clean:
	@rm -f $(TARGETS) *~
