
# SC_MS_based_keyframe_extraction

This repository contains the code of the following paper.
- Yujie Li, Atsunori Kanemura, Hideki Asoh, Taiki Miyanishi, and Motoaki Kawanabe, "Extracting key frames from first-person videos in the common space of multiple sensors", _IEEE International Conference on Image Processing (ICIP)_, pp. 3993–3997, September 2017.

This code costs time, maybe some hours.

This software is licensed under the Apache License 2.0.


## Information

We run this software on the following envirnment.

* Windows 10.
* MATLAB R2017b.
* Python
    * Anaconda2-5.2.0
    * Python 3.6.5
    * tensorflow 1.8.0
    * pandas 0.23.1
    * scipy 1.1.0
    * Pillow 5.1.0
* 7-zip
* Git for windows

This software use the following programs and data.

* Subject 08 Brownie (Video data)
    * http://kitchen.cs.cmu.edu/main.php
* VGG in TensorFlow
    * https://www.cs.toronto.edu/~frossard/post/vgg16/
* Sparse Modeling Representative Selection (SMRS) 
    * http://www.ccs.neu.edu/home/eelhami/codes.htm 
* canoncorr
    * The MathWorks, Inc.


## How to run.

1. Run setup.ps1 with Windows PowerShell.
2. Generate Yn2.mat data.
    1. Run saveYn2.py.
       (You can use any S08_Brownie_3DMGX1's data)
        * $ python saveYn2.py .\\S08_Brownie_3DMGX1\\2794_02-02_11_16_30-time.txt
3. Generate 08a.mat data.
    1. Apply vgg16.patch with patch.exe command.
        * $ patch.exe -p1 -i vgg16\\vgg16.patch
    2. Open and Run savepng.m with MATLAB.
    3. Run vgg16.py
        * $ cd vgg16
        * $ python vgg16.py
    4. Move generated vgg16\\08a.mat file to the current working directory.
        * $ cp 08a.mat ..\\
3. Open main.m by MATLAB.
4. Run main.


