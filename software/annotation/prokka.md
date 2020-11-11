# PROKKA

[Github](https://github.com/tseemann/prokka) | [Project](https://www.vicbioinformatics.com/software.prokka.shtml)

# Ubuntu 20.04
```
sudo apt update && sudo apt install -y libdatetime-perl libxml-simple-perl libdigest-md5-perl git default-jre bioperl
sudo cpan Bio::Perl
git clone https://github.com/tseemann/prokka.git $HOME/prokka
$HOME/prokka/bin/prokka --setupdb
```

```
# this does work until next reboot
export prokka=$HOME/prokka/bin/prokka
# this also works until reboot
alias prokka="$HOME/prokka/bin/prokka"
```
Now, can be ran as `$prokka`, alternativelly, add as permanent alias by editing `~/.bashrc`:

```
alias prokka=$HOME/prokka/bin/prokka
```
And now, can be run as `prokka`. THis will be enugh to run from interactive shell, but not for scripts!

The better way:
```
sudo mv $HOME/prokka /usr/local
export PATH=$PATH:/usr/local/prokka/bin
```
Now, it can be ran as `prokka`

## Fedora 33

```
sudo dnf install -y git perl-Time-Piece perl-XML-Simple perl-Digest-MD5 perl-App-cpanminus git java perl-CPAN perl-Module-Build
sudo cpanm Bio::Perl
git clone https://github.com/tseemann/prokka.git $HOME/prokka
$HOME/prokka/bin/prokka --setupdb
```
