[HISAT2](https://daehwankimlab.github.io/hisat2/) + [HISAT-genotype](https://github.com/DaehwanKimLab/hisat-genotype)

# Ubuntu 20.04
```
sudo apt install hisat2 --help
git clone https://github.com/DaehwanKimLab/hisat-genotype.git ~/hisatgenotype
cd hisatgenotype
bash setup.sh -r
# to replace all association with Python2 as with Python3
find ./ -type f -name *.py -exec sed -i '1 s/python/python3/g' {} \;

hisatgenotype --help
```

**NB! :** hisat is not available anymore for installation via `apt install`
