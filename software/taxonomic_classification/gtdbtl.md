# GTDB-Tk

[Documentation](https://ecogenomics.github.io/GTDBTk/) | [GitHub](https://github.com/Ecogenomics/GTDBTk)

## Installation with `conda` and automatic database download

```
cd ~/Downloads
conda create -n gtdbtk -c conda-forge -c bioconda gtdbtk
wget https://github.com/bioconda/bioconda-recipes/blob/master/recipes/gtdbtk/download-db.sh
sudo chmod +x ./download-db.sh
./download-db.sh

rm  -f ./download-db
```
