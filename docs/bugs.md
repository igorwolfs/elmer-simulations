# Meshing
## Multiple Body's

It might be that due to bad meshing, you get multiple bodies.

If you check out Model -> Summary, you can see how many bodies / Boundaries were detected.

More than expected -> means something went wrong during meshing. Might be due to chamfering, or might be because internally it consists of solids + shells mixed. This is called Netgen behavior.

Check-out separate bodies 
- ElmerFEM Body Property i
- View->hide/show selected

Solutions
1. Select chamfered Cube
2. Run part->check geometry->enable BOPCheck
3. Run part -> refine shape
4. Export as STEP