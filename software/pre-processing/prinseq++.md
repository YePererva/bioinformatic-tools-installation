# Ubuntu 20.04
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
