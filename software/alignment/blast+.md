# Blast+

[Basic Local Alignment Search Tool](https://blast.ncbi.nlm.nih.gov/Blast.cgi)

[FTP server](https://ftp.ncbi.nlm.nih.gov/blast/executables/blast+/LATEST/)

## Ubuntu 20.04
```
sudo apt install ncbi-blast+
```

## Fedora 33
```
# Prerequisites
sudo dnf install -y perl-core
# Installation
wget https://ftp.ncbi.nlm.nih.gov/blast/executables/blast+/LATEST/ncbi-blast-2.10.1+-x64-linux.tar.gz
tar -xvzf ./ncbi-blast-2.10.1+-x64-linux.tar.gz
mv ./ncbi-blast-2.10.1+/bin/* /usr/local/bin
# test installation
blastn -help
blastn -version
# update database
update_blastdb.pl --passive --decompress 16S_ribosomal_RNA
```
