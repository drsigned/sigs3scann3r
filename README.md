# sigs3scann3r

[![release](https://img.shields.io/github/release/drsigned/sigs3scann3r?style=flat&color=0040ff)](https://github.com/drsigned/sigs3scann3r/releases) ![maintenance](https://img.shields.io/badge/maintained%3F-yes-0040ff.svg) [![open issues](https://img.shields.io/github/issues-raw/drsigned/sigs3scann3r.svg?style=flat&color=0040ff)](https://github.com/drsigned/sigs3scann3r/issues?q=is:issue+is:open) [![closed issues](https://img.shields.io/github/issues-closed-raw/drsigned/sigs3scann3r.svg?style=flat&color=0040ff)](https://github.com/drsigned/sigs3scann3r/issues?q=is:issue+is:closed) [![license](https://img.shields.io/badge/license-MIT-gray.svg?colorB=0040FF)](https://github.com/drsigned/sigs3scann3r/blob/master/LICENSE) [![twitter](https://img.shields.io/badge/twitter-@drsigned-0040ff.svg)](https://twitter.com/drsigned)

sigs3scann3r is tool to scan AWS S3 bucket permissions and dump bucket contents where applicable.

## Resources

* [Usage](#usage)
* [Installation](#installation)
	* [From Binary](#from-binary)
	* [From source](#from-source)
	* [From github](#from-github)
* [Contribution](#contribution)

## Usage

To display help message for sigs3scann3r use the `-h` flag:

```
$ sigs3scann3r -h

     _           _____                           _____      
 ___(_) __ _ ___|___ / ___  ___ __ _ _ __  _ __ |___ / _ __ 
/ __| |/ _` / __| |_ \/ __|/ __/ _` | '_ \| '_ \  |_ \| '__|
\__ \ | (_| \__ \___) \__ \ (_| (_| | | | | | | |___) | |   
|___/_|\__, |___/____/|___/\___\__,_|_| |_|_| |_|____/|_| v1.1.1
       |___/

USAGE:
  sigs3scann3r [OPTIONS]

OPTIONS:
  -dump          dump found open buckets locally (default: false)
  -iL            input buckets list (use `iL -` to read from stdin)
  -nC            no color mode (default: false)
  -o             buckets dump directory (default: ./buckets)
  -v             verbose mode
```

sigs3scann3r takes buckets in the format:
* name - e.g. `flaws.cloud`
* path style - e.g `https://s3.amazonaws.com/flaws.cloud`
* virtual hosted style - e.g `flaws.cloud.s3.amazonaws.com`

## Installation

#### From Binary

You can download the pre-built binary for your platform from this repository's [releases](https://github.com/drsigned/sigs3scann3r/releases/) page, extract, then move it to your `$PATH`and you're ready to go.

#### From Source

sigs3scann3r requires **go1.14+** to install successfully. Run the following command to get the repo

```bash
▶ GO111MODULE=on go get -u -v github.com/drsigned/sigs3scann3r/cmd/sigs3scann3r
```

#### From Github

```bash
▶ git clone https://github.com/drsigned/sigs3scann3r.git
▶ cd sigs3scann3r/cmd/sigs3scann3r/
▶ go build .
▶ mv sigs3scann3r /usr/local/bin/
▶ sigs3scann3r -h
```

## Contribution

[Issues](https://github.com/drsigned/sigs3scann3r/issues) and [Pull Requests](https://github.com/drsigned/sigs3scann3r/pulls) are welcome!