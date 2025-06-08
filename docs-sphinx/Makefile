# Minimal makefile for Sphinx documentation
#
# Note: you will need wget, make and sphinx.
# On Windows you can use Chocolatey:
#   choco install wget make sphinx
# On Mac you can use Homebrew:
#   brew install wget make sphinx-doc

# You can set these variables from the command line, and also
# from the environment for the first two.
SPHINXOPTS    ?=
SPHINXBUILD   ?= sphinx-build
SOURCEDIR     = source
BUILDDIR      = build

# Put it first so that "make" without argument is like "make help".
help:
	@$(SPHINXBUILD) -M help "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)

.PHONY: help Makefile

# TODO fix this path
source/strype_sphinx_conf_defaults.py:
	wget https://raw.githubusercontent.com/neilccbrown/Strype/refs/heads/library-docs-demos/docs-sphinx/source/strype_sphinx_conf_defaults.py -O $@

# TODO fix this path
source/_static/custom.css:
	mkdir source/_static
	wget https://raw.githubusercontent.com/neilccbrown/Strype/refs/heads/library-docs-demos/docs-sphinx/source/_static/custom.css -O $@


# Catch-all target: route all unknown targets to Sphinx using the new
# "make mode" option.  $(O) is meant as a shortcut for $(SPHINXOPTS).
%: Makefile source/strype_sphinx_conf_defaults.py source/_static/custom.css
	@$(SPHINXBUILD) -M $@ "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)
