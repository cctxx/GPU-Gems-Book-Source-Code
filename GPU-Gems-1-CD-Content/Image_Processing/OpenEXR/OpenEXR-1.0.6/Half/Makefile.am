## Process this file with automake to produce Makefile.in

lib_LTLIBRARIES = libHalf.la

libHalf_la_SOURCES = half.cpp half.h halfFunction.h halfLimits.h

libHalfincludedir = $(includedir)/OpenEXR

libHalfinclude_HEADERS = half.h halfFunction.h halfLimits.h

# these are used to build eLut.h and toFloat.h dynamically
EXTRA_DIST = eLut.cpp toFloat.cpp

CLEANFILES = eLut eLut.h toFloat toFloat.h

eLut_SOURCES = eLut.cpp

toFloat_SOURCES = toFloat.cpp

eLut.h:	eLut
	./eLut > eLut.h

toFloat.h: toFloat
	   ./toFloat > toFloat.h

BUILT_SOURCES = eLut.h toFloat.h

noinst_PROGRAMS = eLut toFloat
