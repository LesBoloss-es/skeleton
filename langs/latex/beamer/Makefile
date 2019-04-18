LATEXMK = latexmk -outdir=build -xelatex
MAIN = {project_name}.tex
TARGET = $(MAIN:.tex=.pdf)
DEPS = $(wildcard includes/*.tex)

.PHONY: build clean

build: $(MAIN) $(DEPS)
	$(LATEXMK) $(MAIN)
	cp build/$(TARGET) .

clean:
	rm -rf build
	rm -f $(TARGET)
