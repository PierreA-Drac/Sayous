## Variables.
##==========================================================================

# LaTeX compiler.
LATEX = pdflatex

# LaTeX compiler parameters.
LATEX_ARGS = --shell-escape

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
	cd $(REPORT_DIR) && $(LATEX) $(LATEX_ARGS) $(REPORT_NAME)
	cd $(REPORT_DIR) && $(LATEX) $(LATEX_ARGS) $(REPORT_NAME)
report: $(REPORT).pdf

clean:
	rm -rf $(REPORT).aux $(REPORT).log $(REPORT).out $(REPORT).toc ./svg-inkscape
	
mrproper: clean
	rm -f $(REPORT).pdf
