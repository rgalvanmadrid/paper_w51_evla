# latex Makefile
texpath=/usr/texbin/
PDFLATEX=${texpath}pdflatex -halt-on-error -synctex=1 --interaction=nonstopmode
LATEX=${PDFLATEX}
BIBTEX=bibtex
DVIPS=dvips
PS2PDF=ps2pdf

all: w51_evla_h2co

w51_evla_h2co: 
	@rm -f w51_evla_h2co*.aux w51_evla_h2co*.bbl w51_evla_h2co*.blg w51_evla_h2co*.dvi w51_evla_h2co*.log w51_evla_h2co*.lot w51_evla_h2co*.lof
	${LATEX} w51_evla_h2co.tex
	${BIBTEX} w51_evla_h2co
	${LATEX} w51_evla_h2co.tex
	${BIBTEX} w51_evla_h2co
	${LATEX} w51_evla_h2co.tex
	gs -q -dNOPAUSE -dBATCH -sDEVICE=pdfwrite -sOutputFile=w51_evla_h2co_compressed.pdf w51_evla_h2co.pdf
