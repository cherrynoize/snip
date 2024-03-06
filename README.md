# snip - screenshot/screencast utility

I had been using `peek` for a while. Since it stopped working I
couldn't find *any* screencast utility that worked for me in all
scenarios (switching desktops, windows, window managers, ...).

Eventually I was wasting so much time looking through the [list
of screencast utilies on the Arch wiki](https://wiki.archlinux.org/title/Screen_capture#Screencast_software)
that I just figured I'd write my own.

You can't say that it's perfect but it does everything I need and
some.

## Dependencies

```
bash scrot ffcast ffmpeg
dunstify optipng # (optional)
```

## Install

```
git clone https://github.com/cherrynoize/snip
cd snip
chmod +x snip
cp snip /usr/local/bin/snip
# if one doesn't exist copy example configuration
cp -n sniprc.example "${SNIPRC:-"${XDG_CONFIG_HOME:-"$HOME/.config/snip"}"}/sniprc"
```

Or use any other location that you like.

## Uninstall

```
rm /usr/local/bin/snip
```

## Usage

```
snip help
```

## TODO

- 'convert' command, to convert between different file formats

- Support for other notification utilies than `dunstify`
