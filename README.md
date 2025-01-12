# Python Bulk Image Compressor + Resizer

![animation](https://github.com/georgekhananaev/py-image-compressor/blob/main/screenshots/animation.gif?raw=true)

### Basics

![Generic badge](https://img.shields.io/badge/Python_3.11-Supported-green.svg)

1. Install [Python 3+](https://www.python.org/downloads/)
2. Install [git](https://github.com/georgekhananaev/py-image-compressor)
3. Clone this repository: ```git clone https://github.com/georgekhananaev/py-image-compressor.git```
4. Install [requirements.txt](https://note.nkmk.me/en/python-pip-install-requirements/), cd into main folder and
   type: ```pip install -r requirements.txt```

### Usage:

| Command |  Weight  | Default Values |   Meaning   | Details                                                                                                                                                                                                                 |        Usage example         |
|:-------:|:--------:|:--------------:|:-----------:|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------:|
| **-l**  | required |      N/A       |  location   | your images path, where your original images located.                                                                                                                                                                   |  `-l "C:/Original Images/"`  |
| **-d**  | optional | /data/output/  | destination | your destination path, compressed images will be saved here                                                                                                                                                             | `-d "C:/Compressed Images/"` |
| **-w**  | optional |      1920      |  max width  | if larger resolution will be set to max width without breaking the image ratio                                                                                                                                          |          `-w 1920`           |
| **-q**  | optional |       80       |   quality   | images quality by percentage.<br/>lower quality to save more space                                                                                                                                                      |           `-q 80`            |
| **-f**  | optional |      jpeg      |   format    | supported format ".png", ".jpeg", ".jpg", ".ppm", ".gif", ".tiff", ".bmp", ".webp", ".heic", ".heif" <br/>for more check [PIL Documentation](https://pillow.readthedocs.io/en/stable/handbook/image-file-formats.html). |          `-f jpeg`           |
| **-r**  | optional |       no       |   remove    | remove images from destination path, <br/>if compression is worst than original file.                                                                                                                                   |            `-r y`            |
| **-h**  |    -     |       -        |    help     | if you forgot what command you want to use can write python main.py --help                                                                                                                                              |        `-h or --help`        |

_Import: for -l and -d, use quotation marks if have spaces._

**Examples:**

```
python main.py -l <Your Location> -d <Your Destination> -f <File Format> -w <Max Width> -q <Max Quality> -r <Remove Larger Files>
```

COMMAND:

```
python main.py -l "D:/Programming/React/resume-website/" -d "./data/out/" -f webp -w 500 -q 100
```

OUTPUT:
![terminal](https://github.com/georgekhananaev/py-image-compressor/blob/main/screenshots/screenshot.jpg?raw=true)

## Updates:

**06/04/2023
> 1. Updated readme.md.
> 2. Updated requirements.txt with latest versions packages.

**12/12/2022 👇️**
> 1. Added 'resources' folder, with configurations.ini file, all program settings will be stored there. This is a
     preparation for upcoming gui interface with memory.
> 2. Removed PySimpleGUI from dependencies, will use customtkinter instead for modern looking GUI.

**06/12/2022 👇️**
> 1. Added default values for -d, -f, -q -f, is no longer required fields. You can execute the code simply by
     typing: `python main.py -l "C:/Your Folder/"`, _default values is: jpeg format, quality 80%, max width 1080p,
     destination /data/output/_
> 2. Simplified the code with *args, **kwargs

**05/12/2022 👇️**
> 1. Added .heif, heic support, now you can convert photos from your iPhone too.
> 2. Updated requirements.txt, added PySimpleGUI(for future implementations), pillow-heif

**04/12/2022 👇️**
> 1. Added multicore image processing, now this is nearly 10 times faster.
     > ![terminal](https://github.com/georgekhananaev/py-image-compressor/blob/main/screenshots/multicore.gif?raw=true)
> 2. Better output for each image, you can see how much size you actually saved.
> 3. Started working on the GUI interface, will be executable at least on Windows/Ubuntu.
> 4. New command -r y, to avoid keeping larger compression images


#### GUI interface will be added if this project will get at least 50 stars...
- Due to my busy schedule, I will continue the development only if there will be actual demand.
- If you find bugs, feel free to open a issue.
- I personally use this script to compress images for react based websites and covert entire folder to webp with a single command.

