# Component_lib
Just a component database until I get a NAS running...

# How to install the library
Put the repo Component_lib in the desired location. 
## Symbols
Then in KiCad, open symboal editor, go to Preference->Configure symbol library and then add with the + button, and select the path to the SamacSys_Parts.kicad_sym file. The symbol library should be working now.
## Footprints
In footprint editor you can repeat the same process Preference->Configure footprint library, + button, and select the path to the SamacSys_Parts.pretty folder this time.
## 3D
In footprint editor, select any Component_lib footprints (u.fl for example), in footprint properties, go to 3D model.
First click "Config Paths" and add COMPONENT_LIB name with the path to the SamacSys_Parts.3dshapes folder. Once this is done all 3D should be visible. If you started a layout without configuring the 3D path you may have to update the footprints of the components.
click on the + button, and select path 


# How to add components:
You can (and should use Library Loader)
Once you dowloaded the .zip of your component (from mouser for example), library loader should do the job (if you are lucky), if not, start Library Loader and press `Open ECAD Model`
The component should now be in your Component_lib library
If you do not want to use Library Loader you can do the job manually. You will have to put the .kicad_mod file the the SamacSys_Parts.pretty folder (Footprints), put the .step file in SamacSys_Parts.3dshapes (3D file).
The schematic part is a bit more tricky as they all stay in one file SamacSys_Parts.kicad_sym, add your symbol in the alphabetic order and everything should be fine. 

# How to commit:
Once you added components, do
```
git add --all
git commit -a
git push
```
