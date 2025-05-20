SHELL := /bin/bash

PF03842.clean.faa.gz: PF03842.faa.gz 
	gunzip -c $< | sed '/>/s/ .*//' | gzip -c > $@

PF03842.best_ranked.faa.gz: PF03842.clean.faa.gz lmo_polyA.hmmrank.tsv.gz
	seqtk subseq $< <(zgrep -P '\t1$$' $(word 2,$^) | cut -f 2) > $@
