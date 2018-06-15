
all: ../HTML/index.html ../HTML/style.css


id='id="tableau_ecole" class="pure-table pure-table-responsive pure-table-striped"'

../HTML/%.html: %.md Ecoles_TSI.csv  template.html Makefile
	~/.local/bin/pp $< | \
		pandoc -s --template=template.html | \
		sed -e s/\<table/\<table\ id=\"tableau\_ecole\"\ class=\"pure-table\ pure-table-responsive\ pure-table-striped\"/g >$@


../HTML/%.css: %.scss
	sass $< $@ --style compressed
