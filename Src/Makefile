Site=../HTML
commit=$(shell zenity --entry --title="Commit" --text="Info du Commit")



all: $(Site)/index.html $(Site)/style.css

$(Site)/%.html: %.md Ecoles_TSI.csv template.html Makefile
	@echo "\033[0;31m$< --> $@\033[0m"
	@~/.local/bin/pp $< | \
		pandoc -s --template=template.html | \
		sed -e s/\<a\ /\<a\ target=\"_blank\"\/g | \
		sed -e s/\<table/\<table\ id=\"tableau\_ecole\"\ class=\"pure-table\ pure-table-responsive\ pure-table-striped\"/g > $@


$(Site)/%.css: %.scss
	@echo "\033[0;31m$< --> $@\033[0m"
	@sass $< $@ --style compressed
	@rm $@.map

%.csv: %.xls
	@echo "\033[0;31m$< --> $@\033[0m"
	@libreoffice --convert-to \
		csv:"Text - txt - csv (StarCalc)":"44,34,0,1,,0" \
		--headless --outdir . $<

upload: $(Site)/index.html $(Site)/style.css
	@echo "\033[0;31mMise à jour version en ligne\033[0m"
	@cd .. ; git add --all ; git commit -m '$(commit)' ;  git push

.phony: view clean upload

clean: 
	rm -f $(Site)/index.html
	rm -f $(Site)/style.css

view:
	chromium-browser $(Site)/index.html
