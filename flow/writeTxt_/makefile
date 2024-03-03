ROOT_DIR := $(shell dirname $(realpath $(firstword $(MAKEFILE_LIST))))
ROOT_DIR := $(strip $(ROOT_DIR))

export PYTHONPATH := $(ROOT_DIR)/../src:$(PYTHONPATH)

.PHONY: all

all: 
	poetry run python src/writeTxt.py input output > logs/info.log

%:
	poetry run python src/writeTxt.py input/$@.pdf output/$@.pdf.doc.json