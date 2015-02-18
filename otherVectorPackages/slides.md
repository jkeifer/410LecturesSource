name: inverse
layout: true
class: center, middle, inverse
---
# Other Packages for Vector Analysis
---
layout: false
## Other Packages for Vector Analysis

### Overview

1. Scipy

2. PySAL

3. CGAL

4. SymPy
---
template: inverse
## Scipy
---
## Scipy

- SciPy, or **Sci**entific **Py**thon is two things:

    - a python package containing many tools for scientific
      computation and data analysis

    - an [ecosystem of scentific computing packages for python](http://scipy.org/),
      including numpy, IPython, Matplotlib, SymPy, and pandas

- SciPy has [many tools of potential utility to the GIS professional](http://docs.scipy.org/doc/scipy/reference/)

- Docs are of fairly high quality

- Good interfacing with numpy

    - broad support

    - FAST
---
template: inverse
## PySAL
---
## PySAL

- [PySAL](https://pysal.readthedocs.org/en/latest/index.html)
  is the **Py**thon **S**patial **A**nalysis **L**ibrary

    - Made by the same folks that made GeoDa, if you are into
      spatial statistics

- Indeed spatial statistics and spatial econometrics seem to
  be the primary focus but also includes geometry operations

- Docs are hit-or-miss

- Also includes support for reading/writing geospatial data

- Interface to work with Shapely
---
template: inverse
## CGAL
---
## CGAL

- [CGAL](http://www.cgal.org/) is a C++ library for computational geometry

    - Very feature packed and capable of performing advanced analysis

    - Has some algorithms I have not found in other libraries

- Problem: it is a C++ library (like GDAL)

    - Python supported through [auto-generated bindings](https://code.google.com/p/cgal-bindings/)
      lacking good documentation

- There if you need it, but probably not the best choice for most things
---
template: inverse
## SymPy
---
## SymPy

- [SymPy](http://docs.sympy.org/latest/index.html)
  is part of the SciPy ecosystem

- SymPy is **Sym**bolic **Py**thon: a computer algebra system for python

- Includes a [geometry module](http://docs.sympy.org/latest/modules/geometry/index.html)
  that allows operations using points, line, polygons, and other such geometries

- Not so much a GIS library, but perhaps useful

    - Also used in some examples about computational geometry,
      so it is good to be familiar with it if you are interested
      in that sort of thing
