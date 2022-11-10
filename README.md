# Rembg

Rembg Flask is a flask based web tool to remove background from images.

<p style="display: flex;align-items: center;justify-content: center;">
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/car-1.jpg" width="100" />
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/car-1.out.png" width="100" />
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/car-2.jpg" width="100" />
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/car-2.out.png" width="100" />
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/car-3.jpg" width="100" />
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/car-3.out.png" width="100" />
</p>

<p style="display: flex;align-items: center;justify-content: center;">
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/animal-1.jpg" width="100" />
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/animal-1.out.png" width="100" />
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/animal-2.jpg" width="100" />
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/animal-2.out.png" width="100" />
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/animal-3.jpg" width="100" />
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/animal-3.out.png" width="100" />
</p>

<p style="display: flex;align-items: center;justify-content: center;">
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/girl-1.jpg" width="100" />
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/girl-1.out.png" width="100" />
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/girl-2.jpg" width="100" />
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/girl-2.out.png" width="100" />
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/girl-3.jpg" width="100" />
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/girl-3.out.png" width="100" />
</p>

**If this project has helped you, please consider making Sba Stuff a [donation](https://www.buymeacoffee.com/sbastuff).**

### Configuration of Python
This is done on windows (Windows 10: x64 Bit) . If you want to implement follow same workflow.
1. Python 3.7.9 (x64 Bit) Portable (Released On 2020-10-02	Size: 35.6 MB): [Download From Source Forge](https://sourceforge.net/projects/portable-python/files/Portable%20Python%203.7/)
<p style="display: flex;align-items: center;justify-content: center;">
  <img src="https://github.com/Sba-Stuff/rembg-flask-by-sbastuff/blob/main/Guide/Download%20Python.png"/>
 </p>
 
2. Extract Downloaded Python Portable Exe. You Got lots of files and folders. Delete every folder except **App/Python/**
<p style="display: flex;align-items: center;justify-content: center;">
  <img src="https://github.com/Sba-Stuff/rembg-flask-by-sbastuff/blob/main/Guide/Kepp%20App%20Python%20Folder%20Only.png"/>
 </p>

### Installation

CPU support (I Used This):

Navigate to App/Python Folder. (You find Python.exe there.) Run CMD at that location and run following command
```bash
python.exe -m pip install rembg
```
<p style="display: flex;align-items: center;justify-content: center;">
  <img src="https://github.com/Sba-Stuff/rembg-flask-by-sbastuff/blob/main/Guide/Install%20RemBG.png"/>
 </p>
 
 
GPU support (If you are rich enough to buy Nividia CUDA GPUS, you can also try this.):

```bash
pip install rembg[gpu]
```

Download ZIP of this file and extract contents in IBR Folder in **App/Python/IBR/**

### Usage as a Flask

Install Flask Using this Command. This is as same as you did for RemBG.
```bash
python.exe -m pip install flask
```
Run CMD at location **App/Python/** and then run **Server.py** Present in IBR Folder using given command: 

```bash
"Full Path\"Python.exe "Full Path\IBR\Server.py"
```

### Models

On Windows, Type **%Username%** in Address Bar of Explorer, Hit Enter. Create a Folder Named  `.u2net` there. Download all these Models given below and place ins this `.u2net` folder.

The available models are:

-   u2net ([download](https://drive.google.com/uc?id=1tCU5MM1LhRgGou5OpmpjBQbSrYIUoYab) - [alternative](http://depositfiles.com/files/ltxbqa06w), [source](https://github.com/xuebinqin/U-2-Net)): A pre-trained model for general use cases.
-   u2netp ([download](https://drive.google.com/uc?id=1tNuFmLv0TSNDjYIkjEdeH1IWKQdUA4HR) - [alternative](http://depositfiles.com/files/0y9i0r2fy), [source](https://github.com/xuebinqin/U-2-Net)): A lightweight version of u2net model.
-   u2net_human_seg ([download](https://drive.google.com/uc?id=1ZfqwVxu-1XWC1xU1GHIP-FM_Knd_AX5j) - [alternative](http://depositfiles.com/files/6spp8qpey), [source](https://github.com/xuebinqin/U-2-Net)): A pre-trained model for human segmentation.
-   u2net_cloth_seg ([download](https://drive.google.com/uc?id=15rKbQSXQzrKCQurUjZFg8HqzZad8bcyz) - [alternative](http://depositfiles.com/files/l3z3cxetq), [source](https://github.com/levindabhi/cloth-segmentation)): A pre-trained model for Cloths Parsing from human portrait. Here clothes are parsed into 3 category: Upper body, Lower body and Full body.

#### How to train your own model

If You need more fine tunned models try this:
https://github.com/danielgatis/rembg/issues/193#issuecomment-1055534289

### Advance usage

Sometimes it is possible to achieve better results by turning on alpha matting. Example:

```bash
curl -s http://input.png | rembg i -a -ae 15 > output.png
```

<table>
    <thead>
        <tr>
            <td>Original</td>
            <td>Without alpha matting</td>
            <td>With alpha matting (-a -ae 15)</td>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/food-1.jpg"/></td>
            <td><img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/food-1.out.jpg"/></td>
            <td><img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/food-1.out.alpha.jpg"/></td>
        </tr>
    </tbody>
</table>

### In the cloud

Please contact me at danielgatis@gmail.com if you need help to put it on the cloud.

### References

-   https://arxiv.org/pdf/2005.09007.pdf
-   https://github.com/NathanUA/U-2-Net
-   https://github.com/pymatting/pymatting

### Buy me a coffee

Liked some of my work? Buy me a coffee (or more likely a beer)

<a href="https://www.buymeacoffee.com/danielgatis" target="_blank"><img src="https://bmc-cdn.nyc3.digitaloceanspaces.com/BMC-button-images/custom_images/orange_img.png" alt="Buy Me A Coffee" style="height: auto !important;width: auto !important;"></a>

### License

Copyright (c) 2020-present [Daniel Gatis](https://github.com/danielgatis)

Licensed under [MIT License](./LICENSE.txt)
