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
