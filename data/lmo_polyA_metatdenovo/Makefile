DARDEL_DOWNLOAD = rsync -avhP --size-only dardel:/cfs/klemming/projects/supr/snic2020-16-76/projects/assembly/metaT/LMO_2016-17_polyA_metat/
DARDEL_SUMMARY_DOWNLOAD = $(DARDEL_DOWNLOAD)/results/summary_tables/$@ ./.

all: PF03842.faa.gz megahit_assembly.contigs.fa.transdecoder.pep.gz megahit202503.transdecoder202503.counts.tsv.gz megahit202503.transdecoder202503.emapper.tsv.gz megahit202503.transdecoder202503.hmmrank.tsv.gz megahit202503.transdecoder202503.overall_stats.tsv.gz megahit202503.transdecoder202503.mmetsp.eukulele.taxonomy.tsv.gz megahit202503.transdecoder202503.ncbi-refseq-20250115.diamond.taxonomy-taxdump.tsv.gz

clean:
	rm -r PF03842.faa.gz megahit_assembly.contigs.fa.transdecoder.pep.gz megahit202503.transdecoder202503.counts.tsv.gz megahit202503.transdecoder202503.emapper.tsv.gz megahit202503.transdecoder202503.hmmrank.tsv.gz megahit202503.transdecoder202503.overall_stats.tsv.gz megahit202503.transdecoder202503.ncbi-refseq-20250115.diamond.taxonomy-taxdump.tsv.gz

megahit_assembly.contigs.fa.transdecoder.pep.gz:
	$(DARDEL_DOWNLOAD)/megahit202503.transdecoder202503/$@ ./.

megahit202503.transdecoder202503.counts.tsv.gz:
	$(DARDEL_SUMMARY_DOWNLOAD)

megahit202503.transdecoder202503.emapper.tsv.gz:
	$(DARDEL_SUMMARY_DOWNLOAD)

megahit202503.transdecoder202503.hmmrank.tsv.gz:
	$(DARDEL_SUMMARY_DOWNLOAD)

megahit202503.transdecoder202503.mmetsp.eukulele.taxonomy.tsv.gz:
	$(DARDEL_SUMMARY_DOWNLOAD)

megahit202503.transdecoder202503.overall_stats.tsv.gz:
	$(DARDEL_SUMMARY_DOWNLOAD)

megahit202503.transdecoder202503.ncbi-refseq-20250115.diamond.taxonomy-taxdump.tsv.gz:
	$(DARDEL_SUMMARY_DOWNLOAD)

PF03842.faa.gz:
	$(DARDEL_DOWNLOAD)/results/hmmer/hits/megahit202503.transdecoder202503.$@ $@
