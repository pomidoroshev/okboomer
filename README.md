# okboomer Package manager

A simple tool for building and installing apps from source code.

## Preparing local storage

```bash
$ mkdir ~/local
$ echo "export PATH=$HOME/local/bin:$PATH" > ~/.bashrc
$ cd ~/local
$ git clone https://github.com/pomidoroshev/okboomer.git
$ cd okboomer
```

## Usage

### Install

```bash
$ ./okboomer install <pkg_name>
```

By default `okboomer` calls `make -j` with unlimited jobs. Job limit can be set via `JOBS` variable:

```bash
$ JOBS=2 ./okboomer install <pkg_name>
```

### Uninstall

```bash
$ ./okboomer uninstall <pkg_name>
```

### Example

Install `vim` from official Github repository:

```bash
$ ./okboomer install vim
# ...
$ hash -r
$ which vim
/home/username/local/bin/vim
```

Uninstall `vim`:

```bash
$ ./okboomer uninstall vim
```

## Currently supported apps

- `vim`
- `mosh` (with `protobuf` dependency)
