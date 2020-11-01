#ABYSS
ABySS is a de novo, parallel, paired-end sequence assembler that is designed for short reads.

[Project](https://www.bcgsc.ca/resources/software/abyss) | [Github](https://github.com/bcgsc/abyss)

# Fedora 33
```
# install prerequisites
sudo dnf install -y boost-devel sparsehash-devel openmpi
#
cd
wget https://github.com/bcgsc/abyss/releases/download/2.2.5/abyss-2.2.5.tar.gz
tar -xzf ./abyss-2.2.5.tar.gz
cd ./abyss-2.2.5
./autogen.sh
# to install at /usr/local
./configure
make
sudo make install
# to install to a different directory
./configure --prefix=/opt/abyss
make
sudo make install
# purge leftovers
cd ..
rm -rf ./abyss*
# test installation
wget http://www.bcgsc.ca/platform/bioinfo/software/abyss/releases/1.3.4/test-data.tar.gz
tar xzvf test-data.tar.gz
abyss-pe k=25 name=test in='test-data/reads1.fastq test-data/reads2.fastq'
abyss-fac test-unitigs.fa
```
