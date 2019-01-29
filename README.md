# 2018 - 2019 Winter Break Greek Homework
St. John's College 2018 - 2019 Winter Break homework for the Freshman Language Tutorial. 60 exercises from C.A.E. Luschnig's Introduction to Ancient Greek: A Literary Approach. Completed by Shen Zhou Hong

**Notice to people coming here from Google or other search engines: These are my answers to a homework assignment. While I have completed them to the best of my ability, I cannot gurrantee that all translations are as accurate as they can be. If there is any errors or badly translated responses, please let me know. I'll be happy to correct them! :)**

### Compiling document
In order to compile latex source files, run `make` in the terminal:
```
cd latex
make
make clean
```

Note: for any partial compiles where compilation fails at a certain point, you
should run `make clean` followed by make again. Trying to run make after a
failed compile would result in additional errors.

### Dependencies
This template uses a makefile to compile the latex source files. The makefile
uses `latexmk`, which runs latex the correct number of times. This is because
due to the presense of figures, tables, and biblatex databases, latex needs to
be called multiple times in some cases. Latexmk should be included in your
latex installation, but if it is now, you may download it here:

* http://personal.psu.edu/jcc8//software/latexmk-jcc/

Additionally, this template uses XeLaTeX by default, as it allows the inclusion
of unicode characters in the latex source files. If XeLaTeX is not installed, or
plain LaTeX is required, simply alter the `makefile` at the appropriate call:

```
# MAIN LATEXMK RULE
$(source_name).pdf: $(source_name).tex
  ...
	latexmk -pdf -xelatex -use-make $<
```

XeLaTeX allows one to use foreign characters like ü or æ natively in the latex
source files, though. So it's probably a good idea to install XeLaTeX:

* http://xetex.sourceforge.net/

### Related documentation
For an overview of how to populate biblatex `citations.bib` files, visit the
biblatex-mla manual at CTAN.

* https://www.ctan.org/pkg/biblatex-mla

### Copyright
The assigned sentences are excerpts from C.A.E. Luschnig's Introduction to Ancient Greek: A Literary Approach. They are reproduced here under the fair use clause of U.S. Copyright law. The translated sentences are my own intellectual property.
