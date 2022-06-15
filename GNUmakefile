DIR=$(shell echo ~/Repos/tkurtbond.github.io/files/trampolines)
SUBDIRS=ada c common-lisp oberon-2 revised-oberon
ALLDIRS=$(DIR) $(foreach e,$(SUBDIRS),$(DIR)/$(e))

all:
	for i in $(SUBDIRS); \
	do \
	    echo $$i; \
	    (cd $$i && make -k); \
	done


install:
	-rm -rfv $(DIR)/*
	-mkdir $(ALLDIRS)
	-cp forever.scm $(DIR)/
	-for i in $(SUBDIRS); \
	do \
	    cp $$i/* $(DIR)/$$i/; \
	done

clean:
	for i in $(SUBDIRS); \
	do \
	    (cd $$i && make clean); \
	done
