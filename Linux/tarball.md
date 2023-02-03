# Tarball

[GNU Tar](https://www.gnu.org/software/tar/) provides the ability to create tar archives, as well as various other kinds of manipulation. For example, you can use Tar on previously created archives to extract files, to store additional files, or to update or list files which were already stored.

## Install

GNU Tar should be installed by default, but if it is not, type on Debian based Distributions

```bash
sudo apt install -y tar tar-doc
```

## Usage
To create a [gzip](https://www.gzip.org/) compressed Tarball, or to extract one, type

```bash
# create tarball

tar -czvf example.tar.gz [DIRECTORY]

# extract tarball

tar -xzvf example.tar.gz
```