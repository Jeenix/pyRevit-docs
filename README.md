# pyRevit Docs
###### Adding some *BVN* flavour to pyRevit ...keep in mind these tools were intended to automate Revit workflows on health projects.

Do you often find yourself doing the same tiny tasks and wish they could be a teeny bit faster? *Me too!* </br>
I created these docs to try and make things a little less painful by showing you how I've been experimenting with pyRevit to automate some of the things we do a lot in health projects.

These tools are based on your active Revit project, so these shortcuts should work for other projects too if following the standard BVN project folder structure.  </br>
*Just so long as the _Revit folder structure is the same!* 

###### How do I add the toolbar? 
To add custom pyRevit Toolbars, go to pyRevit, click on the dropdown “pyRevit” in the bottom left of the ribbon.
Select Settings > add folder > then paste the toolbar location. Select folder > Save Settings and Reload. 
PyRevit will reload and the toolbar will be ready to use. More info available <a href="https://bvn.zendesk.com/hc/en-us/articles/4787426471311">here</a>. 


###### BIM (pulldown menu)
- Export Shared Parameters - Exports GUIDs of each parameter in a project. This is something that the everyday user is unlikely to use but useful for developers and BIM managers to identify shared parameters and communicate with Revit’s API. This is an existing script that was previously designed for the Revit Python Shell but adding it to pyRevit makes it more user-friendly and accessible. 

###### Help (pulldown menu)
- BVN Learning Portal – This is a link to the BVN learning portal landing page. If BVN were to adopt a BVN specific pyRevit toolbar and had associated training within the portal, the link to it would be here. 
- Toolbar Help – This takes you to this GitHub page, so that the toolbar remains well documented and the information doesn’t get lost. The long-term plan is to also detail what the ‘traditional’ workflow for each tool would be to compare as well as how to make modifications for other projects’ requirements. 

###### Project Library  
- Project Library - shortcut to the project library. These are based on your active Revit project, so these shortcuts should work for other projects too, just so long as the _Revit folder structure is the same. I’ve tried to maintain as non-specific pathing where possible so that we could potentially leverage it across other projects. In essence, Revit/python is using where the central file is located to determine where the project folder is. 
- Clinical Library - shortcut to the clinical library for families. Same comment applies as above. 
- Edit selected family – Clicking on this button while you have a family selected will open the selected family in Revit. The typical workflow to open and edit a family would be find the name of the family you want to edit, open the clinical folder, navigate to the corresponding “.rfa” family in the folder to open. Often people resort to opening the family from the project (which means that you may be overwriting a newer version with a possibly older family when saving the family from the project), whereas not only does this reduce the time taken to find the family but make it easier to avoid bad practices altogether. I’ve since updated the script to open anything from the project library - this includes doors, windows, unions, MSPs, etc. 
- Load family - a smarter way to search and load in families from clinical folder since Revit’s native “Load families” is clunky. It can also load in multiple families. 

###### RLS 
- Check RLS Schedules – We rely heavily on the schedule’s filter to display the correct information on our RLS, this is a quick means to QA whether we are in fact reporting the correct information without printing or opening every view or sheet. The Schedule name is (typically) determined by default settings in Sonar, i.e. “ITEM SCHEDULE – (Room Number)” so we have a baseline to run our checks against. The same scripting method could likely be leveraged to bulk-update schedule filters. 

###### Sheets
- Update Sheet Info – This gives the users a few options. The most useful is being able to copy data from the room parameter to a sheet parameter (Functional group name and HPU name). This was originally developed in Dynamo by RH and I, however this is a python replacement. Scripts in python are more stable than in Dynamo as the nodes / packages that dynamo relies on changes considerably between versions of Revit whereas python is interacting directly with the Revit API and is therefore more stable. The other options are to capitalise the sheet name and add the RLS drawing name prefix “AR_4A-H50”, as these are typically left off by Sonar.  

###### Note on Scalability 
pyRevit has greater flexibility and is easier to update than BVN tools. Once loaded into a users’ pyRevit profile, the extension will appear on all versions of Revit, and they will get updates the next time they open Revit without them needing to do anything. 

###### Hint 
You can assign all add-ins (including the pyRevit tools) to your own custom keyboard shortcuts. (View > User Interface >  Keyboard shortcuts)
