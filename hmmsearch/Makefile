include ~/dev/biomakefiles/lib/make/makefile.hmmer
include ~/dev/biomakefiles/lib/make/makefile.pfam
include ~/dev/biomakefiles/lib/make/makefile.misc

HMMSEARCH_OPTS = --cpu 4
HMMER_DB_FAA = <(gunzip -c transdecoder.faa.gz)
HMMRANK_OPTS   = --minscore=26.8

best.ranked.shorter_names.faa: best.ranked.faa
	sed 's/_ *ORF.*//' $< | sed 's/>/>QUERY@/' > $@
