
This is the code exposed in the article "FINITE ELEMENT APPROXIMATION OF FRACTIONAL NEUMANN
PROBLEMS" available online here: https://arxiv.org/abs/XXXXXXXXXX. 

This code is a simple modification of the one given in "A short implementation for a 2D Dirichlet problem of a fractional laplacian" available online here: https://arxiv.org/abs/1610.05558. 
 
----------------------------------------------------------------------------------------

For a quick test, load "example_mesh.mat" in the MATLAB workspace and
then execute "main.m". 

----------------------------------------------------------------------------------------

Alternatively, we provide a couple of basic mesh generators (mesh_generator_circle.m and
mesh_generator_square.m) providing meshes with a data structure compatible with the 
main code. 

In these programs a unitary ball and an unitary square are meshed togheter with a
 suitable auxiliary ball, using the geometry files "circleincircle.m" and 
"squareincircle.m"  respectively. The user may find it easy to modify them and create
customized examples.    

In order to use these meshes, just execute either "mesh_generator_circle.m" 
or "mesh_generator_square.m" and then "main.m".  

----------------------------------------------------------------------------------------

In case the user wants to provide a custom mesh, the main code needs the
following data loaded in the MATLAB workspace before the execution: 
  
`-p` , All the mesh vertex coordinates (including those lying in the auxiliary domain).

```
    | x1 | x2 | ... |xn |
p = |-------------------|
    | y1 | y2 | ... |yn |
```
     

`-t` , All the mesh triangles (those triangles that belong to the auxiliary domain must be
listed at the end).
```
t =   

| t11 | t12 | t13 |
|-----------------|
| t21 | t22 | t23 |
|-----------------|
   .     .     .
   .     .     .  
   .     .     .
|-----------------| 
| tk1 | tk2 | tk3 |
```

`-nt_aux` , The number of triangles in the auxiliary domain.

`-R`  , The radius of the auxiliary domain.  

----------------------------------------------------------------------------------------
  

   
