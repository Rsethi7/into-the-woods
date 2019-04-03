# Creating a Tile

All tiles are scenes that inherit from a base Tile scene. Terrain tiles have static bodies, while structure tiles don't. Tiles are imported to a tile set, which is used by tile maps in the game.

1. Create a scene, inheriting from *map/base-tile/Tile.tscn* (or one of its descendants). Save it in *map/terrain/tiles* or *map/structure/structure_name/tiles* (depending on the type of tile).
2. Add an instance of the scene to *map/TileSet.tscn*, and assign a 1 pixel texture to the sprite node.
3. Export the TileSet scene (as a tile set) to *map/tile_set.tres*. Right now, you have to manually set the shape's (rectangle) bounds to 4,4 and the shape offset to 4,4 for all tiles with collision shapes.
4. Now it can be used in generator algorithms!