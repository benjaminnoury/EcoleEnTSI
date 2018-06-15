
all: ../HTML/ecoles.html ../HTML/style.css


id='id="tableau_ecole" class="pure-table pure-table-responsive pure-table-striped"'

../HTML/%.html: Ecoles_TSI.csv %.md template.html Makefile
	~/.local/bin/pp ecoles.md | \
		pandoc -s --template=template.html | \
		sed -e s/\<table/\<table\ id=\"tableau\_ecole\"\ class=\"pure-table\ pure-table-responsive\ pure-table-striped\"/g >$@


../HTML/%.css: %.scss
	sass $< $@ --style compressed
