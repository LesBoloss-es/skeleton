LATEXMK = latexmk -outdir=build -xelatex
MAIN = {project_name}.tex
TARGET = $(MAIN:.tex=.pdf)
DEPS = $(wildcard includes/*.tex)

.PHONY: all build clean

all: build
	killall -HUP mupdf 2>/dev/null || true # reload mupdf
	@if command -v pdfinfo >/dev/null 2>&1; then \
		echo "Nb of pages: $$(pdfinfo $(TARGET) | awk '/Pages:/ {{print $$2}}')"; \
	fi

build: $(MAIN) $(DEPS)
	$(LATEXMK) $(MAIN)
	cp build/$(TARGET) .

clean:
	rm -rf build
	rm -f $(TARGET)
