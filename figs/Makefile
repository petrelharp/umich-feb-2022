SHELL := /bin/bash
.PHONY: figs modeling_figs

figs: modeling_figs \
	ts_ex/tree_sequence_site.png \
	ts_ex/tree_sequence_branch.png \


modeling_figs: modeling_empty.png \
			   modeling_reality.png \
			   modeling_model_parameters.png \
			   modeling_model_parameters_inverse.png \
			   modeling_parameters_inverse_computer.png

modeling_%.pdf: modeling.ink.svg
	./export-layers-svg.sh $< $@ data $(subst _, ,$*)

include ../rules.mk
