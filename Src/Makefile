
all: ../HTML/index.html ../HTML/style.css


../HTML/%.html: %.md Ecoles_TSI.csv  template.html Makefile
	~/.local/bin/pp $< | \
		pandoc -s --template=template.html | \
		sed -e s/\<table/\<table\ id=\"tableau\_ecole\"\ class=\"pure-table\ pure-table-responsive\ pure-table-striped\"/g >$@


../HTML/%.css: %.scss
	sass $< $@ --style compressed

%.csv: %.xls
	libreoffice --convert-to \
		csv:"Text - txt - csv (StarCalc)":"44,34,0,1,,0" \
		--headless --outdir . $<

.phony: view clean

clean: 
	rm -f ../HTML/index.html
	rm -f ../HTML/style.css
	rm -f Ecoles_TSI.csv


view:
	chromium-browser ../HTML/index.html
