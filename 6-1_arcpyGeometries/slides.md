name: inverse
layout: true
class: center, middle, inverse
---
# arcpy Geometry Objects
---
layout: false
## arcpy Geometry Objects

# Overview

1. What is a Geometry object?

2. Types of Geometry objects

3. Some Geometry object properties and methods

3. arcpy Point and Array objects

4. How to use Geometry object: an example
---
template: inverse
## What is a geometry object?
---
## What is a geometry object?

- Geometry objects are used to store geometries

- Other things that store geometries:

    - Feature classes

    - [Well-know text (WKT) string](http://en.wikipedia.org/wiki/Well-known_text)

    - Well-known binary (WKB; see above link)

    - [GeoJSON](http://geojson.org/geojson-spec.html)
---
## What is a geometry object?

- Geometry objects are im memory (not persistent)

- They have properties and methods

- They cannot store attributes
---
template: inverse
## Types of Geometry objects
---
## Types of Geometry objects

- arcpy.PointGeometry (not to be confused with Point)

- arcpy.Polyline

- arcpy.Polygon

- arcpy.Muiltpoint

- **Note:** different names, different types,
  all the same properties and methods
---
template: inverse
## Geometry object properties and methods
---
## Geometry object properties and methods

- Object can return geometry in a number of other formats:

    - .JSON (assuming ESRI JSON, not GeoJSON)

    - .WKB

    - .WKT
---
## Geometry object properties and methods

- Geometric properties:

    - .area, .length

    - .centroid (always within the feature)

    - .trueCentroid (feature center of gravity)

    - .extent

    - etc.

- Others:

    - .type (point, polyline, polygon?)

    - .spatialReference
---
## Geometry object properties and methods

- Many [spatial methods:](http://resources.arcgis.com/en/help/main/10.2/index.html#//018z00000070000000)

    - .boundary()

    - .buffer(distance)

    - .clip(envelope)

    - .contains(second_geometry)

    - .distanceTo(other)

    - .intersect(second_geometry)

    - .projectAs(spatial_reference, {transformation name})
---
template: inverse
## arcpy Point and Array objects
