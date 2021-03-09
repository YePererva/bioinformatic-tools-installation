## Ubuntu 20.04
```
sudo apt install -y g++ cmake libbz2-dev zlibc zlib1g-dev
wget https://cab.spbu.ru/files/release3.15.1/SPAdes-3.15.1.tar.gz
tar -xzf ./SPAdes-3.15.1.tar.gz
rm ./SPAdes-3.15.1.tar.gz
cd ./SPAdes-3.15.1
sudo PREFIX=/usr/local ./spades_compile.sh
export PATH=/usr/local/bin:$PATH
```
  edit file `/usr/local/bin/spades.py` as `sudo nano /usr/local/bin/spades.py`:
  - find the first line: `#!/usr/bin/env python`
  - and replace it with: `#!/usr/bin/env python3`

## Fedora 33

```
# Install prerequisites
sudo dnf install -y g++ cmake zlib bzip2 bzip2-libs
# Download and unpack
wget http://cab.spbu.ru/files/release3.14.1/SPAdes-3.14.1.tar.gz
tar -xzvf SPAdes-3.14.1.tar.gz
cd SPAdes-3.14.1
# Install
sudo PREFIX=/usr/local ./spades_compile.sh
```
**NB! :** Compiling to `/usr/local` will require super user privileges and for both compiling and running SPAdes, **unless** adding `/usr/local/bin` to `$PATH` variable:
```
export PATH=/usr/local/bin:$PATH
```

SPAdes will try to run with Python 2, which is deprecated. To run by default with Python 3, edit the `/usr/local/bin/spades.py` script:
```
sudo nano /usr/local/bin/spades.py
```
And edit the first line:
```
#!/usr/bin/env python
```
to run with Python 3:
```
#!/usr/bin/env python3
```

Now try to run
```
spades.py --test
# or
spades.py --test --isolate
```
from any location.
