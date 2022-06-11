# Revit-Room-Schedule
Automated Revit Room Schedule (w Clockwork and archilab)
This Dynamo graph was created to retrieve basic room finishes (floors, walls, ceilings) and to write these finishes to a room schedule.
The graph includes Clockwork and archilab nodes. Thanks to them, kinds of filters for walls, floors, ceilings and roofs were created. 
Other elements such as, columns, beams are excluded.

Before running it, “Areas and Volumes” must be selected to find exact room boundaries (check Area and Volume Computations in Revit). 
By doing this, possible problems with floor and ceiling finishes will be prevented. 
Some problems may arise if there are stacked walls in models. 
In general, if lower part of these stacked walls/walls are thicker than upper part causes of this kind of problem. 
Finishes of upper part cannot be gathered and written. It is all about room boundaries.

Designating finish layers (Finish 1 [4] or Finish 2 [5]) for model elements in Type Properties is not necessary. 
If model elements consist of only structural parts , materials of these parts are written as finishes.

If same kind of elements in a same room have different materials, these materials are written to the room schedule with designated seperator string. 
For instance, plaster and tile are finishes of walls in a room, in room schedule wall finish will be written as Plaster “and” Tile or etc. 
Instead of “and” + sign may be used.

If there is no finish in a room (that means no walls, no roofs no ceilings) , hypen (-) will be written to proper cells on room schedule. 
It may be used for shafts that have no ceilings and floors.
