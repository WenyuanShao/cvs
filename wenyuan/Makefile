RES=res
FINAL=wenyuan_resume.pdf

.PHONY: develop research full all clean

all: clean full #research develop full

full:
	latexmk -xelatex $(RES)-all.tex
	mv $(RES)-all.pdf all-$(FINAL)
	evince all-$(FINAL) &

develop:
	latexmk -xelatex $(RES)-dev.tex
	mv $(RES)-dev.pdf dev-$(FINAL)
	evince dev-$(FINAL) &

research:
	latexmk -xelatex $(RES).tex
	mv $(RES).pdf $(FINAL)
	evince $(FINAL) &

clean:
	rm -f *.log *.aux *.fls *.fdb_latexmk $(RES)-dev.pdf $(RES)-all.pdf $(RES).pdf
