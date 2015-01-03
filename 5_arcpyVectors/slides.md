name: inverse
layout: true
class: center, middle, inverse
---
# Workng with Vectors in arcpy
---
layout: false
## Working with Vectors in arcpy

### Overview

1. Using More Toolbox Tools

2. Feature Layers

3. SQL Queries with arcpy

4. Selecting Data

5. An Example Vector Workflow
---
template: inverse
## Using More Toolbox Tools
---
## Using More Toolbox Tools

- Online documentation of all tools is geared toward arcpy

    - See [the Tool Reference](http://resources.arcgis.com/en/help/main/10.2/index.html#/A_quick_tour_of_geoprocessing_tool_references/002t0000000z000000/)
---
template: inverse
## Layers and Views in arcpy
---
## Layers and Views in arcpy

- When a dataset is opened in ArcMap it becomes a Layer

- A table is opened as a View

- Layers and Views allow some non-destructive operations

    - Selection

    - Symbolization
---
## Layers and Views in arcpy

- Many types of layers/views:

    - Feature Layer

    - Image Server Layer

    - LAS Dataset Layer

    - Mosaic Layer

    - Query Layer

    - Query Table

    - Raster Catalog Layer

    - Raster Layer

    - Table View

    - WCS Layer

    - XY Event Layer
---
## Layers and Views in arcpy

- Create a feature layer in ArcMap by adding feature class to map document

- How to create in arcpy?

```py
>>> import arcpy

# an point feature class
>>> featureclass = r"C:\GIS\Data\NatlForests.gdb\Trees"

>>> featurelayer = arcpy.MakeFeatureLayer_management(featureclass,
                                                     "TreesLayer")

>>> featurelayer
(Result 'TreesLayer')

# the layer is a Layer object from the arcpy.mapping module
>>> featurelayer[0]
(map layer u'TreesLayer')
```
---
template: inverse
## SQL Queries
---
## SQL Queries

---
## SQL Queries


---
template: inverse
## Selecting Data
---
## Selecting Data

---
## Selecting Data: By Attributes

---
## Selecting Data: By Location

---
## Selecting Data: arcpy.Select_management()


---
template: inverse
## An Example Vector Workflow
---
## An Example Vector Workflow

---
