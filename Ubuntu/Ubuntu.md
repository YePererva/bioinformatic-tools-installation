
## Quality assessment of raw sequences
### FastQC
  ```
  sudo apt install fastqc
  ```
### QUAST
  ```
  sudo apt install -y zlib1g-dev pkg-config libfreetype6-dev libpng-dev python3-matplotlib
  cd ~
  wget https://github.com/ablab/quast/releases/download/quast_5.1.0rc1/quast-5.1.0rc1.tar.gz
  tar -xzf quast-5.1.0rc1.tar.gz
  rm ./quast-5.1.0rc1.tar.gz
  cd ./quast-5.1.0rc1
  ```
  Now, edit the `setup.py` script as `sudo nano ./setup.py`
  - find the first line: `#!/usr/bin/env python`
  - and replace it with: `#!/usr/bin/env python3`

  ```
  # install
  sudo ./setup.py install_full
  # test installation
  ./setup.py test
  ```

## Alignment tools:
### BLAT
[Sources](https://users.soe.ucsc.edu/~kent/src/)
[Binaries](http://hgdownload.cse.ucsc.edu/admin/exe/linux.x86_64/blat/)
[Other options](https://bioinformaticsonline.com/pages/view/37677/installing-blat-on-linux)
  ```
  wget http://hgdownload.cse.ucsc.edu/admin/exe/linux.x86_64/blat/blat
  sudo mv ./blat /usr/local/bin
  sudo chmod 755 /usr/local/bin/blat
  ```

### Bowtie / bowtie2
  ```
  sudo apt install -y bowtie bowtie2
  ```

### Clustal Omega [website](http://www.clustal.org/)
  ```
 sudo apt install clustalo
 # or for wversion with web-interface
 sudo apt install clustalx
 ```

### TopHat2 (low maintenance, replaced by HISAT)
```
wget https://ccb.jhu.edu/software/tophat/downloads/tophat-2.1.1.Linux_x86_64.tar.gz
tar -xvzf tophat-2.1.1.Linux_x86_64.tar.gz
mv tophat-2.1.1.Linux_x86_64/ /usr/local/bin/tophat/
export PATH=/usr/local/bin/tophat:$PATH
```

### HISAT2 + HISAT-genotype
[github](https://daehwankimlab.github.io/hisat2/)
```
sudo apt instal hisat2
hisat2 --help
git clone https://github.com/DaehwanKimLab/hisat-genotype.git ~/hisatgenotype
cd hisatgenotype
bash setup.sh -r
# to replace all association with Python2 as with Python3
find ./ -type f -name *.py -exec sed -i '1 s/python/python3/g' {} \;

hisatgenotype --help
```

### BLAST2
  ```
  sudo apt install ncbi-blast+
  ```
### Burrows-Wheeler Aligner (BWA)
  ```
  sudo apt install bwa
  ```

## Data Manipuation Tools:
### SRAtoolkit
```
wget --output-document sratoolkit.tar.gz http://ftp-trace.ncbi.nlm.nih.gov/sra/sdk/current/sratoolkit.current-ubuntu64.tar.gz
tar -xvzf ./sratoolkit*.tar.gz
sudo mv ./sratoolkit*/ /usr/local/sratoolkit
export PATH=$PATH:/usr/local/sratoolkit/bin
```

### BamTools
  ```
  sudo apt install bamtools
  ```
- SAMtools
  ```
  sudo apt install samtools
  ```

## *De novo* assembly tools

### Velvet / Oases
  ```
  git clone https://github.com/dzerbino/velvet
  cd ./velvet
  make
  cd ..
  git clone --recursive https://github.com/dzerbino/oases
  cd ./oases
  make OPENMP=1
  ```

### Ray
[WebSite](http://denovoassembler.sourceforge.net/), [Github](https://github.com/sebhtml/ray)
  ```
  sudo apt install ray
  ```
### SOAPdenovo2
  ```
  sudo apt install soapdenovo2
  ```
### SOAPdenovo
  ```
  sudo apt install soapdenovo
  ```
### Trinity
Don't be confused with trinity desktop environment

[GitHub](https://github.com/trinityrnaseq/trinityrnaseq/wiki)
  ```
  sudo apt install trinityrnaseq
  ```
### SPAdes
```
sudo apt install -y g++ cmake libbz2-dev zlibc zlib1g-dev
wget http://cab.spbu.ru/files/release3.14.1/SPAdes-3.14.1.tar.gz
tar -xzf ./SPAdes-3.14.1.tar.gz
rm ./SPAdes-3.14.1.tar.gz
cd ./SPAdes-3.14.1
sudo PREFIX=/usr/local ./spades_compile.sh
export PATH=/usr/local/bin:$PATH
```
  edit file `/usr/local/bin/spades.py` as `sudo nano /usr/local/bin/spades.py`:
  - find the first line: `#!/usr/bin/env python`
  - and replace it with: `#!/usr/bin/env python3`

## Preprocessing tools

### Cutadapt
  ```
  sudo apt install cutadapt
  ```

- PRINSEQ

### PRINSEQ++
```
# prerequisites
sudo apt-get install libcairo2-dev libpthread-stubs0-dev libboost-all-dev g++ make
wget https://github.com/Adrian-Cantu/PRINSEQ-plus-plus/releases/download/v1.2/prinseq-plus-plus-1.2.tar.gz
tar -xvf prinseq-plus-plus-1.2.tar.gz
cd prinseq-plus-plus-1.2
./configure
make
make test
sudo make install
# check installation
prinseq++ -h
```

### Scythe
```
sudo apt install -y scythe
```
### Sickle
```
sudo apt install -y sickle
```
- TagCleaner

## QIIME II

## Reference based assembly tools
### Cufflinks
  ```
  sudo apt install cufflinks
  ```

## Tools for removing / Detecting redundant sequences
### CAP3
  ```
  wget http://seq.cs.iastate.edu/CAP3/cap3.linux.x86_64.tar
  tar -xvf ./cap3.linux.x86_64.tar
  sudo cp -puv CAP3/{cap3,formcon} /usr/local/bin/
  rm CAP3 -rf
  ```

### CD-HIT
```
	sudo apt install zlib1g-dev
	git clone --recursive https://github.com/weizhongli/cdhit
	cd ./cdhit
	make
```

## General purpose tools:
### BioPerl:
  ```
  sudo apt install bioperl
  ```
### BioPython
  ```
  sudo apt install python3-pip && pip install biopython
  ```
### Bio++ Suite
	```
  sudo apt install bppsuite
  ```
