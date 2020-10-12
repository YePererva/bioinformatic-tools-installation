# Ubuntu 20.04
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
