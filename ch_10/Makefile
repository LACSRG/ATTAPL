BOOK=attapl
CHAPTER=10
SECTION=10.1
SHOW=evince
BUILD=pdflatex
INCLUDEDIR=../common
DEPS=\
		 $(INCLUDEDIR)/bussproofs.sty \
		 $(INCLUDEDIR)/MathematicsWorkbook.sty \
		 $(INCLUDEDIR)/$(BOOK).sty \


BOOKCH=$(BOOK)_ch$(CHAPTER)
BOOKSEC=$(BOOK)_$(SECTION)
TEXFILE=$(BOOKSEC).tex
PDFFILE=$(BOOKSEC).pdf

$(PDFFILE): $(TEXFILE) $(DEPS)
	TEXINPUTS=..//:$(TEXINPUTS) $(BUILD) $(TEXFILE)

all: show_$(BOOKCH)

show_$(BOOKCH): $(PDFFILE)
	$(SHOW) $(PDFFILE)

clean:
	rm -f *.bak *.aux *.log *.pdf *.sav *.ans *.inx *.ref
