


```
# python-opencv tutorial
https://opencv-python-tutroals.readthedocs.io/en/latest/py_tutorials/py_tutorials.html

# conda env support in jupyter notebook
conda install nb_conda

# select conda env for jupyter notebook
conda env create -f cv_project.yml
conda activate cv_project

# download the datasets 
python3 demosaicing/download_kodak.py --output-dir=data/kodak
```


## Questions 

+ is R,G,B in exposure space or log of that ...
+ psnr comparison 
    + numbers are different (even for bilinear)
    + the results are often times conflicting, i.e. 2016 Klatz is a lot worse than 2014 flexISP in `demosaicnet` but the reverse is true in Klatz's paper


## Learning

+ light transport, lambertian reflectance, albedo, image formation model (Forsyth 2503 multiview geometry)
+ photometric stereo (2503 slides+a1)
+ structured light
    + https://www.osapublishing.org/DirectPDFAccess/FBC163A9-EDFF-9962-3464BD70B5AC1546_211561/aop-3-2-128.pdf?da=1&id=211561&seq=0&mobile=no
+ compressive sensing 
    + http://www.cs.toronto.edu/~kyros/courses/2530/papers/Lecture-10/Hitomi2011.pdf
    + https://ieeexplore.ieee.org/document/7442841?tp=&arnumber=7442841
+ computational photography
    + http://www.cs.toronto.edu/~kyros/courses/2530/
    + https://stanford.edu/class/ee367/
+ discrete differential geometry 
    + https://graphics.stanford.edu/courses/cs468-13-spring/


## Random

+ can do hrdr with 2-bit camera as well
+ for c2b, rgb packed into rggb, g channel does not have additional information since they are simply the same subsampled image duplicated.
+ regarding goals for different reconstruction tasks
    + spectral imaging: constant-hue, no abrupt hue change over edges
    + structured light, stereo: devoid of artifacts
+ arbitrary mosaic tiling: adaptive graph laplacian