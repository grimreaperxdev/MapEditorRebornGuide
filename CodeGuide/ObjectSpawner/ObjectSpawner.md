# How to spawna a schematic via code?

You can spawn a schematic using the code doing ```ObjectSpawner.SpawnSchematic(("Schematic name"), (Vector3Position), (Rotation), (Position), null``` if you don't want to put anything in rotation and position then just put "null"

## Example

Vector3 position = new Vector3(121.745f, 295.456f, -43.384f);

1) Object.SpawnSchematic("LuckyBlock", position, null, null, null);

# How do I define a schematic?

You can define a schematic by writing ```private SchematicObject? (InstanceName) = null;```.

## Example

private void SchematicObject? _schematic = null;

# How do I attach a schematic to a player?

to spawn a schematic on a player you need to have the player instance, to do this you will have to do it in your private void, for example, private void SpawnSchematic(Player player), once you have done this, you will have to write ``` _schematic.gameObject.transform.parent = player.GameObject.transform;```, this code attaches the GameObjectDefined to the player gameobject.

