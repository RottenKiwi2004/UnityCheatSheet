The master version of an object, edit one, all change.

By dragging the object to project window, we have successfully created the prefab of that object.

To modify the prefab, just move the object into the parent element and click Apply on the inspector tab

You can also revert the change of any prefab by clicking the Revert button

### Spawner

To make an object spawner, we have to create empty game object and attach spawner script to it.

Prefab can also be assigned to GameObject variable by declaring public field and drag that prefab into the inspector panel

To create new prefab from script, we can call function Instantiate which accepts object, position and rotation respectively.

Example:

```cs
Instantiate(
	objectPrefab,
	new Vector3(),
	Quarternion.Euler(new Vector3())
);
```

This function also returns the reference to that object itself as type Object

So, we can also write
```cs
GameObject refToObj = (GameObject) Instantiate();
```

Notice that we need to typecast from type Object to GameObject

In order to keep things tidy, we can append our new objects to the spawner (or other parents)
```cs
// Append to the spawner object
refToObj.transform.parent = transform;
```

