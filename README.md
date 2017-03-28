# AutoPKG Stuff
Working on an implementation of AutoPKG, AutoPKGr, and JSSImporter for my work environment. 

Some things to note about the recipes here. 

Because my JAMF Pro server is in a non-centralized envrionment, we are running with Sites, in a similar manner to which a Windows Admin might assign OUs to an organization. Because of this, my .pkg.recipe files and my jss.recipe files will be significantly different from most of the ones that you would see in the standard AutoPKG repositories. 

Because of our current naming conventions on our JAMF Pro DP, we are going sideways from the standard naming conventions of %NAME%-%VERSION% seen in most APPLICATION.pkg.recipe files. For every application that we create a .pkg file for, we will have two different recipes. One that creates a recipe with the name in format "All-%NAME%-%VERSION%" and one with the name in format "All-%NAME%-Latest". The latter is so that we will have a way to replace like-named files on the DP so that we can have a group of standard policies which always offer the latest version of whatever application has been packaged. 

At this point, all of the JSS recipes that I am writing incorporate sites specific to my envioronment. Additionally, for the time being, I am scoping everything to static groups, although I do expect that to change as we move forward with AutoPKG. 
