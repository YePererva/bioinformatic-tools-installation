# GTDB-Tk

[Documentation](https://ecogenomics.github.io/GTDBTk/) | [GitHub](https://github.com/Ecogenomics/GTDBTk)

Refer to [hardware requirements](https://ecogenomics.github.io/GTDBTk/installing/index.html#hardware-requirements) for this software: 250 GB of RAM!!!!

## Installation with `conda` and automatic database download

Currently, version 1.7  + R202

```
cd ~/Downloads
conda create -n gtdbtk -c conda-forge -c bioconda gtdbtk
wget https://github.com/bioconda/bioconda-recipes/blob/master/recipes/gtdbtk/download-db.sh
sudo chmod +x ./download-db.sh
./download-db.sh

rm  -f ./download-db.sh
```


## For less performative PCs

1.42 + R95

```
cd ~/Downloads
conda create -n gtdbtk-1.4.2 -c conda-forge -c bioconda gtdbtk=1.4
conda activate gtdbtk-1.4.2

# make sure it is not pointing to the freshest installation
echo ${GTDBTK_DATA_PATH}

wget https://data.gtdb.ecogenomic.org/releases/release95/95.0/auxillary_files/gtdbtk_r95_data.tar.gz -P ${GTDBTK_DATA_PATH}

tar xvzf gtdbtk_r95_data.tar.gz -C ${GTDBTK_DATA_PATH} --strip 1
rm gtdbtk_r95_data.tar.gz

conda deactivate
```
