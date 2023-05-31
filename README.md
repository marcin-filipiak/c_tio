## Introduction

tio is a simple TTY terminal application which features a straightforward
commandline interface to easily connect to TTY devices for basic input/output.

It was created because the author needed a simple no-nonsense TTY terminal
application to easily connect to various terminal TTY devices.




## 2. Usage

The commandline interface is straightforward as reflected in the output from
'tio --help':
```
    Usage: tio [<options>] <tty-device>

    Options:
      -b, --baudrate <bps>        Baud rate (default: 115200)
      -d, --databits 5|6|7|8      Data bits (default: 8)
      -f, --flow hard|soft|none   Flow control (default: none)
      -s, --stopbits 1|2          Stop bits (default: 1)
      -p, --parity odd|even|none  Parity (default: none)
      -o, --output-delay <ms>     Output delay (default: 0)
      -n, --no-autoconnect        Disable automatic connect
      -e, --local-echo            Do local echo
      -l, --log <filename>        Log to file
      -m, --map <flags>           Map special characters
      -v, --version               Display version
      -h, --help                  Display help

    See the man page for list of supported mapping flags.

    In session, press ctrl-t q to quit.
```

The only option which requires a bit of elaboration is perhaps the
`--no-autoconnect` option.

By default tio automatically connects to the provided device if present.  If
the device is not present, it will wait for it to appear and then connect. If
the connection is lost (eg. device is unplugged), it will wait for the device
to reappear and then reconnect. However, if the `--no-autoconnect` option is
provided, tio will exit if the device is not present or an established
connection is lost.

Tio features full bash autocompletion support.

Tio also supports various key commands. Press ctrl-t ? to list the available
key commands.

See the tio man page for more details.


## License

Tio is GPLv2+. See COPYING file for license details.


## Authors

Created by Martin Lund \<martin.lund@keep-it-simple.com>
This version is modified by Marcin Filipiak

