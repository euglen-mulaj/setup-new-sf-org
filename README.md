# setup-new-sf-org
How to easily setup new project with manifest and retrieve all metadata from the org into vscode.

Follow these steps:

1-Delete the default folder from force-app/main/default

2-Run this command where wolves -> your org alias 
sfdx force source manifest create --fromorg wolves --manifestname=allMetadata --outputdir manifest

3-Move the allMetadata.xml file outside the force-app folder into the project folder

4-Run this command:
sfdx force:source:retrieve -x allMetadata.xml
