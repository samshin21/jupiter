# src/Makefile.  Generated from Makefile.in by configure.

# Package-specific substiution variables
package		= Jupiter
version 	= 1.0
tarname		= jupiter
distdir		= $(tarname)-$(version)

# Prefix-specifc substitution variables
prefix		= /usr/local
exec_prefix 	= ${prefix}
bindir		= ${exec_prefix}/bin

# VPATH-related substitution variables
srcdir		= ../../src
VPATH		= ../../src

all: jupiter

CXXFLAGS = -g -O0

jupiter: main.cpp
	$(CXX) $(CPPFLAGS) $(CXXFLAGS) -o $@ $<

clean:
	-rm jupiter

check: all
	./jupiter | grep "Hello from .*jupiter"
	@echo "*** ALL TESTS PASSED ***"

install:
	install -d $(DESTDIR)$(bindir)
	install -m 0755 jupiter $(DESTDIR)$(bindir)

uninstall:
	-rm $(DESTDIR)$(bindir)/jupiter

Makefile: Makefile.in ../config.status
	cd .. && ./config.status src/$@

../config.status: ../configure
	cd .. && ./config.status --recheck

.PHONY: all clean check install uninstall
