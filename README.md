# Flavoured pyRevit
###### You could say its adding some strawberries to pyRevit milk

##Tools specific to health projects 

Find yourself stuck doing the same micro tasks and just wish it could just be a teeny bit faster? Me too!
So in an attempt to make things a little less painful, these docs are going to take you through the tools I've been tinkering around with pyRevit to automate some of the stuff we do a lot in health projects. 

- Project Library - shortcut to the project library
- Clinical Library - shortcut to the clinical library for families 
- Edit selected family - it will open the selected family in Revit from the clinical folder
- Load family - a smarter way to search and load in families from clinical folder, can (should) also be able to load in multiple families 
- Update Sheet info - Update Sheet number prefix, Capitalise sheet name  and copy data from room shared parameters to sheet shared parameters (based on matching room and sheet numbers). 

These are based on your active Revit project, so these shortcuts should work for other projects too, just so long as the _Revit folder structure is the same! 

## How do I add the toolbar? 
To add custom pyRevit Toolbars, go to pyRevit, click on the dropdown “pyRevit” in the bottom left of the ribbon.
Select Settings > add folder > then paste the toolbar location. Select folder > Save Settings and Reload. 
PyRevit will reload and the toolbar will be ready to use.

## Hint 
You can assign all add-ins (including the pyRevit tools) to your own custom keyboard shortcuts. (View > User Interface >  Keyboard shortcuts)

