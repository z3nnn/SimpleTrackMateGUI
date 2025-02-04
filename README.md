
# Simple TrackMate GUI v0.0.1

This plugin was created to simplify the process of running TrackMate to a batch of files. It has a simple interface with only a few of the parameters that the intended user has to use.


## Installation

There are a few prerequisites for installing this plugin:

1. Download FIJI from this website
   https://imagej.net/software/fiji/downloads

2. Once you have downloaded FIJI choose a place to locate the folder of installation, if you have Windows you may have issues placing it in some folders that have administration restrictions like "C:\Program Files\", so its advised to place it in other folder of your user that does have them.

3. Install TrackMate, this plugin uses TrackMate v7.13.2, older versions won't work.

4. Place the "SimpleTrackMateGUI-0.0.1.jar" (it may be another version) file in your plugins folder  "./Fiji.app/plugins"

5. Restart FIJI, and run SimpleTrackMateGUI in the "Plugins" list.

## Features

Bolded features are what is actually visible in the interface

Simple TrackMate GUI has the following characteristics:

- **You can choose the root folder where the files are located**

- **You can choose the name of the channel for which you will use the tool**

- Physical Units set to "μm" for distance and "sec" for time
- Detector settings:
    - LoG detector:
        - **Estimated Object Diameter (μm): User selection**
        - **Threshold: User selection**
        - Subpixel localization: true
        - Radius: 0.25
        - Target Channel: 1
        - Median filtering: True
    - **Spot filter:**
        - **Remove percentage of border in X from both sides.** (must be below 50%)
        - **Remove percentage of border in Y from both sides.** (must be below 50%)

- Tracker settings:
    - Nearest Neighbor Tracker Factory:
        - Linking Max Distance: 0.5

- All spot and track statistics generated

After the tracking is done the all spots table file is generated, "allspotstable_automated.csv", the file is converted for MTrackJ use to 2 ".mdf" files, "tracks_automated_curated.mdf" and "tracks_automated.mdf", the curated file is the one that will be manually edited to the user needs, and the automated file will remain the same to provide a point of contrast.

## Folder structure

This is what your root folder structure should look, inside of it it has subfolders, 
which have a video for which you will use SimpleTrackMateGUI with the parameters mentioned before.

Following is an example used for mitochondrial nucleoid tracking automation, with both the channels
for the shape of the mitochondria (mito.tif) not used here, and the nucleoid of the
mitochondria (nuc.tif) used for the tracking.

```
├── Root folder
│   ├── Folder_0
│   │   ├── Video.tif
│   │   ├── mito.tif
│   │   ├── nuc.tif
│   ├── Folder_1
│   │   ├── Video.tif
│   │   ├── mito.tif
│   │   ├── nuc.tif
│   ├── Folder_2
│   │   ├── Video.tif
│   │   ├── mito.tif
│   │   ├── nuc.tif
│   ├── ...
```

## Screenshots

![interface](https://github.com/user-attachments/assets/3a20343e-9f2d-413a-8b61-725a4c93ef99)

![borders](https://github.com/user-attachments/assets/da0642a5-012f-457a-a08a-f7350c48ae79)


## Support

If you have any issue using this plugin contact me at this email please :)\
matias.berasain@ug.uchile.cl
