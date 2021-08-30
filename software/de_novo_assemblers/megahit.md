# Megahit

MEGAHIT is an ultra-fast and memory-efficient NGS assembler. It is optimized for metagenomes, but also works well on generic single genome assembly (small or mammalian size) and single-cell assembly.

[Github](https://github.com/voutcn/megahit)

Installation on Ubuntu (21.04):

```
# Install prerequisites
sudo apt update && sudo apt install zlib1g cmake gzip bzip2 -y
# copy the GitHub repository
cd ~ && git clone https://github.com/voutcn/megahit.git
cd megahit
git submodule update --init
# build and install
mkdir build && cd build
cmake .. -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_PREFIX=/usr/local
make -j4
sudo make install

# purge leftovers
cd ~ && rm -rf ./megahit

# test installation
megahit --test
```

Now, the start can be done systemwise just running `megahit`, but if occurred problem with `python` vs `python3`:
```
sudo nano /usr/local/bin/megahit
```

replace the first line `#!/usr/bin/env python` with `#!/usr/bin/env python3`

Nw, it should work fine.
