# PROKKA

[Github](https://github.com/tseemann/prokka) | [Project](https://www.vicbioinformatics.com/software.prokka.shtml)

# Ubuntu 20.04
```
sudo apt update
sudo apt install -y libdatetime-perl libxml-simple-perl libdigest-md5-perl git default-jre bioperl
sudo cpan Bio::Perl
sudo cpan Bio::SearchIO::hmmer3
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
And now, can be run as `prokka`. This will be enough to run from interactive shell, but not for scripts!

The better way:
```
sudo mv $HOME/prokka /usr/local
export PATH=$PATH:/usr/local/prokka/bin
```
Now, it can be ran as `prokka`

As stated [here](https://www.biostars.org/p/473293/), there is a conflict between NCBI annotation and PROKKA for prokaryotic genomes. Possibly, due to a different databases.
Fixable as:
```
cd /usr/local/prokka/db/hmm
rm -f ./*.hmm.*
# check link here for the latest release ftp://ftp.jcvi.org/pub/data/TIGRFAMs
wget ftp://ftp.jcvi.org/pub/data/TIGRFAMs/TIGRFAMs_15.0_HMM.LIB.gz
wget ftp://ftp.ebi.ac.uk/pub/databases/Pfam/current_release/Pfam-A.hmm.gz

# unpack and purge archives
gunzip ./*.gz

# Renaming databases to specify the order
# don't use '-' and '.' in names! it results in problems
mv TIGRFAMs_15.0_HMM.LIB 1_TIGRFAMs.hmm
mv Pfam-A.hmm 2_Pfam_A.hmm
mv HAMAP.hmm 3_HAMAP.hmm

# repeat indexing of databases
prokka --setupdb
```

May require purge:
```
prokka --cleandb
prokka --setupdb --dbdir /usr/local/prokka/db
```

**NB!**: There is a [known issue](https://github.com/tseemann/prokka/issues/139) that tool [tbl2asn](https://www.ncbi.nlm.nih.gov/genbank/tbl2asn2/) within `prokka` distribution is outdated. It results in errors alike ` Could not run command: tbl2asn ...`. The fresh tbl2ans can be taken [here](https://ftp.ncbi.nih.gov/toolbox/ncbi_tools/converters/by_program/tbl2asn/) and should replace the `tbl2asn` in the `prokka` distro.

Buy default it is located at `$home/prokka/binaries/linux/tbl2asn`. To do so:

```
# remove old file
rm -f $home/prokka/binaries/linux/tbl2asn
# download the new file as archive
wget https://ftp.ncbi.nih.gov/toolbox/ncbi_tools/converters/by_program/tbl2asn/linux64.tbl2asn.gz
# unpack the archive
gunzip ./linux64.tbl2asn.gz
# move / copy the binary to the target location (may require sudo depending on your location)
# or to any other location within $PATH variable
mv ./linux64.tbl2asn $home/prokka/binaries/linux/tbl2asn
# add permission to execute
sudo chmod +x $home/prokka/binaries/linux/tbl2asn
```


## Fedora 33

```
sudo dnf install -y git perl-Time-Piece perl-XML-Simple perl-Digest-MD5 perl-App-cpanminus git java perl-CPAN perl-Module-Build perl libnsl
sudo cpan XML::DOM::XPath --force
sudo cpan Bio::Perl
sudo cpan Bio::SearchIO::hmmer3
# this doesn't work for now:
sudo cpan Bio::Root::Version
sudo cpan Bio::DB::BioFetch
sudo cpan Bio::DB::WebDBSeqI

git clone https://github.com/tseemann/prokka.git /usr/local/prokka
/usr/local/prokka/bin/prokka --setupdb
```
