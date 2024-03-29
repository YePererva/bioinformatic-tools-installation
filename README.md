# [Bioinformatic tools installation guides](https://yepererva.github.io/bioinformatic-tools-installation/)
Collection of instructions for installation of various bioinformatic tools.

Some categorisation and software list were borrowed from:
- [Holland Computing Center](https://hcc.unl.edu/docs/applications/app_specific/bioinformatics_tools/)
- [Metagenomics.wiki](http://www.metagenomics.wiki/tools/assembly)
- [The University of Texas in Austin](https://wikis.utexas.edu/display/bioiteam/Software)
- [Hummingbird Computational Cluster](https://www.hb.ucsc.edu/documentation/hummingbird-hardware-configurations/)
- [BioLinux](http://environmentalomics.org/bio-linux-software-list/)

## List of software in instructions

- Quality assessment of raw sequences:
  - [FastQC](./software/quality_assessment/fastqc.md)
  - [QUAST](./software/quality_assessment/quast.md)

- Annotation:
  - [prokka](./software/annotation/prokka.md)

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
  - [Abyss](./software/de_novo_assemblers/abyss.md)
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

- Taxonomic classification
  - [GTDB-Tk](./software/taxonomic_classification/gtdbtk.md)

- General purpose tools:
  - [BioPerl](./software/general_purpose/bioperl.md)
  - [BioPython](./software/general_purpose/biopython.md)
  - [Bio++ Suite](./software/general_purpose/bio++suite.md)
  - [Anaconda3](./software/general_purpose/anaconda.md)

## Remark regarding Ubuntu
**NB! :** When referring to Ubuntu, it refers to both native Ubuntu installation and Ubuntu running from under Windows

To install Ubuntu from under Windows 10:
1. `Start` button -> type `Control Panel` -> navigate to `Programs and Features` -> Click on `Turn Windows Features on or off`
In the popped-up windows find `Windows Subsystem for Linux` checkbox and make sure it's checked.
2. Reboot Windows.
3. OPTIONAL:\
  - If windows is not fully updated, it uses WSL 1, but WSL2 is more preferable. To force use of WSL2, open `PowerShell` and type `wsl.exe --set-default-version 2`
  - after that update Windows 10, reboot may be required
4. `Start` button -> Type `Microsoft Store` -> Find `Ubuntu` or `Ubuntu 20.04 LTS` and install it.
5. To run `Ubuntu`: `Start` button -> type `bash` and hit `Enter`
6. There are issues with `snapd` running at `WSL`. Better to remove it: `sudo apt remove snapd -y`


To upgrade the Ubuntu on Windows 10 WSL (not from 20.04!)

1. [Download](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) and install [WSL2 core update](https://docs.microsoft.com/en-gb/windows/wsl/install-manual#step-4---download-the-linux-kernel-update-package)
2. Force use of WSL 2
  - Open `PowerShell` and run `wsl.exe --set-default-version 2`
3. Convert the existing installation of Ubuntu to WSL2 :
  - Open `PowerShell` and run`wsl.exe --set-version Ubuntu 2`
4. Update Windows 10 (reboot may be required)
5. run `bash` and perform:
  - `sudo apt remove snapd -y`
  - `sudo apt update && sudo apt full-upgrade -y`
  - edit `/etc/update-manager/release-upgrades` file and make sure that line with `Prompt=` is `Prompt=normal`
  - `sudo do-release-upgrade -d`
6. Restart the linux terminal

## Environment Modules

[Project Website](http://modules.sourceforge.net/) | [Github](https://github.com/cea-hpc/modules) | [Wikipedia](https://en.wikipedia.org/wiki/Environment_Modules_(software))

`Environment Modules` can be installed for:
- Ubuntu 20.04, 21.10:\
  `sudo apt install environment-modules -y`
- Fedora 33:\
  `sudo dnf install environment-modules -y`
- CentOS 8:\
  `sudo yum install environment-modules`
- Arch:\
  `sudo pamac -S env-modules` (not tested yet)
