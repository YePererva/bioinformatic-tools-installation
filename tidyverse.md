
## Ubuntu 20.04
```
# install prerequisites
sudo apt install -y r-base
sudo apt install -y libcurl4-openssl-dev libssl-dev libxml2-dev
# call for R
R
# now in R terminal
install.packages("tidyverse", dependencies = TRUE, INSTALL_opts = '--no-lock')
```

## Fedora 33
```
sudo dnf install -y R
sudo dnf install -y libcurl-devel openssl-devel libxml2-devel
# call for R
R
# now in R terminal
install.packages("tidyverse", dependencies = TRUE, INSTALL_opts = '--no-lock')
```
