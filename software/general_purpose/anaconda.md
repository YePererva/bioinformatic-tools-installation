# Anaconda

The instruction on web-site for Anaconda installation is quite straight forward, but results in some issues for use with SLURM. Here is recommendation for global installation.

## Installation

Assuming installation to `/opt/anaconda3`

```
sudo mkdir /opt/anaconda3
sudo chmod ugo+w /opt/anaconda3
#go to https://www.anaconda.com/products/individual to check the latest release and get its link
wget https://repo.anaconda.com/archive/Anaconda3-2021.05-Linux-x86_64.sh
# run installation with -u addition!
bash Anaconda3*.sh -u
```

Now, after agreeing with use licence it will ask for installation location. Type `/opt/anaconda3` and continue installation:
```
# set hooks
/opt/anaconda3/bin/conda shell.bash hook
/opt/anaconda3/bin/conda init
conda config --set auto_activate_base false
```

## After installation

Now, edit `sudo nano /etc/profile` and add following line to the end:
```
export PATH=""/opt/anaconda3/bin:$PATH"
```

To invoke the `conda` in SLURM task script, use the following line prior to activation of any `conda` environments:
```
source /opt/anaconda3/etc/profile.d/conda.sh
```
