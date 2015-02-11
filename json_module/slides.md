name: inverse
layout: true
class: center, middle, inverse
---
# The json Module
---
layout: false
## The json Module

### Overview

1. What is JSON?

2. What is GeoJSON?

3. Loading JSON data in python

4. Dumping JSON data in python
---
template: inverse
## What is JSON?
---
## What is JSON

- JSON stands for Javascript Object Notation

- A data-interchange format aimed at serializing data

- Made to be machine readble and human readable

- Extremely popular interchange format for web services
---
template: inverse
## What is GeoJSON?
---
## What is GeoJson

- [GeoJSON](http://geojson.org/geojson-spec.html#introduction)
  is an OGC standard for expressing geospatial data in JSON

- Allows a simple format for geospatial web applications

- Harder to see the implications of GeoJSON from the geography
  perspective, but it is taking over the internet via web mapping
---
template: inverse
## Loading JSON data in python
---
## Loading JSON data in python

- The json module allows loading and dumping of JSON data to and
  from native python dictionaries

- Loading is the process of taking a string of JSON and converting
  it to a dictionary

- Two functions in the json module for loading:

    - `json.load()`: to load JSON from a file object

    - `json.loads()`: to load JSON from a string (loads = load string)

```py
import json

with open(filepath) as fileobj:
    data = json.load(fileobj)

# data is a dictionary representation of the JSON data
```
---
template: inverse
## Dumping JSON data in python
---
## Dumping JSON data in python

- Dumping is the process of converting a dictionary into
  serailized JSON-formatted string

- Two functions in the JSON module for dumping:

    - `json.dump()`: to dump a dictionary to a file object

    - `json.dumps()`: to dump a dictionary to a JSON string

```py

data = {'name': 'Joe', 'age': 25, 'friends': ['Sam', 'Jane', 'Maria']}

with open(filepath, 'w') as fileobj:
    json.dump(data, fileobj)
```
