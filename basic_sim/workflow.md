# Option 1: Separate Meshing Module
## Step 1: FreeCad model creation
- Create model
- Export as format: .STL

## Step 2: Salome mesher
- Take .STL format
- Mesh
- Export as 

## Step 3: 

# Option 2: Meshing with FreeCad
## Step 1: Create model with freecad
- e.g.: simple cube

## Step 2: Mesh with Freecad
Options
- Standard mesher
- Mefisto Mesher
- Netgen mesher
- Gmsh mesher -> Use gmesh

### Go to: FEM-workbench
- Press mesh with gmesh
- Select "apply"
- Select export as "unv"-format

## Step 3: Import / View Mesh in Elmer FEM
```
ElmerGrid 8 4 TwoBallsExport.unv -autoclean
```


# UNV file
Consists of
- Dataset-number
- Dataset

Following each other one after the other:
- https://victorsndvg.github.io/FEconv/formats/unv.xhtml

## Conversion of unv to VTK
In order to view a .unv file with paraview, you need sw like FEconv to view it with VTK.
