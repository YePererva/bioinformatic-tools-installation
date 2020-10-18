# FastQC
[Project web page](http://www.bioinformatics.babraham.ac.uk/projects/fastqc/) | [Github](https://github.com/s-andrews/FastQC)

## Ubuntu 20.04 LTS
```
sudo apt install fastqc
```

## Fedora 33
```
sudo dnf install -y perl

cd ~/genetics
wget https://www.bioinformatics.babraham.ac.uk/projects/fastqc/fastqc_v0.11.9.zip

unzip ./fastqc_v0.11.9.zip
rm ./fastqc_v0.11.9.zip

cd ./FastQC
chmod 755 ./fastqc

sudo ln -s /path/to/FastQC/fastqc /usr/local/bin/fastqc
```
