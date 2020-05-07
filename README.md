# Revit Dynamo - Dynamic Parameters Export
This script takes dynamic instance parameters such as an element's length, width, or area, and copies the parametric values to a shared parameter for export.  The shared parameters file is included in the repository and must be added when creating a new project.  User can modify script and shared parameters if other parameters are needed.  Ultimately, the primary intent of this script is part of a workflow to allow these dynamic parameters to get exported to Unreal Engine 4 via Revit Datasmith add-in.  These metadata parameters can then be accessed within Unreal Engine 4.

## Getting Started
Environment setup regarding script development logistics.

* IDE:
  * Revit Dynamo

* Language:
  * Visual Programming / Python for Custom Node Creation

* Output File Type:
  * dyn

* Additional Library Packages Implemented: </br>
  * Default Dynamo Library

## Dynamo Script Development & Structure
#### Script features and specs.
* Software Required
  - Revit (any version with Dynamo 2.1 and above installed)
    
* User Interface
  - User to select which element(s) from Revit 3D view UI to process

#### Dynamo Script Layout
Overall graph view
<p align="center">
  <img src="https://user-images.githubusercontent.com/44215479/81253410-5c75f480-8fdd-11ea-9512-8514686a6725.png" width="600">
</p>

1. User Input
<p align="center">
  <img src="https://user-images.githubusercontent.com/44215479/81253905-85e35000-8fde-11ea-8d98-efc1499fd302.png" width="400">
</p>

2. Example of Backend Process for a parameter
    * **Note:** A warning may be indicated as an elements(s) may not have the parameter applicable to it.  See Output (Watch node) which element has a null value.  This can be ignored. 
<p align="center">
  <img src="https://user-images.githubusercontent.com/44215479/81253998-c93dbe80-8fde-11ea-99f7-df813fc4c3af.png" width="600">
</p>

3. Mapping Script to UI
<p align="center">
  <img src="https://user-images.githubusercontent.com/44215479/81255262-1707f600-8fe2-11ea-847a-2806dda91c97.png" width="600">
</p>
       
## Running Script & User Implementation Instructions
1. Clone or download project. </br>
2. In own Revit project or using example Revit model in Example Revit Model folder, load shared parameters from Revit_DynamicParameter_Export.txt
<p align="center">
  <img src="https://user-images.githubusercontent.com/44215479/81255753-5be05c80-8fe3-11ea-897c-1e05fd6803f1.png" width="400">
</p>
3. Select an model element (e.g. wall, floor, etc.), to confirm shared parameters are loaded.
<p align="center">
  <img src="https://user-images.githubusercontent.com/44215479/81255898-c1344d80-8fe3-11ea-8dfd-5aa9977640ee.png" width="600">
</p>
4. Open the Dynamo script (RevitMetaDataExporter.dyn) in Dynamo. </br>
5. In the User Input section (Select Model Elements node), select and drag select all the desired elements to be processed in the Revit 3D view and select Run in Dynamo.
   <p align = "center">
      <img src="https://user-images.githubusercontent.com/44215479/81256281-db226000-8fe4-11ea-8c00-5fb1068cd275.png" width="600">
   </p>
6. In a Revit 3D view, select an element and check that shared parameters have been updated
   <p align = "center">
      <img src="https://user-images.githubusercontent.com/44215479/81256570-c09cb680-8fe5-11ea-8a4d-5c5e7e185723.png" width="400">
   </p>

## References for Further Learning
- [Using Datasmith with Revit - Epic Games Unreal Engine](https://docs.unrealengine.com/en-US/Engine/Content/Importing/Datasmith/SoftwareInteropGuides/Revit/index.html)
- [Using Datasmith Metada - Epic Games Unreal Engine](https://docs.unrealengine.com/en-US/Engine/Content/Importing/Datasmith/Overview/UsingDatasmithMetadata/index.html)


