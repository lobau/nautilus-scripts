# nautilus-scripts
A repository of scripts for Nautilus, also known as Files (or Gnome Files)

Most of those scripts are related to UI design, graphic design, or motion design. 

Nautilus Scripts are just bash scripts, so you will need to install the appropriate command line tools for them to work (super easy):

- icotool to generate .ico files
- inkscape to convert vector files
- jpegoptim to optimize JPEG (aka Crunch)
- pngquant to optimize PNGs (aka Crunch)
- ffmpeg to manipulate videos (extract audio, remove audio, resize video, convert format or generate GIFs)

## Installing the command-line tools

The simplest way if you are on Fedora is to run:

`sudo dnf install icoutils inkscape jpegoptim pngquant ffmpeg`

I assume it would work the same on Debian with apt-get but I cannot test it.

## Installing the scripts

Just move the scripts you want to use to `Home/.local/share/nautilus/scripts` or just right click on anything in Nautilus, and select "Open Script Folder"

## Warning
Some of the scripts overwrite the original file. For example the scripts to crunch PNGs or JPG have a variant which create a new file and a variant which overwrite the original (clearly labeled "overwrite"). Please be careful! 

## Contributing

Call to all designers using Gnome! Help me build a great repository of scripts to make our live so much easier :-)
Pull requests are welcome!