### Set position of the object

```cs
transform.position = new Vector3(0, 0, 0);
```

This also works with Input.getAxis()

```cs
new Vector3(
	Input.GetAxisRaw("Horizontal"),
	0, 
	Input.GetAxisRaw("Vertical")
);
```

### Translate object to new location

```cs
Vector3 moveAmount = new Vector3(0, 1, 0);
transform.Translate(moveAmount);
```

#### Appending object to another parent object

```cs
public Transform childrenTransform;
public Transform parentTransform;
void Start(){
	childrenTransform.parent = parentTransform
}
```

or if we are working in the script attached to that parent object

```cs
public Transform childrenTransform;
void Start(){
	childrenTransform.parent = transform
}
```

### Rotating object

```cs
// Rotate object around its local space
transform.Rotate(Vector3(0, 1, 0));
```

to change to global space, you can insert another parameter after Vector3

```cs
// Rotate object around its local space
transform.Rotate(Vector3(0, 1, 0), Space.Self);
// Rotate object around its global space
transform.Rotate(Vector3(0, 1, 0), Space.World);
```
