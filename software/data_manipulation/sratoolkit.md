# Ubuntu 20.04
```
wget --output-document sratoolkit.tar.gz http://ftp-trace.ncbi.nlm.nih.gov/sra/sdk/current/sratoolkit.current-ubuntu64.tar.gz
tar -xvzf ./sratoolkit*.tar.gz
sudo mv ./sratoolkit*/ /usr/local/sratoolkit
export PATH=$PATH:/usr/local/sratoolkit/bin
```
