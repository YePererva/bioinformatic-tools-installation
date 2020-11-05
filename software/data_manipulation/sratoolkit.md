# sratoolkit

[Latest versions](https://trace.ncbi.nlm.nih.gov/Traces/sra/sra.cgi?view=software)

## Ubuntu 20.04
```
wget --output-document sratoolkit.tar.gz http://ftp-trace.ncbi.nlm.nih.gov/sra/sdk/current/sratoolkit.current-ubuntu64.tar.gz
tar -xvzf ./sratoolkit*.tar.gz
sudo mv ./sratoolkit*/ /usr/local/sratoolkit
export PATH=$PATH:/usr/local/sratoolkit/bin
```

## Fedora 33

```
wget --output-document sratoolkit.tar.gz https://ftp-trace.ncbi.nlm.nih.gov/sra/sdk/2.10.8/sratoolkit.2.10.8-centos_linux64.tar.gz
tar -xvzf ./sratoolkit*.tar.gz
# installing ncbi-magicblast
wget https://ftp.ncbi.nlm.nih.gov/blast/executables/magicblast/LATEST/ncbi-magicblast-1.5.0-x64-linux.tar.gz
tar zxvf ./ncbi-magicblast-*.tar.gz
sudo mv ./ncbi-magicblast-1.5.0/bin/* /usr/local/bin
```

Refer [to ](ftp://ftp.ncbi.nlm.nih.gov/blast/executables/magicblast/LATEST) for the latest Magiblast binary
