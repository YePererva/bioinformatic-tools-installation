# Bowtie2
Refer to [build from source installation manual](http://bowtie-bio.sourceforge.net/bowtie2/manual.shtml#building-from-source)

## Ubuntu 20.04
```
sudo apt install -y bowtie bowtie2
```

## Fedora 33
Refer to [Sourceforge page](https://sourceforge.net/projects/bowtie-bio/files/bowtie2/) or [Github page](https://github.com/BenLangmead/bowtie2/releases) for the latest release.

I use the instalation from source since at the mooment of writing the installtion with conda (as recommended on [Github page of project](https://github.com/BenLangmead/bowtie2) doesn't work with Fedora 33 and Python 3.9)

```
sudo dnf install -y tbb-devel
cd
wget https://sourceforge.net/projects/bowtie-bio/files/bowtie2/2.4.2/bowtie2-2.4.2-source.zip
unzip ./bowtie2*.zip
rm ./bowtie2-2.4.2-source.zip
cd ./bowtie2-2.4.2
make
make static-libs
make sra-deps
```
