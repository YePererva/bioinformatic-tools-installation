# QUality ASsessment Tool for Genome Assemblies
[Project web page](http://quast.sourceforge.net/quast)

As of the moment of writing this, the latest stable version [QUAST 5.0.2]() contains a [known bug](https://github.com/ablab/quast/issues/140) `AttributeError: module 'cgi' has no attribute 'escape'`. It's [suggested](https://github.com/ablab/quast/issues/140#issuecomment-624808866) to use pre-release [QUAST 5.1.0 RC1](https://github.com/ablab/quast/releases/tag/quast_5.1.0rc1) where this bug is fixed.
## Ubuntu 20.04

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

## Fedora 33
```
# Install prerequisites
sudo dnf install -y python3-matplotlib freetype freetype-devel zlib-devel pkgconf-pkg-config libpng-devel

wget https://github.com/ablab/quast/releases/download/quast_5.1.0rc1/quast-5.1.0rc1.tar.gz
tar -xzvf quast-5.1.0rc1.tar.gz
cd ./quast-5.1.0rc1
```

Installer is supposed to use Python 2, which is deprecated. To force use of Python 3, edit the `./setup.py` script:
```
  nano ./setup.py
```
And edit the first line:
```
#!/usr/bin/env python
```
to run with Python 3:
```
#!/usr/bin/env python3
```

Run and verify installation:
```
sudo ./setup.py install_full
./setup.py test
```
By defaults, it installs itself to `/usr/local/bin`, no need to keep installation files:
```
cd ~
sudo rm -rf ./quast
```
To check if it can run from any location:
```
wget quast.sf.net/test_data.tar.gz && tar -xvzf test_data.tar.gz
quast.py --test
```
