# How to spawna a schematic using code?

You can spawn a schematic using the code doing ```ObjectSpawner.SpawnSchematic(("Schematic name"), (Vector3Position), (Rotation), (Position), null``` if you don't want to put anything in rotation and position then just put "null"

## Example

Vector3 position = new Vector3(121.745f, 295.456f, -43.384f);

1) Object.SpawnSchematic("LuckyBlock", position, null, null, null);

2) Object.SpawnSchematic("LuckyBlock, player.Position, null, null, null

# How do I define a schematic?

You can define a schematic by writing ```private SchematicObject? (InstanceName) = null;```.

## Example

1) private void SchematicObject? _schematic = null;

# How do I attach a schematic to a player?

to spawn a schematic on a player you need to have the player instance, to do this you will have to do it in your private void, for example, private void SpawnSchematic(Player player), once you have done this, you will have to write ``` _schematic.gameObject.transform.parent = player.GameObject.transform;```, this code attaches the GameObjectDefined to the player gameobject.

# How to position the schematic at specific points of the player?

To position the schematic in a specific point of the player you have to do```InstanceName.GameObject.transform.localposition = Vector3.Zero + new vector3(PositionX, PositionY, PositionZ);, 

## Example

_schematic.GameObject.Transform.LocalPosition = Vector3.zero + new Vector3(0f, 0f, 0f);


# How do I rotate my schematic using code?

To rotate the schematic via code you need to do ```InstanceName.gameObject.transform.localRotation = Quaternion.Euler(RotationX, RotationY, RotationZ);```

## Example

_schematic.GameObject.Trasform.LocalRotation = Quarernion.Euler(0f, 90f, 0f);

# Code Example

        private void SpawnSchematic(Player player)
        {
            try
            {
                _schematic = ObjectSpawner.SpawnSchematic("LuckyBlock", player.Position, null, null, null!);


                _schematic.gameObject.transform.parent = player.GameObject.transform;
                _schematic.gameObject.transform.localPosition = Vector3.zero + new Vector3(0f, -0.82f, -0.35f);
                _schematic.gameObject.transform.localRotation = Quaternion.Euler(0, -90, 0);
            }
            catch
            {
                Log.Error("Unable to spawn schematic!");
            }
        }
