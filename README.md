# snip - screenshot/screencast utility

I had been using `peek` for a while. Since it stopped working I
couldn't find *any* screencast utility that worked for me in all
scenarios (switching desktops, windows, window managers, ...).

Eventually I was wasting so much time looking through the [list
of screencast utilies on the Arch wiki](https://wiki.archlinux.org/title/Screen_capture#Screencast_software)
that I just figured I'd write my own.

You can't say that it's perfect but it does everything I need and
some.

## Install

```
git clone https://github.com/cherrynoize/snip
cd snip
chmod +x snip
ln snip /usr/local/bin/snip
```

Or just place it anywhere that is easily reachable.

## Usage

```
snip help
```

## TODO

Add support for different formats, such as `mp4` for record:

```
ffmpeg -f x11grab -video_size 1920x1080 -framerate 25 -i $DISPLAY -f alsa -i default -c:v libx264 -preset ultrafast -c:a aac screen.mp4
```
