# Ubuntu 20.04

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
