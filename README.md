# nautilus-scripts
A repository of scripts for Nautilus, also known as Files (or Gnome Files)

Most of those scripts are related to UI design, graphic design, or motion design. 

Nautilus Scripts are just bash scripts, so you will need to install the appropriate command line tools for them to work (super easy):

- [icotool](https://www.systutorials.com/docs/linux/man/1-icotool/) to generate .ico files
- [inkscape](https://inkscape.org/) to convert vector files
- [jpegoptim](https://github.com/tjko/jpegoptim) to optimize JPEG (aka Crunch)
- [pngquant](https://pngquant.org/) to optimize PNGs (aka Crunch)
- [ImageMagick](https://imagemagick.org/) to convert image files
- [ffmpeg](https://ffmpeg.org/) to manipulate videos (extract audio, remove audio, resize video, convert format or generate GIFs)
- [Background Remover](https://github.com/nadermx/backgroundremover) to remove image backgrounds

## Installing the command-line tools on Fedora

Install [rpm-fusion](https://rpmfusion.org/) if you don't have it, and run:

```sh
sudo dnf install icoutils inkscape jpegoptim pngquant ffmpeg ImageMagick
```

It should work the same on Debian with `apt` instead of `dnf` but I cannot test it.

To install the requirements for Background Remover:
```sh
pip3 install torch torchvision torchaudio
pip install --upgrade pip
pip install backgroundremover
```

The first time you will run backgroundremover, it will download the model, so don't be alarmed if it takes a long time :)

## Installing the scripts

Just move the scripts you want to use to `Home/.local/share/nautilus/scripts` or just right click on anything in Nautilus, and select "Open Script Folder"

## Create an alias of this repository
Optionally, you can create an alias of this repository's "script" folder, so you can just pull new scripts directly.
First, create a backup of your current script folder

```sh
mv  ~/.local/share/nautilus/scripts/ ~/.local/share/nautilus/scripts_backup/
```

Then, create an alias of the repository folder (replace PATH_TO_THE_REPO with the actual path where you cloned this repository):

```sh
ln -s PATH_TO_THE_REPO/scripts ~/.local/share/nautilus/scripts
```

## Warning
Some of the scripts overwrite the original file. For example the scripts to crunch PNGs or JPG have a variant which create a new file and a variant which overwrite the original (clearly labeled "overwrite"). Please be careful! 
