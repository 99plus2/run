# Run

[![TravisCI status](https://secure.travis-ci.org/runscripts/run.png)](http://travis-ci.org/runscripts/run) [![GoDoc](https://godoc.org/github.com/runscripts/run?status.svg)](https://godoc.org/github.com/runscripts/run) [![Gitter](https://badges.gitter.im/Join Chat.svg)](https://gitter.im/runscripts/runscripts?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

## Introducatoin

[Run](https://github.com/runscripts/run) is awaited manager for scripts, just like [homebrew](https://github.com/Homebrew/homebrew) and [bower](https://github.com/bower/bower).

It helps to manage your scripts and make reuse of scripts much easier. After installing run, you get the command `run`. Please `run pt-summary` and it will download the well-known pt-summary to run. If you push your scritps to GitHub, you can simply use it like `run github:runscripts/scripts/pt-summary`.

## Install

* From Scratch (Go 1.3+)

  Download the source code and execute `sudo GOPATH=$GOPATH make install`.

* From Binary

  Operating System | Architectures
  ---------------- | -------------
  Linux            | [386](https://raw.githubusercontent.com/runscripts/run/packages/packages/linux_386/run), [amd64](https://raw.githubusercontent.com/runscripts/run/packages/packages/linux_amd64/run), [arm](https://raw.githubusercontent.com/runscripts/run/packages/packages/linux_arm/run)
  Mac OS           | [386](https://raw.githubusercontent.com/runscripts/run/packages/packages/darwin_386/run), [amd64](https://raw.githubusercontent.com/runscripts/run/packages/packages/darwin_amd64/run)
  FreeBSD          | [386](https://raw.githubusercontent.com/runscripts/run/packages/packages/freebsd_386/run), [amd64](https://raw.githubusercontent.com/runscripts/run/packages/packages/freebsd_amd64/run)
  Debian/Ubuntu    | [386](https://raw.githubusercontent.com/runscripts/run/packages/packages/deb/run_20141202-0.2.2_386.deb), [amd64](https://raw.githubusercontent.com/runscripts/run/packages/packages/deb/run_20141202-0.2.2_amd64.deb)
  
  Download binary in the table according to your OS/Arch and place it in **$PATH** (like /usr/bin/). Then execute `sudo run --init`.

## Usage

:point_right: Watch the [one-minute video](https://www.youtube.com/watch?v=WXUcJvrZP6M) before you're using it.

```
Usage:
	run [OPTION] [SCOPE:]SCRIPT

Options:
	-c, --clean     clean out all scripts cached in local
	-h, --help      show this help message, then exit
	-i INTERPRETER  run script with interpreter(e.g., bash, python)
	-I, --init      create configuration and cache directory
	-u, --update    force to update the script before run
	-v, --view      view the content of script, then exit
	-V, --version   output version information, then exit

Examples:
	run pt-summary
	run github:runscripts/scripts/pt-summary

Report bugs to <https://github.com/runscripts/run/issues>.
```

## Scripts

We have provided [official scripts](https://github.com/runscripts/scripts) and everyone can easily `run pt-summary` and `run -i python get-pip.py`.

Feel free to manage your scripts in Github and send pull-request to official scripts.
