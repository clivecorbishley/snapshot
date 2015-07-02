# Snapshot

## Install

You will need to install the following packages:

- ImageMagick
- Pdftk

Both of these can be installed using Homebrew, or apt-get.

You will also need to make sure that the script is executable:
```
$ chmod +x ./snapshot
```

### OSX

```
$ brew update
$ brew install imagemagick pdftk
```

### Linux

```
$ apt-get update
$ apt-get install imagemagick pdftk
```

## Config

### Hosts File
This is where the `hosts` file comes in. It's the scripts source for which hosts you would like to snapshot. 
Your hosts file should look like this, with one line per host.

```
host1.example.com
192.168.1.123
```

### SSH Key

You will need to ensure that your ssh-key is in the `authorized_keys` file for the root user on the host.

On OSX, the quickest way to get your ssh-key onto your clipboard is:
```
$ cat ~/.ssh/id_rsa.pub | pbcopy
```

## Running

```
$ ./snapshot
```

