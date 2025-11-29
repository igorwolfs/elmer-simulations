# CAD design and Meshing
## Option 1: Separate Meshing Module
### Step 1: FreeCad model creation
- Create model
- Export as format: .STL

### Step 2: Salome mesher
- Take .STL format
- Mesh
## Option 2: Meshing with FreeCad
### Step 1: Create model with freecad
- e.g.: simple cube

### Step 2: Mesh with Freecad
Options
- Standard mesher
- Mefisto Mesher
- Netgen mesher
- Gmsh mesher -> Use gmesh

### Go to: FEM-workbench
- Make sure to link GMSH in preferences
- Mesh with GMSH
- Export as .unv

### Step 3: Import / View Mesh in Elmer FEM and ParaView

```
ElmerGrid 8 4 chamfered_cube.unv -autoclean
ElmerGrid 8 5 chamfered_cube.unv -autoclean
ElmerGrid 8 2 chamfered_cube.unv -autoclean
```


# UNV file
Consists of
- Dataset-number
- Dataset

Following each other one after the other:
- https://victorsndvg.github.io/FEconv/formats/unv.xhtml

## Conversion of unv to VTK
In order to view a .unv file with paraview, you can convert it with ElmerGrid-software

# Creating a boundary condition on one end
The goal now is to apply a "force" only on one edge / face of the chamfered cube.

## Option 1: freecad mesh group creation
1. Select the face / edge you want
2. Create FEM -> Constraint -> "Group" / Use the FemMeshGroup object
3. Give the group a name
4. Export as unv
	- This will then be a separate boundary entity