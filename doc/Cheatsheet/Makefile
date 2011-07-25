## ein aussagekraeftiger Name zum Benennen der Endprodukte (PDFs, ZIPs, ...)
PROJECTNAME = "org-mode_Cheatsheet_Voit"
MAINDOCUMENT = "main"

## -----------------------------------------
##       DO NOT EDIT BELOW THIS LINE
## -----------------------------------------

## Makefile von Karl Voit (Karl@Voit.net)

## some Makefile-hints taken from: 
## http://www.ctan.org/tex-archive/help/uk-tex-faq/Makefile


## COMMANDS:
PDFLATEX_CMD = pdflatex
LATEX_CMD = latex
DVIPS_CMD = dvips
BIBTEX_CMD = bibtex
MAKEIDX_CMD = makeindex
TIMESTAMP = `/bin/date +%Y-%m-%dT%H.%M`
#PDFVIEWER = xpdf
PDFVIEWER = acroread
DVIVIEWER = xdvi

#help
#helpThe main targets of this Makefile are:
#help	help	this help
.PHONY: help
help:
	@sed -n 's/^#help//p' < Makefile

#help	all	see "pl"
.PHONY: all
all: pl

#help	pdf	makes a pdf-file per pdflatex
.PHONY: pdf
pdf:
	${PDFLATEX_CMD} ${MAINDOCUMENT}.tex
	-mv ${MAINDOCUMENT}.pdf ${PROJECTNAME}.pdf


# --------------------------------------------------------

#help	view	view the PDF-file
.PHONY: view
view: pdf
	${PDFVIEWER} *_${PROJECTNAME}.pdf

# --------------------------------------------------------


#help	clean	clean up temporary files
.PHONY: clean
clean:
	-rm -r _*_.* *~ *.aux *.bbl ${MAINDOCUMENT}.dvi *.ps *.blg *.idx *.ilg *.ind *.toc *.log *.log *.brf *.out *.lof *.lot *.gxg *.glx *.gxs *.glo *.gls -f

#help	purge	cleaner than clean ;-)
.PHONY: purge
purge: clean
	-rm *.pdf *.ps -f

#help	force	force rebuild next run
.PHONY: force
force:
	touch *tex




#end
