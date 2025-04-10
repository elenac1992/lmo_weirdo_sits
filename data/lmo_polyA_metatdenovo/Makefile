DARDEL_DOWNLOAD = rsync -avhP --size-only dardel:/cfs/klemming/projects/supr/snic2020-16-76/projects/assembly/metaT/LMO_2016-17_polyA_metat/
DARDEL_SUMMARY_DOWNLOAD = $(DARDEL_DOWNLOAD)/results/summary_tables/$@ ./.

all: PF03842.faa.gz megahit_assembly.contigs.fa.transdecoder.pep.gz megahit.transdecoder.counts.tsv.gz megahit.transdecoder.emapper.tsv.gz megahit.transdecoder.hmmrank.tsv.gz megahit.transdecoder.mmetsp_taxonomy.tsv.gz megahit.transdecoder.overall_stats.tsv.gz

megahit_assembly.contigs.fa.transdecoder.pep.gz:
	$(DARDEL_DOWNLOAD)/results/transdecoder/megahit.transdecoder/$@ ./.

megahit.transdecoder.counts.tsv.gz:
	$(DARDEL_SUMMARY_DOWNLOAD)

megahit.transdecoder.emapper.tsv.gz:
	$(DARDEL_SUMMARY_DOWNLOAD)

megahit.transdecoder.hmmrank.tsv.gz:
	$(DARDEL_SUMMARY_DOWNLOAD)

megahit.transdecoder.mmetsp_taxonomy.tsv.gz:
	$(DARDEL_SUMMARY_DOWNLOAD)

megahit.transdecoder.overall_stats.tsv.gz:
	$(DARDEL_SUMMARY_DOWNLOAD)

PF03842.faa.gz:
	$(DARDEL_DOWNLOAD)/results/hmmer/hits/megahit.transdecoder.$@ $@
