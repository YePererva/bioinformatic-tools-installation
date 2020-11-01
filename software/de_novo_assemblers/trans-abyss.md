# Trans-ABySS
De novo assembly of RNAseq data using ABySS

[Project](https://www.bcgsc.ca/resources/software/trans-abyss) | [Github](https://github.com/bcgsc/transabyss)

## Fedora 33
```
# install prerequisites
pip install python-igraph
#
cd
wget https://github.com/bcgsc/transabyss/releases/download/2.0.1/transabyss-2.0.1.zip
unzip ./transabyss-*.zip
```
Also, install [BLAT](/software/alignment/blat.md) and after that test installation:
```
bash ./transabyss-2.0.1/sample_dataset/assemble.sh
```
