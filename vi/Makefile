# This is a hand-built makefile; it does not use Automake and suchlike.
TEXI2DVI = texi2dvi
MAKENFO = makeinfo
RM = rm -f

TARGETS = gnu-c-manual.dvi gnu-c-manual.info 
GNU_C_MANUAL_SOURCES = gnu-c-manual.texi  \
	expressions.texi		  \
	fdl.texi			  \
	functions.texi			  \
	lexical.texi			  \
	preface.texi			  \
	program.texi			  \
	sample.texi			  \
	statements.texi			  \
	types.texi

CLEANFILES = \
	gnu-c-manual.vr   \
	gnu-c-manual.tp	  \
	gnu-c-manual.toc  \
	gnu-c-manual.pg	  \
	gnu-c-manual.log  \
	gnu-c-manual.ky	  \
	gnu-c-manual.fn	  \
	gnu-c-manual.cps  \
	gnu-c-manual.cp	  \
	gnu-c-manual.aux
DISTCLEANFILES = \
	gnu-c-manual.dvi  \
	gnu-c-manual.info \
	gnu-c-manual.html

all: $(TARGETS)

gnu-c-manual.dvi:  $(GNU_C_MANUAL_SOURCES)
	$(TEXI2DVI) gnu-c-manual.texi

gnu-c-manual.info: $(GNU_C_MANUAL_SOURCES)
	$(MAKEINFO) gnu-c-manual.texi

gnu-c-manual.html: $(GNU_C_MANUAL_SOURCES)
	$(MAKEINFO) --html --no-split gnu-c-manual.texi

clean:
	$(RM) $(CLEANFILES)

distclean: clean
	$(RM) $(DISTCLEANFILES)
