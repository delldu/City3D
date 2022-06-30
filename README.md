## City3D: Large-scale Building Reconstruction from Airborne LiDAR Point Clouds

City3D implements the hypothesis-and-selection based building reconstruction method described in the following [paper](https://www.mdpi.com/2072-4292/14/9/2254):
```
Jin Huang, Jantien Stoter, Ravi Peters, Liangliang Nan. 
City3D: Large-scale Building Reconstruction from Airborne LiDAR Point Clouds.
Remote Sensing. 14(9), 2254, 2022.
```

This implementation is based on [PolyFit](https://github.com/LiangliangNan/PolyFit).

---

### Obtaining City3D

You can build City3D from the source code˙

* Download the [source code](https://github.com/tudelft3d/City3D).
* Dependencies
    - [Qt](https://www.qt.io/) (v5.12 and later)
    - [CGAL](http://www.cgal.org/index.html) (v5.0 and later)
    - [OpenCv](https://opencv.org/releases/) (v4.0 and later, only the main modules are needed)
    - [Gurobi](https://www.gurobi.com/) (v9.5)

* Build
    - There are many ways to build City3D. Choose one of the following (or whatever you are familiar with):
        - Option 1: Use any IDE that can directly handle CMakeLists files to open the CMakeLists.txt in the root directory of City3D. Then you should have obtained a usable project and just build. I recommend using [CLion](https://www.jetbrains.com/clion/).
        - Option 2: Use CMake to generate project files for your IDE. Then load the project to your IDE and build.
        - Option 3: Use CMake to generate Makefiles and then `make` (on Linux/macOS) or `nmake`(on Windows with Microsoft Visual Studio). For Windows users,  you can also install Linux on Windows with  [WSL](https://docs.microsoft.com/en-us/windows/wsl/install). For Linux or macOS, you can simply
            ```
            $ cd City3D
            $ mkdir Release
            $ cd Release
            $ cmake -DCMAKE_BUILD_TYPE=Release ..
            $ make
            ```
---

### Run City3D
This demo version adapts the UI of [PolyFit](https://github.com/LiangliangNan/PolyFit), which provides a simple user interface with a few buttons (with numbered icons) and screen hints corresponding to these steps. Just click the buttons following the hints.

---
![](./images/GUI.png)
### Data
Some test data can be downloaded from the [data](https://github.com/tudelft3d/City3D/tree/main/data) directory.

---

### About the solvers
We recommend using Gurobi 9.5, which is the fastest solver for integer programming. You may need to obtain a license (free for academic use) from [here](https://www.gurobi.com/downloads/end-user-license-agreement-academic/).

---

### Citation
If you use the code/program (or part) of City3D in a scientific work, please cite our paper:

```bibtex
@Article{HuangCity3d_2022,
    AUTHOR = {Huang, Jin and Stoter, Jantien and Peters, Ravi and Nan, Liangliang},
    TITLE = {City3D: Large-Scale Building Reconstruction from Airborne LiDAR Point Clouds},
    JOURNAL = {Remote Sensing},
    VOLUME = {14},
    YEAR = {2022},
    NUMBER = {9},
    ARTICLE-NUMBER = {2254},
}

```

## TODOs
This is an academic prototype of LoD2 building reconstruction from LiDAR point clouds. Many intermediate steps can be improved.
- [ ] Integrate with other line segments detector, like [LSD](http://www.ipol.im/pub/art/2012/gjmr-lsd/?utm%20source=doi)
- [ ] Use more robust plane segmentation methods, like [PDPC](https://github.com/STORM-IRIT/Plane-Detection-Point-Cloud)
- [ ] Compare our cluster based shape regularization scheme with the one in [CGAL](https://doc.cgal.org/latest/Shape_regularization/index.html)
                           

---

### License
This program is free software; you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation; either version 3 of the License or (at your option) any later version. The full text of the license can be found in the accompanying LICENSE file.

---

Should you have any questions, comments, or suggestions, please feel free to contact me at:
J.Huang-1@tudelft.nl 

**_Jin Huang_**

https://yidahuang.github.io/

June 28, 2022

Copyright (C) 2022 

