name: inverse
layout: true
class: center, middle, inverse
---
# Editing Attributes and Geometries with arcpy
---
layout: false
## Editing Attributes and Geometries

### Overview

1. What is a cursor?

2. Types of Cursors

3. arcpy.da Cursors

4. Cursors Example

5. Cursors and Geometries
---
template: inverse
## What is a cursor?
---
## What is a cursor?

- A cursor indicates position

    - A cursor in a text editor

- Databases use cursors move through rows in a table

- The cursor stores the position in the table

- We use cursors to retrieve, edit, and insert data into a table
---
template: inverse
## Types of Cursors
---
## Types of Cursors

- Three types of cursors:

    - Search

    - Update

    - Insert
---
## Types of Cursors

### Search Cursor

- Used to retrieve data

- Can not manipulate data: read-only

```py
EXAMPLE!!!!!!
```
---
## Types of Cursors

### Update Cursor

- Retrieves data

- Allows overwriting of data: read/write

- Cannot create new records

```py
EXAMPLE!!!!!!
```

---
## Types of Cursors

### Insert Cursor

- Does not retrieve data; works only on new rows

- Used to insert new records into a table: write-only

```py
EXAMPLE!!!!!!
```
---
template: inverse
## arcpy.da Cursors

- arcpy supplies `SearchCursor()`, `UpdateCursor()`, and `InsertCursor()`

- also `arcpy.da.SearchCursor()`, `arcpy.da.UpdateCursor()`, and `arcpy.da.InsertCursor()`

- `da` is Data Access module:
    
    - `da` cursors are faster

    - Require more explicit instructions

    - Should be used unless a good reason not to
---
## arcpy.da Cursors

---
## arcpy.da Cursors

---
template: inverse
## Cursors Example
---
## Cursors Example

---
## Cursors Example

---
template: inverse
## Cursors and Geometries
---
## Cursors and Geometries

---
## Cursors and Geometries

