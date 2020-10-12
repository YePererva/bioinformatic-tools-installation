# Bioinformatic tools installation guides
Collection of instructions for installation of various bioinformatic tools.

Some categorisation and software list were borrowed from [Holland Computing Center](https://hcc.unl.edu/docs/applications/app_specific/bioinformatics_tools/)

## Some of software, listed in instructions

- Quality assessment of raw sequences:
  - [FastQC](./software/quality_assessment/fastqc.md)
  - [QUAST](./software/quality_assessment/quast.md)

- Alignment tools:
  - [BLAT](./software/alignment/blat.md)
  - [Bowtie / Bowtie2](./software/alignment/bowtie.md)
  - [Clustal Omega](./software/alignment/clustal.md)
  - [TopHat2](./software/alignment/tophat2.md) (low maintenance, replaced by HISAT)
  - [HISAT2 + genotype](./software/alignment/hisat.md)
  - [BLAST2](./software/alignment/blast+.md)
  - [Burrows-Wheeler Aligner](./software/alignment/bwa.md) (BWA)

- Data Manipulation Tools:
  - [SRAtoolkit](./software/data_manipulation/sratoolkit.md)
  - [BAMTools](./software/data_manipulation/bamtools.md)
  - [SAMtools](./software/data_manipulation/samtools.md)

- *De novo* assembly tools:
  - [Velvet + Oases](./software/de_novo_assemblers/velvet+oases.md)
  - [Ray](./software/de_novo_assemblers/ray.md)
  - [SOAPdenovo2](./software/de_novo_assemblers/soapdenovo2.md)
  - [SOAPdenovo](./software/de_novo_assemblers/soapdenovo.md)
  - [SPAdes](./software/de_novo_assemblers/spades.md)
  - [QIIME II](./software/de_novo_assemblers/qiime_ii.md)
  - [TrinityRNAseq](./software/de_novo_assemblers/trinityrnaseq.md)

- Pre-processing tools:
  - [Cutadapt](./software/pre-processing/cutadapt.md)
  - [PRINSEQ](./software/pre-processing/prinseq.md)
  - [PRINSEQ++](./software/pre-processing/prinseq++.md)
  - [Scythe](./software/pre-processing/scythe.md)
  - [Sickle](./software/pre-processing/sinkle.md)
  - [TagCleaner](./software/pre-processing/tagcleaner.md)

- Reference based assembly tools:
  - [Cufflinks](./software/reference-based_assemblers/cufflinks.md)

- Tools for removing / Detecting redundant sequences
  - [CAP3](./software/redundancy_detectors_and_removers/cap3.md)
  - [CD-HIT](./software/redundancy_detectors_and_removers/cd-hit.md)

- General purpose tools:
  - [BioPerl](./software/general_purpose/bioperl.md)
  - [BioPython](./software/general_purpose/biopython.md)
  - [Bio++ Suite](./software/general_purpose/bio++suite.md)

## Remark regarding Ubuntu
**NB! :** When referring to Ubuntu, it refers to both native Ubuntu installation and Ubuntu running from under Windows

To install Ubuntu from under Windows 10:
1. `Start` button -> type `Control Panel` -> navigate to `Programs and Features` -> Click on `Turn Windows Features on or off`
In the popped-up windows find `Windows Subsystem for Linux` checkbox and make sure it's checked.
2. Reboot Windows.
3. `Start` button -> Type `Microsoft Store` -> Find `Ubuntu` or `Ubuntu 20.04 LTS` and install it.
4. To run `Ubuntu`: `Start` button -> type `bash` and hit `Enter`
