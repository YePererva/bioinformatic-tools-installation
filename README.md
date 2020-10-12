# Bioinformatic tools installation guides
Collection of instructions for installation of various bioinformatic tools.

Some categorisation and software list were borrowed from [Holland Computing Center](https://hcc.unl.edu/docs/applications/app_specific/bioinformatics_tools/)

## Some of software, listed in instructions

### Quality assessment of raw sequences
- FastQC
- QUAST

### Alignment tools:
- BLAT
- Bowtie / bowtie2
- Clustal Omega [website](http://www.clustal.org/)
- TopHat2 (low maintenance, replaced by HISAT)
- [HISAT2](https://daehwankimlab.github.io/hisat2/) + [HISAT-genotype](https://github.com/DaehwanKimLab/hisat-genotype)
- BLAST2
- Burrows-Wheeler Aligner (BWA)

### Data Manipulation Tools:
- SRAtoolkit
- BamTools
- SAMtools

### *De novo* assembly tools
- [Velvet](https://github.com/dzerbino/velvet) / [Oases](https://github.com/dzerbino/oases)
- [Ray](https://github.com/sebhtml/ray)
- SOAPdenovo2
- SOAPdenovo
- [TrinityRNAseq](https://github.com/trinityrnaseq/trinityrnaseq/wiki)

  Don't be confused with trinity desktop environment

- SPAdes
- QIIME II

### Preprocessing tools
- Cutadapt
- PRINSEQ
- PRINSEQ++
- Scythe
- Sickle
- TagCleaner


### Reference based assembly tools
- Cufflinks

### Tools for removing / Detecting redundant sequences
- CAP3
- CD-HIT

### General purpose tools:
- BioPerl
- BioPython
- Bio++ Suite

## Remark regarding Ubuntu
**NB! :** When referring to Ubuntu, it refers to both native Ubuntu installation and Ubuntu running from under Windows

To install Ubuntu from under Windows 10:
1. `Start` button -> type `Control Panel` -> navigate to `Programs and Features` -> Click on `Turn Windows Features on or off`
In the popped-up windows find `Windows Subsystem for Linux` checkbox and make sure it's checked.
2. Reboot Windows.
3. `Start` button -> Type `Microsoft Store` -> Find `Ubuntu` or `Ubuntu 20.04 LTS` and install it.
4. To run `Ubuntu`: `Start` button -> type `bash` and hit `Enter`
