

## Fedora 33
AS of `QIIME II 2020.8`

```
sudo dnf install conda wget
wget https://data.qiime2.org/distro/core/qiime2-2020.11-py36-linux-conda.yml
conda env create -n qiime2-2020.11 --file qiime2-2020.8-py36-linux-conda.yml
rm ./qiime2-2020.8-py36-linux-conda.yml
```

```
# activate the environment
conda activate qiime2-2020.8
# test intallation
qiime --help
```

[Example use with SLURM](https://hcc.unl.edu/docs/applications/app_specific/bioinformatics_tools/qiime/)
