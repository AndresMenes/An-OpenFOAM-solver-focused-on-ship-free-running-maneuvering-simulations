# An OpenFOAM solver focused on free-running maneuvering simulations - CustoHOsource branch

Summary

These modifications are based on the "overInterDyMFoam" solver in OpenFOAM v2206.
---This has been compiled using OpenFOAM v2306---

Functions
  1. Added a modified HOsource (myHOsource) to calculate power produced by the propeller, both predicted and actual based on the current code. 
  2. Added make/ folders with files and options to showcase a possible way of compiling the libraries. 
  3. Modified the tutorial to incorporate the new changes.
  
P.S.

The code compiles but the tutorial is not working, currently under investigation why. An issue was opened on the original code of Balabibo to see what has been done incorrectly. 
myHOsource compiles correctly and seems to produce correct results (currently under validation).
