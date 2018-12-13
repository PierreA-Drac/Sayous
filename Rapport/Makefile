## Variables.
##==========================================================================

# LaTeX compiler.
LATEX = pdflatex

# Report directory name.
REPORT_DIR = .

# Report file name.
REPORT_NAME = report.tex

# Report full path (without extension).
REPORT = $(REPORT_DIR)/report

## Targets.
##==========================================================================

# Create the report (2-times to generate the TOC).
$(REPORT).pdf: $(REPORT).tex
	cd $(REPORT_DIR) && $(LATEX) $(REPORT_NAME)
	cd $(REPORT_DIR) && $(LATEX) $(REPORT_NAME)
report: $(REPORT).pdf

clean:
	rm -f $(REPORT).aux $(REPORT).log $(REPORT).out $(REPORT).toc
