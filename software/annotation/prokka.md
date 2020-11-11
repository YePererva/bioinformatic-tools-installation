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
export prokka=$HOME/prokka/bin/prokka
```

Now, can be ran as `$prokka`

## Fedora 33

```
sudo dnf install -y git perl-Time-Piece perl-XML-Simple perl-Digest-MD5 perl-App-cpanminus git java perl-CPAN perl-Module-Build
sudo cpanm Bio::Perl
git clone https://github.com/tseemann/prokka.git $HOME/prokka
$HOME/prokka/bin/prokka --setupdb
```
