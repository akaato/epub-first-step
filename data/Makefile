GRAPHVIZ = dot

prefix = ../OEBPS

all: png jpeg gif svg

svg: $(prefix)/sample.svg

$(prefix)/sample.svg: sample.dot
	$(GRAPHVIZ) -Tsvg -o $@ $^

#
# convert
#
CONVERT = convert
png: $(prefix)/sample.png
$(prefix)/sample.png: $(prefix)/sample.svg
	$(CONVERT) $^ $@

jpeg: $(prefix)/sample.jpeg
$(prefix)/sample.jpeg: $(prefix)/sample.svg
	$(CONVERT) $^ $@

gif: $(prefix)/sample.gif
$(prefix)/sample.gif: $(prefix)/sample.svg
	$(CONVERT) $^ $@
