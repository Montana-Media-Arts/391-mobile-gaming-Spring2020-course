---
title: Unity Tilemap
module: 12
jotted: true
---

# Unity Tilemaps

<iframe width="560" height="315" src="https://umontana.zoom.us/rec/play/68Z7fuz--mg3TtzB4QSDUP9xW9W-f6OsgSRI-_AOzRrhUHBVY1SgMrsaM7B36oBpfIxDsJv6Yc44AHCJ?continueMode=true" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Now that we have background, we need to add something to it.  First, we need to add the ground so that our character has something to walk on.

## Adding and Opening the Tile Palette

The Tile Palette allows us to `paint` something onto the scene easily without having to copy and paste the same component on each time.

To access the Tile Palette, you go to Window -> 2D -> Tile Palette.

What do you do if it's not there?

Go to Windows -> Package Manager.

In the Packages dialog window, click on 2D Tilemap Editor and then in the bottom right-hand corner click Install.

Then close the window and try and to open the Tile Palette window.

Once open, find the tiles you want to paint onto the scene.

I chose the Autumn ones in the Tiles -> 2D Tiles -> Autumn 512x512.  

First, in the Tile Palette Window, click Create New Palette.  Then, name it something appropriate like `Ground`.

Then, select all the tiles in the Project folder and drag them into the Tile Palette window. Tehy should all appear.

## Read to Draw

To draw the palette images, we must first add a Grid to the Scene.

First, click the Scene name and then go to GameObject -> 2D Object -> TileMap.

Then, click on the Grid in the Hierarchy and then select the tile you want to paint onto the scene. Make sure the paint brush is selected before painting.

Did you get something painted?  Great!

## TileMap Collision

The TileMap is great, however, it won't stop the character from falling through the floor.  So, we have to add collision to it.  So, one might think we need put collission on each item we painted.  In a large scene, that would be painful.  

Unity helps by adding TileMap collsion.  

Again, select the TileMap in the Heirarchy.  Then, click on AddComponent.  Then search for Tilemap Collider 2D.  Now, it should highlight green around all the tiles you added.

Now, let's add a character.