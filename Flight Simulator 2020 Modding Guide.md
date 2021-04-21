# Flight Simulator 2020 Modding Guide

From [playlist](https://www.youtube.com/playlist?list=PL_Up4sAmkCfXIOqIRzS9OpQEJRyW-rnoq)

## Installing the SDK

[Reference](https://youtu.be/3K0XhAf0WYw?list=PL_Up4sAmkCfXIOqIRzS9OpQEJRyW-rnoq)

1. Run game.
2. Option > General > Developers
3. Turn Developer Mode on
4. Help > SDK Installer

> Download the SDK installer and run. Install it to a folder outside of the FS2020 folder. Let's call it `MSFS SDK`


## Creating a Project (Scenery Project)

[Reference](https://youtu.be/3K0XhAf0WYw?list=PL_Up4sAmkCfXIOqIRzS9OpQEJRyW-rnoq)

### Prepare the project

1. Copy the `MSFS SDK/Samples/SimpleScenery` sample project to a new directory.
2. Rename to a custom project name. e.g. `TutorialScenery`
  a. Rename `./SimpleScenery.xml` to `TutorialScenery.xml`
    i. Open the file and rename the `<Package>` file entry.
  a. Rename the `./PackageDefinitions` folder/file.
    i. Open the file and rename every reference to `mycompany-scene`
3. Clear the `./PackageSources/modelLib/` folder
  a. Delete `Light_Sample` folder.
  b. Delete the `SampleMyBox` folder.
  c. Delete all files within `textures` folder, but not the folder itself.
4. Clear the `./PackageSources/scene` folder
  a. Delete the `objects.xml`

### Load the project

Prep game:

1. Load into the world at your desired location.
2. Options > Pause Simulation
3. Camera > Developer Camera

Load project:

1. Tools > Project Editor
2. Project > Open... (Browse to the project `.xml`)
3. Build project
   a. Click project dropdown
   b. View > Inspector
   c. Build package

## Replacing Default Scenery

[Reference](https://youtu.be/IOhnU_w3Us8?list=PL_Up4sAmkCfXIOqIRzS9OpQEJRyW-rnoq)

### Polygon to Remove Default Scenery

Either

- Click "myscene" under Project Editor > Load in Editor
- Tools > Scenery Editor

To draw polygons (for exclusion bounds, etc.)

- In Objects view > "Polygon" object type.
- Ctrl + click to draw polygon
- Double-click to finish

Polygon now appears in Scenery Editor

- View > Properties
- Select desired behaviour

### Placement of Objects

- Objects view > select object type
- Select object from  filterable list
  - "One-click placing" is useful for previewing

- Scenery Editor > View > Gizom allows object adjustment
- Scenery Editor > click on object > Duplicate creates a copy

### Save

- Scenery Editor > Save Scenery
- For Shape Files: Save as `PackageSources/scene/projectNameSHP`
- For Scenery Files: Browse to `PackageSources/scene/projectNameSCN`

### Bring Into Game

To double check Community folder location

- Tools > Virtual File System
- Opened Watched Bases and see Community folder path

Build the package

- Build project
  a. Project Editor > click project dropdown
  b. View > Inspector
  c. Build package
- Copy `./Packages/projectName` folder into your Community folder


## Adding User Created Scenery

[Reference](https://youtu.be/IOhnU_w3Us8?list=PL_Up4sAmkCfXIOqIRzS9OpQEJRyW-rnoq)