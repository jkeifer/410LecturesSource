name: inverse
layout: true
class: center, middle, inverse
---
# arcpy
---
layout: false
## Overview

1. What is arcpy?

2. Examples and concepts

3. Tips for getting started with arcpy
---
template: inverse
## What is arcpy?
---
## What is arcpy?

- the python API ESRI provides for accessing ArcGIS functions

- wrapper around ArcObjects classes and functions, not pure python

- how to access it:

```py
>>> import arcpy

# wanna know more?
>>> help(arcpy)
```
---
## What is arcpy?

arcpy is organized into functions, modules, and classes:

- each toolbox is a module under arcpy:
    - arcpy.management
    - arcpy.analysis
    - arcpy.cartography
    - arcpy.conversion
    - arcpy.sa (spatial analyst)
    - arcpy.na (network analyst)
    - etc.

- functions are then like:
    - arcpy.analysis.Buffer
    - arcpy.Buffer_analysis
---
## What is arcpy?

arcpy is organized into functions, modules, and classes:

- some functions are arcpy-only:
    - arcpy.da (data analysis functions)
    - arcpy.Describe
    - arcpy.Exists
    - arcpy.ListFeatureClasses
    - arcpy.RasterToNumPyArray
    - arcpy.mapping (for map document automation)    
    - etc.

- arcpy has some classes:
    - SpatialReference
    - Cursor and Row
    - Fields
    - Result
    - Extent
    - Geometry (and Point, Polyline, Polygon, etc.)
    - etc.
---
template: inverse
## Examples and concepts
---
## Examples and concepts

```py
>>> import arcpy

# need to set environment variables
>>> from arcpy import env

# for example, overwrite any existing files
>>> env.overwriteOutput = True  # default False

# set input file
>>> shapefile = r"Z:\Documents\ArcGIS\roads_clipped.shp"

# set output path: doesn't exist, we are creating
>>> output = r"z:\Documents\ArcGIS\roads_buff.shp"

# run the analysis
>>> result = arcpy.Buffer_analysis(shapefile, output, "12 Yards", "LEFT", "ROUND")

# inspect the result: Buffer returns an object
>>> result
<Result 'z:\\Documents\\ArcGIS\\roads_buff.shp'>

>>> result.getOutput(0)
u'z:\\Documents\\ArcGIS\\roads_buff.shp'

# continued on next slide
```
---
## Examples and concepts

```py
# we can use the result as the input to other arcpy functions
# we can get the result's properties for further inspection
>>> desc = arcpy.Describe(result)

# what is its spatial reference? SpatialReference is a class...
>>> desc.SpatialReference
<geoprocessing spatial reference object object at 0x12360788>

# but we can get the SpatialReference name with this property
>>> desc.SpatialReference.name
u'NAD_1983_Albers'

# we can also see what type of data the result is
>>> desc.datasetType
u'FeatureClass'

# and its extent...oh, another object
>>> desc.extent
<Extent object at 0x2608cd0[0x12360788]>

# what about properties of the extent object
>>> desc.extent.height
472619.79527816735  # hmm, what units are these?

# let's find out
>>> desc.SpatialReference.linearUnitName
u'Meter'
```

---
template: inverse
## Tips for getting started with arcpy
---
## Tips for getting started with arcpy

- Read the docs.

- Read the docs.

- Try the ArcGIS python console

- Experiment

- "Copy as python snippet" in ArcGIS

- Read the docs.
